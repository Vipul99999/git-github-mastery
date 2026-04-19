
# 🕵️ Git Reflog (Recover Lost Work)

<p align="center">
  <img src="https://img.shields.io/badge/Level-Advanced-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Recovery-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Use-Debugging-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Skill-Git%20Internals-purple?style=for-the-badge" />
</p>

<p align="center">
  <b>Recover commits, branches, and lost work using Git's hidden history.</b>
</p>

---

## 📌 What Is Git Reflog?

`git reflog` shows:

> A log of all HEAD movements (your Git activity history)

---

## 🧠 Why Reflog Is Powerful

Even if you:

- delete a branch ❌
- reset commits ❌
- lose changes ❌

👉 Reflog can recover them.

---

## 🗺️ Big Picture

```mermaid
flowchart LR
    A[Commits] --> B[HEAD Moves]
    B --> C[Reflog Records]
    C --> D[Recover Lost Work]
````

---

## 🧬 What Reflog Tracks

```text id="4xv1tk"
- commits
- checkouts
- resets
- rebases
- merges
```

---

## 🧱 Basic Command

```bash id="h3y6qf"
git reflog
```

---

## 🔍 Example Output

```text id="9l3zfd"
a1b2c3 HEAD@{0}: commit: fix bug
d4e5f6 HEAD@{1}: checkout: moving to feature
g7h8i9 HEAD@{2}: commit: add feature
```

---

## 🧠 Key Concept

Reflog is:

```text id="5e3tqa"
Local only
Temporary (expires)
Hidden safety net
```

---

## 🧪 Real-World Scenario

```text id="d6u9g2"
1. You commit work
2. You accidentally run git reset --hard
3. Work seems gone
4. Use reflog → recover commit
```

---

## 🧱 Recover Lost Commit

---

### Step 1 — View reflog

```bash id="1z0o7s"
git reflog
```

---

### Step 2 — Identify commit

```text id="p3k8ru"
HEAD@{2}
```

---

### Step 3 — Recover

```bash id="s6y8t3"
git checkout HEAD@{2}
```

---

OR:

```bash id="6t2w0v"
git reset --hard HEAD@{2}
```

---

## 🧬 Internal Behavior

Git stores:

```text id="h6q9rx"
HEAD movements → reflog entries
```

---

## 🧠 HEAD Movement

```text id="m9d3zc"
HEAD → current commit pointer
```

Every time HEAD moves:

👉 Reflog records it

---

## 🔄 Visual Flow

```text id="4t8dwl"
Commit A → Commit B → Commit C
        ↑
     HEAD moves

Reflog tracks all moves
```

---

## 🧪 Recover Deleted Branch

```bash id="1okp1g"
git reflog
```

Find commit → recreate branch:

```bash id="kztfwm"
git checkout -b recovered-branch <commit-hash>
```

---

## 🧪 Recover After Reset

```bash id="jtkp4m"
git reset --hard HEAD~2
```

Oops 😱

Recover:

```bash id="hbn4tq"
git reflog
git reset --hard HEAD@{1}
```

---

## ⚠️ Important Notes

---

### Reflog is local

Not shared with remote.

---

### Reflog expires

```text id="g6r1lz"
default ~90 days
```

---

## 🚨 Common Mistakes

---

### ❌ Not using reflog after mistake

Many think work is lost forever.

---

### ❌ Using reset incorrectly

Reflog helps recover.

---

### ❌ Ignoring commit hashes

---

## ✅ Best Practices

* use reflog for recovery
* act quickly before expiration
* combine with log for clarity
* understand HEAD movement

---

## 🧠 Reflog vs Log

| Reflog                | Log                    |
| --------------------- | ---------------------- |
| shows history of HEAD | shows commit history   |
| includes lost commits | only reachable commits |

---

## 🎤 Interview Questions

### What is git reflog?

Tracks HEAD movement history.

---

### Can reflog recover deleted commits?

Yes (if not expired).

---

### Is reflog shared?

No, it is local.

---

### Difference between log and reflog?

Log shows commits, reflog shows actions.

---

## 🧪 Practice Lab

```bash id="i3u2c7"
# create commit
echo "test" >> file.txt
git commit -am "test commit"

# reset
git reset --hard HEAD~1

# recover
git reflog
git reset --hard HEAD@{1}
```

---

## 🎯 Final Takeaway

Reflog is your **safety net**.

It allows you to:

* recover lost commits
* undo mistakes
* debug history

---

## 👉 Next Step

➡️ `04-git-bisect.md`

