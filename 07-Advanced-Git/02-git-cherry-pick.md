
# 🍒 Git Cherry-Pick (Selective Commit Transfer)

<p align="center">
  <img src="https://img.shields.io/badge/Level-Advanced-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Selective%20Commits-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Use-Real%20Team%20Fixes-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Skill-Precision%20Git-purple?style=for-the-badge" />
</p>

<p align="center">
  <b>Apply specific commits from one branch to another without merging everything.</b>
</p>

---

## 📌 What Is Git Cherry-Pick?

`git cherry-pick` allows you to:

> Take a specific commit from one branch and apply it to another branch.

---

## 🧠 Why Cherry-Pick?

Scenario:

```text
You fixed a bug in develop
But production needs the same fix urgently
````

Instead of merging entire branch:

👉 Use cherry-pick to bring ONLY that commit

---

## 🗺️ Big Picture

```mermaid
flowchart LR
    A[Branch A] --> B[Commit X]
    B --> C[Cherry Pick]
    C --> D[Branch B]
```

---

## 🧬 Visual Example

```text id="k2t91v"
main:     A --- B --- C
                    \
feature:             D --- E (fix commit)

Cherry-pick E → main

Result:
main:     A --- B --- C --- E'
```

👉 `E'` = new commit (copy of E)

---

## 🧱 Basic Command

```bash id="n8cz2p"
git cherry-pick <commit-hash>
```

---

## 🧠 Important Concept

Cherry-pick does NOT move commit.

It creates a **new commit with same changes**.

---

## 🔍 How to Find Commit Hash

```bash id="7hzj0a"
git log
```

---

## 🧪 Real-World Scenario

```text id="4d3b8r"
1. Bug fixed in feature branch
2. Production needs fix
3. Cherry-pick commit
4. Deploy fix
```

---

## 🧱 Step-by-Step Example

---

### Step 1 — Go to target branch

```bash id="s8j3lp"
git checkout main
```

---

### Step 2 — Cherry-pick commit

```bash id="p1a2zx"
git cherry-pick abc123
```

---

### Result

```text id="5dzf7k"
New commit added to main
```

---

## 🔄 Multiple Commits

```bash id="x8o9lm"
git cherry-pick commit1 commit2 commit3
```

---

## 🔁 Range of Commits

```bash id="b0o6kf"
git cherry-pick A^..D
```

---

## ⚠️ Cherry-Pick Conflicts

If changes overlap:

```bash id="3g3o5j"
git cherry-pick abc123
```

May result in:

```text id="bq9d0u"
CONFLICT (content): Merge conflict
```

---

### Fix Conflict

```bash id="l2a4wr"
# resolve manually
git add .
git cherry-pick --continue
```

---

## 🧠 Internal Behavior

```text id="z1u9fj"
1. Git takes commit changes
2. Applies diff to current branch
3. Creates new commit
```

---

## 🧬 Internal Flow

```text id="v7r6tm"
Commit (source branch)
        ↓
Diff extracted
        ↓
Applied to target branch
        ↓
New commit created
```

---

## 🔀 Cherry-Pick vs Merge

| Cherry-Pick        | Merge            |
| ------------------ | ---------------- |
| specific commits   | full branch      |
| creates new commit | combines history |
| precise            | broader          |

---

## 🔀 Cherry-Pick vs Rebase

| Cherry-Pick    | Rebase             |
| -------------- | ------------------ |
| select commits | replay full branch |
| manual         | automatic sequence |

---

## 🚨 Common Mistakes

---

### ❌ Duplicate commits

Cherry-pick creates new commit → duplicates possible.

---

### ❌ Losing context

Commit may depend on earlier commits.

---

### ❌ Overusing cherry-pick

Can create messy history.

---

## ✅ Best Practices

* use for hotfixes
* use for small changes
* avoid large features
* understand dependencies
* test after applying

---

## 🧪 Real Use Cases

* hotfix in production
* applying patch across branches
* backporting changes
* selective bug fixes

---

## 🎤 Interview Questions

### What is git cherry-pick?

Apply a specific commit from one branch to another.

---

### Does cherry-pick move commit?

No, it copies changes and creates new commit.

---

### When to use cherry-pick?

For selective changes, hotfixes, or backports.

---

### What happens if conflict occurs?

Resolve manually and continue.

---

## 🧪 Practice Lab

```bash id="4m2n3o"
# create commit in branch
git checkout -b feature
echo "fix" >> file.txt
git commit -am "Fix bug"

# go to main
git checkout main

# cherry-pick
git cherry-pick <commit-hash>
```

---

## 🎯 Final Takeaway

Cherry-pick is a **precision tool**.

Use it when you need:

* exact change
* quick fix
* minimal impact

---

## 👉 Next Step

➡️ `03-git-reflog.md`
