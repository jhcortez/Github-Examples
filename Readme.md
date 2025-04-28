

## Git hidden folder
There is a hidden folder called '.git' that tells you our project is a repo.
To create a new repo, create a new folder and run 'git init'
```
mkdir /workspace/temp/new-project
cd /workspace/temp/new-project
git init
touch Readme.md
code Readme.md
git status
git add . 
# make changes to readme.md
git commit -a -m "add readme file"
```
## Cloning
There are 3 ways to clone: HTTPS, SSH, GitHub CLI
Since we are using GitHub CodeSpaces we'll create a temporary directory in our workspace.
```sh
mkdir /workspace/temp
cd /workspace/temp
```
## HTTPS
```sh
git clone https://github.com/jhcortez/Github-Examples.git
cd GitHub-Examples
```
You'll need to generate a Personal Access Token (PAT)
https://github.com/settings/personal-access-tokens
You will use the PAT as your password when you login
Give it access to contents to commits
## SSH
```ssh
git clone git@github.com:jhcortez/Github-Examples.git
cd GitHub-Examples
```
We will need to create our own SSH rsa key pair
```ssh
ssh-keygen -t rsa
```
For WSL users and if you create a non default key you might need to add it
```ssh
eval `ssh-agent`
ssh-add /home/codespace/.ssh/id_rsa
```
We can test our connection here:
```
ssh -T git@github.com
```
```
gh auth login
gh repo clone jhcortez/Github-Examples
```
## Commits
When we want to commit code we can write git commit which will open uo the commit edit message in the editor of choice.
```sh
git commit
```
Set the global editor
```
git config --global core.editor emacs
```
Make the commit and commiting message withour opening an editor
```sh
git commit -m "Add another message"
```
## Branches

```
git branch
```

Create a new branch
```
git branch branch-name
```

Checkout branch

```
git checkout branch-name
```

## Remote
## Stashing
## Merging
## Add
When we want to stage changes that will be included in the commit we can use the . to add all possible files.
```
git add Readme.md
git add .
```
## Reset
Reset allows you to move staged changed to unstaged. 
```
git add .
get reset
```
git reset will revert a git add .
## Status
Git status shows you what files will or will not be commited.
```
git status
```
## Gitconfig file
The gitconfig file is what stored your global configurations for git such as email, name, editor and more.
Showing the contents of our .gitconfig
```
git config --list
```
When your first install git on a machine you are supposed yo set up your name and email
```sh
git config --global user.name "John Doe"
git config --global user.name johndoe@example.com
```
## Log
git log will show recent commits to the git tree
```
git log
```
## Push
When we want to push a repo to our remote origin
```
git push
```




## Git hidden folder
There is a hidden folder called '.git' that tells you our project is a repo.
To create a new repo, create a new folder and run 'git init'
```
mkdir /workspace/temp/new-project
cd /workspace/temp/new-project
git init
touch Readme.md
code Readme.md
git status
git add . 
# make changes to readme.md
git commit -a -m "add readme file"
```
## Cloning
There are 3 ways to clone: HTTPS, SSH, GitHub CLI
Since we are using GitHub CodeSpaces we'll create a temporary directory in our workspace.
```sh
mkdir /workspace/temp
cd /workspace/temp
```
## HTTPS
```sh
git clone https://github.com/jhcortez/Github-Examples.git
cd GitHub-Examples
```
You'll need to generate a Personal Access Token (PAT)
https://github.com/settings/personal-access-tokens
You will use the PAT as your password when you login
Give it access to contents to commits
## SSH
```ssh
git clone git@github.com:jhcortez/Github-Examples.git
cd GitHub-Examples
```
We will need to create our own SSH rsa key pair
```ssh
ssh-keygen -t rsa
```
For WSL users and if you create a non default key you might need to add it
```ssh
eval `ssh-agent`
ssh-add /home/codespace/.ssh/id_rsa
```
We can test our connection here:
```
ssh -T git@github.com
```
```
gh auth login
gh repo clone jhcortez/Github-Examples
```
## Commits
When we want to commit code we can write git commit which will open uo the commit edit message in the editor of choice.
```sh
git commit
```
Set the global editor
```
git config --global core.editor emacs
```
Make the commit and commiting message withour opening an editor
```sh
git commit -m "Add another message"
```
## Branches

List of branches

```
git branch
```

Create a new branch

```
git branch branch-name
```

Checkout branch

```
git checkout branch-name
```

## Remote

Usually add remote via upstream when adding a branch

```sh
git remote add ...
git branch -u origin new-feature
```

## Stashing

```
git stash list
git stash
git stash save stash-name
git stash apply
git stash pop
```
## Merging

```
git checkout branch-name
git merge main
```
## Add
When we want to stage changes that will be included in the commit we can use the . to add all possible files.
```
git add Readme.md
git add .
```
## Reset
Reset allows you to move staged changed to unstaged. 
```
git add .
get reset
```
git reset will revert a git add .
## Status
Git status shows you what files will or will not be commited.
```
git status
```
## Gitconfig file
The gitconfig file is what stored your global configurations for git such as email, name, editor and more.
Showing the contents of our .gitconfig
```
git config --list
```
When your first install git on a machine you are supposed yo set up your name and email
```sh
git config --global user.name "John Doe"
git config --global user.name johndoe@example.com
```
## Log
git log will show recent commits to the git tree
```
git log
```
## Push
When we want to push a repo to our remote origin
```
git push
```

