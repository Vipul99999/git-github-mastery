# 🧪 Practice Lab — Basics Mastery

---

## 🎯 Objective

By completing this lab, you will:

* Create a Git repository
* Track files properly
* Use staging area correctly
* Make clean commits
* Understand history

---

## 📸 Visual (Workflow You’ll Practice)

![Image](https://images.openai.com/static-rsc-4/AY4pqqz3IDO2w8CbNGYvI5yDmRkQn1-_ZAIV85XutCptmZJWWbGlF8CPGLgkpufPnKHYLKVBgiaWed-olTGSJHycf6lQop-NZG7Gkt7AaQIaOaXzeVCu6OGZg3NeoI3MbIgrS3GJOfhummNLcN8Mi1CuvGOEv_rLvre-sahOE_yEcUDJVW869xfefLz8ebSc?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/FSmcH0ATEoMDq6mGVQ4ZzZHdeU-jWRvpRrH4mAjWgBwcEDVZHgW96gbDSvkGjHcxH7PGjy3JaQ2hwGCSqTzmFEs4pPg3nIN522yRJh07NxYdH2pCyFivjeBXR1Ej6rZKEj5GQJgppLjgCQKPWy0XRyqKbpsEcZZb3qLt-Cp5U0Lo5Rhl9qgwpKyc5OUeVRPE?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/1mppVlNfEimK9fpr1lRlzXaAqGCRMqWQS8L7Ki9iaWGiH1ENGf9pk5hkl-DVOPSIiC4P2XPlWdReuR7XyqWQxZe5HqjWb9EtC_PJRIWqAcuLP-qMmuzk7ukZRCgfxD62YsqE-bo7QZ_oHbI2aLdauJl4fW0EcirbhVSNAMKT-1BAWJFZhi4zadq183qrm53G?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Tqlqljd2HJNdD6v4M7fswRbk_5fFUn2eAE8HZ9SLhCHysfibyKqgbIoHUjs6Jmk1KYkZKolcOX1CvuNPASeweMUaOe2ZFAxbwlKqHL6uF2a8coq4P5o9lebP8HfDL0OS7qZ8wTMAa2PNek4WXbB9lhtCTy1YYcHWqqscazX495jhHqCYKVMcqnNp9AAX4kOK?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/jzXv1lj8ZQxU3RyWldOkPNeX_zrGD-bYjZJGQpayY_OQGC0Bub9_LjPDlDpkqykQVHr1BQPxH115vSWpcrcg-R7lpXXrF9wHCZLCyqmkgNtDeh3X9ca89uPnDe4w7OtIne7-BCrfyDAeSHu_JMwjIhYsgW6TXkl2aFUUJCs80jcWFFj6hlipChwcQyD2k55D?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/brf8-74ilNrU5n1KJMqyAZnxJG9x3hsZrUFulJ2BZ9InyaCXTT7YGj-gtOEqBleXg8_TP0BSHStpY4zgmr4iKZW63qjoY875y8OKNsLKf-PUQS76nN_SrqusO42vy84EcCdSC-Mnki2VRlbW1nFic_dk565XgB85baDf-dXjyfSvHDpiR73FbwUrXiXoloaL?purpose=fullsize)

---

## 🛠 Setup

```bash
mkdir git-basics-lab
cd git-basics-lab
git init
```

---

## 🧩 Task 1 — Create First File

```bash
echo "Hello Git" > app.txt
git status
```

👉 Observe: file is **untracked**

---

## 🧩 Task 2 — Stage File

```bash
git add app.txt
git status
```

👉 Observe: file is **staged**

---

## 🧩 Task 3 — First Commit

```bash
git commit -m "Initial commit"
```

---

## 🧩 Task 4 — Modify File

```bash
echo "New line added" >> app.txt
git status
```

👉 Observe: file is **modified**

---

## 🧩 Task 5 — Check Differences

```bash
git diff
```

👉 Understand what changed

---

## 🧩 Task 6 — Commit Changes

```bash
git add app.txt
git commit -m "Update app.txt with new line"
```

---

## 🧩 Task 7 — View History

```bash
git log --oneline
```

---

## 🧠 Internal Observation

After commits:

* `.git/objects/` contains blobs & commits
* `.git/index` tracks staged files
* `.git/HEAD` points to current branch

---

## 🎯 Expected Outcome

* 2 commits created
* file tracked
* history visible

---

## 🔥 Bonus Challenge

Try:

```bash
echo "Another file" > notes.txt
git add notes.txt
git commit -m "Add notes file"
```

---

## ⚠️ Common Mistakes

* skipping `git status`
* using `git add .` blindly
* bad commit messages

---

## 🧠 What You Learned

* full Git workflow
* staging vs commit
* tracking changes
* reading history

---

## 🚀 Next Step

👉 Move to: `02-Branching/README.md`
