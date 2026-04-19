
# 🧪 Practice Lab — Rebasing Mastery

---

## 🎯 Objective

By completing this lab, you will:

- perform basic rebase
- compare merge vs rebase
- resolve rebase conflicts
- use interactive rebase
- squash and reword commits

---

## 📊 Target Graph

```text
main:     A --- B --- C --- X --- D' --- E'
````

---

## 🛠 Setup

```bash
mkdir rebase-lab
cd rebase-lab
git init

echo "start" > app.txt
git add .
git commit -m "Initial commit"
```

---

## 🧩 Task 1 — Create Feature Branch

```bash
git switch -c feature
echo "feature work" >> app.txt
git commit -am "Feature commit 1"

echo "more work" >> app.txt
git commit -am "Feature commit 2"
```

---

## 🧩 Task 2 — Update Main

```bash
git switch main
echo "main update" >> app.txt
git commit -am "Main change"
```

---

## 🧩 Task 3 — Rebase Feature

```bash
git switch feature
git rebase main
```

---

## 📊 Expected

```text
main:     A --- B --- C --- X --- D' --- E'
```

---

## 🧩 Task 4 — Create Conflict

```bash
git switch main
echo "conflict A" > app.txt
git commit -am "Main conflict"

git switch feature
echo "conflict B" > app.txt
git commit -am "Feature conflict"
```

---

## 🧩 Task 5 — Rebase with Conflict

```bash
git rebase main
```

---

## ⚠️ Resolve Conflict

1. open file
2. remove markers
3. choose final content

Then:

```bash
git add app.txt
git rebase --continue
```

---

## 🧩 Task 6 — Interactive Rebase

```bash
git rebase -i HEAD~3
```

Try:

* squash commits
* reorder commits
* reword messages

---

## 🧩 Task 7 — Abort Rebase

```bash
git rebase --abort
```

---

## 🧩 Task 8 — Compare with Merge

```bash
git switch main
git merge feature
```

---

## 📊 Compare

```bash
git log --oneline --graph --all
```

---

## 📊 Visual Output

```text
Rebase → linear history
Merge → graph history
```

---

## 🔥 Bonus Challenges

---

### 🔹 Use fixup

```text
fixup commit
```

---

### 🔹 Create multiple conflicts

---

### 🔹 Reorder commits logically

---

## ⚠️ Common Mistakes

* forgetting `--continue`
* editing wrong section
* not testing after rebase
* rebasing shared branch

---

## 🧠 What You Learned

* rebase workflow
* conflict resolution
* interactive rebase
* history rewriting

---

## 🧠 Memory Trick

> Rebase = replay + fix conflicts

---

## 🚀 Next Step

👉 Move to: `05-Advanced-Git/README.md`
