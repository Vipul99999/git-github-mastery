
# 🧪 Practice Lab — Branching Mastery

---

## 🎯 Objective

By completing this lab, you will:

- create branches
- switch between branches
- observe commit separation
- understand branch pointers
- simulate feature workflow
- simulate hotfix workflow

---

## 📊 Visual (What You Will Build)

```text
main:   A --- B --- C
                     \
feature:              D --- E
                     \
hotfix:               F
````

---

## 🛠 Setup

```bash
mkdir branching-lab
cd branching-lab
git init

echo "start" > app.txt
git add .
git commit -m "Initial commit"
```

---

## 🧩 Task 1 — Create Feature Branch

```bash
git switch -c feature-login
```

---

## 🧩 Task 2 — Work on Feature

```bash
echo "login code" >> app.txt
git commit -am "Add login feature"
```

---

## 🧩 Task 3 — Switch Back to Main

```bash
git switch main
```

👉 Notice: login code is NOT here

---

## 🧩 Task 4 — View History

```bash
git log --oneline --graph --all
```

---

## 🧩 Task 5 — Create Hotfix

```bash
git switch -c hotfix-bug
echo "fix bug" >> app.txt
git commit -am "Fix bug"
```

---

## 🧩 Task 6 — Merge Hotfix

```bash
git switch main
git merge hotfix-bug
```

---

## 🧩 Task 7 — Merge Feature

```bash
git merge feature-login
```

---

## 🧩 Task 8 — Delete Branches

```bash
git branch -d feature-login
git branch -d hotfix-bug
```

---

## 🧠 Internal Observation

Check:

```bash
ls .git/refs/heads/
```

👉 See branch files

---

## 🎯 Expected Outcome

* separate histories created
* branches merged correctly
* understanding of isolation achieved

---

## 🔥 Bonus Challenges

### 🔹 View graph clearly

```bash
git log --oneline --graph --decorate --all
```

---

### 🔹 Create multiple features

```bash
git switch -c feature-dashboard
```

---

### 🔹 Try wrong merge order

Observe conflicts or differences

---

## ⚠️ Common Mistakes

* working on wrong branch
* forgetting to switch
* merging without checking
* deleting unmerged branch

---

## 🧠 What You Learned

* branch isolation
* pointer movement
* feature workflow
* hotfix workflow
* merging basics

---

## 🧠 Memory Trick

> Branch = separate timeline

---

## 🚀 Next Step

👉 Move to: `03-Merging/README.md`
