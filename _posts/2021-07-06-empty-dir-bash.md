---
layout: post
title: Checking if a directory is empty using bash script
subtitle :  
tags: [bash]
author: Clifford
comments : True
---


Checking whether a directory is empty can be acheived using an if-else construct. 

It has the following syntax:

```bash
if [[ condition ]] # there must be a space between the condition and the square brackets
then
  <execute command>
else # this is optional
  <execute another command>
fi # this closes the statement
```

<br/>


Condition for checking if empty:

`-z "$(ls -A /path/to/dir/)"`

<br/>

So in summary this can be achieved as follows:

```bash
temp_dir = "some-path"

if [ -z "$(ls -A $temp_dir)" ]; then
   echo "$temp_dir empty"
else
    echo "Not Empty"
fi
```

<br/>


## Sources:

- <https://superuser.com/questions/352289/bash-scripting-test-for-empty-directory>
- <https://devconnected.com/bash-if-else-syntax-with-examples/>