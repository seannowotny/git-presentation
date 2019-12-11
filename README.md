# Git for people new to Git :)

Git is a popular version control system and is widely used

## Repositories

A repository is a collection of data (project) which is avaibale online

To create a new repository on github use the github website

To pull (copy) a repository you can do this via http or SSL protocol

SSL allows you to modify branches of the online repository without entering your github password while http does not

## Branches

Every repository has a master branch which usually has working code

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
