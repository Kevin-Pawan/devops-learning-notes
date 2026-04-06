# Day 05 — April 11, 2026

## Course Progress
- Course: Decoding DevOps — Imran Teli
- Section: GIT (Section 5)
- Lectures completed: 40 to 47 (8/8) ✅
- Hours spent: 5 hours

---

## Topics I Studied Today

### Lecture 40 — Git Introduction
Git is a distributed version control system, where the clients and server communicate each other. Each clients can have their own local repo, which means they can make the changes to their local repo and do all the versioning once its good they will sync the local repo to remote server repo(Github).

- It's easy to use tool and commands.
- It provides as a cloud based remote repo (GitHUb).
- In terms of speed, It supports for non liner development.
- It is fully distributed (everyone can have all the copies)
- It is able to handle larger projects.

### Lecture 41 — Versioning
In this lecture, I have created my complete setup in the local computer. Then i used the commands called git init, which creates .git directory it maintains allthe versions, history and configuration data of my git repo.

Then, I have created a few directories and files inside my git repo.
Then I have used the below commands resulted in to integrate my local repo to github repo.

git status
git add .
git commit -m "message"
(If you doing it first time, you need to give you mail and name)
git config --global user.email "email address"
git config --global user.name "user name"

Now if you want to add the local repo to git repo, do the following

git branch -M main (As at first you made a git repo which will be in master)
git remote add origin https URL
git push -u origin main


-- we can clone the repo from github using https and ssh
git clone http url / SSH URL


### Lecture 42 — Branches & More
Branching is nothing but, to maintain the stable code in the main branch. To do that we simply create a new branch which is an exact copy of the main branch. The user will do all the changes in the newly created branch but the main branch is stable. If the user wants to push the same changes to main branch, he can use merge command to do that.

### Lecture 43 — Rollback
You can rollback from the staging stage, before staging stage, after comitting stage using checkout, restore --staged, revert HEAD, rest --hard 

### Lecture 44 — Git SSH Login
To do SSH login, you need to generate the ssh key and copy the public key to the github acc.

### Lecture 45 — Git Tags & Semantic Versioning
learned completely how the developers push the tags along with the commit.

---

## Commands I Learned Today
```bash
# Basic Git
git init                    — initialize new repo
git status                  — check what changed
git add .                   — stage all changes
git add filename            — stage specific file
git commit -m "message"     — save changes with message
git log --oneline           — see commit history short

# Branching
git branch                  — list branches
git branch -c branchname       — create new branch
git checkout or switch branchname     — switch to branch
git checkout -b branchname  — create and switch together
git merge branchname        — merge branch into current

# Remote
git clone url               — download repo
git push origin main        — push to GitHub
git pull origin main        — get latest from GitHub
git remote -v               — see remote URLs

# Rollback
Before staging stage 
git checkout filename
After staging stage
git restore --cached filename
After commit stage
git revert --HEAD commit ID
If you don't want to see the revert commit ID, then use the below.
git reset --hard commit ID

git revert commitid         — undo a commit safely
git reset --hard commitid   — go back to old commit

# Tags
git tag v1.0.0              — create tag
git tag -a tagname -m "message" [commit]
git tag                     — list all tags
git push origin v1.0.0      — push tag to GitHub
```

---

## Hands On Practice I Did Today
I performed complete handson of today lectures successfully.

---

## What Confused Me and How I Fixed It
Git SSH login , git branching

---

## Interview Questions I Can Now Answer
1. What is the difference between git merge and git rebas
2. What does git stash do?
3. How do you undo the last commit without losing changes?
4. What is a branch and why do we use it?
5. What is semantic versioning — what does v2.1.3 mean?

---

## Tomorrow's Plan
- Day 6: Section 6 — Vagrant & Linux Servers (Lectures 48–58)
- Goal: Set up multiple VMs, deploy a website inside VM
- Hands on: Run vagrant up and access website from browser
