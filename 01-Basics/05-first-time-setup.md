# ⚙️ First-Time Git Setup

---

## 🎯 Goal

Configure Git so your commits have identity.

---

## 🧠 Why This Matters

Every commit in Git stores:

* author name
* email
* timestamp

Without setup → commits are incomplete or incorrect.

---

## ✅ Basic Setup Commands

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## 🧪 Verify Setup

```bash
git config --list
```

---

## 📸 Visual (Config Flow)

![Image](https://images.openai.com/static-rsc-4/638nr2LN6qGVl7PtlTf3ZJDU0_qdkzid7lH_aNmCBtjMYGkwt4a0cPSNWvOwbCaXGD2Yo65ytoGmc9Mw7WFAnxy9b6FG7HEfaLVO4Pz7s_aA0F-Cuvj0q9hvzSZEVvmqcLKAcJfbwTGZq7ZAjS0mV-WaUv72_MwYgstUfFzUxCilqO7e7rrjS4fd8REtEiiG?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/fX8GoAB7jA8SqpNX4V2-kLK0cmy5JMUymQX9iX37StH0deNGq5PEgEC5BwPuw_kpqhd6W8OkpmEIHBeLfRsJFMS3GqprwNRXsLJaKi5EhZ48Mfx8LnO2_sBcdoawG_Kg3-0-NbHDmovlKvCnuW2njWz05AsCZEDjTgFIaYQpRzD_H5FlZLuNP8fn2I0AHhvs?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/6xPWnQPQsvCi_ZC7M11yIz_qg30P5QwiMS2WbujhgTjxj6ycN-4npKOIZ-YYCk24a-fWGT0_12NJcEBvWrRH3T7CQ1LN5MNzwuBjrGh3DUf3NBdXL0lvXtYHXwAinhkNDOzhT8k_cxyjVJIUgScBHxCcCwqybMqhs89nM2R8fU-4EG207yLo_xXVKK2i21DR?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/dpFRaBAjoKZ5tdYplFWJSpHXtU6SfKnYNvxCoRzxA_HmA_dlD_RUk-s5yWQKYO7U5T6i8_hGlM93_v-Dpt-OOfgqFctZQ4sZgBM2OQQW7cy65IyTLO2pWNblaICE3-buYNM9ZeYeboyKuTI7lyAwNWUkjQyO7cvYg0OvWhyLO0DLw-8cf9UOespcZUVA8E07?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/WMSEbdgv8TXPodrkd_1u48GK1xpOf4CKIe7WgVba-osNytdD0pNpK1rBYJ2A-cTkExzJh50_Z1xA-d68R-6d62H8pqnptFarve-fHElvoEudYaMh3LRnMQsQaR2lKvLRgFf2q_vlmatNtpe_Gxb5YzO-oplDeQ8W0bHF3J4K1XHvpQdXRoQpSvUM-lARIMLS?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/exGw1Cwpxkt9Jovi3MIz3gkmMBDCsEoBToy6ebJhuFi49FB1IqFl5GP80hxp_fIyljZRq_KNNCdDF2-Zh16jR0wu7SpGfmWpxexRJY6EZ8ZfT_j_e04P-RfL3oeXgkkhZjaHQ6SfVXeXxtqK0vHXL8M57eWcNJoa3drUKf66P0kqZRjjrFMkjjSLUYBRDQBK?purpose=fullsize)

---

## 🏗 Internal Architecture

Git stores config in 3 levels:

### 1. System Level

```bash
/etc/gitconfig
```

### 2. Global Level (most common)

```bash
~/.gitconfig
```

### 3. Local Level (per repo)

```bash
.git/config
```

---

## 🔬 Example `.gitconfig`

```ini
[user]
    name = Your Name
    email = your@email.com
```

---

## 🧠 Priority Order

Local > Global > System

👉 Local overrides global

---

## ⚠️ Common Mistakes

* forgetting to set email
* wrong identity in commits
* mixing work & personal emails

---

## 🧠 Memory Trick

> Config = identity for commits

---

## ➡️ Next Step

👉 `06-git-init.md`
