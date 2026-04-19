# 🏁 git init (Start a Repository)

---

## 🎯 What It Does

Initializes a Git repository.

---

## 🧪 Command

```bash
git init
```

---

## 📁 What Happens?

A hidden folder is created:

```text
.git/
```

👉 This is the **heart of Git**

---

## 📸 Visual (.git Structure)

![Image](https://images.openai.com/static-rsc-4/6xPWnQPQsvCi_ZC7M11yIz_qg30P5QwiMS2WbujhgTjxj6ycN-4npKOIZ-YYCk24a-fWGT0_12NJcEBvWrRH3T7CQ1LN5MNzwuBjrGh3DUf3NBdXL0lvXtYHXwAinhkNDOzhT8k_cxyjVJIUgScBHxCcCwqybMqhs89nM2R8fU-4EG207yLo_xXVKK2i21DR?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Z0NZELz793F75LLh8pqdYj2TNKnTCpMeo3V6wfuRjKhhfq2SOjRyQdxkB2GoLypVLd2if-4PAYrFAV4fBQm5qsIJdAWma6yVuzYQsGdg9Qck7Sv1qDiN7lPqtpFGzZNrrL2Z2dLmrB6z_FKnCKq_L-0sV1xgIZ9y_O2Hl1UQNwMPCGsCiFxmQhnVJ4XJUNQp?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/ECyDUAPiKrtQfhBo6eC8Nce4ldH1O_FkZqAIHrGH6BfmwugW-Jacp6KgKbEfdAA4GzbU7XwX9FZoVdvapsdcwRcyoarZSZjXUbj2xwlxXeTxSvWWkEv8as8wUhybCyNMsSpWCa_y4l4D_qlMAEB3YmkSQ3zzw5Pphqom84ncJ-4dPrMzYd4wibkdNjVf6DRW?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/hVNBF6meEEAK90itfOMGVzcQV4jLThV2EYe4Om6K-I24mrsvpgnSajm4OBlOrIWYM2AE3--zf9tSbr6W8ttOk-_lf520_TR_6g3Fyvz6QRolAJYYKEO5EZZ-yY7W46SbHr1dr6zjYT6QS2KDGkjQUwor794saOm7bPmPNmgMrCP43_EnUl-xXWrsyZgZVQFs?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/_8S8LGHN-_qsvG0v-PLdD32KotRWwBUPqWzR6F60kYNY53VDYLzmuxW7de_Jm1ocW3kE01QmjLByiw4Eh63SgguYb7ok5ml7u4UipVRWaMF6jjs8MKxDHV_SkDwwwdYIIjdTeCSIWSo3NCx3OqhvjOmMlFh3VR8l9N9nkHi8c_Cy8v0tFqbHzBjDZa3uH7oV?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Xj6qYm5zNWkrfZpQNkqsaLaxt_gk5SpMMSIYzOSbVznIIGPtJcB6VVj6QDgQhBjKn8DvUxD10EkGner0VgaLVn3c7TrDGNpadQzqvxp-NGomyWz2WEaYgJtkBOomaoVktWv9wha1zHDmR-BzFJEfi8quHjXgPXo00AOpxmMoutex0cQAIB-p5OuUaJyj2igj?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/-k3r_EgNGqPmUMZvzccV4K8-YvxIwaFLjpQGWD-PDA91Aw2txAOGD68UGZLgJ4h1ZEHXaSGrSlg6Q6CzNv_JJaxBWUMolgan-uw0IUoaj0TXWzlNETV-R4c-IcH2XqYSMzbSjFfGv0WIutW-o1KSykvIsIG3G5JfqsjfOlZoSSIfcMgtRYZqNaUeVqsgWCeR?purpose=fullsize)

---

## 🏗 Inside `.git/` Folder

```text
.git/
├── HEAD
├── config
├── description
├── hooks/
├── info/
├── objects/
└── refs/
```

---

## 🔬 Important Files Explained

### 1. HEAD

```text
ref: refs/heads/main
```

👉 Points to current branch

---

### 2. config

```ini
[core]
    repositoryformatversion = 0
```

👉 Stores repo-specific settings

---

### 3. objects/

👉 Stores all Git data:

* blobs (files)
* trees (folders)
* commits

---

### 4. refs/

Stores pointers:

```text
refs/
 └── heads/
      └── main
```

👉 Branch references

---

### 5. hooks/

* scripts triggered by Git actions
* example: pre-commit hook

---

### 6. info/

* additional repo info
* rarely used by beginners

---

## 🔥 Key Insight

> Git repository = `.git/` folder

If `.git/` is deleted → history is gone.

---

## 🧠 What Has NOT Happened Yet

After `git init`:

* ❌ no commits
* ❌ no tracked files
* ❌ empty repo

---

## 🧠 Memory Trick

> git init = create Git brain (.git)

---

## ⚠️ Common Mistakes

* running inside wrong folder
* nesting repositories
* deleting `.git` accidentally

---

## ➡️ Next Step

👉 `07-git-status.md`
