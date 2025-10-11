# Git log

### 📖 Description
> The `git log` command shows a **history of commits** in your repository — who made them, when, and what changed.

---

### 💡 Why It’s Important
Understanding history helps you:
- Track changes over time.
- Debug issues by pinpointing when something broke.
- Review code before merging.

---

### 🧠 Syntax
```bash
git log [options]
```

---

### 🧩 Examples

#### 1. Basic Log View

```bash
git log
```

**Explanation:**
Shows commits with author, date, and message.

---

#### 2. Compact Log View

```bash
git log --oneline
```

**Example Output:**

```
a1b2c3d Fix login issue
e4f5g6h Add navbar component
```

---

#### 3. Graphical Log

```bash
git log --oneline --graph --all
```

**Explanation:**
Displays a visual graph of branches and merges.

---

#### 4. Log with File History

```bash
git log -- <file>
```

**Explanation:**
Shows all commits that modified a specific file.

---

#### 5. Log by Author

```bash
git log --author="Abhijit"
```

**Explanation:**
Filters commit history by a particular author.

---

#### 6. Show Commit Patches

```bash
git log -p -2
```

**Explanation:**
Displays the last 2 commits *and* their code changes.

---

### ✅ Quick Recap

| Command                 | What It Does                 |
| ----------------------- | ---------------------------- |
| `git log`               | View detailed commit history |
| `git log --oneline`     | View compact log             |
| `git log --graph --all` | Visualize branch merges      |
| `git log -- <file>`     | View history of a file       |

---

### 🧩 Example Workflow

```bash
# Check commit history
git log --oneline --graph --decorate

# Inspect details of a specific commit
git show a1b2c3d
```

---

### 🧠 Related Commands

| Command                   | Purpose                 |
| ------------------------- | ----------------------- |
| [`git diff`](diff.md)     | View commit differences |
| [`git revert`](/commands/3_Advanced/revert.md) | Undo specific commits   |
| [`git tag`](tag.md)       | Mark specific versions  |

---

### 🏁 Summary

* `git log` helps you understand your repository’s evolution.
* Use flags like `--oneline` and `--graph` for clarity.
* Great for debugging, reviewing, and auditing.

---

**Next Step:** 👉 Learn how to mark milestones in history using [git tag](tag.md).

