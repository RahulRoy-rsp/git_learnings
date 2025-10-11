# Git status

### 📖 Description
> The `git status` command shows the **state of your working directory and staging area**.  
> It helps you see which files are untracked, modified, or staged for commit.

---

### 💡 Why It’s Important
`git status` is your **dashboard** — it tells you exactly what Git is tracking and what it’s not.  
Running this command before a commit ensures you don’t miss or include unintended changes.

---

### 🧠 Syntax
```bash
git status
```

---

### 🧩 Examples

#### 1. Check Current Status

```bash
git status
```

**Explanation:**
Displays new, modified, or deleted files and whether they’re staged or not.

---

#### 2. Short Status View

```bash
git status -s
```

**Explanation:**
Shows a compact output — great for quick checks.
Example:

```
M  app.js
?? newfile.py
```

---

#### 3. Status for a Specific Path

```bash
git status src/
```

**Explanation:**
Limits the status output to files under the `src/` folder.

---

### ✅ Quick Recap

| Command              | What It Does             |
| -------------------- | ------------------------ |
| `git status`         | Show full details        |
| `git status -s`      | Short summary            |
| `git status folder/` | Check only certain files |

---

### 🧩 Example Workflow

```bash
git add file1.py
git status
# shows file1.py is staged
git commit -m "Added file1.py"
git status
# shows nothing to commit
```

---

### 🧠 Related Commands

| Command                               | Purpose                |
| ------------------------------------- | ---------------------- |
| [`git add`](add.md)                   | Stage files for commit |
| [`git diff`](/commands/2_Intermediate/diff.md) | See exact changes      |
| [`git commit`](commit.md)             | Save staged files      |

---

### 🏁 Summary

* Use `git status` frequently — it keeps you aware of what’s going on.
* Combine with `git diff` and `git add` for complete control.

---

**Next Step:** 👉 Learn to [commit your changes](commit.md).
