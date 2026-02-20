# 🚀 42 Team Git Workflow

> [!CAUTION] The Golden Rule of `main`
> NEVER push directly to `main`! > `main` is the "Holy Grail". It represents the final, flawless, evaluation-ready project. We only merge into `main` at the very end of the project when everything works perfectly.

---

### 🌳 Branch Architecture (The Traffic Light System)

> [!INFO] Our 3 Types of Branches
> 1. 🔴 `main`: Production code only. Untouchable during daily work.
> 2. 🟢 `feat/branch-name`: The Sandbox. Temporary branches where we actually write the code (e.g., `feat/s1-maze-model` or `feat/s2-display`).

---

### 🔄 The Daily 5-Step Loop (How to Code Every Day)

> [!CMD] Step 1: Sync with the Cloud (Morning Routine)
> *Always start by downloading your partner's latest approved work.*
> ```bash
> git checkout main
> git pull origin main
> ```

> [!CMD] Step 2: Create Your Sandbox
> *Never code on main. Make a temporary room for today's task.*
> ```bash
> git checkout -b feat/my-new-task
> ```

> [!CMD] Step 3: Work, Save, and Push
> *Write your Python code, then upload it to GitHub.*
> ```bash
> git add .
> git commit -m "feat(module): description of what I did"
> git push -u origin feat/my-new-task
> git checkout main
> git merge feat/my-new-task
> ```

> [!CMD] Step 4: The 42 Handshake (Pull Request)
> *Merge your code into the shared `main` space.*
> 1. Go to GitHub.com.
> 2. Click **Compare & pull request**.
> 3. Set base to `main`.
> 4. **Partner Review:** Explain the code to your partner. Your partner must click **Merge**.

> [!CMD] Step 5: Clean Up
> *Delete the old branch and download the merged result to start fresh.*
> 1. Delete branch on GitHub (click the trash can 🗑️).
> 2. In terminal: `git checkout main`
> 3. In terminal: `git pull origin main`
> 4. In terminal: `git branch -d feat/my-new-task` (Deletes local copy)

---

### 🛡️ Why we do this (42 Defense)
By forcing Pull Requests into `develop` and making the partner review the code, **both students learn the entire codebase**. When the evaluator asks Younes to explain Ahmed's Config Parser, Younes will know how it works because he reviewed the PR!