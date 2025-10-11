# Git push

### 📖 Description
> The `git push` command uploads your local commits to a **remote repository**.  
> It’s how your work becomes visible to others.

---

### 💡 Why It’s Important
Without pushing, your changes remain local.  
`git push` ensures your progress is shared, reviewed, or deployed.

---

### 🧠 Syntax
```bash
git push [remote] [branch]
```

---

### 🧩 Examples

#### 1. Push to Default Remote and Branch

```bash
git push
```

**Explanation:**
Pushes current branch commits to its remote tracking branch.

---

#### 2. Push to a Specific Remote

```bash
git push origin main
```

**Explanation:**
Uploads your local `main` branch to the remote named `origin`.

---

#### 3. Push and Set Upstream

```bash
git push -u origin main
```

**Explanation:**
Links your local `main` with remote `main` for future pulls/pushes.

---

#### 4. Force Push (Use with Caution)

```bash
git push --force
```

**Explanation:**
Overwrites remote branch history with local commits. Only use when necessary.

---

#### 5. Push All Branches

```bash
git push --all
```

**Explanation:**
Pushes all local branches to the remote.

---

### ✅ Quick Recap

| Command                   | Description             |
| ------------------------- | ----------------------- |
| `git push`                | Push current branch     |
| `git push origin main`    | Push to specific branch |
| `git push -u origin main` | Set upstream            |
| `git push --force`        | Force push changes      |

---

### 🧩 Example Workflow

```bash
git add .
git commit -m "Add new feature"
git push -u origin feature/login
```

---

### 🧠 Related Commands

| Command                               | Purpose                        |
| ------------------------------------- | ------------------------------ |
| [`git pull`](pull.md)                 | Fetch and merge remote changes |
| [`git remote`](remote.md)             | Manage remote connections      |
| [`git branch`](/commands/1_Beginner/branch.md) | Manage local branches          |

---

### 🏁 Summary

* Push uploads commits to a shared repo.
* Use `-u` once to link tracking branches.
* Avoid `--force` unless you know why.

---

**Next Step:** 👉 Learn how to [merge branches](merge.md).
