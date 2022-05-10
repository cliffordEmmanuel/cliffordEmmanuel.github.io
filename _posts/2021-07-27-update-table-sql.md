---
layout: post
title: Updating a column based on condition on another column
subtitle :  
tags: [PostgreSQL]
author: Clifford
comments : True
---


Updating an existing table value based on a certain condition.

<br>

Syntax:

```sql
Update <table-name>
set column = <new value>
where other column = condition
```

I've had to ran an update on an existing table for an instance where the logic for creating a product type column needed to be updated based on another column.

<br>

<hr>

## _Source:_  
- <https://chartio.com/learn/sql-tips/how-to-update-a-column-based-on-a-filter-of-another-column/>