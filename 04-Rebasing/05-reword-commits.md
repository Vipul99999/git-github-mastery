

# ✏️ Reword Commits (Edit Commit Messages)

---

## 🎯 Why This Matters

Commit messages are critical for:

- understanding history
- debugging
- collaboration
- code reviews

Sometimes you need to:

- fix typos
- improve clarity
- follow conventions

---

## ✅ Definition

Rewording is:

> changing the commit message without changing its content

---

## 🧠 Mental Model

Before:

```text
A --- B --- C ("fix")
````

After:

```text id="rw1"
A --- B --- C' ("Fix login bug properly")
```

👉 same code
👉 new commit message
👉 new commit hash

---

## 📊 Visual (Mermaid)

```mermaid id="rw2"
gitGraph
   commit id: "A"
   commit id: "B"
   commit id: "C"
```

(C becomes C' after reword)

---

## 🛠 Main Command

```bash id="rw3"
git rebase -i HEAD~3
```

---

## 🧪 Example

You see:

```text id="rw4"
pick A commit A
pick B commit B
pick C fix
```

Change:

```text id="rw5"
pick A commit A
pick B commit B
reword C fix
```

---

## ✏️ Then Git Opens Editor

You update message:

```text id="rw6"
Fix login bug properly
```

---

## 🔬 What Happens Internally

1. Git selects commit
2. pauses rebase
3. allows message edit
4. creates new commit

---

## 🏗 Internal Architecture

---

### Before

```text id="rw7"
C → B → A
```

---

### After

```text id="rw8"
C' → B → A
```

---

## ⚡ Key Insight

> Even message change creates new commit hash

---

## 🛠 Command Variants

---

### Reword last commit

```bash id="rw9"
git commit --amend
```

---

### Reword older commits

```bash id="rw10"
git rebase -i HEAD~n
```

---

## 🧩 Real Use Cases

---

### 🔹 Fix typo

```text id="rw11"
fixt login → fix login
```

---

### 🔹 Improve clarity

---

### 🔹 Follow commit standards

---

### 🔹 Add meaningful description

---

## ⚠️ Common Mistakes

---

### ❌ Forgetting hash change

👉 commit ID changes

---

### ❌ Rewriting shared history

👉 dangerous

---

### ❌ Poor messages even after reword

---

## 🧠 Best Practices

* use clear, descriptive messages
* follow commit conventions
* reword before pushing
* keep messages concise

---

## 🧠 Interview-Level Explanation

**Q: What is rewording a commit?**

Answer:

> Rewording a commit means changing its commit message without modifying its content, typically done using interactive rebase or `git commit --amend`.

---

## 🧠 Memory Trick

> Reword = change message, not code

---

## ✅ Quick Recap

* changes commit message
* creates new commit hash
* done via rebase or amend
* improves history readability

---

## Check Yourself

1. Does reword change commit content?
2. Why does commit hash change?
3. When should you use reword?
4. What is difference between amend and reword?

---

## ➡️ Next Step

Go to: `practice-lab.md`