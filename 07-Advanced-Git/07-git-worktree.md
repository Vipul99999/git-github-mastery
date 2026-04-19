
# 🌳 Git Worktree (Multiple Working Directories)

<p align="center">
  <img src="https://img.shields.io/badge/Level-Advanced-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Multi%20Branch%20Work-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Use-Parallel%20Development-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Skill-Productivity%20Boost-purple?style=for-the-badge" />
</p>

<p align="center">
  <b>Work on multiple branches simultaneously without switching — a powerful alternative to stashing.</b>
</p>

---

## 📌 What Is Git Worktree?

`git worktree` allows you to:

> Have multiple working directories (folders) linked to the same repository.

---

## 🧠 Why Use Worktree?

Problem:

```text
You are working on Feature A
→ Need to quickly check Feature B
→ Switching branches disrupts work
````

Solution:

👉 Use multiple working directories

---

## 🗺️ Big Picture

```mermaid
flowchart LR
    A[Main Repo] --> B[Worktree 1 (main)]
    A --> C[Worktree 2 (feature)]
    A --> D[Worktree 3 (bugfix)]
```

---

## 🧬 Concept Visualization

```text id="l3t9m2"
Single Git Repository
        │
        ├── Folder 1 → main branch
        ├── Folder 2 → feature/login
        └── Folder 3 → bugfix/navbar
```

---

## 🧱 Basic Command

```bash id="b2q6zn"
git worktree add <path> <branch>
```

---

## 🧪 Example

```bash id="n8t2a7"
git worktree add ../feature-login feature/login
```

### Result:

```text id="3c7k5m"
Current folder → main
New folder     → feature/login
```

---

## 🧠 Internal Behavior

```text id="u7f3px"
Single .git directory
Multiple working directories
Each linked to a branch
```

---

## 🔄 Worktree Flow

```text id="h9d1rq"
Repo
 ├── main (folder A)
 ├── feature (folder B)
 └── bugfix (folder C)
```

---

## 🧱 Common Commands

---

### List worktrees

```bash id="z6w2fd"
git worktree list
```

---

### Remove worktree

```bash id="r1m8kx"
git worktree remove <path>
```

---

### Prune unused

```bash id="s9v2hf"
git worktree prune
```

---

## 🧪 Real-World Scenario

```text id="m8k4yt"
1. Working on feature/login
2. Need urgent bug fix
3. Create new worktree
4. Fix bug without touching current work
```

---

## 🧠 Worktree vs Checkout

| Worktree         | Checkout           |
| ---------------- | ------------------ |
| multiple folders | single folder      |
| parallel work    | switching branches |
| no interruption  | context switching  |

---

## 🧠 Worktree vs Stash

| Worktree              | Stash                   |
| --------------------- | ----------------------- |
| separate workspace    | temporary save          |
| no hiding changes     | hides changes           |
| better for long tasks | better for short switch |

---

## ⚠️ Important Rules

---

### ❗ One branch per worktree

```text id="7f3z2y"
Same branch cannot be active in multiple worktrees
```

---

### ❗ Clean removal required

```bash id="j8r1kp"
git worktree remove <path>
```

---

## 🚨 Common Mistakes

---

### ❌ Forgetting worktree exists

Leads to confusion.

---

### ❌ Editing same branch in multiple places

Not allowed.

---

### ❌ Not cleaning unused worktrees

Clutters system.

---

## ✅ Best Practices

* use for parallel tasks
* name folders clearly
* remove unused worktrees
* use for debugging or hotfix

---

## 🧠 Advanced Use Case

---

### Scenario: Review PR while coding

```text id="p2y8zx"
Worktree 1 → main work
Worktree 2 → review PR branch
```

---

### Scenario: Compare branches

```text id="t4n6kp"
Open two folders side-by-side
```

---

## 🧬 Internal Architecture

```text id="z8y1kr"
.git/
 ├── objects
 ├── refs
 └── worktrees/
       ├── worktree1
       ├── worktree2
```

---

## 🧪 Practice Lab

```bash id="u3n6hz"
# create new worktree
git worktree add ../test-branch test

# list
git worktree list

# remove
git worktree remove ../test-branch
```

---

## 🎤 Interview Questions

### What is git worktree?

Allows multiple working directories for one repo.

---

### Why use worktree?

To work on multiple branches simultaneously.

---

### Difference from checkout?

Checkout switches branch, worktree keeps multiple active.

---

### Can same branch be used twice?

No.

---

## 🎯 Final Takeaway

Git worktree is a **power productivity tool**.

Use it when:

* working on multiple tasks
* reviewing PRs
* debugging without interruption

---

## 👉 Next Step

➡️ `08-submodules.md`
