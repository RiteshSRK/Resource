# Let's Create our Github Account

- ***Create a new account*** or ***log in***
- Create a new ***repository***:

## Configoring Git
```js
git config --global user.name "Your Name"
```
```js
git config --global user.email "someone@email.com"
```

## Clone commands

```bash
# Initialize new local repo
git init  
```

```bash
# Cloning a repository on our local machine
git clone <-some link->
```

```bash
# Display the state of the code
git status
```

---
## Basic commands / Daily Workflow
```bash
# To add files to the staging area
git add  <- file name ->
```

```bash
# Adds all files to staging area
git add .
```

```bash
# Saves changes with messages
git commit -m "some massage"
```

```bash
# Upload local repo content to Remote repo
git push origin main
```

```bash
# First time push karte waqt use hota hai
git push -u origin main
```

```bash
# View your commit history
git log
```

## Git have 4 type of file
### Untracked:
> New files that git doesn't yet track

### Modified:
> Changed

### Staged: 
> file is ready to be commited

### Unmodified:
> Unchanged

---

## Working with GitHub

```bash
# Used to create a new git repo
git init
```

```bash
# Connect local repo to GitHub (only needed once)
git remote add origin <- link ->
```

```bash
# to verify remote
git remote -v
```

```bash
git add .
git commit -m "message"
git push origin main
```

```bash
# Force Push (overwrite remote history)
git push origin main --force
```

---
## Branch Commands

```bash
# to check branch
git branch
```

```bash
# to rename branch
git branch -m main
```

```bash
# switch to a branch
git checkout <-branch name->
```

```bash
# Create and switch to new branch (shortcut)
git checkout -b <-new feature->
```

```bash
# Delete a branch
git branch -d <-branch name->
```

```bash
# Change remote URL
git remote set-url origin https://github.com/RiteshSRK/newJavaScript.git
```

## Merging Code
### 1. Using git
```bash
# to compare commit, branches, files, & more
git diff <-branch name->
```

```bash
# merge two branches
git merge <-branch name->
```

### 2. Create a PR ( `Pull Request` ) in Github
> It lets you tell others about changes you've pushed to a branch in a repository on Github.

### Basic pull Commands 
```bash
git pull origin main
```

> Used to fetch and downdoad Content from a remote repo and immidiately Update the local repo to match that content.

---

## Fixing Mistakes
### Case 1 : staged changes

```bash
# Removes the file from staging
git reset <- file name ->
```

```bash
# Removes the all file from staging
git reset
```

### Case 2 : commited changes (for one commit)

```bash
# go back one step commit
git reset HEAD~1
```

### Case 3 : commited changes (for many commits)

```bash
# HEAD peeche le jata hai, changes unstaged ho jaate hain
git reset <- commit hash ->
```

```bash
# HEAD peeche jata hai aur saare changes delete ho jaate hain ⚠️
git reset --hard <- commit hash ->
```

---

## What is Forking in GitHub?
> Forking ek process hai jisme aap kisi doosre developer ke GitHub repository ka full copy bana lete hain apne GitHub account me, taaki aap us par apne changes bina original project ko affect kiye kar sakein.

> Forking means duplicating someone else's GitHub project into your own account, where we can freely make changes.

### Fork vs Clone:
| Fork                                      | Clone                                               |
| ----------------------------------------- | --------------------------------------------------- |
| Online copy banata hai (GitHub to GitHub) | Local system pe copy banata hai (GitHub to your PC) |
| Mostly GitHub pe hota hai                 | Mostly terminal/VS Code me hota hai                 |
| Required for Pull Requests in open-source | Required for local development                      |

### `git clone` vs `git remote add origin` – Basic Difference
| Command                       | Kya karta hai?                                                                         | Kab use hota hai?                                                                |
| ----------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `git clone`                   | GitHub se **repo ko local machine pe copy** karta hai (aur `origin` bhi set karta hai) | Jab aap **existing repo** se kaam shuru kar rahe ho                              |
| `git remote add origin <url>` | Aapke local repo ko **GitHub repo se connect** karta hai                               | Jab aapne **local se project shuru** kiya ho aur baad me GitHub se link karna ho |

### Real-Life Analogy:
| Situation                                                       | Kaun Use Karein?        |
| --------------------------------------------------------------- | ----------------------- |
| Already bana hua project GitHub pe hai, use leke kaam karna hai | `git clone`             |
| Naya project local me shuru kiya hai, GitHub pe bhejna hai      | `git remote add origin` |


---

## What is Git?
Free & Open Source **Version Control System**
- tools that help to tracks changes in code
1. track history
2. help to collaborate

---

## What is Github?
Website where we host **repositories online**

Made with ❤️ by [Ritesh Gupta](https://github.com/RiteshSRK)
