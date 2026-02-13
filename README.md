# Learning Git & GitHub Basics

Welcome! This repository teaches the fundamentals of Git and how to push your work to GitHub. It is designed for beginners and focuses on small, practical steps.

## What you will learn
- What Git is and why it is useful
- How to track changes with commits
- How to create and use branches
- How to connect a local project to GitHub
- How to push and pull changes

## Prerequisites
- A GitHub account
- Git installed on your computer
- A code editor (VS Code recommended)

## Quick start (first-time setup)
1. **Configure Git (once per machine)**
	```bash
	git config --global user.name "Your Name"
	git config --global user.email "you@example.com"
	```

2. **Create a project folder and initialize Git**
	```bash
	mkdir my-first-repo
	cd my-first-repo
	git init
	```

3. **Create a file and make your first commit**
	```bash
	echo "Hello Git" > README.md
	git add README.md
	git commit -m "Add first README"
	```

4. **Create a repository on GitHub**
	- Go to https://github.com/new
	- Name it the same as your folder (optional, but helpful)
	- Do **not** add a README if you already created one locally

5. **Connect local repo to GitHub and push**
	```bash
	git remote add origin https://github.com/<your-username>/my-first-repo.git
	git branch -M main
	git push -u origin main
	```

## Core Git commands (cheat sheet)
| Command | What it does |
|---|---|
| `git status` | Shows current changes and branch |
| `git add <file>` | Stages a file for commit |
| `git commit -m "message"` | Saves a snapshot of staged changes |
| `git log --oneline` | Shows commit history |
| `git branch` | Lists branches |
| `git checkout -b <name>` | Creates and switches to a new branch |
| `git merge <branch>` | Merges a branch into the current branch |
| `git remote -v` | Shows remote URLs |
| `git push` | Uploads local commits to GitHub |
| `git pull` | Downloads and merges remote changes |

## Learning path
Work through these in order:
1. [Getting started](#quick-start-first-time-setup)
2. [Making commits](#core-git-commands-cheat-sheet)
3. [Working with branches](#branching-workflow)
4. [Pushing to GitHub](#pushing-to-github)
5. [Pulling updates](#pulling-updates)

## Branching workflow
1. Create a branch
	```bash
	git checkout -b feature/my-change
	```
2. Make changes and commit
	```bash
	git add .
	git commit -m "Describe the change"
	```
3. Merge back to main
	```bash
	git checkout main
	git merge feature/my-change
	```

## Pushing to GitHub
```bash
git push origin main
```

## Pulling updates
```bash
git pull origin main
```

## Common mistakes and fixes
- **Forgot to add files before committing**
  ```bash
  git add .
  git commit -m "Your message"
  ```
- **Pushed to the wrong branch**
  ```bash
  git checkout correct-branch
  git cherry-pick <commit-hash>
  ```
- **Need to undo the last commit (not pushed)**
  ```bash
  git reset --soft HEAD~1
  ```

## Contributing
Contributions are welcome! Open an issue or submit a pull request with improvements.

