## Git Hidden Files
We can indicate that the project is a Git repo by adding a `.git` folder
The folder can be initialized using `git init`

The following shows how to create a project in a temporary directory in a Workspace, create a readme file, and commit to the repo
```sh
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init
touch README.md
code README.md
# Make changes to README.md
git status
git add README.md
git commit -m "added readme file" 
```

## Cloning
We can clone using HTTPS, SSH, or GitHub CLI
Using the Workspaces, we would clone the repo into a temp directory

```sh
mkdir /workspaces/tmp
cd /workspaces/tmp
```

### HTTPS
To clone this repo, for example, use this:

```sh
git clone https://github.com/baba-tope/GitHub-Demo-Lab.git
```

Use Personal Access Token to authenticate if using a local machine
https://www.github.com/settings/tokens


### SSH
To clone a private repo to your local machine, use the following
```ssh
git clone git@github.com:$USER_NAME/REPO_NAME.git
cd REPO_NAME
```

SSH authentication requires keypair generated and added to the GitHub account
```sh
ssh-keygen -t rsa
```

Test the connection
```sh
ssh -T git@github.com
```

Add key to local machine key storage
```sh
ssh-add /home/$USER/.ssh/PRIVATE_KEY
```

### GitHub CLI


## Commits
To commit the code and write a message for context, use `git commit`

```sh
git commit
```

## Branches

## Remotes

## Stashing

## Merging

## Git Status
Use the `git status` to view the tracked changes and what would be committed to the repo.

```sh
git status
```

## Git Add
When you want to add files to the staging area, use `git add`
```sh
git add README.md
git add .
```

## Git Reset

Reset allows you to change staged changes to unchanged (backtracking).
```sh
git reset
```

## Git Config

Use `git config` to set the email, name, editor, etc.

To view and set up config file:
```sh
git config --list
```

To show origin:
```sh
git config --list --show-origin
```

When you set up Git on your machine, you should set up the global config:
```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor emacs
```

## Git Log
To show recent commits to the tree, use `git log`

```sh
git log
```

## Git Push
To push code to the remote origin, use `git push`

```sh
git push
```