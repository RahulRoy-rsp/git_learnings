# Git reflog

### 📖 Description
> The `git reflog` command records every change to the **HEAD** — including commits, merges, checkouts, rebases, and resets.  
> It’s your **safety net** when you lose track of commits.

---

### 💡 Why It’s Important
`git reflog` helps you:
- Recover lost commits after a reset or rebase.
- See your full branch movement history.
- Restore mistakenly deleted branches.

Every time you move HEAD, Git logs it in the reflog.

---

### 🧠 Syntax
```bash
git reflog [show]
```

---

### 🧩 Examples

#### 1. View Recent HEAD Movements

```bash
git reflog
```

**Example Output:**

```
a1b2c3d HEAD@{0}: commit: Add dashboard page
e4f5g6h HEAD@{1}: reset: moving to HEAD~1
i7j8k9l HEAD@{2}: rebase: checkout feature/api
```

---

#### 2. Restore a Lost Commit

```bash
git reset --hard HEAD@{2}
```

**Explanation:**
Resets your branch to the state it was in two steps ago — perfect for undoing bad resets or rebases.

---

#### 3. Restore a Deleted Branch

```bash
git checkout -b recovery HEAD@{5}
```

**Explanation:**
Creates a new branch from a commit reference found in the reflog.

---

#### 4. Clear Reflog Entries

```bash
git reflog expire --expire=now --all
```

Removes all reflog entries (cleanup operation).

---

### ✅ Quick Recap

| Command                             | What It Does            |
| ----------------------------------- | ----------------------- |
| `git reflog`                        | View HEAD history       |
| `git reset --hard HEAD@{n}`         | Restore state from past |
| `git checkout -b <branch> HEAD@{n}` | Recover deleted branch  |
| `git reflog expire --all`           | Clean reflog entries    |

---

### 🧩 Example Workflow

```bash
# Check reflog after accidental reset
git reflog

# Identify previous HEAD
# e.g., HEAD@{3}

# Restore to that point
git reset --hard HEAD@{3}
```

---

### 🧠 Related Commands

| Command                                   | Purpose                    |
| ----------------------------------------- | -------------------------- |
| [`git reset`](reset.md)                   | Undo commits               |
| [`git rebase`](rebase.md)                 | Reapply commits            |
| [`git checkout`](/commands/1_Beginner/checkout.md) | Switch branches or commits |

---

### 🏁 Summary

* `git reflog` tracks every HEAD change in your repo.
* Use it to recover lost commits or branches.
* It’s your **lifesaver** after a bad reset or rebase.

---