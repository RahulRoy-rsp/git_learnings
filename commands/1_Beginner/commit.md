
# Git commit

### 📖 Description
> The `git commit` command records the staged changes into your local repository.  
> It creates a permanent **snapshot** of your project’s current state.

---

### 💡 Why It’s Important
Committing is how you **save progress** in Git.  
Each commit represents a checkpoint — allowing you to track history, revert mistakes, and understand how the project evolved.

---

### 🧠 Syntax
```bash
git commit -m "commit message"
```

---

### 🧩 Examples

#### 1. Commit with a Message

```bash
git commit -m "PROD me hotfix daal diya"
```

**Explanation:**
Commits all staged changes with a clear, short message.

---

#### 2. Commit All Changes Without Using `git add`

```bash
git commit -am "hotfix in lambda function"
```

**Explanation:**
Stages and commits all tracked file changes in one go. (Doesn’t include new untracked files.)

---

#### 3. Edit the Most Recent Commit Message

```bash
git commit --amend -m "Refined data quality"
```

**Explanation:**
Updates the last commit message — useful for typos or clarifications.

---

#### 4. Open Editor for Detailed Commit

```bash
git commit
```

**Explanation:**
Opens your default editor (e.g., Vim or VS Code) to write a multi-line message.

---

### ✅ Quick Recap

| Command                | What It Does                 |
| ---------------------- | ---------------------------- |
| `git commit -m "msg"`  | Commit staged files          |
| `git commit -am "msg"` | Stage + commit tracked files |
| `git commit --amend`   | Modify last commit           |

---

### 🧩 Example Workflow

```bash
git add .
git commit -m "Implement user registration"
git log --oneline
```

---

### 🧠 Related Commands

| Command                                   | Purpose                       |
| ----------------------------------------- | ----------------------------- |
| [`git add`](add.md)                       | Stage files before committing |
| [`git log`](/commands/3_Advanced/log.md)       | View commit history           |
| [`git revert`](/commands/3_Advanced/revert.md) | Undo commits safely           |

---

### 🏁 Summary

* `git commit` captures your project’s snapshot.
* Always write meaningful messages.
* Use `--amend` for small corrections.

---

**Next Step:** 👉 Learn about [branching](branch.md).
