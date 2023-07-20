
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
Git A/c          : gitaccount
Git Repository   : git@github.com:gitaccount/gitrepo.git
```


## Create a folder .ssh under C:\Users\Admin 
```
C:\Users\Admin\.ssh
```

## Create a new SSH Key ( Private and Public key pair)

<p>Go to the folder C:\Users\Admin\.ssh, then issue below command</p>

```
ssh-keygen -t rsa -C "your_email@example.com"
//above command will ask for the name of file and passkey, you can ignore the passkey.
// And it will create two files 
//user1      => private key file
//user1.pub  => public  key file 
now extract the content of user1.pub and update it in git site
open git web site, then under settings/SSH and GPG keys add a new SSH key and update the key
and you can give any title
```

## Create config file
<p>
Create a file config under the .ssh folder and enter below lines
</p>

```
# User1
HOST github.com-[user1]
HOSTNAME github.com
USER git
IdentityFile  ~/.ssh/user1
```

## Identifying multiple git accounts
<p>
you can give an identifier at the end of the host by entering a hyphen and an identifier
.the same will be used while refereing the git url
</p>

## Multiple git account settings
```
HOST github.com-[user1] 
git@github.com-[user1]:gitaccount/gitrepo.git
```

## Clone Git Repository
<p> goto a local folder and enter below command to clone a git repository </p>

```
git clone git@github.com-[user1]:gitaccount/gitrepo.git
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

## change https url to ssh / ssh to https url
```
git remote -v // will show the current remote url
git remote set-url origin git@github.com-[user1]:gitaccount/gitrepo.git 
git remote set-url origin https://github.com/gitaccount/gitrepo.git

```

## Git Commands
```
// add all files or single file to repository
git add .
git add filename
// Commit files to repository
git commit -am "save"
// push the changes to repository
git push
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
