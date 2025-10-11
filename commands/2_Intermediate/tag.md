# Git tag

### 📖 Description
> The `git tag` command is used to **mark specific points** in history — usually releases or major milestones — with a human-readable label.

---

### 💡 Why It’s Important
Tags are commonly used to:
- Mark **version releases** (e.g., `v1.0`, `v2.0`).
- Identify important commits like production-ready states.
- Reference stable snapshots easily.

---

### 🧠 Syntax
```bash
git tag [options] <tag-name> [commit-id]
```

---

### 🧩 Examples

#### 1. Create a Lightweight Tag

```bash
git tag v1.0
```

**Explanation:**
Tags the latest commit with `v1.0`.

---

#### 2. Create an Annotated Tag

```bash
git tag -a v1.0 -m "First stable release"
```

**Explanation:**
Stores tag metadata such as author, date, and a message — recommended for release tags.

---

#### 3. View All Tags

```bash
git tag
```

**Example Output:**

```
v1.0
v1.1
v2.0
```

---

#### 4. Tag a Specific Commit

```bash
git tag -a v2.0 a1b2c3d -m "Version 2 release"
```

**Explanation:**
Applies a tag to an older commit (identified by its hash).

---

#### 5. Push Tags to Remote

```bash
git push origin --tags
```

**Explanation:**
Uploads all local tags to the remote repository.

---

#### 6. Delete a Tag

```bash
git tag -d v1.0
```

#### 7. Delete Remote Tag

```bash
git push origin --delete v1.0
```

---

### ✅ Quick Recap

| Command                    | What It Does             |
| -------------------------- | ------------------------ |
| `git tag v1.0`             | Create a lightweight tag |
| `git tag -a v1.0 -m "msg"` | Create annotated tag     |
| `git push origin --tags`   | Push all tags            |
| `git tag -d v1.0`          | Delete local tag         |

---

### 🧩 Example Workflow

```bash
# Tag current release
git tag -a v2.0 -m "Stable release v2.0"

# Push to remote
git push origin v2.0

# Verify
git show v2.0
```

---

### 🧠 Related Commands

| Command                                   | Purpose                    |
| ----------------------------------------- | -------------------------- |
| [`git log`](log.md)                       | View commits to tag        |
| [`git push`](push.md)         | Push tags or branches      |
| [`git checkout`](/commands/1_Beginner/checkout.md) | Switch to a tagged version |

---

### 🏁 Summary

* Tags mark important history points like releases.
* Annotated tags store more detail — ideal for versioning.
* Always push tags for team visibility.

---

**Next Step:** 👉 Move on to the [Advanced Level Commands](/commands/3_Advanced/) for deeper control over Git internals.
