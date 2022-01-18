---
layout: post
title: SQL order by 1
subtitle : What does it mean? 
tags: [PostgreSQL, sql]
author: Clifford
comments : True
---


When i first saw `Order by 1` at the tail end of an sql script. I was terribly confused.

<br>

```sql
Select 
    *
From table1
Order by 1
```

<br>

In this rather crude example above, all the columns from table1 are selected and then ordered by the first column returned by the select.

<br>

The number in the where clause is called an "Ordinal". As it references the columns defined in the select clause 

<br>

It turns out it is not a good practice to use numbers to represent columns. So i guess my confusion was justified. But here's the reason why it is not recommended:
- You can't know at a glance what columns are being explicitly referenced
- Although the query will remain valid even when the column order changes, you risk ordering by some unexpected column.

<br>

_So yeah this is what it means when you look at some old SQL script and please use it sparingly or better still not at all._

<br>
<br>

<hr>

## _Sources:_
- <https://stackoverflow.com/questions/3445118/what-is-the-purpose-of-order-by-1-in-sql-select-statement#:~:text=This%3A%20ORDER%20BY%201,It's%20not%20obvious%2Fexplicit?>