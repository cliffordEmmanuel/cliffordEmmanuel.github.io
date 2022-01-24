---
layout: post
title: Getting the difference between two dates
subtitle :  
tags: [PostgreSQL, redshift]
author: Clifford
comments : True
---

There are several approaches to this.  

### Using the '-' operator  
<br>

Syntax: `SELECT 'date1'::date - 'date2'::date`  

This approach usually returns the difference in days. There are some scenarios where sometimes the difference is needed in months, or years, or seconds even. With that we use the `DATEDIFF` function.   

<br>

### Using the DATEDIFF function   
<br>  

Syntax: `DATEDIFF(interval, date1, date2)`  

The interval parameter can be:
- year, yyyy, yy = Year
- quarter, qq, q = Quarter
- month, mm, m = month
- dayofyear = Day of the year
- day, dy, y = Day
- week, ww, wk = Week
- weekday, dw, w = Weekday
- hour, hh = hour
- minute, mi, n = Minute
- second, ss, s = Second
- millisecond, ms = Millisecond  

<br>

Redshift also extends this with the `DATE_PART` which refers to the specific part of the date or time that the function operates on. With it you can also get the millennium, epoch, century.  

<br>

<hr>

## _Sources:_  
- <https://docs.aws.amazon.com/redshift/latest/dg/r_Dateparts_for_datetime_functions.html>
- <https://docs.aws.amazon.com/redshift/latest/dg/r_DATEDIFF_function.html>
- <https://www.w3schools.com/sql/func_sqlserver_datediff.asp>