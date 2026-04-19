# 🔎 git diff (See Changes)

---

## 🎯 What It Does

Shows differences between versions.

---

## 🧪 Command

```bash
git diff
```

---

## 📸 Visual (Diff Comparison)

![Image](https://images.openai.com/static-rsc-4/CEkRvlByTIQWUMQElmdB-KKGvNwCEOrjbo2vvgj-ktHGgutxvp8PLG6ISM1fTqyZ6HySnDHg2XCcPCkjIJm7jVV64wKzKEVoJO_eKmOhbE5HkiuaGG6uOBxr9fgcJQeu8m7bO-1ou7e50GC_wA__ZIll3HyCLCDkQ2iskppr9piw40_ycgUWRDza0sJWedWM?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/3uPNMZLOkOUgSA256HUd6S1XE7zurZWgCFog9I5TFVwEFXP56uwgwd6-A7CSE2teq-14louzblTBxtmhPspxifzkGrtSd9SXNiA9QZAKh-zAbhHOYYhb_aA9vFo5hjcxk15Sa4JMsx1H3HmJsCrVw3SdZ4v_KnY1VYEYAE5ZSk5r15xKDESbAFRboYYkuf11?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/T9XkLVa2q-xRcZHlOWP0jD9zukQ-sR3GoHKEdwBMr_rRTxJ057B7707b7KEJCozC9Plp9rBtx87cucdkbtquZPhjVgMEOCiYqpEmw5a4LMLxpkOJQx2Pd8U7X09p4R92y61DtI1wI51-4yBXrS666PVRmrH0WnKUCHi811Z7yvGbXXGFS8DgoG3DeaN75Bua?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/IM8C-rNbVqcyXuo6x4nQYE9IdGgIhy_NDfhdbyeOrZwYoFA7SzR8NpZpsTsqWEJM8TqsyTxfb1h9yXyRuMMT0I52HXolyOTo65Xzqj-atl1ZhtiMXpgv6c0Aevp46k25MK_tY0vQHFVZeV9_fa4VmmgPjsExsRJnvlapxiLWQyH35aP3QFO7e6qa2UCaM67T?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/u2g8XQmeb1z0YC0zUd4EyPGJ8U2KS4tGm4MqjNsgsNyFdC266Ufe7rvZndmP5w9ELlPZ4L4HE-YdFGXs-lKlL0dOvwmg6wSJ66HAaneTHTF1nCGshQt8mnqGvTT59JFXGWyv5Q41Rq_M8KkYWuN-9nVLh56EgafHJnbPGcfEeNe7tZD0yvVJwAC2mu3Bit7Y?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/m6W2W-uBYOYySj0lkJMGBVn82UU-LVkZTZ5dr790qJmLh3D7LrNn7KQHGitXHN7DXRFC17Bsk7hU1OpVYt-OkNQqMZJV6tll2K5qUVcQaDHhYs8vQTII7FW894XDQJki9U4FJku9mCMaqGxydcwIpVKZ1fcROVgGeyIfiOOHUH91XTaZYA6FP-ixLrbceC8u?purpose=fullsize)

---

## 🧠 Mental Model

> git diff = compare snapshots

---

## 🏗 Internal Architecture

Git compares:

```text
Working Directory ↔ Index ↔ HEAD
```

---

## 🔬 Diff Types

### 1. Working vs Staging

```bash
git diff
```

### 2. Staging vs Last Commit

```bash
git diff --staged
```

---

## 🧩 Example

Before:

```text
Hello
```

After:

```text
Hello World
```

Diff:

```diff
+ World
```

---

## 🧠 How Git Computes Diff

Git uses algorithms (like Myers diff) to:

* find added lines
* find removed lines
* show minimal changes

---

## ⚠️ Common Mistake

Not checking diff before commit.

👉 Leads to wrong commits

---

## 🧠 Why This Matters

Because:

* helps debugging
* shows exact changes
* prevents mistakes

---

## 🧠 Memory Trick

> diff = what changed

---

## ➡️ Next Step

👉 `12-ignore-files.md`
