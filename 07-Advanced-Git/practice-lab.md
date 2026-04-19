

# 🧪 Advanced Git Practice Lab

<p align="center">
  <img src="https://img.shields.io/badge/Mode-Hands--On-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Level-Advanced-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Real%20Scenarios-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Outcome-Expert%20Git-purple?style=for-the-badge" />
</p>

<p align="center">
  <b>Practice advanced Git concepts through real-world scenarios.</b>
</p>

---

## 🎯 Objective

You will practice:

- stash
- cherry-pick
- reflog
- bisect
- tags
- hooks
- worktree
- submodules

---

## 🧪 LAB 1 — Git Stash

```bash id="y7d9kl"
echo "change" >> file.txt
git stash
git stash list
git stash pop
````

---

## 🧪 LAB 2 — Cherry-Pick

```bash id="r3k8tz"
git checkout -b feature
echo "fix" >> file.txt
git commit -am "fix"

git checkout main
git cherry-pick <commit>
```

---

## 🧪 LAB 3 — Reflog Recovery

```bash id="t6w4pn"
git commit -am "test"
git reset --hard HEAD~1

git reflog
git reset --hard HEAD@{1}
```

---

## 🧪 LAB 4 — Git Bisect

```bash id="x1j7qp"
git bisect start
git bisect bad
git bisect good <old>
```

---

## 🧪 LAB 5 — Git Tag

```bash id="k2m9xy"
git tag -a v1.0 -m "release"
git push origin v1.0
```

---

## 🧪 LAB 6 — Git Hooks

```bash id="f8q2zr"
cd .git/hooks
touch pre-commit
chmod +x pre-commit
```

---

## 🧪 LAB 7 — Git Worktree

```bash id="n4p8zv"
git worktree add ../test test
git worktree list
```

---

## 🧪 LAB 8 — Submodules

```bash id="c9k2rm"
git submodule add <repo>
git submodule update --init
```

---

## 🧠 Final Challenge (🔥)

---

### Scenario

```text id="k8t1rp"
You:
- broke code
- lost commit
- need fix from another branch
- must tag release
```

---

### Tasks

```text id="p7m3zn"
1. Recover commit (reflog)
2. Apply fix (cherry-pick)
3. Debug issue (bisect)
4. Save work (stash)
5. Tag version
```

---

## 🧠 Self Evaluation

```text id="r6y2pv"
[ ] Can I recover lost work?
[ ] Can I debug history?
[ ] Can I apply specific commits?
[ ] Can I manage multiple branches?
[ ] Can I use advanced tools?
```

---

## 🎯 Final Outcome

You are now:

```text id="v4p9tw"
🔥 Advanced Git User
🔥 Debugging Expert
🔥 Workflow Optimizer
```

---

## 🏁 Final Message

> If you can complete this lab confidently,
> you understand Git better than most developers.

---

## 🚀 Next Level

Move to:

👉 `08-GitHub-Pro-Level/README.md`
