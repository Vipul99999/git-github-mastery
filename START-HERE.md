# 🟢 START HERE (Beginner Friendly)

If you’re new to Git — start here.

---

## 🎯 Your Goal

After this section, you will:

* Understand what Git is
* Make your first commit
* Push code to GitHub

---

## 📌 Step 1: Install Git

Download Git:

👉 https://git-scm.com/downloads

Verify installation:

```bash
git --version
```

---

## 📌 Step 2: Setup Git

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## 📌 Step 3: Create Your First Project

```bash
mkdir my-first-repo
cd my-first-repo
git init
```

---

## 📌 Step 4: Add a File

```bash
echo "Hello Git" > file.txt
git add file.txt
git commit -m "First commit"
```

---

## 📌 Step 5: Connect to GitHub

* Create a repo on GitHub
* Copy URL

```bash
git remote add origin <repo-url>
git push -u origin main
```

---

## 🧠 What Just Happened?

* You created a Git repository
* You added a file
* You saved a snapshot (commit)
* You uploaded it to GitHub

---

## ➡️ Next Step

👉 Go to: `00-Mental-Models/README.md`
