---
layout: post
title: The SQL Grant statement 
subtitle :  
tags: [PostgreSQL]
author: Clifford
comments : True
---


The **Grant** statement is used to define access privileges. That is, it can be used to grant access to database objects such us tables, views , sequence etc..

<br>

**Grant access to database object**  

<br>

Syntax: `GRANT SELECT ON <schema>.<table-name> TO user`  

- In place of `SELECT` we could have `INSERT` , `UPDATE`, `DELETE` etc.  
 
<br>

- In place of `<schema>.<table-name>` you could have a view name or a sequence etc.  

<br>

- Access privileges could be given to multiple users by comma separating them. Also could be given to a group etc.   

<br>

<hr>

## _Sources:_
- <https://www.postgresql.org/docs/9.0/sql-grant.html>
