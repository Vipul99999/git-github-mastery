
# 🚑 Git Emergency Guide (Ultimate Recovery Playbook)

> “When everything breaks — this is where you think clearly and recover everything.”

---

## 🧠 Rule #1: STOP

```mermaid
flowchart TD
    A[Something broke 💥] --> B[STOP ❗]
    B --> C[Don't run random commands]
    C --> D[Check status]
    D --> E[Run reflog]
```

👉 Most damage happens after panic.

---

## 🧭 Step 0: Diagnose the Situation

Run:

```bash
git status
git log --oneline --graph --all
git reflog
```

---

## 🧠 Identify Your Problem Type

```mermaid
flowchart TD
    A[Problem] --> B{What happened?}

    B --> C[Lost commit]
    B --> D[Deleted file]
    B --> E[Wrong branch]
    B --> F[Force push issue]
    B --> G[Broken repo state]
```

---

# 🔍 1. Recover Lost Commit

---

## 💥 Situation

* `git reset --hard`
* commit disappeared

---

## ✅ Solution

```bash
git reflog
```

Find:

```text
abc123 commit: important work
```

Restore:

```bash
git reset --hard abc123
```

---

## 🧠 Visual

```mermaid
graph LR
    A --> B --> C --> D

    HEAD --> B
    C -. hidden .- D
```

---

# 🗑️ 2. Restore Deleted File

---

## ✅ Quick Fix

```bash
git restore file.txt
```

---

## 🔎 From old commit

```bash
git checkout HEAD~1 -- file.txt
```

---

# 🌿 3. Fix Wrong Branch Commit

---

## ✅ Safe Method

```bash
git checkout correct-branch
git cherry-pick <commit>
```

---

## ❌ Avoid

```bash
git push --force
```

(unless you know what you’re doing)

---

# 💣 4. Force Push Disaster

---

## 💥 Situation

* Team commits lost

---

## 🚑 Recovery

```bash
git reflog
git checkout -b recovery <commit>
git push origin recovery
```

---

## 🧠 Team Recovery Flow

```mermaid
flowchart TD
    A[Force push damage] --> B[Ask team members]
    B --> C[Find commit via reflog]
    C --> D[Restore branch]
```

---

# 🧭 5. Detached HEAD Panic

---

## ✅ Fix

```bash
git checkout -b safe-branch
```

---

👉 Always save before switching branches

---

# ⚙️ 6. Broken Merge / Conflict Chaos

---

## 💥 Situation

* Merge conflicts everywhere

---

## ✅ Abort safely

```bash
git merge --abort
```

---

## Or for rebase:

```bash
git rebase --abort
```

---

# 🧠 MASTER TOOL: Reflog

---

## 🔥 Why it's powerful

```mermaid
graph TD
    A[Every Git action] --> B[Stored in reflog]
    B --> C[Even lost commits tracked]
    C --> D[Recover anything]
```

---

## 🧪 Use

```bash
git reflog
```

---

## ⚡ Restore anything

```bash
git checkout <commit>
git reset --hard <commit>
```

---

# 🔬 Advanced Debugging Handbook (Internals)

---

## 🧠 How Git Actually Works

```mermaid
flowchart TD
    A[Working Directory] --> B[Staging Area]
    B --> C[Commit Object]
    C --> D[Git Object Database]
```

---

## 🧩 Git Object Types

| Object | Description         |
| ------ | ------------------- |
| Blob   | File content        |
| Tree   | Folder structure    |
| Commit | Snapshot + metadata |

---

## 🔎 Inspect Internals

```bash
git cat-file -p <hash>
```

---

## 🧠 HEAD Internals

```mermaid
graph LR
    HEAD --> main
    main --> Commit
```

Detached:

```mermaid
graph LR
    HEAD --> Commit
```

---

# 🧪 Deep Debug Commands

---

## 🔍 Find lost objects

```bash
git fsck --lost-found
```

---

## 📦 Show commit details

```bash
git show <commit>
```

---

## 🧭 Visual history

```bash
git log --graph --oneline --all
```

---

## 🧠 Track file history

```bash
git log -- file.txt
```

---

# ⚠️ Dangerous Commands (Use Carefully)

---

| Command            | Risk                    |
| ------------------ | ----------------------- |
| `git reset --hard` | Deletes working changes |
| `git push --force` | Overwrites remote       |
| `git clean -fd`    | Deletes untracked files |

---

# 🧭 Ultimate Recovery Flow

```mermaid
flowchart TD
    A[Problem 💥] --> B[Run git status]
    B --> C[Run git reflog]
    C --> D[Find correct commit]

    D --> E{Goal?}

    E -->|Restore state| F[git reset --hard]
    E -->|Save safely| G[Create branch]
    E -->|Partial fix| H[cherry-pick]

    F --> I[Recovered ✅]
    G --> I
    H --> I
```

---

# 🧠 Pro-Level Safety Rules

* ✅ Always create a backup branch before risky actions
* ✅ Use `--force-with-lease` instead of `--force`
* ✅ Never rewrite shared history casually
* ✅ Learn reflog deeply

---

# ⚡ Elite Debugging Mindset

```mermaid
flowchart LR
    A[Problem] --> B[Analyze]
    B --> C[Understand state]
    C --> D[Recover safely]
    D --> E[Verify]
```

---

# 🧪 Real-World Debug Example

### 💥 You ran:

```bash
git reset --hard HEAD~3
```

---

### ✅ Recovery:

```bash
git reflog
git reset --hard HEAD@{1}
```

---

# 🏁 Final Thought

> “Git is not dangerous — blind commands are.”

---

# 🚀 Next Step

➡️ Move to:

* `12-Interview-Questions/`
