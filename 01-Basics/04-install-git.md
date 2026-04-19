# 🛠 Install Git

---

## 🎯 Goal

Install Git and understand what gets installed internally.

---

## ✅ Step 1: Download

👉 https://git-scm.com/downloads

---

## ✅ Step 2: Verify

```bash
git --version
```

---

## 📸 Visual (Install Flow)

![Image](https://images.openai.com/static-rsc-4/AkMSQs9VvKcnDaeDiTBtJUTJZ-GEJz3K5zqQsnMzoZAGISkpZGH7iLAmD7GyYPtf_XQWkpUCFWPewgkJKyFlkb9C3LUCqgzPh39HThn3rR3rj3bdWRe0fzQXczfjy75d6BPgAWIUH1UeOZc7o3Is63-IPGTcEZo0TBP4R2ns_mLN68KRidELBTZj9hRLOFEF?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/ZNt0N4YKI01ZhBbODAz2ARR0ANptQ-TpN9fGuQrRK54MnzE25SjKsL8GoeFXTMEu8k3SIHSfDUmhTSJ04zuB49EiN6izbjGLkE4dq_7TealD4wewEgxz9nCTECDDyzWwKEpTz8-OqUTtgqdmOs__nG6FYSD5v22knGn7ucOzTpWpFnwOQc3pjdXo0tkozAiY?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/c1rF7AIcJbiV6ShRXVx9vvwTrvJxGH8FddRGdbJ20NMWGRUD7mrF5o7V_0O7NPCTKnSOcBs3F6N2D0lpN30jPJgPsoL6NpQ61sgMdcgkwYpbLDSg9P8RCmwcMfaTQWO5saKwg3liwgLbP6W4tMFYGyuC4I5fK-gvhEQeZvDAM-9Nlonqgn1lYH3uxeH3pbTd?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/qamdsNooI-_B3Z5YK4087xL0rdFcVVnV1YLNqeTNTbLteYfR_BrBLa1PJT2HnV4uCwlczXjldgT7B4gmINEkCFE200cuNNkLo2zyX-C5AzpFoGtb7D3K4P01ReF8LdB3-yk4N2L8CN05faJ6hYdrCaigsTUheQmwerhb8eNzXbTenHU2aY6L8HJt2z2tIRCr?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Tqlqljd2HJNdD6v4M7fswRbk_5fFUn2eAE8HZ9SLhCHysfibyKqgbIoHUjs6Jmk1KYkZKolcOX1CvuNPASeweMUaOe2ZFAxbwlKqHL6uF2a8coq4P5o9lebP8HfDL0OS7qZ8wTMAa2PNek4WXbB9lhtCTy1YYcHWqqscazX495jhHqCYKVMcqnNp9AAX4kOK?purpose=fullsize)

---

## 🏗 What Gets Installed Internally?

When Git is installed, it adds:

* Git binaries (core commands)
* CLI tools
* help files
* config system
* SSH tools (sometimes)
* shell integration

---

## 🧩 Important: PATH

Git is added to system `PATH`.

👉 That’s why you can run:

```bash
git
```

from any directory.

---

## 🧪 OS-Specific Notes

### 🪟 Windows

* Git Bash
* Git CMD
* SSH tools
* OpenSSL

### 🍎 macOS

* Installer / Homebrew / Xcode tools

### 🐧 Linux

```bash
sudo apt install git
```

---

## 🔬 What Git Does NOT Do Yet

Installing Git does NOT create:

* repository
* `.git/` folder
* commits

That happens with:

```bash
git init
```

---

## ⚠️ Common Mistakes

* Git not in PATH
* not restarting terminal
* confusing Git with GitHub

---

## 🧠 Memory Trick

> Install → Verify → Then Initialize

---

## ✅ Quick Recap

* Git installed globally
* command available via PATH
* no repo created yet

---

## ➡️ Next Step

👉 `05-first-time-setup.md`
