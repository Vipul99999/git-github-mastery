
# 🌱 Create a Branch

---

## 🎯 Why This Matters

Creating branches is the foundation of safe development in Git.

Instead of working directly on `main`, you create branches to:

- build features
- fix bugs
- experiment safely
- prepare releases

---

## ✅ Basic Command

```bash
git branch feature
````

👉 This creates a new branch named `feature`

⚠️ Important:

> It does NOT switch to the branch

---

## 🧠 Mental Model

Before creating a branch:

```text
A --- B --- C   (main)
```

After:

```text
A --- B --- C   (main, feature)
```

👉 Both branches point to the same commit

---

## 📊 Visual (Mermaid)

```mermaid
gitGraph
   commit id: "A"
   commit id: "B"
   commit id: "C"
   branch feature
```

---

## 🏗 Internal Architecture

When you run:

```bash
git branch feature
```

Git creates a file:

```bash
.git/refs/heads/feature
```

Inside it:

```text
<commit-hash>
```

Example:

```text
a1b2c3d4e5f6...
```

👉 This means:

feature → commit C

---

## 🔬 Internal Flow

Steps Git performs:

1. Reads current commit from HEAD
2. Creates new reference file
3. Stores commit hash in it

No files are copied.

---

## ⚡ Key Insight

> Branch creation is instant because Git only creates a pointer

---

## 🛠 Command Variants

### 1. Create branch (basic)

```bash
git branch feature
```

---

### 2. Create from specific commit

```bash
git branch feature <commit-hash>
```

Use when starting from older history.

---

### 3. Create from another branch

```bash
git branch feature main
```

---

### 4. Create + switch (recommended)

```bash
git switch -c feature
```

OR

```bash
git checkout -b feature
```

---

### 5. Verify branches

```bash
git branch
```

---

## 🧩 Real Use Cases

### 🔹 Feature Development

```bash
git branch feature-login
```

---

### 🔹 Bug Fix

```bash
git branch bugfix-header
```

---

### 🔹 Hotfix

```bash
git branch hotfix-payment
```

---

### 🔹 Backup Before Risky Change

```bash
git branch backup-before-refactor
```

---

### 🔹 Work From Old Commit

```bash
git branch test-old abc1234
```

---

## 🧪 Example Walkthrough

```bash
git init
echo "Hello" > file.txt
git add .
git commit -m "Initial commit"

git branch feature
git branch
```

Output:

```text
* main
  feature
```

---

## ⚠️ Important Difference

| Command               | Behavior           |
| --------------------- | ------------------ |
| git branch feature    | creates only       |
| git switch feature    | switches           |
| git switch -c feature | creates + switches |

---

## ⚠️ Common Mistakes

### ❌ Forgetting to switch

You created branch but still on main

Fix:

```bash
git switch feature
```

---

### ❌ Creating branch from wrong location

Always check:

```bash
git branch
git log --oneline
```

---

### ❌ Bad naming

Avoid:

```text
test1
abc
branch2
```

Use:

```text
feature-login
bugfix-navbar
hotfix-payment
```

---

## 🧠 Best Practices

* create branch from correct base
* use clear names
* keep branches focused
* verify before committing

---

## 🧠 Interview-Level Explanation

**Q: What happens when you create a branch in Git?**

Answer:

> When you create a branch, Git creates a new reference inside `.git/refs/heads/` that points to the current commit.
> No files are copied. It is just a pointer to a commit, which is why branch creation is very fast.

---

## 🧠 Memory Trick

> git branch = create pointer
> git switch = move pointer

---

## ✅ Quick Recap

* `git branch name` creates a branch
* does NOT switch automatically
* stored inside `.git/refs/heads/`
* points to current commit

---

## Check Yourself

1. Does `git branch feature` switch branches?
2. Where is the branch stored internally?
3. Why is branch creation fast?
4. How do you create + switch in one command?

---

## ➡️ Next Step

Go to: `03-switch-branch.md`

```
```


## 🧠 What Happens Internally

* new pointer created
* points to current commit

---

## 📸 Visual

![Image](https://images.openai.com/static-rsc-4/vD5ov7DSIk8r_ryLYk-Szh1Gp2ASUoardKGLuXJh-skWorImsTJ18BXq07qPPCZsvmTNQnPW_gtJ9WsyIm_U41BxVlgormhKPNe8QFV8zv2BjNNXwGIonX9W-HuituINedVIQIAkpb1YV2Lcbn4qtpkMa6Nei0QDnxFPuBWkJpzszzUVRuWZHlpfM01QKrkO?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/26NEVeou_zBi3xIOxeAQv9Vv5sEKJ4CLPCrXz_mx3RAJO1fS6vy3tUpvQy5106P7NaHwnOVn0yoMSJdDPuaA21OaA22-iswlH1QaMQfeKOW3tk2xcBSu-0jm1yCzGvqgZkHObgDPT0rmQmH_QHMWGvBDMYpLq8s_cOVENPrMACi64a3EbXEGJcYs_KNmR69u?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/TBsdJDliH9zshzavhTn6Ws3aF3g87chaEUwpESIFinvUPMkP8Tpk2pOC0LjzBq5yntleXSEq7Ia6mrtPfsRX8AX7peVRyy1Ou0oAJTDROt_SxSvkyZVOzNVwshVWcl_TEBlCiCpAhAwN3mpXJZZaGgN1aibv4FdMsbTmRz0ZlzPf0WL4CgZztYhO7S_xDl2v?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/JgkhmyrzS9srs2TtEtwlayjHJCP-LPfvmxe0ADaVYgPVkcA-g-aYW1Tj8jPMiIVSNwJx3Esgya0zNFF9-7bcVEynuIGNQ37h-Vd3Bqbkf-9NMrtmEdNIgwQO057zYnvWF8onRE5T69dyj7KyzUrlNZ7cMiEc3vVz513fl2OlI_tJD6uHAST97jhiX5MSmBAb?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/I6egHGSxj66u8jsOqcqHF3hwEOj7L4jlDOJoFQJ8e-cZu1Uu576GJUKaChJjTVEFhK2QASCR4Kx06UfNdwPBMw7Qgin12UXJZynBF1rdZLbpQgf83v8R2vS_8lw3iELfR4IeWgybILxGE3-8NAcs791nLN3BxmFs61OIXRWwrXJ-nm9-FlpFc1kAtoiCAOJB?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/NWvthdODVikEK5aJweKnPK6JkMPkDLYw7QVmCoWKNdN_3_s6AJnlnHKdRZ84d8QPF2b6ktpXUs2yHmWm2o9LiYeY_ByQoMAA3IXh45GR3To5J9yayDy8KbTQKw-2YbjxBNsaKRn9x0uzU2C61eW7Y_oBhxHzw-vr1dKTDNp6Z4im4tzDHnMf4YCM_vfsAYiz?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/N4Xp5qknY1DfL2ryg_7nIOWXK10kLz3xhdpQ1uuIUuBcknU7iI7l8g9BX-6ocqNmUManrkYR1wyGE7BcU5YOUTCyQUcAEYI920hLiHBw6uzh4ZZOWhl4VcIKWFekhaXmcLmaMgD-NzfmdnufwEjVwNaipOAbo93yS_kAj527JuhJ-FZp9qzsO2HImU0IOUnF?purpose=fullsize)

---

## ⚠️ Important

This does NOT switch branch.

---

## ➡️ Next

👉 `03-switch-branch.md`
