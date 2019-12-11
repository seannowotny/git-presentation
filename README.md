# Git for people new to Git :)

Git is a popular version control system and is widely used.

## Repositories

A repository is a collection of data (project) which is avaibale online.

To create a new repository on github use the github website.

To pull (copy) a repository you can do this via http or SSL protocol.

SSL allows you to modify branches of the online repository without entering your github password while http does not.

## Setup

Setting up a local repository on your machine and connecting to a remote (online) branch is simple

To initialize a branch simply navigate to your project directory and write the following

′′′ cli
git init
′′′

This created the .git file which stores your history, branches, etc.

To save the files to git (track), first take a look at which files aren't tracked by typing

′′′ cli
git status
′′′

This will list all untracked files as red

Now let's add all untracked files

′′′ cli
git add .
′′′

Finally we need to commit the tracked files to a local branch

′′′ cli
git commit -m "Create initial commit"
′′′

The commit message has a convention- It should describe what you are changing

For instance "Add navbar"

## Branches

A branch is a seperate project version. Branches are created to implement different features. For instance you could have the "menu" branch which was created for developers to work on the menu.

Every repository has a master branch which usually has working code.

You can easily create a branch either via github or the cli by entering

′′′ cli
git checkout -b new-branch-name
′′′

Note that this branch only exists locally on your machine until you push (upload) it to the repository

′′′ cli
git push origin new-branch-name
′′′

To list your local branches type the following

′′′ cli
git branch
′′′

To merge a branch, first checkout (switch to) the branch you want to merge to

′′′ cli
git checkout master
′′′

and then merge the branch

′′′ cli
git merge dev
′′′

## Popular repositories

Github is the most popular free repository hosting service

Popular alternatives are GitLab and BitBucket

git remote add origin git@github.com:seannowotny/laravel-pj-first-project.git

git push -u origin master



Git init

Git add .

Git commit -m

git commit --amend --no-edit

Git push origin master

Git checkout other-branch

Git checkout -b my-new-branch

Git merge other-branch

Git rebase other-branch

Git clone

Git remote set-url origin ...



Git diff asd896ui 978asdf

Git show HEAD^

git log --oneline --graph --author="lalorosas" --grep=#2 --since=1.hour

Git annotate my_file



git checkout -- dist/404.html		//Undo unstaged changes

git reset dist/404.html			//Undo staged changes

git checkout HEAD^ dist/404.html	//Undo pushed changes

git checkout -B add-bootstrap		//Set branch to HEAD position



git clean -fX

git clean -fd



git fetch

git checkout --track origin/test



git branch -d add-bootstrap



git tag -a v1.0 12asd6hk "First Public Release"

git push origin --tags



git cherry-pick as3h5 ag5h jkl5j



from google.colap import drive

drive.mount('/content/drive')


git stash --include-untracked save "Worked on add function"

git stash apply stash@{0}

// Undo stash apply

$ git stash show -p stash@{0} | git apply -R

git stash drop stash@{0}
