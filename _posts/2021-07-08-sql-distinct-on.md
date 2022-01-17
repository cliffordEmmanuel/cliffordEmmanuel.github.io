---
layout: post
title: SQL distinct on
subtitle : when to use it  
tags: [PostgreSQL, redshift, sql]
author: Clifford
comments : True
---


The `DISTINCT` keyword used in a select statment is used to remove duplicates from a query result. It keeps one row from each group of duplicates. 

This query shows its usage:

```sql
SELECT 
    DISTINCT column_1
FROM
    table1
;
```

<br>

It can be used on multiple columns. In that instance all the columns the distinct values are based on the combination of all the specified columns.

Like so:

```sql
SELECT 
    DISTINCT column_1
    , column_2
FROM
    table1
;
```

Sometimes however, you'd want to only keep the distinct values for just a single column. This is where the Postgres `DISTINCT ON` comes in.

```sql
SELECT 
    DISTINCT ON (column_1) alias
    , column_2
FROM
    table1
ORDER BY
    column_1
    , column_2
;
```

In this instance, the duplicates are only evaluated on the column specified by the `DISTINCT ON`. It is a good idea to add an order by clause to prevent unexpected results.  

_Note that, the column on which the distinct on is performed should be the first specified in the select statement and also in the order by clause._

<br>

`Redshift` however doesn't support the `DISTINCT ON` feature although it is built on postgres.
To bypass however you can use a combination of `ROW_NUMBER` and `PARTITION BY`.

_This example assumes column_1 is the column on which the distinct on should be evaluated:_

```sql
SELECT  
    *
FROM
    (SELECT column_1
            , column_2
            , column_3
            ROW_NUMBER() OVER (PARTITION BY column_1
                             ORDER BY column_2, column_3) AS column_1_ranked
    FROM table1
    ORDER BY column_1
             , column_2
             , column_3
    LIMIT 10) AS ranked
WHERE ranked.column_1_ranked = 1;
```
<br>

## _Sources:_
- <https://www.postgresqltutorial.com/postgresql-select-distinct/>
- <https://gist.github.com/jmindek/62c50dd766556b7b16d6>