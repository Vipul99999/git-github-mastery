

# 🟢 Beginner Git Interview Answers

> “Clarity > complexity. Interviewers want simple, correct explanations.”

---

## 🧠 Q1. What is Git?

👉 **Answer:**

Git is a **distributed version control system** used to track changes in code and collaborate with others.

---

### 🔍 Visual

```mermaid id="g1"
flowchart LR
    A[Developer 1] --> B[Local Repo]
    C[Developer 2] --> D[Local Repo]
    B --> E[Remote Repo]
    D --> E
```

---

## 🧠 Q2. Git vs GitHub

👉 **Answer:**

* Git → version control system (tool)
* GitHub → hosting platform for Git repositories

---

```mermaid id="g2"
flowchart LR
    A[Git] --> B[Track code changes]
    C[GitHub] --> D[Store & share repos online]
```

---

## 🧠 Q3. What is a repository?

👉 **Answer:**

A repository is a **project folder tracked by Git**, containing:

* Code
* History
* Configuration

---

## 🧠 Q4. What is a commit?

👉 **Answer:**

A commit is a **snapshot of your project at a specific point in time**.

---

```mermaid id="g3"
graph LR
    A[Commit A] --> B[Commit B] --> C[Commit C]
```

---

## 🧠 Q5. What is the staging area?

👉 **Answer:**

The staging area is where changes are **prepared before committing**.

---

```mermaid id="g4"
flowchart LR
    A[Working Directory] --> B[Staging Area]
    B --> C[Commit]
```

---

## 🧠 Q6. git add vs git commit

👉 **Answer:**

* `git add` → moves changes to staging area
* `git commit` → saves snapshot to history

---

## 🧠 Q7. What does git init do?

👉 **Answer:**

Initializes a new Git repository by creating a `.git` folder.

---

## 🧠 Q8. What does git clone do?

👉 **Answer:**

Copies a remote repository to your local machine.

---

```mermaid id="g5"
flowchart LR
    A[Remote Repo] --> B[Local Repo]
```

---

## 🧠 Q9. What is git status?

👉 **Answer:**

Shows the current state of:

* modified files
* staged files
* branch info

---

## 🧠 Q10. What is git log?

👉 **Answer:**

Displays commit history.

---

```mermaid id="g6"
graph LR
    A --> B --> C --> D
```

---

## 🧠 Q11. What is a branch?

👉 **Answer:**

A branch is a **separate line of development**.

---

```mermaid id="g7"
graph LR
    A --> B --> C
    B --> D --> E
```

---

## 🧠 Q12. Default branch

👉 **Answer:**

Usually `main` (earlier `master`)

---

## 🧠 Q13. Create & switch branch

👉 **Answer:**

```bash
git checkout -b feature
```

or

```bash
git switch -c feature
```

---

## 🧠 Q14. Why use branches?

👉 **Answer:**

* Isolate features
* Avoid breaking main code
* Enable parallel work

---

## 🧠 Q15. What is a remote repository?

👉 **Answer:**

A repository hosted on a server (e.g., GitHub) for collaboration.

---

## 🧠 Q16. git push vs git pull

👉 **Answer:**

* `push` → send changes to remote
* `pull` → get changes from remote

---

```mermaid id="g8"
flowchart LR
    A[Local] -->|push| B[Remote]
    B -->|pull| A
```

---

## 🧠 Q17. What is git fetch?

👉 **Answer:**

Downloads changes from remote **without merging**.

---

```mermaid id="g9"
flowchart LR
    A[Remote] -->|fetch| B[Local]
    B -. no merge .- C[Working Branch]
```

---

# ⚡ Rapid Revision (Bonus)

```text
Git = version control
Commit = snapshot
Branch = separate line
Add = stage
Commit = save
Push = upload
Pull = download + merge
Fetch = download only
```

---

# 🚀 Next Step

➡️ Move to: `02-Intermediate/`

---

### 🔥 What You’ll Learn Next

* Merge vs Rebase
* Reset vs Revert
* Conflict resolution
* Real workflows

---

```mermaid id="next1"
flowchart LR
    A[Beginner ✅] --> B[Intermediate 🔥]
    B --> C[Advanced 🚀]
```

---

## 🏁 Final Thought

> “If you can explain Git simply, you understand it deeply.”