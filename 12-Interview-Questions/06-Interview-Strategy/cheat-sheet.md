
# 🧠 Git Ultimate Cheat Sheet (Memory + Recall)

> “If you remember this, you can answer almost any Git question.”

---

# ⚡ 1. Core Mental Model

```mermaid id="cs1"
graph LR
    A[Commits] --> B[Branches]
    B --> C[HEAD]
```

```text id="csm1"
Git = commits + pointers
Branch = pointer to commit
HEAD = current pointer
```

---

# ⚙️ 2. Git Workflow

```mermaid id="cs2"
flowchart LR
    A[Working Directory] --> B[Staging Area]
    B --> C[Commit]
    C --> D[Repository]
```

```text id="csm2"
edit → add → commit → push
```

---

# 🧩 3. Git Internals (Must Know)

```text id="csm3"
Blob = file content
Tree = directory structure
Commit = snapshot + metadata
SHA = unique ID
```

---

```mermaid id="cs3"
flowchart TD
    A[Commit] --> B[Tree]
    B --> C[Blob]
```

---

# 🌿 4. Branching

```text id="csm4"
Branch = pointer
Switch = move HEAD
Merge = combine
Rebase = rewrite
```

---

```mermaid id="cs4"
graph LR
    A --> B --> C
    B --> D --> E
```

---

# 🔀 5. Merge vs Rebase

```text id="csm5"
Merge = keeps history (safe)
Rebase = linear history (clean but rewrites)
```

---

```mermaid id="cs5"
graph LR
    A --> B --> C
    B --> D --> E
```

---

# 🔄 6. Reset vs Revert

```text id="csm6"
Reset = move pointer (danger)
Revert = new commit (safe)
```

---

```mermaid id="cs6"
flowchart LR
    A[Reset] --> B[Rewrite history]
    C[Revert] --> D[Preserve history]
```

---

# 📦 7. Staging Area

```text id="csm7"
git add = stage changes
git commit = save snapshot
```

---

# 🌍 8. Remote Basics

```text id="csm8"
origin = remote repo
push = upload
pull = fetch + merge
fetch = download only
```

---

```mermaid id="cs8"
flowchart LR
    A[Local] -->|push| B[Remote]
    B -->|pull| A
```

---

# 🧠 9. Reflog (Recovery Tool)

```text id="csm9"
reflog = history of HEAD
used to recover lost commits
```

---

```mermaid id="cs9"
graph TD
    A[HEAD@{0}]
    B[HEAD@{1}]
    C[HEAD@{2}]
```

---

# 🧪 10. Undo Cheats

```text id="csm10"
Undo commit keep changes → git reset --soft
Undo commit unstage → git reset
Delete commit → git reset --hard
Safe undo → git revert
```

---

# 🗑️ 11. File Recovery

```text id="csm11"
restore file → git restore file.txt
old version → git checkout <commit> -- file
```

---

# 🧭 12. Common Fixes

```text id="csm12"
Wrong branch → cherry-pick
Lost commit → reflog
Detached HEAD → create branch
Conflict → edit + add + commit
```

---

# ⚡ 13. Cherry-Pick

```text id="csm13"
copy commit from one branch to another
```

---

# ⚠️ 14. Dangerous Commands

```text id="csm14"
git reset --hard → deletes changes
git push --force → overwrites history
git clean -fd → deletes untracked files
```

---

# 🔍 15. Debug Toolkit

```bash id="csm15"
git status
git log --oneline --graph --all
git reflog
git show <commit>
git diff
```

---

# 🧪 16. Conflict Markers

```text id="csm16"
<<<<<<< HEAD
=======
>>>>>>> branch
```

---

# 🧭 17. Decision Rules

```mermaid id="cs17"
flowchart TD
    A[Undo needed] --> B{Pushed?}

    B -->|No| C[Use reset]
    B -->|Yes| D[Use revert]
```

---

# 🧠 18. Interview Traps

```text id="csm18"
merge vs rebase
reset vs revert
fetch vs pull
```

👉 Always explain with:

* difference
* use case

---

# ⚡ 19. Power Words

```text id="csm19"
snapshot
pointer
object database
history rewrite
reference
```

---

# 🧪 20. Fast Debug Flow

```mermaid id="cs20"
flowchart TD
    A[Problem] --> B[git status]
    B --> C[git log]
    C --> D[git reflog]
    D --> E[Recover]
```

---

# ⚡ 21. 10-Second Full Revision

```text id="csm21"
Git = snapshots
Branch = pointer
HEAD = current
Merge = combine
Rebase = rewrite
Reset = dangerous
Revert = safe
Reflog = recovery
```

---

# 🧭 22. Master Thought

```mermaid id="cs22"
flowchart LR
    A[Commits] --> B[Branches]
    B --> C[HEAD]
    C --> D[History Control]
```

---

# 🏁 Final Thought

> “If you understand pointers and history, Git becomes simple.”

---

# 🚀 You Are Now

```mermaid id="csfinal"
flowchart LR
    A[Beginner] --> B[Intermediate]
    B --> C[Advanced]
    C --> D[Scenario Master]
    D --> E[Interview Ready 🚀]
```

---

## 🎯 Final Message

> “This cheat sheet is not for reading —
> it’s for **thinking instantly under pressure**.”

