
# 🔍 Project 05: Git Debugging Simulation

---

## 🎯 Objective

Fix a broken repository.

---

## 🧪 Scenario

* commits lost
* branch deleted
* wrong merge

---

## 🧠 Debug Flow

```mermaid
flowchart TD
    A[Broken repo] --> B[git status]
    B --> C[git log]
    C --> D[git reflog]
    D --> E[Recover]
```

---

## ⚙️ Tasks

```bash
git reflog
git checkout -b recovery <commit>
git reset --hard <commit>
```

---

## 🏁 Outcome

```text
You can fix any Git issue
```
