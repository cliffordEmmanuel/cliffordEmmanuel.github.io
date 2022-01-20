---
layout: post
title: String concatenation in Redshift
subtitle :  
tags: [redshift]
author: Clifford
comments : True
---


When joining strings in redshift we can use these options:   
- The concatenation operator
- The concat() function

<br>

**The concatenation operator**  

Syntax: `Select <column containing string1> || <column containing string2>`  
  
You can add an extra `|| <column containing string3>` and more to concatenate multiple strings

<br>

<br>

**The concat() function**   

Syntax: `Select concat(<string1>,<string2>)`   
  
You can concat multiple strings by nesting the concat:  
`Select concat(<string1>, concat(<string2>,<string3>))`  

<br>

In all instance when there's a null in any of the columns the resulting expression will be a null. To specify a different output use the [nvl](https://docs.aws.amazon.com/redshift/latest/dg/r_NVL_function.html) expression.  

Syntax: `Select concat(<column1>, nvl(column2,<default value>))`   

<br>

<hr>

## _Sources:_
- <https://docs.aws.amazon.com/redshift/latest/dg/r_CONCAT.html>