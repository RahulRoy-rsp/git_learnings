# Git pull

### 📖 Description
> The `git pull` command updates your local branch by **fetching and merging** changes from a remote repository.

---

### 💡 Why It’s Important
It keeps your local branch in sync with the remote — essential when collaborating with teammates who are also pushing changes.

---

### 🧠 Syntax
```bash
git pull [remote] [branch]
```

---

### 🧩 Examples

#### 1. Pull from Default Remote

```bash
git pull
```

**Explanation:**
Fetches and merges updates from the default remote (usually `origin`) and current branch.

---

#### 2. Pull from a Specific Remote and Branch

```bash
git pull origin develop
```

**Explanation:**
Pulls updates from the `develop` branch of `origin`.

---

#### 3. Rebase Instead of Merge

```bash
git pull --rebase
```

**Explanation:**
Applies your local commits on top of fetched changes for a cleaner history.

---

#### 4. Pull Without Committing Automatically

```bash
git pull --no-commit
```

**Explanation:**
Merges fetched changes but pauses before committing — letting you review the merge.

---

### ✅ Quick Recap

| Command                  | Description             |
| ------------------------ | ----------------------- |
| `git pull`               | Fetch + merge           |
| `git pull origin branch` | Pull specific branch    |
| `git pull --rebase`      | Rebase instead of merge |

---

### 🧩 Example Workflow

```bash
git status
git pull origin main
```

**Explanation:**
Keeps your local code up to date with remote changes.

---

### 🧠 Related Commands

| Command                               | Purpose               |
| ------------------------------------- | --------------------- |
| [`git fetch`](fetch.md)               | Download changes only |
| [`git merge`](merge.md)               | Combine branches      |
| [`git rebase`](/commands/3_Advanced/rebase.md) | Linearize commits     |

---

### 🏁 Summary

* `git pull` = `fetch` + `merge`.
* Use `--rebase` for a linear history.
* Always pull before pushing to avoid conflicts.

---
**Next Step:** 👉 Learn how to [push your changes](push.md).

