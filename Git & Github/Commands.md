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

```js
//  Cloning a repository on our local machine
git clone <-some link->
```

```bash
# Display the state of the code
git status
```

---
## Basic commands
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

```js
# Upload local repo content to Remote repo
git push origin main
```

```bash
# First time push karte waqt use hota hai
git push -u origin main
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

## What is Git?
Free & Open Source **Version Control System**
- tools that help to tracks changes in code
1. track history
2. help to collaborate

---

## What is Github?
Website where we host **repositories online**