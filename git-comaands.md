# Git & GitHub Commands with Examples

---

## 1. Git Configuration
```
git config --global user.name "Your Name"  -> Set your username
git config --global user.email "your@email.com"  -> Set your email
git config --list  -> Show configuration

Example:
git config --global user.name "Manvir Singh"
git config --global user.email "manvir@kubearc.com"
```

---

## 2. Repository Setup
```
git init  -> Initialize repository
git clone <repo-url>  -> Clone from GitHub
git remote add origin <url>  -> Add remote repo

Example:
git clone https://github.com/kubearc/linux-practice.git
git remote add origin https://github.com/kubearc/project.git
```

---

## 3. Track Files
```
git status  -> Show current status
git add <file>  -> Stage specific file
git add .  -> Stage all files
git diff  -> Show unstaged changes

Example:
git add index.html
git diff --staged
```

---

## 4. Commit Changes
```
git commit -m "message"  -> Commit changes
git log  -> View commit history
git show <commit-id>  -> Show commit details

Example:
git commit -m "Added login feature"
git log --oneline
```

---

## 5. Branching & Merging
```
git branch  -> List branches
git branch <name>  -> Create branch
git checkout <name>  -> Switch branch
git merge <name>  -> Merge branch

Example:
git branch dev
git checkout dev
git merge main
```

---

## 6. Push & Pull (GitHub)
```
git push origin <branch>  -> Push to GitHub
git pull  -> Pull latest changes
git fetch  -> Fetch without merge

Example:
git push origin main
git pull
```

---

## 7. Undo & Reset
```
git restore <file>  -> Undo file changes
git reset <file>  -> Unstage file
git reset --hard  -> Remove all local changes
git revert <commit-id>  -> Revert commit safely

Example:
git restore index.html
git revert 7a1f3b2
```

---

## 8. Tagging
```
git tag v1.0  -> Create tag
git tag -a v1.0 -m "Release"  -> Annotated tag
git push origin v1.0  -> Push tag

Example:
git tag -a v1.0 -m "Initial release"
git push origin --tags
```

---

## 9. Stash
```
git stash  -> Save temporary work
git stash pop  -> Reapply stashed work
git stash list  -> List all stashes

Example:
git stash
git stash pop
```

---

## 10. GitHub CLI Commands
```
gh auth login  -> Login to GitHub
gh repo create  -> Create new repo
gh pr create  -> Create pull request

Example:
gh repo create kubearc-app
gh pr create --title "Bug fix" --body "Resolved issue #12"
```

---

## 11. Complete Example Workflow
```
# Step 1: Initialize repo
git init

# Step 2: Add file
echo "Hello World" > index.html
git add .
git commit -m "Initial commit"

# Step 3: Add remote and push
git remote add origin https://github.com/manvir/testrepo.git
git branch -M main
git push -u origin main

# Step 4: Create and merge branch
git checkout -b dev
echo "New feature" >> index.html
git add . && git commit -m "Added feature"
git checkout main && git merge dev
git push origin main
```
