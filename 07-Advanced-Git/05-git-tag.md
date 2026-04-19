
# 🏷️ Git Tag (Version Marking)

<p align="center">
  <img src="https://img.shields.io/badge/Level-Intermediate-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Versioning-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Use-Releases-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Skill-Version%20Control-purple?style=for-the-badge" />
</p>

<p align="center">
  <b>Mark important commits like releases, versions, and milestones.</b>
</p>

---

## 📌 What Is Git Tag?

A tag is:

> A label pointing to a specific commit.

---

## 🧠 Why Use Tags?

- mark releases
- track versions
- easy rollback
- deployment reference

---

## 🗺️ Example

```text id="8t3qzs"
A --- B --- C --- D
        ↑
      v1.0 tag
````

---

## 🧱 Types of Tags

---

### 1. Lightweight Tag

```bash id="6g9k2f"
git tag v1.0
```

---

### 2. Annotated Tag

```bash id="1l7x8p"
git tag -a v1.0 -m "First release"
```

---

## 🧠 Difference

| Lightweight    | Annotated                |
| -------------- | ------------------------ |
| simple pointer | full object              |
| no metadata    | includes message, author |

---

## 🧱 Common Commands

---

### List tags

```bash id="4j2d8n"
git tag
```

---

### Show tag

```bash id="y4k3pz"
git show v1.0
```

---

### Push tag

```bash id="5m2d7q"
git push origin v1.0
```

---

### Push all tags

```bash id="t6k1y9"
git push origin --tags
```

---

### Delete tag

```bash id="x9n2rp"
git tag -d v1.0
```

---

## 🧠 Internal Behavior

```text id="p7w4nb"
Tag → pointer to commit
Annotated tag → separate object
```

---

## 🧪 Real-World Scenario

```text id="z2k1bv"
v1.0 → first release
v1.1 → bug fixes
v2.0 → major update
```

---

## 🚨 Common Mistakes

* forgetting to push tags
* mislabeling versions

---

## ✅ Best Practices

* use semantic versioning
* prefer annotated tags
* tag releases only

---

## 🎤 Interview Questions

### What is a tag?

Pointer to a commit.

---

### Difference between lightweight and annotated?

Annotated stores metadata.

---

### Why use tags?

For versioning and releases.

---

## 🧪 Practice Lab

```bash id="3f1r6k"
git tag -a v1.0 -m "release"
git push origin v1.0
```

---

## 🎯 Final Takeaway

Tags help you:

* track versions
* manage releases
* simplify deployment

---

## 👉 Next Step

➡️ `06-git-hooks.md`
