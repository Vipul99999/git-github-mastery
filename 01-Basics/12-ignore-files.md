# 🚫 .gitignore (Ignore Files)

---

## 🎯 Why This Matters

Some files should NOT be tracked.

Examples:

* dependencies
* secrets
* logs
* build files

---

## 🧪 Example `.gitignore`

```bash
node_modules/
.env
*.log
dist/
```

---

## 📸 Visual (Ignore Flow)

![Image](https://images.openai.com/static-rsc-4/Dx-ZbwLNCBcWA4VlkY_wZ8JrGApeyiEvGKTJwnVOUOMRrjnokvzKqVVKSbqk4Y0CYPozIK9lhbySqJqjb31bxhcQ-wKDD2ix4N-WrVcJBR1Cv3TRAmXfnno_l9vrz9D6Ze8sIFLO8UQFfd4Au65zNAnly9H_0lUrpxsTHFZGN_o8vHyVyHbzlfZ7ExH54iYF?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/ZPir-1zBroarwz50wcRef0W2cHs-UazEgjDBTYAZX4BPZQYXz8d0FVzZYcA9TSXUYMpJM5eyQaUP8kJQ1EfAHkPuts0HPCyo2lRhdZrvs9lhFd4pghG8AhzGA9JwwAxVGR5ca7auFktz1MUWTLkCbWpr-U2Lm1Lj2su8Epo5cN7f7SGSa5vcUNy1STWxuiaZ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/hA-Fd5v_m-8_deIFNUwtKxXwdn14pNKvEzAZozYupFGWj-1QFqT0as0G1U80cU6y1ok8nwH4Fd-vQ94syLgMtL90iuAT4wHYh5GQu6bg4M6yhBhHNBIetvsJr6a--gJWo5REGul6jYzmVTqHb1VsdJzV_wvuVTugO4S4WSHnzkWnXqtPwFf-ehkwvaRJcaVQ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/xIx_L9yGa_rKUN7LGstl8zq43kZEu7gl5yHgFvamqrfp95nkvmXira2ryWA8kaM7f2iO5h1rrgpALQcjbn9FTOupc3S8_-caMAqlQHnrz-Ejjo1DzZe2cQ6R2Uuk-iHeAvQL1rQ0VfSKZLDiURHjPZZW9Iwu9S93Lk6TyazxjTyvJN9UlwlQSNOFDi66xzrW?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/dU-sjILycGWTh22XntKqpBTuL0tcAUwqfKrJv4yPd_Te_x99p6omS9poddZjuyka_gZ3LNZMyo1o40AMJcV1E7PUYxqMM2ObDQ95jUAVYdhNpB4_Gsi0YJL7A0bj6FGGlSqSKLx6WGIYm-zG_61Bc-JPpoJocvpfVAfcZbzBfC4Q6tq4d53xJ0spodZDqwvk?purpose=fullsize)

---

## 🧠 Mental Model

> .gitignore = filter before tracking

---

## 🏗 Internal Behavior

Git checks `.gitignore`:

* before adding files
* while scanning untracked files

---

## 🔬 Important Notes

* `.gitignore` does NOT remove tracked files
* only affects untracked files

---

## 🧩 Example Problem

You accidentally committed `.env`

👉 `.gitignore` won’t remove it

Solution:

```bash
git rm --cached .env
```

---

## 📁 Location

`.gitignore` is stored in project root:

```text
project/
 ├── .gitignore
 ├── app.js
```

---

## ⚠️ Common Mistakes

* adding `.gitignore` too late
* assuming it removes tracked files

---

## 🧠 Memory Trick

> ignore = prevent tracking

---

## ➡️ Next Step

👉 `practice-lab.md`
