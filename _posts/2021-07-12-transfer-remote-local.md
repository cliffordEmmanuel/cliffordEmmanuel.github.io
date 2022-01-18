---
layout: post
title: Copying files between to servers
subtitle : Using SCP  
tags: [linux, scp]
author: Clifford
comments : True
---



**SCP -  secure copy**. It is used to copy files between servers securely. The transfer can happen either between a local host and a remote host or between two remote hosts. SCP uses the same authentication and security procedure that is used by the SSH protocol.

<br>

The basic syntax is at follows:

`scp <username>@<source-host>:<path to file>   <username>@<destination-host>:<path to store file>`

<br>

If you're on your local wanting to receive a file from a remote server:

`scp <username>@<remote-host>:/path/to/file   /path/to/store`

<br>

As for all linux commands you can get extra information about its usage by typing `man <command-name>` in the terminal. 

Do a `man scp` to get more information about the scp command.

Cheers!

<br>


<hr>

## _Sources:_
- <https://unix.stackexchange.com/questions/188285/how-to-copy-a-file-from-a-remote-server-to-a-local-machine>
