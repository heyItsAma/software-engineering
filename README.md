# ECE-14-332-452

## USING GIT
### download the current repository
create a directory and cd into it. Afterwards you can clone the repository into your working directory.
```
mkdir workspace
cd workspace
git clone https://github.com/ncm1/ECE-14-332-452
```

### add and commit
You can propose changes (add it to the Index) using
```
git add <filename>   
git add * 
```
This is the first step in the basic git workflow. To actually commit these changes use
```
git commit -m "Commit message"
```
Now the file is committed to the HEAD, but not in your remote repository yet.

### pushing changes

Your changes are now in the HEAD of your local working copy. To send those changes to your remote repository, execute 
```
git push origin master
```
### Branching
Branches are used to develop features isolated from each other. The master branch is the "default" branch when you create a repository. Use other branches for development and merge them back to the master branch upon completion.

reate a new branch named "feature_x" and switch to it using
```
git checkout -b feature_x
```
switch back to master
```
git checkout master
```
and delete the branch again
```
git branch -d feature_x
```
a branch is not available to others unless you push the branch to your remote repository
```
git push origin <branch>
```

### Update and merge
to update your local repository to the newest commit, execute 
```
git pull
```
in your working directory to fetch and merge remote changes.

to merge another branch into your active branch (e.g. master), use
```
git merge <branch>
```
in both cases git tries to auto-merge changes. Unfortunately, this is not always possible and results in conflicts. You are responsible to merge those conflicts manually by editing the files shown by git. After changing, you need to mark them as merged with
```
git add <filename>
```
before merging changes, you can also preview them by using
```
git diff <source_branch> <target_branch>
```

thanks Roger Dudler for the [git-guide](http://rogerdudler.github.io/git-guide/)

## MARKDOWN CHEAT SHEET 
Markdown is what's typically used for README.md pages
[Helpful markdown reference](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) :octocat:
