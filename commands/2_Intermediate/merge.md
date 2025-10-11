# Git merge

### 📖 Description
> The `git merge` command is used to **combine changes** from one branch into another.  
> It helps you bring together parallel lines of development — for example, merging a feature branch into `main` after the feature is completed.

---

### 💡 Why It’s Important
When multiple people (or branches) work on different parts of a project, merging is how you **integrate** those changes together without losing history.

Git merges maintain the commit history from both branches — making collaboration smooth and traceable.

---

### 🧠 Syntax
```bash
git merge <branch-name>
```

---

### 🧩 Examples

#### 1. Merge a Feature Branch into Main

```bash
# Step 1: Switch to the main branch
git checkout main

# Step 2: Merge changes from the feature branch
git merge feature/login
```

**Explanation:**
This combines all commits from `feature/login` into `main`. If there are no conflicts, Git creates a new *merge commit*.

---

#### 2. Fast-Forward Merge

```bash
git checkout main
git merge feature/ui
```

If `main` hasn’t diverged since `feature/ui` was created, Git performs a **fast-forward merge** — simply moving the branch pointer ahead without creating a new merge commit.

> 🧩 Think of it like “skipping ahead” to the latest commit.

---

#### 3. Merge with Conflicts

```bash
git merge feature/payment
```

If both branches modified the same lines of a file, you’ll see a **merge conflict**.
Git will show markers like this inside the file:

```diff
<<<<<<< HEAD
old code
=======
new code
>>>>>>> feature/payment
```

You’ll need to manually fix the conflict, then:

```bash
git add <file>
git commit
```

---

#### 4. Abort a Merge

```bash
git merge --abort
```

**Explanation:**
Cancels an in-progress merge and restores the branch to its previous state (before the merge started).

---

### ✅ Quick Recap

| Command                    | What It Does                                       |
| -------------------------- | -------------------------------------------------- |
| `git merge branch`         | Merge a branch into the current one                |
| `git merge --abort`        | Cancel the merge and revert back                   |
| `git merge --no-ff branch` | Force a merge commit even if fast-forward possible |

---

### 🧩 Example Workflow

```bash
# Create and switch to a new feature branch
git checkout -b feature/add-search

# Make changes, commit them
git add .
git commit -m "Add search feature"

# Switch back to main
git checkout main

# Merge feature into main
git merge feature/add-search

# Delete branch after successful merge
git branch -d feature/add-search
```

---

### 🧠 Related Commands

| Command                               | Purpose                                  |
| ------------------------------------- | ---------------------------------------- |
| [`git branch`](/commands/1_Beginner/branch.md) | Create or list branches                  |
| [`git rebase`](rebase.md)             | Reapply commits on top of another branch |
| [`git log --graph`](/commands/3_Advanced/log.md)           | Visualize merge history                  |

---

### 🏁 Summary

* `git merge` integrates changes between branches.
* Fast-forward merges happen when branches haven’t diverged.
* Conflicts require manual resolution.
* Always verify with `git status` after merging.

---

**Next Step:** 👉 Learn how to rewrite history cleanly with [git rebase](rebase.md).
