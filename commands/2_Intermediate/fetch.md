# Git fetch

### 📖 Description
> The `git fetch` command downloads commits, branches, and files from a **remote repository** without merging them into your current work.  

---

### 💡 Why It’s Important
Fetching allows you to **see what others have changed** before merging or pulling their updates — helping prevent conflicts and surprises.

---

### 🧠 Syntax
```bash
git fetch [remote] [branch]
```

---

### 🧩 Examples

#### 1. Fetch All Branches from Remote

```bash
git fetch origin
```

**Explanation:**
Downloads all branches from the `origin` remote, but doesn’t change your working files.

---

#### 2. Fetch a Specific Branch

```bash
git fetch origin main
```

**Explanation:**
Fetches only the `main` branch updates.

---

#### 3. Fetch and Prune Deleted Branches

```bash
git fetch -p
```

**Explanation:**
Removes stale remote-tracking branches that were deleted on the remote.

---

#### 4. Fetch from All Remotes

```bash
git fetch --all
```

**Explanation:**
Updates all remotes linked to your repo.

---

### ✅ Quick Recap

| Command                   | Description             |
| ------------------------- | ----------------------- |
| `git fetch origin`        | Get updates from remote |
| `git fetch origin branch` | Fetch specific branch   |
| `git fetch -p`            | Remove stale branches   |
| `git fetch --all`         | Fetch all remotes       |

---

### 🧩 Example Workflow

```bash
git fetch origin
git log origin/main --oneline
```

**Explanation:**
You can now inspect changes without merging them.

---

### 🧠 Related Commands

| Command                   | Purpose                   |
| ------------------------- | ------------------------- |
| [`git pull`](pull.md)     | Fetch + merge changes     |
| [`git remote`](remote.md) | Manage remote connections |
| [`git merge`](merge.md)   | Combine fetched updates   |

---

### 🏁 Summary

* `git fetch` is **safe** — it only downloads.
* Use it to preview remote updates before merging.
* Combine with `git log` to review changes.

---

**Next Step:** 👉 Learn how to [pull updates into your branch](pull.md).
