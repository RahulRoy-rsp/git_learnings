# Git rebase

### 📖 Description
> `git rebase` is used to **reapply commits** on top of another base commit.  
> It allows you to **rewrite history** — rearranging, editing, or squashing commits for a cleaner and more linear project timeline.

---

### 💡 Why It’s Important
- Makes your project history **clean and linear**.
- Useful before merging feature branches.
- Helps avoid unnecessary merge commits.
- Enables combining multiple commits into one logical unit.

---

### 🧠 Syntax
```bash
git rebase [options] <upstream> [branch]
```

---

### 🧩 Examples

#### 1. Rebase a Feature Branch onto Main

```bash
git checkout feature/payment
git rebase main
```

**Explanation:**
This replays commits from `feature/payment` on top of `main`.
It’s like pretending you started this branch from the latest main version.

---

#### 2. Interactive Rebase (Squash, Reorder, Edit)

```bash
git rebase -i HEAD~5
```

**Explanation:**
Lets you rewrite the last 5 commits interactively.
You’ll see something like:

```
pick a1b2c3 Add payment form
pick d4e5f6 Fix form validation
pick g7h8i9 Update UI layout
```

Change to:

```
pick a1b2c3 Add payment form
squash d4e5f6 Fix form validation
pick g7h8i9 Update UI layout
```

✅ Result: Cleaner, combined commit history.

---

#### 3. Continue After Conflict

```bash
git rebase --continue
```

After fixing conflicts in files, this command resumes the rebase.

---

#### 4. Skip a Commit During Rebase

```bash
git rebase --skip
```

Skips applying the current conflicting commit and continues with the rest.

---

#### 5. Abort a Rebase

```bash
git rebase --abort
```

Restores your branch to the state it was in before starting the rebase.

---

### ⚠️ Important Guidelines

* **Never rebase shared/public branches.**
* Rebase only **local** feature branches.
* Use `--force-with-lease` when pushing after a rebase.

---

### 🧩 Example Workflow

```bash
# Update local main
git checkout main
git pull origin main

# Switch to feature branch
git checkout feature/api

# Rebase onto main
git rebase main

# Fix conflicts if any
git status
# ... edit and resolve ...
git add .
git rebase --continue

# Push changes
git push origin feature/api --force-with-lease
```

---

### ✅ Quick Recap

| Command                 | What It Does                     |
| ----------------------- | -------------------------------- |
| `git rebase main`       | Reapply commits on top of `main` |
| `git rebase -i HEAD~n`  | Interactive history rewrite      |
| `git rebase --continue` | Continue after conflict          |
| `git rebase --abort`    | Cancel rebase                    |

---

### 🧠 Related Commands

| Command                                 | Purpose                      |
| --------------------------------------- | ---------------------------- |
| [`git merge`](/commands//2_Intermediate/merge.md) | Combine histories safely     |
| [`git cherry-pick`](cherry_pick.md)     | Apply selected commits only  |
| [`git reflog`](reflog.md)               | Recover from rebase mistakes |

---

### 🏁 Summary

* `git rebase` rewrites commit history to keep it clean.
* Use `-i` for interactive rewriting.
* Avoid rebasing public branches.
* Use `--force-with-lease` when pushing rebased work.

---

**Next Step:** 👉 Learn how to extract individual commits using [git cherry-pick](cherry_pick.md).

