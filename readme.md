
# Git Hub Tutorial

## Git Hub Site
#### https://github.com
## Download Git
#### https://git-scm.com/downloads

## Git config name and email

```
git config user.name "YOUR_USER_NAME"
git config user.email "YOUR_EMAIL"

git config --global user.name "YOUR_USER_NAME"
git config --global user.email "YOUR_EMAIL"
```


## Git Branching and merging
<p>
Branching is used to create a working folder (branch) where you can do changes and later when completed it can be merged to the original master branch. Below is a set of commands to create a branch namely hotfix then it is merged to master branch
</p>

```
git branch   hotfix
git checkout hotfix
git checkout master
git merge    hotfix
git branch -d hotfix
```
