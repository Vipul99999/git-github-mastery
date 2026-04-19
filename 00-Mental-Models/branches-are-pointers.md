# 🌿 Branches Are Just Pointers (Not Copies)

---

## 🎯 Why This Matters

Most beginners think:

> “A branch is a copy of my code”

This is WRONG.

A branch is:

> **Just a pointer (label) to a commit**

---

## 🧠 Mental Model

Think of branches like bookmarks:

* They point to a specific commit
* They move forward when you commit
* They don’t duplicate your files

---

## 📸 Visual Explanation

![Image](https://images.openai.com/static-rsc-4/DZAatp73-dB4tngNxL1T7Kwp_DHozQANJHKqxy-MP9Q0uEiihaUlbaj7tsID_mu2Mm3meZrhaElKQv6pLkEF6s4ZChF8jcSUK_gz2Rbx-VnfpfFxAh9pAGG5yEGyE6Ep8gJjqpWFieuLG0abrjAhHasTyy8wiPgAm4JtPtj1k82cQhXEfWbqyZNPuymCFkHD?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/I6egHGSxj66u8jsOqcqHF3hwEOj7L4jlDOJoFQJ8e-cZu1Uu576GJUKaChJjTVEFhK2QASCR4Kx06UfNdwPBMw7Qgin12UXJZynBF1rdZLbpQgf83v8R2vS_8lw3iELfR4IeWgybILxGE3-8NAcs791nLN3BxmFs61OIXRWwrXJ-nm9-FlpFc1kAtoiCAOJB?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/w4ThymMcbikaNnu1Vv-Jqgrnj4bVrxor4C4zQUS0ldMNWrkqAqdpp68PLkshqUAqi8Bra2t37ZlMkr08LznrQzwOcIM6i2TlQw-N0dMAUGDdmevKqFXZ-RQ5RmpjvyB1Joo-mrc-mMFotpPOp7GLDMmr7rQQVxbXlAKZ52DqbAk5sXziWG7sTXDwBtivdz02?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/26NEVeou_zBi3xIOxeAQv9Vv5sEKJ4CLPCrXz_mx3RAJO1fS6vy3tUpvQy5106P7NaHwnOVn0yoMSJdDPuaA21OaA22-iswlH1QaMQfeKOW3tk2xcBSu-0jm1yCzGvqgZkHObgDPT0rmQmH_QHMWGvBDMYpLq8s_cOVENPrMACi64a3EbXEGJcYs_KNmR69u?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/gbBLDIMGyUMEonV3uj0n7vJ2JzoaNYTcr8-jWxs3lSgz6VwqLDrSITURCdUnhHMbli7XPI_pJ4av4k16-hPSUF91tvN70ZTBPLiLABi2KJNJkyCofv1sJ7DGwNMCP0MygxWR6sHKoRzbImy-HpakGD9AYdJrWmfcLcihOLPy4l8DGaAmVCcFrdiUhIKOUX1g?purpose=fullsize)

---

## 🧩 Example

```text
A --- B --- C   (main)
```

Now create a branch:

```bash
git branch feature
```

Result:

```text
A --- B --- C   (main, feature)
```

👉 Both point to same commit.

---

## 🚀 Now Add a Commit on feature

```bash
git switch feature
echo "New feature" >> file.txt
git commit -am "Add feature"
```

Graph becomes:

```text
A --- B --- C   (main)
           \
            D   (feature)
```

👉 Only **feature moved**, not main.

---

## ⚠️ Common Mistake

Thinking branches duplicate files.

Reality:

* They are just lightweight pointers
* That’s why Git branching is fast

---

## 🧯 Why This Helps You

Now you understand:

* Why branching is cheap
* Why merging works
* Why rebasing moves history
* Why switching branches is instant

---

## 🧠 Memory Trick

> A branch is NOT a copy.
> It’s a movable label.

---

## ➡️ Next Step

👉 `head-explained.md`
