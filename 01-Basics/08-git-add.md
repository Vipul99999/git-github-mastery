# ➕ git add (Staging Changes)

---

## 🎯 What It Does

Moves changes to staging area.

---

## 🧪 Commands

```bash
git add file.txt
git add .
```

---

## 📸 Visual (Add Flow)

![Image](https://images.openai.com/static-rsc-4/GqF3hMrx_50-kuqRxHnvadKtzLFCIQ5ILfNxnuUG4Ezxc7VLDlow6-k6K_67j0IIP_ctDwRxqlwIxlClpUaLbXs1hcyq6rSjfKAJ4DfKf7mv8rw2tlBljq8qbUlWx8TdsS1_qEr5Hl_nm1iRkhN-UttJfcTahi4zWQh02mHFllr0cJ-LClkrFTD2LVUdjdN4?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/G2-IDhtdPZcO-ejtY4wrvpTU07gvvnCdrEv0741NBxvujQy9ynLZ_RkA0ZZH5KgB0OqT1kA7BenceD2Cr0cs7gUfmxK4Llc0-gSXoGolGQpNvCkrMvydC5s4fflNgUBng8wettdJTm98oG6_yq0CQ-iTrKRVh6VsZB4I9hmcM2hZxxM2uB260KLT8XYvqROS?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/dL58GVWu9v0ujEgrTVbYnIc5fYg24p6j7uqUijmIzntqGGaAYol5chg6kUxJCY3FVv3g9bqBDTWjDsR3ovY9HPMML4ry-X0mFIgHxSgaQeSXt6Fex5cdTPe9fkzww4K5a3TlqpVw5oRL9WybSx38OHJt90D--VYJ1dTYPPUeFehR9DdRnGhf1hqzSpOOgCu2?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/c0qWmgo5XVDZVaixXP9mgiaYWwk_6rb_wkdf5QCvEJd2UoF2SSKC-eKRpEtRh0_X7HAuEu9ABZcNT2xIegc2ju13w_iMrXuTjZCSrC4n25TAGtLXIQY7hzcbAXg1KpoHXSQvGqiQS7SPDzyr2JH0v6ZFiQMZU8ccAX0HEJ6G1UBG9hdXr6fvWvCplzdVBACf?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/tVmBlw_u4W_0vH7j0m3I_QnBX8U5xFVVCFhU7suvS-rpdTJ_Ld3_6D31n0IUTUX8iHSJ7zgqWZgq5FXYHPc6wToynuiJ_lSC0ePIJQWgzlai6oBEgABh_nDcOTt7y_jfKEAwbqSaI6C5kFhV3Lowm_4P341NBeX0Va3qEP2FVMW4p0vU71sF6RW2sJDwdYAA?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/ltqiym5lxd64IV1F3LIKRIzcFqN_5930KTv2_kF4Wn0Fpbd7P1dy9Ni5MAyIu9FpRVI5xb-CVi01QZJGDFteP44aB98oO7IOLYflAAgNlgxv3-C04BUravr2hIbgvaSvObQ9jhmuvNUA1mFocsrh0UOTxUtKIuRbytFHoyC8-CtPwPvTkZedt6azh9FO9GpS?purpose=fullsize)

---

## 🧠 Mental Model

> git add = select changes for next commit

---

## 🏗 Internal Architecture

When you run:

```bash
git add file.txt
```

Git updates:

```text
.git/index
```

👉 This file = staging area

---

## 🔬 What is `.git/index`?

* binary file
* stores staged files
* maps file → blob object

---

## 🧩 Internal Flow

1. file content → hashed
2. stored in `.git/objects/`
3. index updated to reference it

---

## 📦 Example

```bash
echo "Hello" > file.txt
git add file.txt
```

Internally:

* blob created
* index updated

---

## ⚠️ Common Mistake

```bash
git add .
```

👉 adds everything blindly

---

## 🧠 Better Practice

Add selectively:

```bash
git add file1.txt
```

---

## 🧠 Memory Trick

> add = prepare commit

---

## ➡️ Next Step

👉 `09-git-commit.md`
