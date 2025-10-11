# Git stash

### 📖 Description
> The `git stash` command temporarily **stores (stashes)** your uncommitted changes, allowing you to switch branches or pull updates without committing incomplete work.

---

### 💡 Why It’s Important
You might be mid-way through a feature when you need to:
- Switch branches quickly.
- Pull updates from `main`.
- Test something else.

`git stash` saves your work-in-progress safely, so you can restore it later.

---

### 🧠 Syntax
```bash
git stash [push] [-m "message"]
```

---

### 🧩 Examples

#### 1. Save Your Current Work

```bash
git stash
```

**Explanation:**
Saves modified and staged changes, then resets your working directory to the last commit.

---

#### 2. Stash with a Message

```bash
git stash push -m "WIP: login page update"
```

**Explanation:**
Adds a descriptive message to help identify this stash later.

---

#### 3. List All Stashes

```bash
git stash list
```

**Output Example:**

```
stash@{0}: WIP: login page update
stash@{1}: WIP: footer fix
```

---

#### 4. Apply the Most Recent Stash

```bash
git stash apply
```

**Explanation:**
Restores the latest stash while keeping it in the stash list.

---

#### 5. Apply and Remove a Stash

```bash
git stash pop
```

**Explanation:**
Restores and **removes** the latest stash entry — a one-step recover-and-clean-up.

---

#### 6. Drop a Specific Stash

```bash
git stash drop stash@{1}
```

**Explanation:**
Deletes a particular stash from the list.

---

#### 7. Clear All Stashes

```bash
git stash clear
```

**Explanation:**
Removes all stashed entries — use carefully!

---

### ✅ Quick Recap

| Command           | What It Does             |
| ----------------- | ------------------------ |
| `git stash`       | Save current work        |
| `git stash list`  | View stashes             |
| `git stash apply` | Restore without deleting |
| `git stash pop`   | Restore and delete       |
| `git stash drop`  | Remove a specific stash  |

---

### 🧩 Example Workflow

```bash
# Save changes
git stash push -m "WIP: search feature"

# Switch branch safely
git checkout main
git pull origin main

# Return and restore
git checkout feature/search
git stash pop
```

---

### 🧠 Related Commands

| Command                               | Purpose                              |
| ------------------------------------- | ------------------------------------ |
| [`git diff`](diff.md)                 | Check what’s changed before stashing |
| [`git commit`](/commands/1_Beginner/commit.md) | Save final changes                   |
| [`git reset`](/commands/3_Advanced/reset.md)   | Undo local changes completely        |

---

### 🏁 Summary

* `git stash` lets you pause your work without committing.
* You can apply, pop, or drop stashes anytime.
* Perfect for multitasking across branches.

---

**Next Step:** 👉 Learn how to view your project history with [git log](log.md).
