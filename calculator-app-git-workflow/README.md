# 🧮 Calculator App — Professional Git Workflow Practice

A C++ demonstration project built to practice and master the **Full Production Git & GitHub Workflow**, including local repository management, remote synchronizations, feature branching, and Pull Requests (PR).

---

## 🎯 Project Overview & Objectives

The goal of this repository is to demonstrate a real-world software development lifecycle (SDLC) using Git version control and GitHub. 

Key concepts practiced in this project:
- Setting up a local repository and tracking C++ application files.
- Connecting local repositories to a remote origin on GitHub.
- Simulating online remote changes and pulling updates locally (`git pull`).
- Applying **Feature Branching Strategy** to write code isolated from `main`.
- Opening, reviewing, and merging **Pull Requests (PR)** on GitHub.
- Maintaining branch synchronization post-merge.

---

## 💻 Codebase Features

Written in modular **C++**, the application currently includes:
- [x] **Addition Functionality:** Adds two integers and displays the result.
- [x] **Subtraction Functionality:** Added via feature branch (`feature-subtract`) and merged through PR review.

---

## 🛠️ Step-by-Step Git Workflow Executed

Here is the complete sequence of commands and workflow steps executed during the project lifecycle:

```bash
1️⃣ Local Setup & Initial Commit

# Create project directory and initialize Git
mkdir calculator-app && cd calculator-app
git init

# Stage files and create first snapshot
git add .
git commit -m "Initial commit: Add main.cpp and base README"




2️⃣ Remote Linking & Initial Push

# Link local repo to remote GitHub origin and set default branch
git remote add origin [https://github.com/.../... .git
git branch -M main
git push -u origin main




3️⃣ Simulating Remote Changes & Pulling

# Fetch and merge updates made directly on GitHub
git status
git pull




4️⃣ Feature Branching Strategy

# Create and switch to a dedicated feature branch for subtraction
git switch -c feature-subtract

# Stage and commit feature changes
git add main.cpp
git commit -m "Add subtract function"

# Push feature branch to GitHub
git push -u origin feature-subtract




5️⃣ Pull Request & Post-Merge Synchronization

Opened a Pull Request on GitHub (base: main ⟵ compare: feature-subtract).

Reviewed code diffs and executed merge into main.

Synchronized local main branch:

git switch main
git pull




🧠 Core Learnings & Best Practices

Never Commit Directly to Main: Isolate new features in short-lived branches (feature-*).

Direction Matters: Always verify PR merge direction (main as the base target).

Keep Local Sync: Always run git pull on main after merging PRs online to avoid merge conflicts.
