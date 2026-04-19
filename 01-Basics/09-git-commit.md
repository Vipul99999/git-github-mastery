# 💾 git commit (Create a Snapshot)

---

## 🎯 What It Does

Creates a **snapshot of your staged changes**.

---

## 🧪 Command

```bash
git commit -m "Add feature"
```

---

## 📸 Visual (Commit Snapshot)

![Image](https://images.openai.com/static-rsc-4/ECyDUAPiKrtQfhBo6eC8Nce4ldH1O_FkZqAIHrGH6BfmwugW-Jacp6KgKbEfdAA4GzbU7XwX9FZoVdvapsdcwRcyoarZSZjXUbj2xwlxXeTxSvWWkEv8as8wUhybCyNMsSpWCa_y4l4D_qlMAEB3YmkSQ3zzw5Pphqom84ncJ-4dPrMzYd4wibkdNjVf6DRW?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/b23DP5A6-w007TeiI2a_uJEIUD7_YHmp9jNaMMux085-StMITo5hcsoIY2o3FIi6kg4kIwsClAGja5yVCE4E34sWA8xzfN3Vo3s2Z9RX7IgGlnb6GMsrxecj0lNqdwe6Pu7Riz2_Y_frIRHYKfnfK3lqgTnqIgbD2WIAYLdNqE3FsHA35Wtsaz4QvxiibUi4?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/I6egHGSxj66u8jsOqcqHF3hwEOj7L4jlDOJoFQJ8e-cZu1Uu576GJUKaChJjTVEFhK2QASCR4Kx06UfNdwPBMw7Qgin12UXJZynBF1rdZLbpQgf83v8R2vS_8lw3iELfR4IeWgybILxGE3-8NAcs791nLN3BxmFs61OIXRWwrXJ-nm9-FlpFc1kAtoiCAOJB?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/UxpYrGZygx-7C9aSg-lt6PVm0IDhObrEgOhKqoBAFN8db7Zw_bVyo4_lbGMWnxfJXPWTOhf9QY79uy6qTXYeMMY-UTOBr1FmsJA5YodiHU7ilvoWsz1d2QP1K9pRZCowPK6thFgn0gCRBpMEUanF-S_GpqMpID1A6Zys-f5pgmvSbktDnHNBEw8y-UTG7Hd8?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/OoOPRAorHnlzf1WRXyt3-rx9NLKZDcdLCIJ8Tv9P5OTYDVI62tpYTfogmtd22FtDrPUHTNAgJMlQEam6wnI3QAetWllh-zZu_9_iVTRsQU1zJCiqLyNluOPTowWVAYi6tdF2M-0dODOTK4XBUb3AY_JDQx_GMm_9fL6SmbMfycXvkxmpDAj3JP9YQSClZ6v0?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/jp-uXIeOQsTYtRWle7rXXR6Dvt9yhGIJl6C8g13IOAteP5w7r4GvBWdqCM47N8lS9Vy3oLd6pp6z9laOfFNkpg_Y5K5QCvm7hkv7Z2RJsFRE-aKUcwprWmsY-b020QRKhKZNjzJeYKI_jC3NOz51dugtZ9ngKVYnLh_WsTc2aLVkci_dq6vaymQDzmLZ1oUz?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/G-I_ynafIxoDDKwuNyWzhmyU0uNtwjKq2Q5lTXy2gpqP4Cl_UGU9jiW8BRhUcueW-9TsH1HENj_tZR7tWL4rwlFEZELv86gMOsS-d6gHAphcxzeuekMoydjAQHX9KlaBt7MtLdyFrb_45Q9lvx4xIX0qPiUE1nWoQp_aHjJdV0-HrwAvt7JX4ONoCLmEOK9j?purpose=fullsize)

---

## 🧠 Mental Model

> Commit = snapshot of entire project + metadata

---

## 🏗 Internal Architecture (VERY IMPORTANT)

When you run `git commit`, Git creates a **commit object**.

---

## 🔬 Commit Object Structure

A commit contains:

```text
commit <hash>
Author: Your Name
Date: timestamp

Message: "Add feature"

Points to:
- tree (project snapshot)
- parent commit(s)
```

---

## 📦 Inside `.git/objects/`

Git stores commits here:

```text
.git/objects/
```

Each object is stored using a **SHA-1 hash**.

Example:

```text
a1/b2c3d4e5...
```

---

## 🧩 Object Relationships

```text
Commit → Tree → Blobs
```

### Tree

* represents folder structure

### Blob

* represents file content

---

## 🔗 Parent Relationship

Each commit points to its parent:

```text
A → B → C
```

👉 This creates history chain

---

## 🧠 Why This Matters

Because now you understand:

* commits are not just messages
* commits form a graph
* history is linked via parents

---

## ⚠️ Common Mistakes

* vague messages ("update")
* committing too much at once
* not staging properly

---

## ✅ Good Practice

```bash
git commit -m "Add login validation"
```

---

## 🧠 Memory Trick

> Commit = snapshot + message + history link

---

## ➡️ Next Step

👉 `10-git-log.md`
