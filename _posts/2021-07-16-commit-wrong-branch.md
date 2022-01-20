---
layout: post
title: What to do when you commit to a wrong branch
subtitle :  
tags: [linux]
author: Clifford
comments : True
---

So, I've run into this many issues several times, when I mistakenly make commits on the master branch rather than to another branch. Jeez sometimes this is hell!!

There are two approaches you can follow:
- Undo on master and commit to new branch.
- Move commits to the other branch.

<br>

## Undo and Commit to New Branch

You're less likely to make an error with this approach. Especially if you need to commit the changes to a new branch.
<br/>

- **Make sure you are on the branch you were committing to.**   
`git branch`

<br/>

- **Check how many commits you want to roll back to.**   
`git log`

<br/>

- **Undo the commits.**   
`git reset HEAD~N`   
where `~N` refers to the number of commits to undo.

<br/>

- **Checkout to a new branch.**   
`git checkout -b newBranch`

<br/>

- **Add your changes.**   
`git add -A`   
this flag: `-A` adds all new/modified/deleted files in the current directory to staging. 

<br/>

- **Commit the changes.**   
`git commit -m "commit message goes here!"`  

<br/>

## Move the commits to the other branch.   


There's a higher chance of making an error so be extra careful here!! With this approach the branch you were supposed to commit to exists.  

<br/>

- **Get the commit id of the commit.**   
`git log`   
Copy the commit id

<br/>

- **Reset your current branch back by 1 or as many commits you need.**   
`git reset --hard HEAD~1`

<br/>

- **Move the commits to a newbranch**   
`git checkout -b newbranch`

<br/>

- **Checkout to a new branch.**   
`git checkout -b newBranch`

<br/>

- **Move the commits to the new branch**   
`git reset --hard < commit_id >`

<br/>

- **Push both branches with force**    
`git push --force origin newbranch`

<br/>

<hr/>

## _Source:_

- <https://www.clearvision-cm.com/blog/what-to-do-when-you-commit-to-the-wrong-git-branch/>
- <https://stackoverflow.com/questions/572549/difference-between-git-add-a-and-git-add?rq=1>