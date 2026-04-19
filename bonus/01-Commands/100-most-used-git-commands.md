
# ⚙️ 100 Most Used Git Commands (Ultimate Reference)

> “You don’t need to memorize Git — you need to recognize patterns.”

---

## 🧠 How to Use This File

```mermaid
flowchart LR
    A[Need something] --> B[Find category]
    B --> C[Copy command]
    C --> D[Understand usage]
```

---

# 🟢 1. Setup & Configuration

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
git config --global core.editor "code --wait"
git config --global init.defaultBranch main
```

---

# 📁 2. Repository Setup

```bash
git init
git clone <repo-url>
git clone --depth=1 <repo-url>
git init <folder>
git remote add origin <url>
```

---

# 📦 3. Basic Workflow

```bash
git status
git add .
git add <file>
git commit -m "message"
git commit -am "message"
git log
git log --oneline
git log --graph --oneline --all
```

---

# 🔍 4. Inspect Changes

```bash
git diff
git diff --staged
git show <commit>
git blame <file>
git log -- <file>
```

---

# 🌿 5. Branching

```bash
git branch
git branch <branch>
git checkout <branch>
git checkout -b <branch>
git switch <branch>
git switch -c <branch>
git branch -d <branch>
git branch -D <branch>
git branch -m <new-name>
```

---

# 🔀 6. Merging & Rebasing

```bash
git merge <branch>
git merge --no-ff <branch>
git rebase <branch>
git rebase -i HEAD~n
git merge --abort
git rebase --abort
git rebase --continue
```

---

# ⚔️ 7. Conflict Resolution

```bash
git status
git diff
git add <file>
git commit
git mergetool
git checkout --ours <file>
git checkout --theirs <file>
```

---

# 🔄 8. Undo & Reset

```bash
git reset
git reset HEAD~1
git reset --soft HEAD~1
git reset --mixed HEAD~1
git reset --hard HEAD~1
git revert <commit>
git restore <file>
git restore --staged <file>
```

---

# 🧠 9. Reflog & Recovery

```bash
git reflog
git checkout <commit>
git reset --hard <commit>
git fsck --lost-found
git show <commit>
```

---

# 📦 10. Stash

```bash
git stash
git stash save "message"
git stash list
git stash apply
git stash pop
git stash drop
git stash clear
git stash branch <branch>
```

---

# 🌍 11. Remote Repositories

```bash
git remote -v
git fetch
git pull
git pull --rebase
git push
git push -u origin <branch>
git push --force
git push --force-with-lease
```

---

# 🔗 12. Tags

```bash
git tag
git tag <tag>
git tag -a <tag> -m "message"
git push origin <tag>
git push origin --tags
git tag -d <tag>
```

---

# 📊 13. Logs & Visualization

```bash
git log --oneline --graph --decorate
git log --all --graph
git shortlog
git reflog
```

---

# 📁 14. File Operations

```bash
git rm <file>
git rm --cached <file>
git mv <old> <new>
git clean -fd
git clean -fdn
```

---

# 🧪 15. Cherry-Pick & Patch

```bash
git cherry-pick <commit>
git cherry-pick A^..B
git format-patch -1 <commit>
git apply <patch>
```

---

# ⚙️ 16. Advanced / Internals

```bash
git cat-file -p <hash>
git gc
git prune
git reflog expire
git fsck
```

---

# ⚡ 17. Aliases (Productivity)

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm commit
git config --global alias.lg "log --oneline --graph --all"
```

---

# 🧭 18. Useful Shortcuts

```bash
git checkout -
git switch -
git branch --merged
git branch --no-merged
git diff main..feature
git log main..feature
```

---

# 🧠 Command Mental Model

```mermaid
flowchart LR
    A[Working Directory] --> B[Staging Area]
    B --> C[Commit]
    C --> D[Branch]
    D --> E[Remote]
```

---

# ⚠️ Most Dangerous Commands

```bash
git reset --hard
git push --force
git clean -fd
```

👉 Use with caution

---

# ⚡ 10 Commands You MUST Remember

```text
git status
git add
git commit
git log
git branch
git checkout / switch
git merge
git pull
git push
git reflog
```

---

# 🚀 Pro Tip

```text
Don’t memorize commands.
Understand:
→ state
→ history
→ pointers
```

---

# 🏁 Final Thought

> “Git commands are just tools —
> understanding when to use them is mastery.”
