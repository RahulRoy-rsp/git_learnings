# Git add

### 📖 Description
> The `git add` command is used to **stage changes** in your working directory for the next commit.  
> In Git, editing files doesn’t automatically include them in the next commit — you must explicitly *add* them to the **staging area** (also called the “index”).  
> Think of the staging area as a **preview list** of what will go into your next snapshot.

---

### 💡 Why It’s Important
Git separates **working changes** and **staged changes**:
- **Working Directory:** Where you make edits.
- **Staging Area:** Where you prepare specific files for committing.
- **Repository (History):** Where committed changes live permanently.

By using `git add`, you choose *exactly what* to include in your next commit — giving you full control and cleaner commit histories.

---

### 🧠 Syntax

```bash
git add [options] <file-pattern>
```

Common usage:

* `git add <file>` → Add a single file.
* `git add <file1> <file2>` → Add multiple files.
* `git add .` → Add all modified and new files in the current directory.
* `git add -A` → Add all changes in the repository (including deletions).

---

### 🧩 Examples

#### 1. Add a Single File

```bash
git add file1.py
```

**Explanation:**
Adds `file1.py` to the staging area.
If you run `git status` afterward, it will show this file as “staged for commit.”

---

#### 2. Add Multiple Files

```bash
git add index.html app.js style.css
```

**Explanation:**
Stages all three files together. Useful when you’ve edited multiple related files and want to commit them together.

---

#### 3. Add All Modified and New Files

```bash
git add .
```

**Explanation:**
Stages all modified and newly created files **in the current directory** and its subdirectories.

> ⚠️ **Note:** This does **not** include deleted files — for that, use `git add -A`.

---

#### 4. Add All Changes (Including Deletions)

```bash
git add -A
```

**Explanation:**
Stages everything — new files, modifications, and deletions — across the entire repository.

---

#### 5. Add Files Matching a Pattern

```bash
git add "*.py"
```

**Explanation:**
Stages all Python files in the current directory.
You can use shell-style wildcards (`*`, `?`, etc.) to target specific file types.

---

#### 6. Add Files in a Specific Folder

```bash
git add src/
```

**Explanation:**
Stages all files (new or modified) inside the `src/` directory.
This is helpful when you only want to commit changes from a specific folder.

---

### 🧰 Bonus Tip: Interactive Staging

```bash
git add -p
```

**Explanation:**
Allows you to **interactively select** which changes (hunks) to stage from a file.
Perfect when you want to commit only parts of a file’s changes.

> 💬 For example, if you edited `main.py` in two places but want to commit only one logical change, `git add -p` lets you pick that specific change.

---

### ✅ Quick Recap

| Command            | What It Does                                 |
| ------------------ | -------------------------------------------- |
| `git add file1.py` | Add a specific file                          |
| `git add .`        | Add all modified/new files in current folder |
| `git add -A`       | Add all changes, including deletions         |
| `git add "*.py"`   | Add all Python files                         |
| `git add -p`       | Add changes interactively (by hunks)         |

---

### 🧩 Example Workflow

```bash
# Step 1: Edit some files
vim index.html
vim app.js

# Step 2: Check what changed
git status

# Step 3: Stage changes
git add index.html app.js

# Step 4: Commit staged files
git commit -m "Updated frontend files"
```

---

### 🧠 Related Commands

| Command                                  | Purpose                          |
| ---------------------------------------- | -------------------------------- |
| [`git status`](status.md)    | Check what’s staged and unstaged |
| [`git commit`](commit.md)    | Save staged changes to history   |
| [`git restore`](/commands/2_Intermediate/diff.md) | Unstage or discard changes       |

---

### 🏁 Summary

* `git add` lets you choose what to include in your next commit.
* You can add single files, patterns, or all changes.
* Use `git add -p` to commit selectively.
* Always check your staging area with `git status` before committing.

---

**Next Step:** 👉 Move on to [git commit](/commands/1_Beginner/commit.md) to learn how to record your staged changes into Git history.

