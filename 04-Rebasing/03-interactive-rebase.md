
# 🧠 Interactive Rebase (Power Tool)

---

## 🎯 Why This Matters

Interactive rebase is one of the most powerful Git features.

It lets you:

- edit commits
- reorder commits
- squash commits
- clean history before sharing

---

## 🧠 Core Idea

> Interactive rebase = manually rewrite commit history

---

## 🛠 Command

```bash id="reb302"
git rebase -i HEAD~3
````

👉 opens editor with last 3 commits

---

## 📊 Example Commit History

```text
A --- B --- C --- D --- E
```

Run:

```bash id="reb303"
git rebase -i HEAD~3
```

You get:

```text id="reb304"
pick C commit message C
pick D commit message D
pick E commit message E
```

---

## 🧠 Rebase Actions

| Command | Meaning                |
| ------- | ---------------------- |
| pick    | keep commit            |
| reword  | edit message           |
| edit    | modify commit          |
| squash  | combine commits        |
| fixup   | squash without message |
| drop    | delete commit          |

---

## 📊 Visual (Before)

```text id="reb305"
A --- B --- C --- D --- E
```

---

## 📊 Visual (After Squash)

```text id="reb306"
A --- B --- C --- (DE)
```

---

## 📊 Visual (Mermaid)

```mermaid id="reb307"
gitGraph
   commit id: "A"
   commit id: "B"
   commit id: "C"
   commit id: "D"
   commit id: "E"
```

(After rebase → commits reordered/squashed)

---

## 🧩 Common Operations

---

### 🔹 Reorder commits

Change order:

```text id="reb308"
pick E
pick C
pick D
```

---

### 🔹 Squash commits

```text id="reb309"
pick C
squash D
squash E
```

---

### 🔹 Edit commit

```text id="reb310"
edit D
```

Then:

```bash id="reb311"
git commit --amend
git rebase --continue
```

---

### 🔹 Drop commit

```text id="reb312"
drop D
```

---

## 🔬 What Happens Internally

Interactive rebase:

1. selects commits
2. pauses for user input
3. rewrites commits one by one
4. creates new commit hashes

---

## ⚡ Key Insight

> Interactive rebase gives full control over history

---

## 🧩 Real Use Cases

---

### 🔹 Clean messy commits

Before PR:

```text id="reb313"
fix
fix again
typo
final fix
```

After squash:

```text id="reb314"
Add login feature
```

---

### 🔹 Fix commit messages

```bash id="reb315"
git rebase -i HEAD~3
```

---

### 🔹 Remove unwanted commits

Drop unnecessary changes

---

### 🔹 Reorder commits logically

---

## ⚠️ Common Mistakes

---

### ❌ Rebasing shared commits

👉 dangerous

---

### ❌ Losing commits

👉 due to wrong commands

---

### ❌ Not understanding actions

👉 leads to broken history

---

## 🧠 Best Practices

* use interactive rebase before pushing
* squash related commits
* write meaningful commit messages
* review changes before continuing

---

## 🧠 Interview-Level Explanation

**Q: What is interactive rebase?**

Answer:

> Interactive rebase allows developers to modify commit history by editing, reordering, squashing, or removing commits before integrating them into the main branch.

---

## 🧠 Memory Trick

> Interactive rebase = edit history manually

---

## ✅ Quick Recap

* `git rebase -i` opens editor
* allows commit control
* rewrites history
* creates clean commit log

---

## Check Yourself

1. What does `pick` mean?
2. How do you squash commits?
3. When should you use interactive rebase?
4. Why is it powerful?

---

## ➡️ Next Step

Go to: `04-rebase-conflicts.md`
