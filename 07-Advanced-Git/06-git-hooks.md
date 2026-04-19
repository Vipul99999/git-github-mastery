

# ⚡ Git Hooks (Automation)

<p align="center">
  <img src="https://img.shields.io/badge/Level-Advanced-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Automation-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Use-CI%20%2F%20Validation-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Skill-Productivity-purple?style=for-the-badge" />
</p>

<p align="center">
  <b>Automate tasks before or after Git events like commit, push, and merge.</b>
</p>

---

## 📌 What Are Git Hooks?

Git hooks are:

> Scripts that run automatically on Git events.

---

## 🧠 Why Use Hooks?

- enforce rules
- run tests
- format code
- prevent bad commits

---

## 🗺️ Hook Flow

```mermaid
flowchart LR
    A[Git Action] --> B[Hook Triggered]
    B --> C[Script Runs]
````

---

## 🧱 Common Hooks

| Hook       | Trigger          |
| ---------- | ---------------- |
| pre-commit | before commit    |
| commit-msg | validate message |
| pre-push   | before push      |
| post-merge | after merge      |

---

## 🧱 Location

```text id="f2n7lp"
.git/hooks/
```

---

## 🧱 Example Hook

---

### Pre-commit hook

```bash id="y3d8op"
#!/bin/sh
echo "Running checks..."
npm test
```

---

## 🧠 Behavior

```text id="x9c2lo"
If script fails → commit stops ❌
If script passes → commit continues ✅
```

---

## 🧪 Real-World Use Cases

* lint code before commit
* prevent bad commit messages
* run tests before push
* auto-format code

---

## ⚠️ Important

Hooks are:

```text id="k1v7rs"
local only
not shared by default
```

---

## 🚨 Common Mistakes

* forgetting executable permission
* breaking commit flow

---

## ✅ Best Practices

* keep hooks fast
* use for validation
* combine with CI/CD

---

## 🎤 Interview Questions

### What are Git hooks?

Scripts triggered by Git events.

---

### Where are they stored?

.git/hooks/

---

### Are hooks shared?

No (unless manually shared)

---

## 🧪 Practice Lab

```bash id="b4g8on"
cd .git/hooks
touch pre-commit
chmod +x pre-commit
```

Add script → test commit.

---

## 🎯 Final Takeaway

Git hooks bring:

* automation
* consistency
* quality control

---

## 👉 Next Step

➡️ `07-git-worktree.md`
