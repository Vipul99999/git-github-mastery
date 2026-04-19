
# 🧠 How Git Stores Data (Internal Storage System)

<p align="center">
  <img src="https://img.shields.io/badge/Level-Expert-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Data%20Storage-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Includes-Objects%20%2B%20Snapshots-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Skill-Core%20Git%20Engine-purple?style=for-the-badge" />
</p>

<p align="center">
  <b>Understand how Git stores every file, commit, and change using its internal object database.</b>
</p>

---

## 📌 Core Idea

Git stores data as:

```text id="gi1-core"
Snapshots, not differences
````

---

## 🧠 What Does That Mean?

Instead of saving changes like:

```text id="gi1-diff"
"line 5 changed"
```

Git saves:

```text id="gi1-snap"
Full snapshot of files at that moment
```

---

## 🗺️ Big Picture

```mermaid id="gi1-big"
flowchart TD
    A[Working Directory] --> B[Staging Area]
    B --> C[Git Database (.git)]
    C --> D[Objects]
```

---

## 🧬 Git Storage System

```text id="gi1-arch"
Everything in Git = Object
Objects stored in .git/objects
```

---

## 📦 Types of Objects

---

### 🔹 Blob (File Content)

```text id="gi1-blob"
Stores raw file data
```

---

### 🔹 Tree (Directory)

```text id="gi1-tree"
Stores structure (files + folders)
```

---

### 🔹 Commit (Snapshot)

```text id="gi1-commit"
Stores snapshot + metadata
```

---

## 🔄 Data Flow

```mermaid id="gi1-flow"
flowchart LR
    A[File] --> B[Blob]
    B --> C[Tree]
    C --> D[Commit]
```

---

## 🧠 Step-by-Step Example

---

### Step 1 — Create File

```text id="gi1-step1"
file.txt → "Hello"
```

---

### Step 2 — Add File

```bash id="gi1-step2"
git add file.txt
```

👉 Git creates a **blob object**

---

### Step 3 — Commit

```bash id="gi1-step3"
git commit -m "first commit"
```

👉 Git creates:

* tree object
* commit object

---

## 🧬 What Actually Happens

```text id="gi1-internal"
file → blob → tree → commit
```

---

## 📂 Inside `.git/objects`

```text id="gi1-folder"
.git/objects/
 ├── ab/
 │   └── 123456...
 ├── cd/
 │   └── 789abc...
```

---

## 🧠 Why Split Folders?

```text id="gi1-split"
First 2 characters → folder
Rest → filename
```

---

## 🔐 Content-Addressable Storage

Git uses:

```text id="gi1-content"
Content → Hash → Storage
```

---

### Example

```text id="gi1-hash"
"Hello" → SHA-1 → abcd1234...
```

---

## 🧠 Key Insight

```text id="gi1-insight"
Same content = same hash = stored once
```

---

## 🧪 Try It Yourself

---

### Create Hash

```bash id="gi1-lab1"
echo "Hello" | git hash-object --stdin
```

---

### Store Object

```bash id="gi1-lab2"
echo "Hello" | git hash-object -w --stdin
```

---

### Read Object

```bash id="gi1-lab3"
git cat-file -p <hash>
```

---

## 🔄 Snapshot vs Diff

---

### Traditional VCS

```text id="gi1-old"
Version 1 → Version 2 → Diff stored
```

---

### Git

```text id="gi1-new"
Version 1 snapshot
Version 2 snapshot
```

---

## 🧠 Why Snapshots?

---

### Advantages

```text id="gi1-adv"
- faster operations
- simple structure
- easy recovery
```

---

### Efficiency Trick

```text id="gi1-eff"
Unchanged files are reused (not duplicated)
```

---

## 🧬 Commit Structure

A commit stores:

```text id="gi1-commit-struct"
- tree reference
- parent commit
- author
- message
```

---

## 🧠 Visual Example

```mermaid id="gi1-commit-graph"
flowchart LR
    A[Commit A] --> B[Commit B]
    B --> C[Commit C]
```

---

## 🔗 Commit Chain

```text id="gi1-chain"
Each commit points to previous commit
```

---

## 🧠 Why This Matters

---

### Debugging

```text id="gi1-debug"
Understand broken history
```

---

### Recovery

```text id="gi1-recovery"
Recover lost commits
```

---

### Performance

```text id="gi1-perf"
Efficient storage system
```

---

## 🚨 Common Misconceptions

---

### ❌ Git stores diffs

❌ Wrong

---

### ❌ Files are duplicated each commit

❌ Wrong

---

### ✅ Git stores snapshots efficiently

✔ Correct

---

## ✅ Best Practices

* understand staging area
* commit small changes
* use Git commands carefully
* inspect objects when debugging

---

## 🧠 Pro Tips

* use `git cat-file` to inspect objects
* use `git ls-tree` to explore trees
* use `git log --graph` to visualize commits

---

## 🧬 Internal Model Summary

```text id="gi1-summary"
File → Blob → Tree → Commit → Hash → Stored
```

---

## 🎤 Interview Questions

### How does Git store data?

As objects (blob, tree, commit).

---

### What is a snapshot?

Full state of files at a commit.

---

### What is content-addressable storage?

Data stored based on its hash.

---

### Why is Git efficient?

It avoids duplication using hashing.

---

### What happens during commit?

Git creates tree and commit objects.

---

## 🧪 Practice Lab

---

### Task 1

```bash id="lab1"
git hash-object file.txt
```

---

### Task 2

```bash id="lab2"
git cat-file -p <hash>
```

---

### Task 3

```bash id="lab3"
Explore .git/objects
```

---

## 🎯 Final Takeaway

Git stores data as:

```text id="gi1-take"
Snapshots + Objects + Hashes
```

---

## 🚀 Key Insight

> Git is a content-addressable object database.

---

## 👉 Next Step

➡️ `02-blobs-trees-commits.md`
