# GitHub Setup Checklist - Do This Together!

## ☑️ Day 0: Initial Setup (30 minutes)

### Step 1: Create Repository (Student 1)

- [ ] Go to github.com
- [ ] Click "New Repository"
- [ ] Name: `a-maze-ing`
- [ ] Description: "42 School maze generator project"
- [ ] Visibility: Public (or Private - check 42 requirements)
- [ ] **DON'T** initialize with README
- [ ] Add .gitignore: Python template
- [ ] Click "Create repository"

### Step 2: Add Collaborator (Student 1)

- [ ] Go to Settings → Collaborators
- [ ] Click "Add people"
- [ ] Enter Student 2's GitHub username
- [ ] Send invitation

### Step 3: Accept Invitation (Student 2)

- [ ] Check email for GitHub invitation
- [ ] Click "Accept invitation"
- [ ] Verify access to repository

### Step 4: Clone Repository (Both Students)

```bash
# Replace with your actual repository URL
git clone https://github.com/YOUR-USERNAME/a-maze-ing.git
cd a-maze-ing
```

### Step 5: Create Initial Structure (Student 1)

```bash
# Create directories
mkdir -p src/{display} mazegen tests examples docs package_build

# Create essential files
touch README.md Makefile requirements.txt a_maze_ing.py config.txt

# Create .gitignore (if not created by GitHub)
cat > .gitignore << 'EOF'
# Python
__pycache__/
*.py[cod]
*$py.class
*.so
.Python
build/
develop-eggs/
dist/
downloads/
eggs/
.eggs/
lib/
lib64/
parts/
sdist/
var/
wheels/
*.egg-info/
.installed.cfg
*.egg

# Virtual environments
venv/
env/
ENV/

# IDEs
.vscode/
.idea/
*.swp
*.swo
*~

# Testing
.pytest_cache/
.coverage
htmlcov/

# Type checking
.mypy_cache/
.dmypy.json
dmypy.json

# Project specific
*.txt
!requirements.txt
!config.txt
EOF

# Create initial README
cat > README.md << 'EOF'
# A-Maze-ing

*This project has been created as part of the 42 curriculum by student1, student2*

## Description
A Python-based maze generator with visual representation.

## Status
🚧 Under development

## Team
- Student 1: Maze generation
- Student 2: Pathfinding & Display
EOF

# Initial commit
git add .
git commit -m "[init] Initial project structure"
git push origin main
```

### Step 6: Create Dev Branch (Student 1)

```bash
git checkout -b dev
git push -u origin dev
```

### Step 7: Sync Repository (Student 2)

```bash
git pull origin main
git checkout dev
```

---

## ☑️ Day 0: Configure Repository (15 minutes)

### Step 8: Set Up Branch Protection (Student 1)

**For Main Branch:**

- [ ] Go to Settings → Branches
- [ ] Click "Add rule"
- [ ] Branch name pattern: `main`
- [ ] Check ✓ "Require a pull request before merging"
- [ ] Require approvals: `1`
- [ ] Check ✓ "Dismiss stale pull request approvals when new commits are pushed"
- [ ] Check ✓ "Do not allow bypassing the above settings"
- [ ] Click "Create"

**For Dev Branch:**

- [ ] Click "Add rule"
- [ ] Branch name pattern: `dev`
- [ ] Check ✓ "Require a pull request before merging"
- [ ] Require approvals: `1`
- [ ] Click "Create"

### Step 9: Create Labels (Either Student)

- [ ] Go to Issues → Labels
- [ ] Delete unused default labels
- [ ] Create new labels:

| Label             | Color                    | Description             |
| ----------------- | ------------------------ | ----------------------- |
| `priority-high`   | `#d73a4a` (red)          | Critical tasks          |
| `priority-medium` | `#fbca04` (yellow)       | Important tasks         |
| `priority-low`    | `#0e8a16` (green)        | Nice to have            |
| `bug`             | `#d73a4a` (red)          | Something isn't working |
| `feature`         | `#0075ca` (blue)         | New feature             |
| `docs`            | `#7057ff` (purple)       | Documentation           |
| `student-1`       | `#bfdadc` (light blue)   | Assigned to Student 1   |
| `student-2`       | `#bfd4f2` (light purple) | Assigned to Student 2   |
| `blocked`         | `#6e5494` (gray)         | Blocked task            |
| `in-progress`     | `#d4c5f9` (orange)       | Currently working       |
| `testing`         | `#c5def5` (light blue)   | Needs testing           |

