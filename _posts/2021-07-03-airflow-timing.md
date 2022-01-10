---
layout: post
title: Understanding airflow's timing
subtitle :  An explanation of the timing syntax.
tags: [ariflow]
author: Clifford
comments : True
---

# Syntax
<br>

Scheduling on airflow seems to have inherited a lot from crons and the timing syntax is no exception. The basic syntax looks like this:

`*  *  *  *  *`
<br>

This <emp>*</emp> acts like a place holder for the specific time periods. From left to right, they each represent the following:

1. min (0-59)
2. hour (0-23)
3. day of month (1-31)
4. month (1-12, Jan - Dec)
5. day of week ( 0-6, Sun - Sat)

*Note that the Astericks \* means any or always*

<br/>

<hr/>

# Examples

- `* 05 * * *`
  This means the job should trigger at 5:00 am every day.

- `15 13 * * *`
  This means the job should trigger at 01:15 pm every day.

- `5 0 * * 0`
  This means the job should trigger at 00:05 am every sunday.

- `* * 1 1 *`
  This means the job should trigger on the every first day of January.


# Literals

**Comma(,)**

This is used to specific different values on a single time period. For instance,
`1,2,3 * * * *`
This job would run at 1,2,3 minutes all the time.

**Hyphen(-)**

This represents the range of values. For instance, 
`* * * * 1-5`
This job would run every weekday ie Monday to Friday

**Forward Slash(/)**

This represents step values or interval values. For instance,
`*/5 *  *  *  *`
This job would run after every 5 mins


