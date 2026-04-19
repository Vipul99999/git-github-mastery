
# 🔗 Origin vs Upstream (Remote Repositories Explained)

---

## 🎯 Why This Matters

When working with GitHub (especially forks), you will often see:

- origin
- upstream

Understanding these is critical for:

- collaboration
- open-source contributions
- syncing repositories

---

## 🧠 Core Idea

| Name | Meaning |
|------|--------|
| origin | your remote repository |
| upstream | original repository you forked from |

---

## 📊 Basic Scenario

```text
Original Repo (upstream)
        ↓ fork
Your Repo (origin)
        ↓ clone
Local Repo
````

---

## 📊 Visual (Mermaid)

```mermaid id="rmt802"
flowchart TD
A[Upstream Repository] --> B[Forked Repo (origin)]
B --> C[Local Repository]
```

---

## 🧠 Explanation

---

### Origin

```text id="rmt803"
origin = your GitHub repo
```

* created when you clone
* default remote name
* you push here

---

### Upstream

```text id="rmt804"
upstream = original repo
```

* used when working with forks
* you pull updates from here

---

## 📊 Visual Flow

```mermaid id="rmt805"
flowchart LR
A[Upstream Repo] -->|fetch| B[Local Repo]
B -->|push| C[Origin Repo]
```

---

## 🏗 Internal Architecture

---

### Stored in

```bash id="rmt806"
.git/config
```

---

### Example Config

```text id="rmt807"
[remote "origin"]
    url = https://github.com/your/repo.git

[remote "upstream"]
    url = https://github.com/original/repo.git
```

---

## 🔬 What Happens Internally

* origin → used for push/pull
* upstream → used for syncing updates

---

## 🛠 Commands

---

### Add upstream

```bash id="rmt808"
git remote add upstream <url>
```

---

### Fetch upstream

```bash id="rmt809"
git fetch upstream
```

---

### Merge upstream changes

```bash id="rmt810"
git merge upstream/main
```

---

### Rebase from upstream

```bash id="rmt811"
git rebase upstream/main
```

---

## 🧩 Real Use Cases

---

### 🔹 Open source contribution

* fork repo
* add upstream
* sync changes

---

### 🔹 Sync forked repo

---

### 🔹 Stay updated with original project

---

## ⚠️ Common Mistakes

---

### ❌ Confusing origin with upstream

---

### ❌ Not adding upstream

---

### ❌ Pushing to upstream (not allowed)

---

## 🧠 Best Practices

* use origin for your work
* use upstream for updates
* sync regularly
* avoid pushing to upstream

---

## 🧠 Interview-Level Explanation

**Q: What is origin and upstream in Git?**

Answer:

> Origin refers to your remote repository, while upstream refers to the original repository from which you forked. Origin is used for pushing your changes, while upstream is used to pull updates.

---

## 🧠 Memory Trick

> Origin = mine
> Upstream = original

---

## ✅ Quick Recap

* origin = your repo
* upstream = original repo
* used in fork workflows
* stored in `.git/config`

---

## ➡️ Next Step

👉 `09-private-vs-public-repo.md`
