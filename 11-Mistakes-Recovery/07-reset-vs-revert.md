
# 🔄 Git Reset vs Revert (Master the Difference)

> “Reset rewrites history. Revert writes new history.”

---

## 🎯 What You’ll Learn

* Core difference between `reset` and `revert`
* When to use each (real-world scenarios)
* Internal behavior of both commands
* Safe vs dangerous operations

---

## 🧠 The Core Idea

```mermaid id="r5q7zv"
flowchart LR
    A[Git Reset] --> B[Move pointer backward]
    A --> C[Rewrite history]

    D[Git Revert] --> E[Create new commit]
    D --> F[Preserve history]
```

---

## 🔬 Starting Point

```mermaid id="6ix6mf"
graph LR
    A --> B --> C --> D

    main --> D
```

---

# ⚙️ Git Reset

---

## 🧠 What Reset Does

```mermaid id="n8dzvt"
graph LR
    A --> B --> C --> D

    main --> D

    main -. move back .-> B
```

👉 Moves branch pointer backward
👉 Deletes commits from history (log view)

---

## 🧪 Command

```bash id="98f1tq"
git reset --hard HEAD~2
```

---

## 🧠 Result

```mermaid id="q7m7zq"
graph LR
    A --> B

    main --> B

    C -. dangling .- D
```

👉 Commits `C` and `D`:

* Not visible in history
* Still exist internally (temporarily)

---

## ⚠️ Reset Types Recap

| Type      | Effect               |
| --------- | -------------------- |
| `--soft`  | Keep staged changes  |
| `--mixed` | Keep working changes |
| `--hard`  | Delete everything    |

---

## ❗ When to Use Reset

* Local cleanup
* Before pushing
* Fixing recent commits

---

# 🔁 Git Revert

---

## 🧠 What Revert Does

```mermaid id="fx9y1x"
graph LR
    A --> B --> C --> D

    main --> D

    D --> E[Revert Commit]
    main --> E
```

👉 Creates a new commit that **undoes changes**

---

## 🧪 Command

```bash id="7q7xch"
git revert HEAD
```

---

## 🧠 Result

```mermaid id="s8k1po"
graph LR
    A --> B --> C --> D --> E

    E[Undo D]
    main --> E
```

👉 History is preserved
👉 No commits are deleted

---

## ❗ When to Use Revert

* Shared branches
* Team projects
* Production code

---

# ⚔️ Side-by-Side Comparison

```mermaid id="8q3u3v"
graph TD
    A[Reset] --> B[Rewrites history]
    A --> C[Deletes commits]

    D[Revert] --> E[Creates new commit]
    D --> F[Keeps history intact]
```

---

## 📊 Comparison Table

| Feature            | Reset     | Revert     |
| ------------------ | --------- | ---------- |
| History            | Rewritten | Preserved  |
| Safe for teams     | ❌ No      | ✅ Yes      |
| Deletes commits    | ✅ Yes     | ❌ No       |
| Creates new commit | ❌ No      | ✅ Yes      |
| Use case           | Local fix | Public fix |

---

## 🔍 Real-World Scenario

### ❌ Wrong Commit Pushed

```mermaid id="w3nz2z"
graph LR
    A --> B --> C

    main --> C
```

---

### Option 1: Reset (Bad for team)

```mermaid id="9wbv4r"
graph LR
    A --> B

    main --> B
```

👉 Breaks team history ❗

---

### Option 2: Revert (Correct)

```mermaid id="gmv1yo"
graph LR
    A --> B --> C --> D

    D[Revert C]
    main --> D
```

👉 Safe & traceable ✅

---

## 🧠 Internal Behavior

```mermaid id="z91x6n"
flowchart TD
    A[Reset] --> B[Move branch pointer]
    B --> C[Old commits become unreachable]

    D[Revert] --> E[Create inverse commit]
    E --> F[History remains intact]
```

---

## 🧭 Decision Flow

```mermaid id="j7lgm1"
flowchart TD
    A[Need to undo commit] --> B{Pushed?}

    B -->|No| C[Use Reset]
    B -->|Yes| D[Use Revert]

    C --> E[Fast cleanup]
    D --> F[Safe for team]
```

---

## ❗ Common Mistakes

* ❌ Using reset on shared branches
* ❌ Force pushing after reset
* ❌ Not understanding history rewrite

---

## 🧠 Interview Insight

👉 Question:
**Difference between `git reset` and `git revert`?**

👉 Answer:

* `reset` → moves pointer, rewrites history
* `revert` → creates new commit, keeps history

---

## ⚡ Pro Tips (Elite Level)

* Use reset only **locally**
* Use revert in **collaborative environments**
* Combine:

  * `revert` + `cherry-pick` for advanced workflows
* Always think:
  👉 “Is this branch shared?”

---

## 🧪 Advanced Trick

Revert multiple commits:

```bash id="tr2z5s"
git revert HEAD~3..HEAD
```

---

## 🚀 Next Step

➡️ Move to: **`emergency-guide.md`**
