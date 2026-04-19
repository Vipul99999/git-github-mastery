

# 🧪 Practice Lab — Merging Mastery

---

## 🎯 Objective

By completing this lab, you will:

- perform fast-forward merge
- perform three-way merge
- create and resolve conflicts
- understand merge commits
- use merge strategies

---

## 📊 Target Graph

```text
main:     A --- B --- C --- X -------- M
                       \            /
feature:                D --- E ----
````

---

## 🛠 Setup

```bash
mkdir merge-lab
cd merge-lab
git init

echo "start" > app.txt
git add .
git commit -m "Initial commit"
```

---

## 🧩 Task 1 — Fast-Forward Merge

```bash
git switch -c feature1
echo "feature1" >> app.txt
git commit -am "Feature1 work"

git switch main
git merge feature1
```

---

## 📊 Expected

```text
main → moves forward (no merge commit)
```

---

## 🧩 Task 2 — Three-Way Merge

```bash
git switch -c feature2
echo "feature2" >> app.txt
git commit -am "Feature2 work"

git switch main
echo "main change" >> app.txt
git commit -am "Main update"

git merge feature2
```

---

## 📊 Expected

```text
Merge commit created
```

---

## 🧩 Task 3 — Create Conflict

```bash
git switch -c conflict-branch
echo "conflict change A" > app.txt
git commit -am "Conflict A"

git switch main
echo "conflict change B" > app.txt
git commit -am "Conflict B"

git merge conflict-branch
```

---

## ⚠️ Resolve Conflict

1. Open file
2. Remove markers
3. Choose final content

Then:

```bash
git add app.txt
git commit
```

---

## 🧩 Task 4 — Use No-FF Strategy

```bash
git switch -c feature3
echo "feature3" >> app.txt
git commit -am "Feature3"

git switch main
git merge --no-ff feature3
```

---

## 📊 Expected

```text
Merge commit even without need
```

---

## 🧩 Task 5 — Use Ours Strategy

```bash
git switch -c feature4
echo "bad code" >> app.txt
git commit -am "Bad change"

git switch main
git merge -s ours feature4
```

---

## 📊 Expected

```text
feature4 ignored, but merge recorded
```

---

## 🧩 Task 6 — Visualize History

```bash
git log --oneline --graph --decorate --all
```

---

## 🎯 Final Outcome

You should see:

* linear history (fast-forward)
* merge commits (three-way)
* conflict resolution
* different merge strategies

---

## 🔥 Bonus Challenges

---

### 🔹 Try `--ff-only`

```bash
git merge --ff-only feature
```

---

### 🔹 Abort merge

```bash
git merge --abort
```

---

### 🔹 Create multiple conflicts

Modify multiple lines

---

## ⚠️ Common Mistakes

* merging wrong branch
* not resolving conflicts fully
* forgetting `git add`
* skipping verification

---

## 🧠 What You Learned

* merge types
* conflict handling
* strategies
* commit graph understanding

---

## 🧠 Memory Trick

> Merge = combine histories + resolve conflicts

---

## 🚀 Next Step

👉 Move to: `04-Rebasing/README.md`
