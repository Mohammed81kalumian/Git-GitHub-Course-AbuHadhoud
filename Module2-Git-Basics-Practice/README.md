# Module 2: Basic Git Workflow & File Lifecycle Practice

## 📌 Overview
Documenting my step-by-step hands-on practice for Git fundamentals, file lifecycle tracking, and commit management from Abu Hadhoud's Git & GitHub Course.

---

## 🛠️ Step-by-Step Practice Log

### 🔹 Stage 1: Setup & Repository Initialization (Steps 1–3)
- **Step 1 (Folder Creation):** Created project folder `Module02-Git-Basics-Practice`.
- **Step 2 (Git Init):** Executed `git init` to initialize local repository tracking (created hidden `.git` folder).
- **Step 3 (Status Check):** Ran `git status` to verify working directory status on the default branch before adding any files.
 
### 🔹 Stage 2: File Creation & Staging (Steps 4–7)
- **Step 4 (Initial Status Check):** Ran `git status` to confirm working directory status before file creation.
- **Step 5 (Creating Files):** Created `index.html` (with HTML header content) and `notes.txt` (with plain text note).
- **Step 6 (Untracked Status Inspection):** Executed `git status` and observed that Git identified both new files as **Untracked**.
- **Step 7 (Staging Changes):** Ran `git add .` to move all new files into the **Staging Area**.
 
### 🔹 Stage 3: First Commit & File Modification (Steps 8–11)
- **Step 8 (Staged Status Verification):** Ran `git status` to verify that files moved to the Staging Area (ready to be committed).
- **Step 9 (First Commit):** Created the initial project snapshot using `git commit -m "Initial project files"`.
- **Step 10 (Commit History Inspection):** Checked the concise commit history using `git log --oneline` to confirm the snapshot hash and commit message.
- **Step 11 (Modifying Content):** Updated `notes.txt` by adding the new line `Learning Git step by step.` to introduce changes to the Working Directory.
 
### 🔹 Stage 4: Unstaged vs Staged Diff Inspections (Steps 12–15)
- **Step 12 (Modified Status Check):** Ran `git status` to observe `notes.txt` identified as modified in the Working Directory.
- **Step 13 (Viewing Unstaged Changes):** Executed `git diff` to inspect the exact unstaged modifications added to `notes.txt`.
- **Step 14 (Targeted Staging):** Staged only the specific modified file using `git add notes.txt`.
- **Step 15 (Viewing Staged Changes):** Ran `git diff --staged` to verify the prepared changes before making a commit.
 
### 🔹 Stage 5: Second Commit, Commit Inspection & Index Updates (Steps 16–19)
- **Step 16 (Second Commit):** Created a second snapshot for the notes update using `git commit -m "Update notes file"`.
- **Step 17 (Log History Verification):** Ran `git log --oneline` to view the growing commit history timeline.
- **Step 18 (Inspecting Specific Commit):** Used `git show <COMMIT_ID>` to inspect author details, timestamp, and specific code diffs of a single commit snapshot.
- **Step 19 (Modifying Index Page):** Updated `index.html` by adding a paragraph line `<p>This project is for Git practice.</p>` to simulate further project developments.
 
### 🔹 Stage 6: Index Modifications & Staged Inspections (Steps 20–23)
- **Step 20 (Status Verification):** Executed `git status` to verify modified state for `index.html`.
- **Step 21 (Reviewing Unstaged Changes):** Ran `git diff` to view the paragraph addition in `index.html` within the Working Directory.
- **Step 22 (Staging HTML Update):** Prepared `index.html` for commit using `git add index.html`.
- **Step 23 (Reviewing Staged Changes):** Executed `git diff --staged` to confirm the prepared HTML change before committing.
 
### 🔹 Stage 7: Third Commit, File Summary & Renaming Mechanics (Steps 24–27)
- **Step 24 (Third Commit):** Saved index changes to Git history using `git commit -m "Update index page"`.
- **Step 25 (Viewing History with File Stats):** Executed `git log --oneline --stat` to review commit logs along with modified file statistics.
- **Step 26 (Renaming File):** Renamed `notes.txt` to `project-notes.txt` to test Git's rename tracking behavior.
- **Step 27 (Renamed Status Inspection):** Ran `git status` to observe how Git initially identifies a normal file rename as a deleted file and a new untracked file before staging.

