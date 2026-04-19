# 📸 Git as Snapshots (Not File Storage)

---

## 🎯 Why This Matters

Most beginners think:

> “Git stores changes line-by-line”

This is WRONG.

Git stores:

> **Snapshots of your entire project**

---

## 🧠 Mental Model

Think of Git like a camera:

* Every commit = a photo of your project
* Not just changed files
* The whole project state

---

## 📸 Visual Explanation

![Image](https://images.openai.com/static-rsc-4/I6egHGSxj66u8jsOqcqHF3hwEOj7L4jlDOJoFQJ8e-cZu1Uu576GJUKaChJjTVEFhK2QASCR4Kx06UfNdwPBMw7Qgin12UXJZynBF1rdZLbpQgf83v8R2vS_8lw3iELfR4IeWgybILxGE3-8NAcs791nLN3BxmFs61OIXRWwrXJ-nm9-FlpFc1kAtoiCAOJB?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/D51gngh6FMAMTsSY3Ekkn6UHP0eUK9cfNN5qA1mZE58phZdWrYRRiCWaNkdQv4w71WrQfS3IpjjK3ed1veOL2ptsndhPCXFgGmEQmpAO_ogkzl7RqZ6QhK40GDip0WKF8EiFG_Nh5WdTiA6lIYzuv5tHQYKnRkpZV5UeouRgiiMOZzVaQMugelLB2-Hy8v8b?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/I6egHGSxj66u8jsOqcqHF3hwEOj7L4jlDOJoFQJ8e-cZu1Uu576GJUKaChJjTVEFhK2QASCR4Kx06UfNdwPBMw7Qgin12UXJZynBF1rdZLbpQgf83v8R2vS_8lw3iELfR4IeWgybILxGE3-8NAcs791nLN3BxmFs61OIXRWwrXJ-nm9-FlpFc1kAtoiCAOJB?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/jp-uXIeOQsTYtRWle7rXXR6Dvt9yhGIJl6C8g13IOAteP5w7r4GvBWdqCM47N8lS9Vy3oLd6pp6z9laOfFNkpg_Y5K5QCvm7hkv7Z2RJsFRE-aKUcwprWmsY-b020QRKhKZNjzJeYKI_jC3NOz51dugtZ9ngKVYnLh_WsTc2aLVkci_dq6vaymQDzmLZ1oUz?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/UXEbqlbLXuikKS3EMOToReV5SUvT7H8Jo9cEZ1rduBLKeG4qDNQrfhH4lwGaGYMiyVC4oGvdrtAilMw-Gx4OrD9fXbCwklej3ZohYNST-LTvKkwtzAwW42dSl8PuU3JpSezQgNytcM3IDQSpPtKnRkAh93L_F50aoNJ0t7GheG6GRDFEBX4Yr0S61REErXEV?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/mg65SWAFfPlhwHGohkuOTnDMWTzEY8sKTZce_chN8ulaoy7VJu4sds34BdeI8SZz-KSzmt4I-FbDvUpUsN3XqhRAvr2_Wcyghe-b7chcuS-m-e6vliFKDpRzFFcGKOiby0vYmXfRtMnGmCrHGCFn3lkUMLxbStFr8CWztB0P21u4zXJBjDuPEbbCiygn5_DR?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/rbm7HDp6aYBvz1rgmnns86wkcjrpad9Rkj-qU8NTyOuQcnNjBoSVqWrFnu_y1TVGTKM47c_yqpcn6jjBvPYzRJuVNE7ZvktuFx317df5f5_oWtNHIHGG49U08LURMiSm8j0MFT_3f0cy6WOH4I08-wbEmIBqbDWhd0fWZ-mo4IelVLyePim9LZWgCg3IIojN?purpose=fullsize)

---

## 🧩 Example

You have:

```text
file.txt → Hello
```

You commit → Snapshot 1

Then change:

```text
file.txt → Hello World
```

Commit again → Snapshot 2

Git stores:

* Snapshot 1 (Hello)
* Snapshot 2 (Hello World)

---

## ⚠️ Common Mistake

Thinking Git stores only differences.

Reality:

* Git **optimizes storage internally**
* But conceptually → it’s snapshots

---

## 🧪 Try This

```bash
git init
echo "A" > file.txt
git add .
git commit -m "A"

echo "B" >> file.txt
git commit -am "B"

git log
```

Now imagine each commit = a full snapshot.

---

## 🧯 Why This Helps You

Because now you understand:

* Why branching is easy
* Why reverting works
* Why history is safe
* Why Git feels “time-travel-like”

---

## 🧠 Memory Trick

> Git is not Dropbox.
> Git is a time machine.

---

## ➡️ Next Step

👉 `branches-are-pointers.md`
