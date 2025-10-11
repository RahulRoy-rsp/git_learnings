# Git checkout

### 📖 Description
> The `git checkout` command switches between branches or restores files in your working directory.

---

### 💡 Why It’s Important
When working on multiple features or versions, `git checkout` lets you **move safely** between different branches or restore lost changes.

---

### 🧠 Syntax
```bash
git checkout <branch-name>
git checkout -- <file-name>
```

---

### 🧩 Examples

#### 1. Switch to Another Branch

```bash
git checkout feature/login
```

**Explanation:**
Moves to the `feature/login` branch and updates your working files.

---

#### 2. Create and Switch to a New Branch

```bash
git checkout -b feature/hotfix
```

**Explanation:**
Shortcut for creating and switching to a new branch.

---

#### 3. Restore a File to Last Commit

```bash
git checkout -- app.py
```

**Explanation:**
Reverts `app.py` to the last committed version — discarding local changes.

---

#### 4. Checkout a Specific Commit

```bash
git checkout 1a2b3c4d
```

**Explanation:**
Moves your HEAD to that commit (detached state). Use with caution.

---

### ✅ Quick Recap

| Command                  | What It Does    |
| ------------------------ | --------------- |
| `git checkout branch`    | Switch branch   |
| `git checkout -b branch` | Create + switch |
| `git checkout -- file`   | Restore file    |

---

### 🧩 Example Workflow

```bash
git checkout -b feature/ui
# make changes
git add .
git commit -m "Update UI"
git checkout main
git merge feature/ui
```

---

### 🧠 Related Commands

| Command                                     | Purpose                         |
| ------------------------------------------- | ------------------------------- |
| [`git branch`](branch.md)                   | Manage branches                 |
| [`git merge`](/commands//2_Intermediate/merge.md)     | Merge changes between branches  |

---

### 🏁 Summary

* `git checkout` moves between branches or restores files.
* Use `-b` to create a new branch quickly.
* Use `-- file` to discard unwanted edits.

---

**Next Step:** 👉 Move on to [Intermediate Git Commands](/commands/2_Intermediate/).