### 🔹 Stage 8: Staging Rename & Heavy File Relocation (Steps 28–31)
- **Step 28 (Staging Renamed File):** Ran `git add .` to allow Git to evaluate file content similarity.
- **Step 29 (Staged Summary Inspection):** Executed `git diff --staged --summary` to confirm Git detected the file rename (`notes.txt => project-notes.txt`).
- **Step 30 (Committing Rename):** Saved the rename snapshot to history using `git commit -m "Rename notes file"`.
- **Step 31 (File Relocation & Heavy Modification):** Created a `docs/` folder, moved `project-notes.txt` into `docs/project-notes.txt`, and made extensive content modifications.

### 🔹 Stage 9: Final Status, Staging & Complete Commit Log (Steps 32–36)
- **Step 32 (Post-Move Status Inspection):** Ran `git status` to observe how Git handles heavily modified and relocated files (detecting changes based on similarity score).
- **Step 33 (Staging Relocated Changes):** Staged the moved folder structure and updated content using `git add .`.
- **Step 34 (Staged Diff Summary):** Executed `git diff --staged --summary` to inspect the final change classification (rename vs delete/create).
- **Step 35 (Final Commit):** Saved the relocated file and content update using `git commit -m "Move notes file and update content"`.
- **Step 36 (Complete History Verification):** Verified the entire project timeline and overall file changes across all commits using `git log --oneline --stat`.




---

## 🎯 Key Concepts & Observations

As I progressed through this hands-on practice, I specifically focused on observing and mastering the following Git behaviors:

- 🔹 **Multi-File Tracking:** Understanding how Git continuously monitors multiple files across different statuses simultaneously.
- 🔹 **File Lifecycles:** Differentiating between **Untracked** files (new) and **Modified** files (existing tracked files with changes).
- 🔹 **Working Directory vs. Staging Area:** Recognizing the core isolation between working space changes and prepared snapshots.
- 🔹 **Unstaged Changes Inspection:** Utilizing `git diff` to review raw modifications prior to staging.
- 🔹 **Staged Changes Inspection:** Utilizing `git diff --staged` to verify finalized changes ready for snapshot.
- 🔹 **Commit Snapshots:** Learning how every individual commit represents a permanent, immutable point-in-time snapshot.
- 🔹 **Timeline Visualization:** Using `git log --oneline` to navigate and interpret the project's historical timeline concise view.
- 🔹 **File Impact Summaries:** Using `git log --oneline --stat` to evaluate history along with precise file-by-file impact summaries.
- 🔹 **Deep Snapshot Inspection:** Inspecting precise line-by-line diffs and author metadata of a specific commit using `git show`.

---

## 🏁 Final Outcomes & Hands-On Achievements

Upon completing this 36-step workflow practice, I have successfully accomplished and mastered:

### 📦 Repository State
- 🔹 A fully configured local Git repository tracking multiple files.
- 🔹 A structured history timeline containing multiple clear commits.
- 🔹 Successfully modified, staged, and committed text files (`.txt`).
- 🔹 Successfully modified, staged, and committed web pages (`.html`).

### 🛠️ Command Mastery & Practical Skills
- 🔹 **Repository Initialization:** Hands-on experience with `git init`.
- 🔹 **Status Monitoring:** Hands-on experience with `git status`.
- 🔹 **Bulk Staging:** Hands-on experience with `git add .`.
- 🔹 **Targeted Staging:** Hands-on experience with `git add <filename>`.
- 🔹 **Snapshot Creation:** Hands-on experience with `git commit -m`.
- 🔹 **Working Diff Analysis:** Hands-on experience with `git diff`.
- 🔹 **Staged Diff Analysis:** Hands-on experience with `git diff --staged`.
- 🔹 **Concise Log Navigation:** Hands-on experience with `git log --oneline`.
- 🔹 **Stat Log Navigation:** Hands-on experience with `git log --oneline --stat`.
- 🔹 **Single Commit Inspection:** Hands-on experience with `git show`.
