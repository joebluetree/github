
# Git Hub Tutorial

## Git Hub Site
#### https://github.com
## Download Git
#### https://git-scm.com/downloads



## Setup a git account in local computer

<p>
Download and install git from site https://git-scm.com/downloads
</p>

<p>
Kindly create a git hub account and a git repository. Below is a sample a/c and repository
</p>

```
Git A/c          : ghaccount
Git Repository   : git@github.com:ghaccount/github.git
```


## Create a folder .ssh under C:\Users\Admin 
```
C:\Users\Admin\.ssh
```

## Create a new SSH Key ( Private and Public key pair)

<p>Open a dos command prompt and move to the folder C:\Users\Admin\.ssh, then issue below command</p>

```
ssh-keygen user1
//above command will create two files 
//user1      => private key file
//user1.pub  => public  key file 
now extract the content of user1.pub and update it in git site
open git web site, then under settings/SSH and GPG keys add a new SSH key and update the key
```

## Create config file
<p>
Create a file config under the .ssh folder and enter below lines
</p>

```
# User1
HOST github.com
HOSTNAME github.com
USER git
IdentityFile  ~/.ssh/user1
```

## Clone Git Repository
<p> goto a local folder and enter below command to clone a git repository </p>

```
git clone git@github.com:ghaccount/github.git
// use dos command to goto the clonned folder and set the default user name and email

```


## Set default name and email
<p>
Use below commands to set default user name and email id, which can be set globally or ocal folder only
</p>

```
git config user.name "YOUR_USER_NAME"
git config user.email "YOUR_EMAIL"

git config --global user.name "YOUR_USER_NAME"
git config --global user.email "YOUR_EMAIL"
```

## Git Commands
```
// add  files to repository
git add .
git add filename
// Commit files to repository
git commit -am "save"
// push the changes to repository
git push origin master
// pull changes from repository to local computer
git pull
```

## Git Branching and merging
<p>
Branching is used to create a working folder (branch) where you can do changes and later when completed it can be merged to the original master branch. Below is a set of commands to create a branch namely hotfix then it is merged to master branch
</p>

```
// Create a branch hotfix
git branch   hotfix
// move to gotfix branch
git checkout hotfix
// move back to master branch
git checkout master
// merge hotfix branch to master branch
git merge    hotfix
// remove hotfix branch
git branch -d hotfix
```
