# Git cherry-pick

### 📖 Description
> The `git cherry-pick` command allows you to **apply specific commits** from one branch into another — without merging the entire branch.

---

### 💡 Why It’s Important
You can use `git cherry-pick` to:
- Move a specific bug fix from one branch to another.
- Backport a commit to an older release branch.
- Copy small, focused commits without merging unrelated work.

---

### 🧠 Syntax
```bash
git cherry-pick <commit-id>
```

---

### 🧩 Examples

#### 1. Cherry-Pick a Single Commit

```bash
git checkout main
git cherry-pick a1b2c3d
```

**Explanation:**
Applies commit `a1b2c3d` from another branch to `main`.

---

#### 2. Cherry-Pick Multiple Commits

```bash
git cherry-pick a1b2c3d e4f5g6h
```

**Explanation:**
Applies both commits in sequence.

---

#### 3. Cherry-Pick a Range of Commits

```bash
git cherry-pick a1b2c3d..e4f5g6h
```

**Explanation:**
Picks all commits from `a1b2c3d` (exclusive) to `e4f5g6h` (inclusive).

---

#### 4. Handle Conflicts During Cherry-Pick

If conflicts occur:

```bash
git status
# Fix conflicting files
git add .
git cherry-pick --continue
```

---

#### 5. Abort a Cherry-Pick

```bash
git cherry-pick --abort
```

**Explanation:**
Stops the operation and restores the branch to its previous state.

---

### 🧩 Example Workflow

```bash
# Find commit hash from develop branch
git log develop --oneline

# Switch to release branch
git checkout release/v1.0

# Apply a single hotfix commit
git cherry-pick f6a9d4c

# Push to remote
git push origin release/v1.0
```

---

### ✅ Quick Recap

| Command                      | What It Does                     |
| ---------------------------- | -------------------------------- |
| `git cherry-pick <commit>`   | Apply a specific commit          |
| `git cherry-pick A..B`       | Apply a range of commits         |
| `git cherry-pick --abort`    | Cancel ongoing cherry-pick       |
| `git cherry-pick --continue` | Resume after resolving conflicts |

---

### 🧠 Related Commands

| Command                                   | Purpose                              |
| ----------------------------------------- | ------------------------------------ |
| [`git rebase`](rebase.md)                 | Reapply commits with history rewrite |
| [`git revert`](revert.md) | Undo commits safely                  |
| [`git log`](/commands/3_Advanced/cherry_pick.md)       | Identify commit hashes               |

---

### 🏁 Summary

* `git cherry-pick` lets you copy specific commits from one branch to another.
* Ideal for hotfixes or patch transfers.
* Always test after cherry-picking to ensure consistency.

---

**Next Step:** 👉 Learn how to undo history carefully with [git reset](reset.md).

