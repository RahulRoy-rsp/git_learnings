# Git diff

### 📖 Description
> The `git diff` command shows **differences** between commits, branches, files, or your working directory and staging area.  
> It helps you see *exactly what changed* before committing.

---

### 💡 Why It’s Important
Before committing or merging, reviewing differences helps you:
- Avoid committing unwanted changes.
- Understand what was modified.
- Detect mistakes early.

---

### 🧠 Syntax
```bash
git diff [options] [<commit>] [<commit>] [--] [<path>...]
```

---

### 🧩 Examples

#### 1. View Unstaged Changes

```bash
git diff
```

**Explanation:**
Shows differences between the working directory and the staging area (unstaged edits).

---

#### 2. View Staged Changes

```bash
git diff --staged
```

**Explanation:**
Shows changes that have been added to the staging area but not yet committed.

---

#### 3. Compare Two Commits

```bash
git diff a1b2c3d e4f5g6h
```

**Explanation:**
Displays all changes between the two commit snapshots.

---

#### 4. Compare Two Branches

```bash
git diff main feature/login
```

**Explanation:**
Highlights the code differences between the `main` branch and `feature/login`.

---

#### 5. Compare a Specific File

```bash
git diff HEAD index.html
```

**Explanation:**
Shows how `index.html` differs between the working directory and the last commit.

---

### ✅ Quick Recap

| Command                        | What It Does                  |
| ------------------------------ | ----------------------------- |
| `git diff`                     | Compare unstaged changes      |
| `git diff --staged`            | Compare staged vs last commit |
| `git diff branch1 branch2`     | Compare two branches          |
| `git diff <commit1> <commit2>` | Compare commits directly      |

---

### 🧩 Example Workflow

```bash
# Edit file
vim app.py

# Check what changed
git diff

# Stage changes
git add app.py

# Double-check staged differences
git diff --staged

# Commit
git commit -m "Refactor app.py"
```

---

### 🧠 Related Commands

| Command                                   | Purpose             |
| ----------------------------------------- | ------------------- |
| [`git log`](/commands/3_Advanced/log.md)                       | View commit history |
| [`git revert`](/commands/3_Advanced/revert.md)                 | Undo changes        |
| [`git checkout`](/commands/1_Beginner/checkout.md) | Switch versions     |

---

### 🏁 Summary

* `git diff` helps visualize what changed before committing.
* Great for debugging, code reviews, and pre-commit checks.
* Combine with `--staged` or commit IDs for targeted comparisons.

---

**Next Step:** 👉 Learn how to temporarily shelve your work with [git stash](stash.md).

