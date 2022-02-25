# Re-learning-git-and-github
I'm relearning and implementing a simple web app

## Git configuration
- View git config
```bash
git config --list
```
- View config origin
```bash
git config --list --show-origin
```
- Config user
```bash
# user fullname
git config --global user.name "Willy Samuel Paz Colque"
# user Email
git config --global user.email "samuelpaz243@gmail.com"
```

## Commands
- remove cached file:    
```bash
git rm --cached main.py
```

- View commits log
```bash
git log <filename>
# or
git log
```
- View diff
```bash
git diff <commit-tag-1> <commit-tag-2>
# Example
git diff aca9c0f e90f25e
```

- Go back in time
```bash
# reset
git reset <commit-tag>
# reset hard
git reset <commit-tag> --hard # this delete the current version and it go to a previous version (commit-tag)
# checkout
```
