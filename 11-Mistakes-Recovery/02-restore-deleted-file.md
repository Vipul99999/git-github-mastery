
# 🗑️ Restore Deleted File in Git

> “Deleted doesn’t mean gone — it means Git is waiting for you to find it.”

---

## 🎯 What You’ll Learn

* Recover deleted files (staged & unstaged)
* Restore from previous commits
* Use Git history as a recovery tool
* Understand how Git tracks files internally

---

## 🧠 Core Idea

Git doesn’t track files — it tracks **snapshots**.

```text
Commit A → Commit B → Commit C
          (file exists) (file deleted)
```

👉 Even if deleted in latest commit,
Git still has the file in **older snapshots**

---

## 🔍 Scenario 1: File Deleted (Not Committed Yet)

### 💥 You ran:

```bash
rm file.txt
```

### ✅ Restore it:

```bash
git restore file.txt
```

---

### 🧠 What happens:

```text
Working Directory → Restored from last commit
```

👉 Git pulls file from latest commit snapshot

---

## 🔍 Scenario 2: File Deleted & Staged

### 💥 You ran:

```bash
rm file.txt
git add .
```

### ✅ Restore:

```bash
git restore --staged file.txt
git restore file.txt
```

---

### 🧠 Flow:

```text
1. Unstage deletion
2. Restore file from commit
```

---

## 🔍 Scenario 3: File Deleted & Committed

### 💥 You ran:

```bash
git commit -m "deleted file"
```

---

### ✅ Option 1: Restore from previous commit

```bash
git checkout HEAD~1 -- file.txt
```

---

### 🧠 Visual:

```text
Before:
A ← B ← C (file deleted)

Restore from:
B → brings file back into working directory
```

---

## 🔍 Scenario 4: Restore Specific Version

```bash
git log -- file.txt
```

Find commit:

```text
a1b2c3 Added file.txt
```

Restore:

```bash
git checkout a1b2c3 -- file.txt
```

---

## 🔍 Scenario 5: File Deleted Long Ago (Use Reflog)

If commit history changed:

```bash
git reflog
```

Find commit:

```text
d4e5f6 HEAD@{3}: commit: had file.txt
```

Restore:

```bash
git checkout d4e5f6 -- file.txt
```

---

## 🧠 Internal Insight (Important)

When you delete a file:

* Git removes it from next snapshot
* BUT old snapshots still contain it

👉 File is stored as a **blob object** inside `.git`

---

## ⚙️ Modern vs Old Commands

| Task           | Modern                 | Old            |
| -------------- | ---------------------- | -------------- |
| Restore file   | `git restore`          | `git checkout` |
| Restore staged | `git restore --staged` | `git reset`    |

---

## 🧭 Visual Summary

```text
Case 1: Deleted (not staged)
→ git restore file.txt

Case 2: Deleted + staged
→ git restore --staged file.txt
→ git restore file.txt

Case 3: Deleted + committed
→ git checkout HEAD~1 -- file.txt

Case 4: Old version
→ git checkout <commit> -- file.txt
```

---

## 🚑 Emergency Trick (Fast Recovery)

```bash
git log --diff-filter=D --summary
```

👉 Shows deleted files

Then restore from commit.

---

## ❗ Common Mistake

> ❌ Running `git reset --hard` after deletion

This may:

* Remove file completely from working directory
* Make recovery harder (but still possible via reflog)

---

## 🧠 Interview Insight

👉 Question:
**How do you restore a deleted file in Git?**

👉 Answer:

* If not committed → `git restore`
* If committed → `git checkout <commit> -- file`
* If lost → use `git reflog`

---

## ⚡ Pro Tips

* Use `git status` to detect deletion early
* Always check history before panic
* Learn `git log -- file.txt` (super useful)
* Prefer `git restore` (modern Git)

---

## 👉 Next Step

➡️ `03-recover-lost-commit.md`

