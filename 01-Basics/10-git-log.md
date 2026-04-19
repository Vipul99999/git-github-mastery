# 📜 git log (View History)

---

## 🎯 What It Does

Shows commit history.

---

## 🧪 Commands

```bash
git log
```

### Short version:

```bash
git log --oneline
```

---

## 📸 Visual (Commit Graph)

![Image](https://images.openai.com/static-rsc-4/I6egHGSxj66u8jsOqcqHF3hwEOj7L4jlDOJoFQJ8e-cZu1Uu576GJUKaChJjTVEFhK2QASCR4Kx06UfNdwPBMw7Qgin12UXJZynBF1rdZLbpQgf83v8R2vS_8lw3iELfR4IeWgybILxGE3-8NAcs791nLN3BxmFs61OIXRWwrXJ-nm9-FlpFc1kAtoiCAOJB?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/kHH_C7M9BIlmnqUJ5BikhqsfaptP_yCrInCklMLBHnx4cAgpVrrj9qKhoKZLvxBdYV4PWLfUS75h-Fc9osIAWvdWapA9Nvwd6x_5wjhoRRxm_WQEfGunew7Q-Bd4XlPat9Lt2bvh_K2ftH6XWPlUwaCZO-eXnXG0CsKTkeE6EJ4Q1pNxot8rtMxCeHHnMj2P?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/PCcMQlfS5DRpIJQJQrtdlCSTYO-EIKMU2zYepHhkva7IMJwYjT6VNkrmuti0E41Iwfk2yvPcfvgkRgrXLpwzuRT8Fbz9J9NrkzSkNAVF94_-SYnPTc7K8gvszouc1XH6TWo1B7tIJH_zj58oxVM3cm3CeXes_QblOSdCioxOIMGJ8GdbXuaclWV52a8FYuYf?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/JgkhmyrzS9srs2TtEtwlayjHJCP-LPfvmxe0ADaVYgPVkcA-g-aYW1Tj8jPMiIVSNwJx3Esgya0zNFF9-7bcVEynuIGNQ37h-Vd3Bqbkf-9NMrtmEdNIgwQO057zYnvWF8onRE5T69dyj7KyzUrlNZ7cMiEc3vVz513fl2OlI_tJD6uHAST97jhiX5MSmBAb?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/bivMxcWSk7UfIyZIs08fAxEf-IY1wGYxZ9m1rfzkVnlDaMXzPkCjfznA0yM0CuueBAqFBQJ90g49pcTXMIrv0VN8Ev0ImsousHOi4Y5jHho2y4YjNvW0ruAdZpoahEx6yD19djX8NpCnwCE20ckHphXttn-TnViaU9869pK3gOXPu4iOBAqTrpXrM1j33J2u?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/I6egHGSxj66u8jsOqcqHF3hwEOj7L4jlDOJoFQJ8e-cZu1Uu576GJUKaChJjTVEFhK2QASCR4Kx06UfNdwPBMw7Qgin12UXJZynBF1rdZLbpQgf83v8R2vS_8lw3iELfR4IeWgybILxGE3-8NAcs791nLN3BxmFs61OIXRWwrXJ-nm9-FlpFc1kAtoiCAOJB?purpose=fullsize)

---

## 🧠 Mental Model

> git log = reading the story of your project

---

## 🏗 Internal Architecture

Git does NOT store history as a list.

It stores it as a **graph (DAG)**:

👉 Directed Acyclic Graph

---

## 🔬 How git log Works

`git log`:

* starts from HEAD
* follows parent commits
* prints history backwards

---

## 🧩 Example

```text
A ← B ← C ← HEAD
```

`git log` shows:

```text
C
B
A
```

---

## 🔥 Useful Commands

```bash
git log --oneline
git log --graph
git log --all
```

---

## ⚠️ Common Mistake

Thinking history is linear.

👉 It becomes complex with branches.

---

## 🧠 Why This Matters

Because:

* debugging depends on history
* merges create graphs
* rebasing rewrites history

---

## 🧠 Memory Trick

> git log = history viewer

---

## ➡️ Next Step

👉 `11-git-diff.md`
