# Bite-sized coding wisdom learned the hard way


## Set Git to use macOS Keychain to remember Token and avoid entering it every time:
```bash 
git config --global credential.helper osxkeychain
```


## Push code for first time:
```bash 
git push -u origin main 
```
-u sets it as default for future pushes, every push after: git push


## Possible to check name of default branch: 
``` bash
git branch
```


## In case of error 'invalid user name and password' after command 'git push -u origin main' without a prompt for entering them, could mean that Git tried to use saved credentials (e.g. expired Token) and error was handled internally by e.g. VS Code


## Force Git to prompt for credentials when pushing:
```bash 
GIT_TERMINAL_PROMPT=1 git push -u origin main
```


## Git remote can be removed and added again:
```bash 
git remote remove origin
git remote add origin https://github.com/username/repo-name.git
```


## Stored Git credentials can be searched for and deleted for example: 
> open Keychain Access App on Mac (Applications > Utilities), select login on
left hand side and Passwords tab and search for 'git'. Right click on name to delete, copy, etc. 
> Delete might help for authentication problems to enter a token fresh.


## Most Github actions can be done inside VS code


## Sign into GitHub in VS Code, even if you only use bash commands it has benefits and VS Code usually remembers your GitHub sign-in:
> Cmd + Shift + P 
> Enter: GitHub: Sign In


## Username and password (=Token) are only required when pushing code with HTTPS not with SSH


## If renaming a repository on Github, the local repo's remote needs to be updated:
```bash 
git remote set-url origin https://github.com/username/new-repo-name.git
```


## Search for Git user.name (shown in commit history) and user.email:
```bash
git config --global --list
```


## Cheat sheet for basic Git commands:
Action	             Command
Check status	     git status
Add all changes	     git add .
Add specific file	 git add filename.py
Commit changes	     git commit -m "Describe changes"
View history	     git log
Short log	         git log --oneline
Push changes	     git push
Pull latest changes	 git pull
