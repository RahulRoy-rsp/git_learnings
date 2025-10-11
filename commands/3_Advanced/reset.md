# Git reset

### 📖 Description
> The `git reset` command moves the **HEAD** (current branch pointer) to a specified commit.  
> It can also modify the **staging area** and **working directory**, depending on the reset mode.

---

### 💡 Why It’s Important
`git reset` is a **powerful undo tool** — but it can also destroy work if used incorrectly.  
It helps you:
- Unstage files.
- Undo commits.
- Move your branch pointer backward.

---

### 🧠 Syntax
```bash
git reset [--soft | --mixed | --hard] <commit>
```

---

### 🧩 Reset Modes Explained

| Mode                | Affects Staging Area | Affects Working Directory | Safe?       |
| ------------------- | -------------------- | ------------------------- | ----------- |
| `--soft`            | ❌ No                 | ❌ No                      | ✅ Safe      |
| `--mixed` (default) | ✅ Yes                | ❌ No                      | ⚠️ Moderate |
| `--hard`            | ✅ Yes                | ✅ Yes                     | ❌ Dangerous |

---

### 🧩 Examples

#### 1. Unstage Files (Keep Changes)

```bash
git reset
```

**Explanation:**
Removes files from staging area, but leaves edits in working directory.

---

#### 2. Reset to a Previous Commit (Soft)

```bash
git reset --soft HEAD~1
```

**Explanation:**
Moves HEAD back by one commit but keeps changes staged.
Useful when you want to amend the previous commit.

---

#### 3. Reset to a Previous Commit (Mixed)

```bash
git reset --mixed HEAD~2
```

**Explanation:**
Moves HEAD back two commits, unstages changes, but preserves files in working directory.

---

#### 4. Full Reset (Hard)

```bash
git reset --hard a1b2c3d
```

**Explanation:**
Moves HEAD to a1b2c3d, discarding all changes since.

> ⚠️ **Warning:** This permanently deletes uncommitted changes.

---

#### 5. Undo a Hard Reset (Recover)

If you made a mistake:

```bash
git reflog
git reset --hard <previous-hash>
```

Use `git reflog` to find the previous state.

---

### ✅ Quick Recap

| Command                    | Effect                              |
| -------------------------- | ----------------------------------- |
| `git reset`                | Unstage files                       |
| `git reset --soft HEAD~1`  | Undo commit but keep staged         |
| `git reset --mixed HEAD~n` | Undo commits, keep files            |
| `git reset --hard <hash>`  | Undo commits and changes completely |

---

### 🧠 Related Commands

| Command                                   | Purpose                     |
| ----------------------------------------- | --------------------------- |
| [`git reflog`](reflog.md)                 | Recover lost commits        |
| [`git revert`](revert.md) | Undo safely with new commit |
| [`git status`](/commands/1_Beginner/status.md)     | Inspect working state       |

---

### 🏁 Summary

* `git reset` repositions your branch’s HEAD.
* Choose `--soft`, `--mixed`, or `--hard` based on how much you want to undo.
* Use `reflog` to recover lost work after resets.

---

**Next Step:** 👉 Learn how to recover from history rewrites with [git reflog](reflog.md).