### Step 10: Create Milestones (Either Student)

- [ ] Go to Issues → Milestones
- [ ] Click "New milestone"

Create these milestones:

1. **Sprint 1: Foundation** (Due: +3 days from start)
    - Description: Project setup, config parser, data structures
2. **Sprint 2: Core Features** (Due: +7 days)
    - Description: Maze generation, pathfinding, file output
3. **Sprint 3: Display & Packaging** (Due: +10 days)
    - Description: ASCII rendering, user interactions, package build
4. **Sprint 4: Final Polish** (Due: +12 days)
    - Description: Testing, documentation, bug fixes

---

## ☑️ Day 0: Create Project Board (10 minutes)

### Step 11: Set Up Kanban Board (Either Student)

- [ ] Go to Projects → New project
- [ ] Choose "Board" view
- [ ] Name: "A-Maze-ing Development"
- [ ] Description: "Task tracking for maze generator project"
- [ ] Click "Create"

### Step 12: Configure Columns

Rename/add columns:

- [ ] 📋 **To Do** - Tasks not yet started
- [ ] 🔄 **In Progress** - Currently working on
- [ ] 👀 **In Review** - PR created, waiting for review
- [ ] ✅ **Done** - Completed and merged
- [ ] 🚫 **Blocked** - Waiting on external factor

### Step 13: Set Up Automation

For each column:

- **To Do**: Newly added items
- **In Progress**: Item assigned
- **In Review**: Pull request opened
- **Done**: Pull request merged/closed
- **Blocked**: Label "blocked" added

---

## ☑️ Day 0: Create Initial Issues (15 minutes)

### Step 14: Create Issues for Sprint 1 (Both Students)

**Student 1 creates:**

```
Issue #1: Setup Makefile
Labels: feature, priority-high, student-1
Milestone: Sprint 1
Assignee: Student 1

Description:
Create Makefile with required rules:
- [ ] install
- [ ] run
- [ ] debug
- [ ] clean
- [ ] lint
- [ ] lint-strict (optional)
```

```
Issue #2: Implement config file parser
Labels: feature, priority-high, student-1
Milestone: Sprint 1
Assignee: Student 1

Description:
Parse configuration file with KEY=VALUE format
- [ ] Handle comments (#)
- [ ] Parse all required keys
- [ ] Validate values
- [ ] Error handling
```

```
Issue #3: Implement maze generation algorithm
Labels: feature, priority-high, student-1
Milestone: Sprint 2
Assignee: Student 1

Description:
Implement recursive backtracker algorithm
- [ ] Research algorithm
- [ ] Create Maze and Cell classes
- [ ] Implement generation logic
- [ ] Add seed-based randomization
- [ ] Ensure perfect maze option
```

**Student 2 creates:**

```
Issue #4: Design maze data structures
Labels: feature, priority-high, student-2
Milestone: Sprint 1
Assignee: Both (discuss together)

Description:
Design Cell and Maze classes
- [ ] Define Cell attributes
- [ ] Define Maze attributes
- [ ] Wall encoding system
- [ ] Coordinate system
```

```
Issue #5: Implement pathfinding algorithm
Labels: feature, priority-high, student-2
Milestone: Sprint 2
Assignee: Student 2

Description:
Implement BFS shortest path
- [ ] BFS implementation
- [ ] Return path as N/E/S/W
- [ ] Handle no path case
- [ ] Optimize for large mazes
```

```
Issue #6: Create ASCII renderer
Labels: feature, priority-medium, student-2
Milestone: Sprint 3
Assignee: Student 2

Description:
Display maze in terminal
- [ ] Box-drawing characters
- [ ] Color support
- [ ] Show entry/exit
- [ ] Highlight path
```

### Step 15: Add Issues to Project Board

- [ ] Go to Project Board
- [ ] Add all created issues
- [ ] Issues should appear in "To Do" column

---

## ☑️ Day 1: Create Feature Branches (5 minutes)

### Step 16: Create Your Feature Branches (Both Students)

**Student 1:**

