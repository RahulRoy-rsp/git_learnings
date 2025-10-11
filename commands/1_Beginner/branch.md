# Git branch

### 📖 Description
> The `git branch` command manages branches — independent lines of development within a repository.

---

### 💡 Why It’s Important
Branches let you **work on features, fixes, or experiments** without affecting the main project.  
Once done, you can merge them back safely.

---

### 🧠 Syntax
```bash
git branch [branch-name]
```

---

### 🧩 Examples

#### 1. List All Branches

```bash
git branch
```

**Explanation:**
Shows local branches; the current one is marked with `*`.

---

#### 2. Create a New Branch

```bash
git branch feature/hotfix
```

**Explanation:**
Creates a new branch named `feature/hotfix`.

---

#### 3. Delete a Branch

```bash
git branch -d feature/login
```

**Explanation:**
Deletes a local branch after it’s merged.

---

#### 4. Rename a Branch

```bash
git branch -m old-name new-name
```

**Explanation:**
Renames your branch easily.

---

### ✅ Quick Recap

| Command                 | What It Does  |
| ----------------------- | ------------- |
| `git branch`            | List branches |
| `git branch name`       | Create branch |
| `git branch -d name`    | Delete branch |
| `git branch -m old new` | Rename branch |

---

### 🧩 Example Workflow

```bash
git branch feature/search
git checkout feature/search
# work and commit changes
git checkout main
git merge feature/search
```

---

### 🧠 Related Commands

| Command                                 | Purpose                 |
| --------------------------------------- | ----------------------- |
| [`git checkout`](checkout.md)           | Switch between branches |
| [`git merge`](/commands/2_Intermediate/merge.md) | Combine branches        |
| [`git log`](/commands/3_Advanced/log.md)     | View commits by branch  |

---

### 🏁 Summary

* Branches isolate work.
* Use clear names (e.g., `feature/login` or `bugfix/header`).
* Merge back when complete.

---

**Next Step:** 👉 Learn how to [switch branches with git checkout](checkout.md).
