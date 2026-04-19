
# 🧩 Squash Commits (Combine Multiple Commits into One)

---

## 🎯 Why This Matters

During development, you often create many small commits:

```text
fix bug
fix typo
update code
final fix
````

This makes history messy.

Squashing helps you:

* combine related commits
* create clean commit history
* improve readability
* prepare for pull requests

---

## ✅ Definition

Squashing is:

> combining multiple commits into a single commit

---

## 🧠 Mental Model

Before squash:

```text
A --- B --- C --- D --- E
```

After squash:

```text id="sq1"
A --- B --- C --- (DE)
```

👉 D and E merged into one commit

---

## 📊 Visual (Mermaid)

```mermaid id="sq2"
gitGraph
   commit id: "A"
   commit id: "B"
   commit id: "C"
   commit id: "D"
   commit id: "E"
```

(After squash → D + E combined)

---

## 🛠 Main Command

```bash id="sq3"
git rebase -i HEAD~3
```

---

## 🧪 Example

Run:

```bash id="sq4"
git rebase -i HEAD~3
```

You see:

```text id="sq5"
pick C commit C
pick D commit D
pick E commit E
```

Modify to:

```text id="sq6"
pick C commit C
squash D commit D
squash E commit E
```

---

## 🔬 What Happens Internally

1. Git takes commits D and E
2. combines their changes
3. creates new commit
4. generates new commit hash

---

## 🏗 Internal Architecture

---

### Before

```text id="sq7"
E → D → C → B → A
```

---

### After

```text id="sq8"
(DE)' → C → B → A
```

👉 New commit replaces old ones

---

## ⚡ Key Insight

> Squashing rewrites history and creates new commits

---

## 🧩 Real Use Cases

---

### 🔹 Clean PR history

Before:

```text id="sq9"
fix
fix again
typo
final fix
```

After:

```text id="sq10"
Add login feature
```

---

### 🔹 Combine related changes

---

### 🔹 Improve commit messages

---

## 🛠 Command Variants

---

### Squash commits

```bash id="sq11"
git rebase -i HEAD~n
```

---

### Fixup (auto squash without message)

```text id="sq12"
fixup D
```

---

### Continue rebase

```bash id="sq13"
git rebase --continue
```

---

## ⚠️ Common Mistakes

---

### ❌ Squashing wrong commits

👉 review carefully

---

### ❌ Losing commit messages

👉 combine messages properly

---

### ❌ Rebasing shared branch

👉 unsafe

---

## 🧠 Best Practices

* squash before PR
* keep commits meaningful
* group related changes
* use clear commit message

---

## 🧠 Interview-Level Explanation

**Q: What is squashing in Git?**

Answer:

> Squashing is the process of combining multiple commits into a single commit, typically using interactive rebase, to create a cleaner and more meaningful commit history.

---

## 🧠 Memory Trick

> Squash = combine commits

---

## ✅ Quick Recap

* combines multiple commits
* uses interactive rebase
* creates new commit
* improves history clarity

---

## Check Yourself

1. What happens to commit hashes after squash?
2. When should you squash commits?
3. What is difference between squash and fixup?
4. Why avoid squashing shared commits?

---

## ➡️ Next Step

Go to: `05-reword-commits.md`
