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
git log ${filename} 
# or
git log
```
- View diff
```bash
git diff ${commit-tag1} ${commit-tag2}
# Example
git diff aca9c0f e90f25e
```
- Go back in time
```bash
# reset
git reset ${commit-tag}
# reset hard
git reset ${commit-tag} --hard # this delete the current version and it go to a previous version (commit-tag)
# checkout}
git checkout ${commit-tag} README.md # get from previous commit and replace to a file
git checkout master README.md # get from a branch and replace to a file
```

- connect to a remote repository
```bash
# First: Save the GitHub repository URL
# with the original name
git remote add origin URL

# Second: Verify that the URL has been saved
# correctly:
git remote
git remote -v

# Third: Fetch the version from the remote repository and
# merge to create a commit with the files
# from both sides. We can use git fetch and git merge
# or just the git pull with the --allow-unrelated-histories flag:
git pull origin main --allow-unrelated-histories

# Finally, now we can do git push to save
# changes from our local repository on GitHub: 
git push origin master
```
- View commits tree
```bash
git log --all --graph --decorate --oneline
```
- Create tags
```bash
# create
git tag -a ${tag-name} -m "message" ${commit-tag}
# delte tag from repository
git tag -d ${tag-name}
# list tags
git show-ref --tags
# or 
git tag
# Publish tags to remote repository
git push origin --tags
# Delete tags from remote repository
git tag -d ${tag-name} && git push origin :refs/tags/${tag-name}
```