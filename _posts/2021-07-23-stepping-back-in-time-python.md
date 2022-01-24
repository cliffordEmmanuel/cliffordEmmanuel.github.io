---
layout: post
title: Stepping back in time using python 
subtitle :  
tags: [pandas, python]
author: Clifford
comments : True
---


I found that working with dates in python can be quite a hurdle. But pandas always comes through. I discovered the `pd.offsets` module and it has been a smooth ride looking to go back and forward in time.

There are several useful classes for different purposes ie:   
<br>

**Getting the last day month from a given date (Monthend)**  

Syntax: `date + pd.offsets.MonthEnd(n)`  
where:
- `date` refers to any datetime object   
- `n` can refer to number of steps. And also takes **+** or **-** for eg:
    - `'2021-01-23'+ pd.offsets.MonthEnd(+2)` returns the last day of the March 2021
    - `'2021-01-23'+ pd.offsets.MonthEnd(12)` returns the last day of the November 2020  
<br>

**Getting the last day week from a given date (Week)**  

This above approach also applies to getting the last day of either the previous or future week, based on a given day.

Syntax: `date + pd.offsets.Week(n)`  
where:
- `date` refers to any datetime object   
- `n` works in the one above.  

**Going back or forward by days**  

Here we can also employ the `pd.DateOffset()`   
Syntax: `date - pd.DateOffset(days=1)`  
Other parameters that can be used to replace the offset value are:  
- year
- month
- weekday
- hour
- minute  

<br>

<hr>

## _Sources:_  
- <https://stackoverflow.com/questions/36764487/pandas-dateoffset-step-back-one-day>
- <https://pandas.pydata.org/docs/reference/offset_frequency.html#dateoffset>
- <https://pandas.pydata.org/docs/reference/api/pandas.tseries.offsets.DateOffset.html>




