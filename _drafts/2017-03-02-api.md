---
layout: post
category : travel
tagline: "git reset --hard???"
tags : [bellevue, microsoft ]
---
{% include JB/setup %}

### Another Git Lesson

A lot of teams at Microsoft are moving from Source Depot to Git for their source and version control. I was able to attend a Q&A session for Git and I learned quite a few new things.


It is commonly known to never commit changes on the master branch. A developer creates a branch with their name and the feature. The developer then commits their changes locally via `git add` and `git commit`. Then, `git push origin BRANCH` to the remote repo. Previously, I would locally merge my feature branch into my master branch, push to remote, then submit my pull request (my remote master branch versus the remote master branch of the project). The better way to do it: push your changes to the remote repo using your branch. Then, submit your pull request (my remote feature branch versus the remote master branch of the project). 


What are the advantages for this new workflow? It is easier for the reviewer to test your pull request. The developer can use `git fetch` to review all the branches for the project. You can list all the branches using `git branch -v` and then switch to the desired branch with `git checkout BRANCH`. Once the changes are confirmed, the developer can accept the pull request, which will merge the branches.

### git stash versus git commit

Another topic that came up: when do you use git stash versus git commit? Well, the answer is avoid using `git stash`. It's a convenient command in the sense that you can `git stash` changes on your server, `git pull` changes from the remote repo, then `git stash pop` to reapply those server changes. If your computer or server crashes during the process, you will lose all the changes in git stash. It is best practice to `git add` and `git commit` often as well as `git push origin master` to push to your remote repo. 

### git reset --hard

`git reset --hard` is an important command. It is actually short for `git reset --hard HEAD`. HEAD is a reference to the current branch. If you don't like the changes made, you can rewind back to a previous state using `git reset --hard <COMMIT>`. How do you get the commit hash? `git log`.

### Merge conflicts

What's the best way to handle merge conflicts? Your work flow may vary, but this is what I recommend:

1. `git status` to see what files have conflicts.
2. Open each file one at a time and look for the git conflict markers `<<<<<<< HEAD`, `======`, and `>>>>>>> <COMMIT>`. The `======` marker indicates where your local version conflicts with the other commit version. The code between `<<<<<<< HEAD` and `======` is your local copy (HEAD points to your current branch/commit). The code between `======` and `>>>>>>> <COMMIT>` is the code from another commit. Simply remove the markers and modify the code to the desired result. Stage the files via `git add .` and commit them via `git commit`. 


### First Pull Request!


As I got familiar with the code base, I ran into several setup issues. With the help of my mentor, we were able to solve the issues. We needed to change a config file as well as add another file to .gitignore.


It was a small change, but I got my first pull request accepted in to a substantial code base. :)


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
