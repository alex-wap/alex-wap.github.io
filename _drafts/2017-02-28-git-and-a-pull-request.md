---
layout: post
category : travel
tagline: "git reset --hard???"
tags : [bellevue, microsoft ]
---
{% include JB/setup %}

### Another Git Lesson

A lot of teams at Microsoft are moving from Source Depot to Git for their source and version control. I was able to attend a Q&A session for Git and I learned quite a few new things.


It is commonly known to never commit changes on the master branch. A developer creates a branch with their name and the feature. The developer then commits their changes locally via `git add` and `git commit`. Then, `git push origin BRANCHNAME` to the remote repo. Previously, I would locally merge my feature branch into my master branch, push to remote, then submit my pull request (my remote master branch versus the remote master branch of the project). The better way to do it: push your changes to the remote repo using your branch. Then, submit your pull request (my remote feature branch versus the remote master branch of the project).

create branch - stage changes via add - commit locally - push remote branch - pr via remote branch (to merge into remote master) 

test locally PR - git fetch - git checkout BRANCH

danger of git stash vs git commit 
computer crash - lost commit

git reset --hard

default way to handle merge conflicts
-git status, open each file, look for >>>>>> ==== <<<<<

### First Pull Request!

simple but necessary
adding to gitignore
config change

### API Provider

cant talk about what service

holes in the api

inconsistant 

unclear

clarification

### Fat Tuesday

Boardwalk
crab hush puppies
live music

---
