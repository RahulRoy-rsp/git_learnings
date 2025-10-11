# Git remote

### 📖 Description
> The `git remote` command lets you **connect your local repository** to one or more remote repositories (like GitHub, GitLab, or Bitbucket).  
> It’s how you push and pull changes between your local machine and the cloud.

---

### 💡 Why It’s Important
Git is **distributed**, meaning every developer has a full copy of the repo.  
Remotes make collaboration possible by serving as a **shared hub** for everyone’s work.

---

### 🧠 Syntax
```bash
git remote [command] [options]
```

---

### 🧩 Examples

#### 1. View Configured Remotes

```bash
git remote -v
```

**Explanation:**
Lists all remote repositories linked to your local repo, including their fetch/push URLs.

---

#### 2. Add a Remote Repository

```bash
git remote add origin https://github.com/user/project.git
```

**Explanation:**
Adds a remote called `origin` pointing to the given GitHub repository.

---

#### 3. Rename a Remote

```bash
git remote rename origin upstream
```

**Explanation:**
Renames your remote connection for clarity.

---

#### 4. Remove a Remote

```bash
git remote remove origin
```

**Explanation:**
Disconnects your local repo from the specified remote.

---

#### 5. Show Detailed Remote Info

```bash
git remote show origin
```

**Explanation:**
Displays detailed information about branches tracked from the `origin`.

---

### ✅ Quick Recap

| Command                       | Description           |
| ----------------------------- | --------------------- |
| `git remote -v`               | List remotes          |
| `git remote add origin <url>` | Add a new remote      |
| `git remote remove origin`    | Remove remote         |
| `git remote rename old new`   | Rename remote         |
| `git remote show origin`      | Show tracking details |

---

### 🧩 Example Workflow

```bash
git init
git remote add origin https://github.com/username/myrepo.git
git add .
git commit -m "Initial commit"
git push -u origin main
```

---

### 🧠 Related Commands

| Command                             | Purpose                  |
| ----------------------------------- | ------------------------ |
| [`git push`](push.md)               | Upload commits to remote |
| [`git pull`](pull.md)               | Get latest changes       |
| [`git clone`](/commands/1_Beginner/clone.md) | Copy a remote repository |

---

### 🏁 Summary

* Remotes connect your local and remote repositories.
* The default remote name is usually `origin`.
* Use `git remote -v` to confirm your connection.

---

**Next Step:** 👉 Learn how to [fetch updates](fetch.md).