```bash
git checkout dev
git pull origin dev

# Create feature branches
git checkout -b feature/makefile
git push -u origin feature/makefile

git checkout dev
git checkout -b feature/config-parser
git push -u origin feature/config-parser

git checkout dev
git checkout -b feature/maze-generation
git push -u origin feature/maze-generation
```

**Student 2:**

```bash
git checkout dev
git pull origin dev

# Create feature branches
git checkout -b feature/data-structures
git push -u origin feature/data-structures

git checkout dev
git checkout -b feature/pathfinding
git push -u origin feature/pathfinding

git checkout dev
git checkout -b feature/ascii-renderer
git push -u origin feature/ascii-renderer
```

---

## ☑️ Verification Checklist

### Repository Setup ✓

- [ ] Repository created on GitHub
- [ ] Both students have access
- [ ] Both students can push
- [ ] .gitignore is working
- [ ] Initial structure committed

### Branch Protection ✓

- [ ] Main branch is protected
- [ ] Dev branch is protected
- [ ] Requires PR approval
- [ ] Both students tested creating PR

### Project Management ✓

- [ ] Labels created
- [ ] Milestones created
- [ ] Project board set up
- [ ] Initial issues created
- [ ] Issues assigned
- [ ] Issues added to board

### Communication ✓

- [ ] Both students have GitHub notifications on
- [ ] Agreed on daily sync time
- [ ] Decided on communication channel (Slack/Discord)
- [ ] Tested GitHub mentions (@username)

---

## 🎯 First Day Workflow Test

### Test the Complete Workflow (Both Students)

**Student 1:**

```bash
# 1. Create a test file
git checkout feature/makefile
echo "# Test Makefile" > Makefile

# 2. Commit
git add Makefile
git commit -m "[feat] Add initial Makefile structure"

# 3. Push
git push origin feature/makefile

# 4. Create PR on GitHub
# - Go to Pull Requests → New
# - Base: dev, Compare: feature/makefile
# - Add description
# - Assign Student 2 as reviewer
# - Link to Issue #1 (write "Closes #1" in description)

# 5. Wait for Student 2 review
```

**Student 2:**

```bash
# 1. Get notification of PR
# 2. Go to PR on GitHub
# 3. Click "Files changed"
# 4. Review code
# 5. Add comment: "Looks good! 👍"
# 6. Click "Review changes" → "Approve"
# 7. Student 1 merges PR

# Now Student 2 creates their PR
git checkout feature/data-structures
# ... create file, commit, push, create PR ...
# Assign Student 1 as reviewer
```

**Both Students:**

```bash
# After PRs are merged, update local dev
git checkout dev
git pull origin dev

# Verify changes are there
ls -la
```

---

## 📱 Enable GitHub Notifications

### Step 17: Configure Notifications

- [ ] Go to Settings (your profile, not repo)
- [ ] Notifications → Watching
- [ ] Check ✓ "Email" and/or "Web and Mobile"
- [ ] Configure notification preferences:
    - ✓ Participating
    - ✓ @mentions
    - ✓ Pull request reviews
    - ✓ Issue comments

### Step 18: Watch Repository

- [ ] Go to repository page
- [ ] Click "Watch" (top right)
- [ ] Select "All Activity"

---

## 🎉 Setup Complete!

If you checked all boxes, you're ready to start coding!

### Next Steps:

1. Move Issue #1 to "In Progress" on project board
2. Start working on your first feature branch
3. Commit regularly (every 1-2 hours)
4. Push daily
5. Create PR when feature is complete
6. Review each other's PRs
7. Merge to dev
8. Repeat!

### Daily Routine:

```bash
# Morning
git checkout dev
git pull origin dev
git checkout your-feature-branch
git merge dev

# During day - commit often!
git add .
git commit -m "[feat] descriptive message"

# Evening
git push origin your-feature-branch

# When feature done
# Create PR on GitHub
```

---

## 📞 Need Help?

### Common Issues:

**"I can't push to main"** → Good! It's protected. Create PR instead.

**"Permission denied"** → Check if you accepted collaborator invitation.

**"Merge conflict"** → Don't panic! See GitHub guide conflict resolution section.

**"I don't see my teammate's changes"** → Run: `git pull origin dev`

**"GitHub Desktop vs Command Line?"** → Both work! Use what you're comfortable with.

---

**Remember: Commit often, push daily, communicate constantly!**

Good luck! 🚀