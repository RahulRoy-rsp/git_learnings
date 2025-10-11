# Git init

---

### 📖 Description
> The `git init` command creates a **new Git repository** in your current directory.  
> It sets up all the necessary internal files and folders (`.git/`) that allow Git to start tracking your project.

---

### 💡 Why It’s Important
Every Git project starts with a repository.  
`git init` transforms an ordinary folder into a **version-controlled project**, allowing you to track file changes, revert history, and collaborate.

---

### 🧠 Syntax
```bash
git init [repository-name]
```

---

### 🧩 Examples

#### 1. Initialize a Repository in Current Directory
```bash
git init
```

**Explanation:**
Creates a `.git` folder in your current directory — you can now start tracking files.

---

#### 2. Initialize a Repository in a New Folder

```bash
git init my_project
```

**Explanation:**
Creates a new folder named `my_project` and initializes Git inside it.

---

#### 3. Initialize with Default Branch Name
```bash
git init -b main
```

**Explanation:**
Initializes a new repository and sets the default branch name to `main` instead of `master`.

---

### ✅ Quick Recap

| Command                 | What It Does                                             |
| ----------------------- | -------------------------------------------------------- |
| `git init`              | Initialize a new Git repository in the current directory |
| `git init project_name` | Create a new folder and initialize Git there             |
| `git init -b main`      | Start with a custom branch name                          |

---

### 🧩 Example Workflow

```bash
mkdir portfolio
cd portfolio
git init -b main
echo "# My Portfolio" > README.md
git add README.md
git commit -m "Initial commit"
```

---

### 🧠 Related Commands

| Command                   | Purpose                          |
| ------------------------- | -------------------------------- |
| [`git clone`](clone.md)   | Create a repo copy from a remote |
| [`git add`](add.md)       | Stage files for committing       |
| [`git commit`](commit.md) | Save changes to history          |


---


### 🏁 Summary

* `git init` starts a new repository.
* You only need to run it once per project.
* The .git folder is where Git stores all version data.

---

**Next Step:** Next Step: 👉 Learn how to [clone](clone.md) existing repositories.
