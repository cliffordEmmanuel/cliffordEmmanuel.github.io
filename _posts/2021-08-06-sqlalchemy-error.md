---
layout: post
title: Weird SQLAlchemy error passing a query with python
subtitle :  
tags: [PostgreSQL,redshift]
author: Clifford
comments : True
---

I ran into an issue one time where a query which worked fine on dbeaver through a weird error when a python script that ran it failed on the remote server.

<br>

Error message was something along these lines:
`TypeError: 'dict' object does not support indexing`.

<br>
After some digging I found the issue had to do with my use `%` in several case statements. Apparently `%` is not parsed as expected by SQLAlchemy and the fix was just to double the sign ie.`%%`

<br>

_As things stand I don't have a really good explanation why so when i get more knowledgeable I'll update!_


<hr>

## _Sources:_
- <https://stackoverflow.com/questions/8657508/strange-sqlalchemy-error-message-typeerror-dict-object-does-not-support-inde>
