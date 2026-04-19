# 🧠 Merge Strategies (How Git Combines Changes)

---

## 🎯 Why This Matters

Git does not merge blindly.

It uses **strategies** to decide how changes are combined.

Understanding strategies helps you:

- control merge behavior
- avoid conflicts
- debug complex merges
- handle real-world edge cases

---

## 🧠 Core Idea

> Merge strategy = algorithm Git uses to combine branches

---

## 📊 Types of Merge Strategies

---

### 1️⃣ Recursive Strategy (Default)

> Used for most merges (two branches)

---

### 📊 Visual

```text
main:     A --- B --- C --- X
                       \
feature:                D --- E
````

Result:

```text
main:     A --- B --- C --- X ---- M
                       \        /
feature:                D --- E
```

---

### 🧠 Key Points

* default strategy
* uses **three-way merge**
* finds common ancestor
* handles most real-world cases

---

## 🛠 Command

```bash
git merge feature
```

(Default = recursive)

---

## 🏗 Internal Behavior

* finds merge base
* compares changes
* creates merge commit

---

## ⚡ Key Insight

> Recursive = standard intelligent merge

---

---

### 2️⃣ Fast-Forward Strategy

> No merge commit, just pointer movement

---

### 📊 Visual

```text
main:     A --- B --- C
                       \
feature:                D --- E
```

Result:

```text
main:     A --- B --- C --- D --- E
```

---

## 🛠 Command

```bash
git merge feature
```

(automatic if possible)

---

### Force fast-forward only

```bash
git merge --ff-only feature
```

---

## ⚠️ Limitation

* only works when no divergence

---

---

### 3️⃣ No Fast-Forward Strategy

> Always create merge commit

---

### 📊 Visual

```text
main:     A --- B --- C -------- M
                       \      /
feature:                D --- E
```

---

## 🛠 Command

```bash
git merge --no-ff feature
```

---

## 🧠 Why Use It?

* keeps branch history visible
* useful for feature tracking

---

---

### 4️⃣ Ours Strategy

> Keep current branch, ignore incoming changes

---

## 🛠 Command

```bash
git merge -s ours feature
```

---

## 📊 Visual

```text
main:     A --- B --- C ---- M
                       \
feature:                D --- E (ignored)
```

---

## 🧠 Use Case

* discard feature changes
* keep history record

---

---

### 5️⃣ Theirs Strategy (via recursive option)

> Prefer incoming branch changes

---

## 🛠 Command

```bash
git merge -X theirs feature
```

---

## 📊 Behavior

* conflicting lines → choose feature version

---

## ⚠️ Important

Not a full strategy, but an **option to recursive**

---

---

### 6️⃣ Octopus Strategy

> Merge multiple branches at once

---

## 🛠 Command

```bash
git merge branch1 branch2 branch3
```

---

## 📊 Visual

```text
main:     A --- B --- C -------- M
                     \   \    /
                      D   E   F
```

---

## 🧠 Use Case

* multiple small branches
* rarely used in daily workflow

---

---

### 7️⃣ Subtree Strategy

> Merge projects with different directory structures

---

## 🧠 Use Case

* mono-repo setups
* combining repositories

---

## 🛠 Command

```bash
git merge -s subtree feature
```

---

---

## 📊 Strategy Comparison

| Strategy     | Merge Commit | Use Case                |
| ------------ | ------------ | ----------------------- |
| Recursive    | ✔ Yes        | Default                 |
| Fast-forward | ❌ No         | Linear history          |
| No-ff        | ✔ Yes        | Preserve branch history |
| Ours         | ✔ Yes        | Ignore incoming         |
| Theirs       | ✔ Yes        | Prefer incoming changes |
| Octopus      | ✔ Yes        | Multiple branches       |
| Subtree      | ✔ Yes        | Repo merging            |

---

## 🧩 Real-World Use Cases

---

### 🔹 Feature tracking

```bash
git merge --no-ff feature-login
```

---

### 🔹 Clean history

```bash
git merge --ff-only feature
```

---

### 🔹 Conflict-heavy merge

```bash
git merge -X theirs feature
```

---

### 🔹 Discard bad branch

```bash
git merge -s ours broken-feature
```

---

## ⚠️ Common Mistakes

---

### ❌ Not knowing default strategy

👉 recursive is default

---

### ❌ Using wrong strategy

👉 can lose changes

---

### ❌ Overusing `ours`

👉 hides bugs

---

### ❌ Ignoring merge structure

👉 leads to confusing history

---

## 🧠 Best Practices

* use default (recursive) in most cases
* use `--no-ff` for important features
* use `--ff-only` for strict workflows
* avoid advanced strategies unless needed

---

## 🧠 Interview-Level Explanation

**Q: What are merge strategies in Git?**

Answer:

> Merge strategies define how Git combines branches. The default recursive strategy uses a three-way merge. Other strategies like fast-forward, no-ff, ours, and subtree provide control over how histories and conflicts are handled.

---

## 🧠 Memory Trick

> Strategy = how Git thinks during merge

---

## ✅ Quick Recap

* Git uses strategies to merge
* recursive = default
* fast-forward = simple pointer move
* no-ff = always create commit
* others = special cases

---

## ➡️ Next Step

Go to: `practice-lab.md`
