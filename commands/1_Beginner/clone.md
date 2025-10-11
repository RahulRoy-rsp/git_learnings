# Git clone

### 📖 Description
> The `git clone` command creates a **local copy** of an existing remote repository.  
> It downloads all branches, commits, and files, allowing you to work on your own copy of the project.

---

### 💡 Why It’s Important
Instead of starting from scratch, developers often **clone repositories** from platforms like GitHub, GitLab, or Bitbucket to collaborate or explore code.

---

### 🧠 Syntax
```bash
git clone <repository-url> [folder-name]
```

---

### 🧩 Examples

#### 1. Clone a Repository

```bash
git clone https://github.com/RahulRoy-rsp/git_learnings.git
```

**Explanation:**
Clones the repository `project.git` into a local folder named `project`.

---

#### 2. Clone into a Specific Folder

```bash
git clone https://github.com/RahulRoy-rsp/git_learnings.git my-local-copy
```

**Explanation:**
Creates a local copy in the folder `my-local-copy`.

---

#### 3. Clone Only a Specific Branch

```bash
git clone -b feature1 https://github.com/RahulRoy-rsp/git_learnings.git
```

**Explanation:**
Downloads only the `feature1` branch instead of all branches.

---

#### 4. Clone Using SSH

```bash
git clone git@github.com:RahulRoy-rsp/git_learnings.git
```

**Explanation:**
Uses SSH for authentication — recommended when pushing changes frequently.

---

### ✅ Quick Recap

| Command                     | What It Does                        |
| --------------------------- | ----------------------------------- |
| `git clone <url>`           | Clone a repo into current directory |
| `git clone <url> folder`    | Clone into a specific folder        |
| `git clone -b branch <url>` | Clone a specific branch             |

---

### 🧩 Example Workflow

```bash
git clone git@github.com:RahulRoy-rsp/git_learnings.git
cd commands
git status
```

---

### 🧠 Related Commands

| Command                                   | Purpose                             |
| ----------------------------------------- | ----------------------------------- |
| [`git init`](init.md)                     | Start a new repository from scratch |
| [`git remote`](/commands/2_Intermediate/remote.md) | Manage remote repositories          |
| [`git pull`](/commands/2_Intermediate/pull.md)     | Get updates from a remote repo      |

---

### 🏁 Summary

* `git clone` copies an existing repo to your machine.
* You can use HTTPS or SSH.
* Ideal for collaboration and open-source contributions.

---

**Next Step:** 👉 Explore your new repo using [git status](status.md).
