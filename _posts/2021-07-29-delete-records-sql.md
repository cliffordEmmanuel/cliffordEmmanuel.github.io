---
layout: post
title: Deleting rows from a table
subtitle :  
tags: [PostgreSQL]
author: Clifford
comments : True
---


Syntax:
```sql
DELETE FROM table_name
WHERE condition;
```

*Always treat deleting commands with extreme caution*

In this case always supply a where clause so you don't end up deleting something you were not supposed to delete. As a fail safe be sure to create a copy of the table before you delete.

<br>

<hr>

## _Source:_  
- <https://www.postgresqltutorial.com/postgresql-delete/>