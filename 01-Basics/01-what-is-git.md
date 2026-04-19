# 🤔 What is Git?

---

## 🎯 Why This Matters

Before using Git, you must understand what it actually is.

If you only memorize commands, Git feels confusing.
If you understand the system, Git becomes logical.

---

## ✅ Simple Definition

Git is a **distributed version control system**.

It helps you:

* track changes in files
* save project history
* go back to previous versions
* collaborate safely

---

## 🧠 Mental Model

Think of Git as a **time machine for your project**.

Every commit = a snapshot of your entire project.

---

## 📸 Visual (How Git Tracks History)

![Image](https://images.openai.com/static-rsc-4/H9x-b7obxWLSZTASmiWikCKk2VQsavMslX5FmsLXXpYhMNmI_u5Fxzt0dGdexo_SKF274Oq1m0ZPclid14BBArs4wagMlXb36_5Fi1zgUHrHrVc2n4hpeW007NNsv2RoDHFnVD9d6kxdtxPlf64OoH2w-trZGzZwBolu95vPhNkzZxmd7b1UU4W6E_GaARpa?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/I6egHGSxj66u8jsOqcqHF3hwEOj7L4jlDOJoFQJ8e-cZu1Uu576GJUKaChJjTVEFhK2QASCR4Kx06UfNdwPBMw7Qgin12UXJZynBF1rdZLbpQgf83v8R2vS_8lw3iELfR4IeWgybILxGE3-8NAcs791nLN3BxmFs61OIXRWwrXJ-nm9-FlpFc1kAtoiCAOJB?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Nt_fWYadbGyFk3Qu8UG81DAWMKodXlEAvV_gonhm8Zyz6z9Z5rxBJwu3WT2VZ2d9Gu4-q2ptYwoPsS_dgj9p_zjqaRaHKhOETEaVoWCia5y1yS3A7eexcmyGV48oCnhVOADLO___HYDBGmq_bHqucc2uRKjzrtbB75LJ8Xw11mzIOe55qhAYHT0-cZ-TYyAi?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/thHNpImlX6kwhTHXoOYdtMQ6z4P2-WLRseijr5Nz-6ftvhYRb53Uk1ofbyEIPrGp5V5ceeS9TiDgfPk4Usf9qcMq-Ul4WRKc_8o57D4K1WwrtQZ4Qdn2Chq3qKWA06N7tbaE7_jygu8F1B5g93yDowDSistgkiDTHSlgv5A5YbEwcq-gkSBlzG_iIup4RMQa?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/UXEbqlbLXuikKS3EMOToReV5SUvT7H8Jo9cEZ1rduBLKeG4qDNQrfhH4lwGaGYMiyVC4oGvdrtAilMw-Gx4OrD9fXbCwklej3ZohYNST-LTvKkwtzAwW42dSl8PuU3JpSezQgNytcM3IDQSpPtKnRkAh93L_F50aoNJ0t7GheG6GRDFEBX4Yr0S61REErXEV?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/jyIltXxzxwuW-S8fPmYlwHMzlrbiAVDhGPmwv2WbBVim5YiII1muYYgd88HnO9CJn7JwCKjalqVay2XZ9rJhuI4SHcHq8c-wKB8lA5J0lDEftf4k2FyiialuCgqglHbhTS2Ml4QL7N_OwBI9TaXhKBxwkP6uXxXn0Z94ERhAKHxp7fHLOPNwI4Fa8_guEV65?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/tlszaTvRYBJbO7tg0tzp7KATEO-a__pRXSx-wkPWyC_kbFPow9zPLGGdTccMfQgkKp8AtvDlVknwqt4wVdPH0ExRXan7xHwW3ys4JuREG57OAaVdDrv3m_vzPfXpNkISXqzSTK8O0G6g5FKnPHP1D_kh97Ozz8xfJytOEnVVOUKU1-diEt04VZhabjYDHZg8?purpose=fullsize)

---

## 🏗 Internal Architecture (High-Level)

Git works with 3 core areas:

### 1. Working Directory

* Your actual files
* Where you edit code

### 2. Staging Area (Index)

* Temporary area
* Select what goes into next commit

### 3. Repository (`.git`)

* Git’s internal database
* Stores:

  * commits
  * branches
  * objects
  * configuration

---

## 🔬 Under the Hood

Git stores data as objects:

* **blob** → file content
* **tree** → folder structure
* **commit** → snapshot + metadata

All objects are stored inside:

```bash
.git/objects/
```

Each object is identified by a **SHA hash**.

---

## 🧩 Real Example

Without Git:

```
project-final/
project-final-v2/
project-final-final/
```

With Git:

* clean history
* structured changes
* easy rollback

---

## ⚠️ Common Mistake

Thinking Git stores only differences.

👉 Conceptually, Git stores snapshots.

---

## 🧠 Memory Trick

> Git = time machine for code

---

## ✅ Quick Recap

* Git tracks history
* Uses snapshots
* Stores data inside `.git/`
* Works with working dir → staging → repo

---

## ➡️ Next Step

👉 `02-why-version-control.md`
