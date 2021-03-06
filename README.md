# Git presentation for people new to Git

### Git is a popular version control system and is widely used.

## Repositories

### A repository is a collection of data (project) which is avaibale online.

To create a new repository on github use the github website.

To pull (copy) a repository you can do this via http or SSL protocol.

SSL allows you to modify the online repository without entering your github password while http does not.

## Setup

Setting up git locally on your machine and connecting to a remote (online) branch is simple

To initialize a branch simply navigate to your project directory and write the following in GitBash

``` cli
git init
```

This created the .git file which stores your history, branches, etc.

To save the files to git (track), first take a look at which files aren't tracked by typing

``` cli
git status
```

This will list all untracked files as red

Now let's add all untracked files

``` cli
git add .
```

Finally we need to commit the tracked files to a local branch

``` cli
git commit -m "Create initial commit"
```

Now your files in this directory are not only saved traditionally but also in git to go back to whenever you want

## Commits

### Commits are how we save changes. Every commit is privided with a description.

The commit message has a convention- It should describe what you are changing and be written in the simple present tense

For instance

``` cli
git commit -m "Add navbar"
```

If you haven't uploaded your changes yet (pushed) you can add to your previous commit afterwards

``` cli
git commit --amend
```

This will prompt you to change the commit message (optional)

Ammending can come in handy if you aren't finished with your commit yet but want to be able to go back to the current state of your application in case you make a mistake.

Don't do amend commits to commits already pushed. This will cause some problems which arent't fatal but are annoying nevertheless.

To undo locally committed changes:

``` cli
git checkout -- dist/404.html
```

To unstage staged changes:

``` cli
git reset dist/404.html
```

When in doubt use both checkout -- and reset

Every commit has a code which allows you to freely navigate to commits in the past and undo changes already commited.

After typing git log navigate the the branch you want to look at by typing

``` cli
git checkout 973hkshf2
```

If you want to undo commits made after this commit type this

``` cli
git reset 973hkshf2
```

Now you still have the 'untracked' changes which you can selectively add or simply delete them completely by typing

``` cli
git reset 973hkshf2 --hard
```

If you made a mistake and want to sync your git up to the remote repository again simply type

``` cli
git pull origin branch-to-pull-to
```

## Stash

### Stashes are the little brother of commits. They are like quicksaves you can go back to later. They are usable and visible locally only.

Be careful though! Stashes don't save file deletions or file creation, only file modifications; so their use is very limited.

When in doubt create a work-in-progress commit and use commit --amend later instead of using stashes

To create a stash first add all your changes with git add... and then write this

``` cli
git stash
```

Don't be suprised, stashes delete your modifications but retain them aswell

To apply your lastest stash, type the following

``` cli
git stash apply
```

In the case you stashed without adding your changes, unexpected results will ensue, so just apply your incorrect stash and stash again

To list all your stashes write this

``` cli
git stash list
```

and to apply a particular stash type this

``` cli
git stash apply stash@{0}
```

and to delete a stash write this

``` cli
git stash drop stash@{0}
```

## Branches

### A branch is a seperate project version. Branches are created to implement different features. For instance you could have the "menu" branch which was created for developers to work on the menu.

Every repository has a master branch which usually has working code.

You can easily create a branch either via github or the cli by entering

``` cli
git checkout -b new-branch-name
```

Note that this branch only exists locally on your machine until you push (upload) it to the repository

``` cli
git push origin new-branch-name
```

To list your local branches type the following

``` cli
git branch
```

To merge a branch, first checkout (switch to) the branch you want to merge to

``` cli
git checkout master
```

and then merge the branch

``` cli
git merge some-feature
```

To delete the merged branch write this

``` cli
git branch -d some-feature
```

## Popular repositories

Github is the most popular free repository hosting service

Popular alternatives are GitLab and BitBucket

git remote add origin git@github.com:seannowotny/laravel-pj-first-project.git

git push -u origin master


## More git commands

``` cli
Git rebase other-branch
```

``` cli
Git remote set-url origin
```

Show difference between commits

``` cli
Git diff asd896ui 978asdf
```

Show commits in graph

``` cli
git log --oneline --graph --author="lalorosas" --grep=#2 --since=1.hour
```


Selectively merge certain commits

``` cli
git cherry-pick as3h5 ag5h jkl5j
```
