---
layout: post
title: Conda virtual environments; handy commands
subtitle :  
tags: [conda, virtual envrionments]
author: Clifford
comments : True
---


## The following are the handy commands I found for managing conda virtual environments.

*Creating a new environment*

- `conda create -n <environment name>`

<br>

*Renaming a virtual environment*

This is not directly possible but a workaround involves 2 steps:
- Create a new virtual environment by cloning the virtual environment
    - `conda create -n <new name> --clone <old name>`
- Remove the now obsolete environment
    - `conda remove -n <old name> --all`

<br>

<hr>

## _Sources:_  
- <https://stackoverflow.com/questions/42231764/how-can-i-rename-a-conda-environment>