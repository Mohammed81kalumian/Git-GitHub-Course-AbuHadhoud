# 🎓 Student Grades System

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

An enterprise-grade reference documenting advanced **Git undo workflows, history manipulation, and staging lifecycle management** across a 10-stage simulation.

---

## 🧭 Git Operations Matrix



| Part | Scenario Target | Key Command | Safety Level |
| :---: | :--- | :--- | :---: |
| **01** | Initial Baseline Setup | `git init && git commit` | 🟢 Safe |
| **02** | Discard Unstaged File Edits | `git restore <file>` | 🟡 Destructive (Local) |
| **03** | Unstage File from Index | `git restore --staged <file>` | 🟢 Safe |
| **04** | Amend Recent Commit Message | `git commit --amend -m` | 🟢 Safe (Local) |
| **05** | Attach Forgotten File to Commit | `git commit --amend --no-edit` | 🟢 Safe (Local) |
| **06** | Cherry-pick Historical File Version | `git restore --source=<hash> <file>` | 🟢 Safe |
| **07** | Soft Reset (Keep Staged Index) | `git reset --soft HEAD~1` | 🟢 Safe |
| **08** | Mixed Reset (Keep Working Tree) | `git reset --mixed HEAD~1` | 🟢 Safe |
| **09** | Hard Reset (Complete Purge) | `git reset --hard HEAD~1` | 🔴 Destructive |
| **10** | Public History Reversion | `git revert HEAD` | 🟢 Public Safe |

---
```
 

1. Initial Baseline

Set up project tracking and create the foundational commit.
git init
git add .
git commit -m "Initial clean project setup"




2. Local File Recovery

Revert uncommitted, bad edits in main.cpp back to the last clean index state.
git restore main.cpp
git status




3. Index De-staging

Remove accidentally staged notes.txt from the index while preserving local modifications.
git restore --staged notes.txt
git commit -m "update"




4. Commit Message Correction

Overwrite vague log message ("update") without generating an unnecessary log node.
git commit --amend -m "Improve the grade output message"




5. Commit Payload Expansion

Inject missing README.md into the latest commit without changing its commit message.
git add README.md
git commit --amend --no-edit




6. Point-in-Time File Extraction

Retrieve historical main.cpp from baseline commit 5ac0dee without rewinding tree state.
git restore --source=5ac0dee main.cpp
git add main.cpp
git commit -m "Part 6: Restore main.cpp to original clean version





7. Soft Rollback (--soft)

Undo commit "add status", retaining changes in the Staging Area for re-committing.
git reset --soft HEAD~1
git commit -m "Add student status output"




8. Mixed Rollback (--mixed)

Undo accidental commit on notes.txt, dropping changes back to Working Directory for review.
git reset --mixed HEAD~1 of Commit Hash
git status




9. Hard Purge (--hard)

Permanently destroy commit and purge physical broken test code from disk.
git reset --hard HEAD~1 or Commit Hash




10. Non-Destructive Public Revert
Safely counteract published commits by creating an inverse commit node.
git revert HEAD or Commit Hash

