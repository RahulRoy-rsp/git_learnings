# 🟡 git revert

### 📖 Description
> The `git revert` command is used to **undo a previous commit** by creating a *new commit* that reverses the changes made by the original one.  
> It’s the **safe** way to undo changes in Git because it doesn’t rewrite history.

---

### 💡 Why It’s Important
While `git reset` moves the branch pointer backward (rewriting history),  
`git revert` **preserves history** by adding a new “undo” commit.  
This makes it ideal for collaborative environments.

---

### 🧠 Syntax
```bash
git revert <commit-id>
```

---

### 🧩 Examples

#### 1. Revert a Single Commit

```bash
git revert a1b2c3d
```

**Explanation:**
This creates a new commit that undoes the changes introduced by commit `a1b2c3d`.

---

#### 2. Revert Multiple Commits

```bash
git revert a1b2c3d..e4f5g6h
```

**Explanation:**
Reverts all commits in the given range, starting from `a1b2c3d` (exclusive) up to `e4f5g6h` (inclusive).

---

#### 3. Revert the Most Recent Commit

```bash
git revert HEAD
```

**Explanation:**
Undo the last commit, keeping all previous ones intact.

---

#### 4. Revert Without Commit (Manual Confirmation)

```bash
git revert --no-commit HEAD~2..HEAD
```

**Explanation:**
Applies the revert changes to your working directory but doesn’t commit automatically.
You can inspect or modify before committing manually.

---

### ✅ Quick Recap

| Command                  | What It Does                          |
| ------------------------ | ------------------------------------- |
| `git revert <commit>`    | Undo a specific commit                |
| `git revert HEAD`        | Undo the latest commit                |
| `git revert --no-commit` | Revert without committing immediately |

---

### 🧩 Example Workflow

```bash
# Check history
git log --oneline

# Revert the latest commit
git revert HEAD

# Review and push changes
git push origin main
```

---

### 🧠 Related Commands

| Command                             | Purpose                         |
| ----------------------------------- | ------------------------------- |
| [`git reset`](reset.md) | Remove commits from history     |
| [`git log`](/commands/2_Intermediate/log.md)                 | Identify commit IDs             |
| [`git diff`](/commands/2_Intermediate/diff.md)               | Review changes before reverting |

---

### 🏁 Summary

* `git revert` safely undoes a commit by adding a new one.
* Keeps commit history intact — safe for shared branches.
* Perfect for reverting a bad merge or faulty deployment commit.

---

**Next Step:** 👉 Learn to compare changes visually with [git diff](diff.md).

