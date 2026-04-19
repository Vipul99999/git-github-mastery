# 🔍 git status (State Checker)

---

## 🎯 What It Does

Shows current state of repository.

---

## 🧪 Command

```bash
git status
```

---

## 📸 Visual (File States)

![Image](https://images.openai.com/static-rsc-4/NTYSUpYHeusYjTNONo5z4kVjugrfzIONbonlCOh3nuzq_Y_nXD_79tC2KSzwC_GauM6ZD8Z_VjURU2lRcTvARV9Xot3RkUWWdmEV4_x3jIAzF8mW3UGo9Sfo18oumK9l4I-Qr0H2KQpHZ8VeyQwNYAe9Srv3Q-O_Bz6fvYPZIXcoJGzLvWE7WDkUoXJEbtSL?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Dx-ZbwLNCBcWA4VlkY_wZ8JrGApeyiEvGKTJwnVOUOMRrjnokvzKqVVKSbqk4Y0CYPozIK9lhbySqJqjb31bxhcQ-wKDD2ix4N-WrVcJBR1Cv3TRAmXfnno_l9vrz9D6Ze8sIFLO8UQFfd4Au65zNAnly9H_0lUrpxsTHFZGN_o8vHyVyHbzlfZ7ExH54iYF?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/uyuR5mOe_GY-jNU_wJ37tbFjjNmGWbfE4sGGFzH4KwBv8wCJUFmHd0NTQKUzRuxIld3RFD4NjN2i2uUCRcG3A3ctjgY_RoOIZv6dcOQ8DXLZrp0qmBUyzAQS9Svev8xy8MnZnHfAKOiWBkOc-xMcqODGSZCMTb5mbjnaUUB69T996onnxzlXyGRJwW1RwOyM?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/VVs1AjyTA8YPg1bS5Gu5MrXZUSA__leTFdBhcY7NJYxVlhZ5Xlk5D43KtTarPnTvuWJvKDRdqmn7rxFgEOeqG435s8jSNiLwMNO752hnztukwZ1K_qqPwNpN2XyKYc1Xbrsq7c_uDgF8FemqSMGpEaxOl2I5FBF6KeJfkzBBQ6u4V__R7oA5QXcluxhuTCp8?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/QRyFtvSh8G8hwDTCcEwFDIhZ6Vghd3pAV3NkL1Nw1kFXHUhdc_dWG1DT8cC1DutVDUaOBkj9mWeavcVvu9lVGfDkk7p3s1vW-GOl2ncVoUn6UuwqL8KhO9NpAVq_6uclgTKo9Y1kQrvB63FqGrh6J8-p60G-4byqX7ecArJVVb0TwBEHLUjU0kidYpGePYow?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/52mFUDSSYGoKeK4MDZuqQw2DapLCTbmINBJy85oDbaZZPtKvo5wSJ1USW6Rlf_lh0e1BL0v17UdG8QeDAqgIAve9lwXkVnl_qUe6Z7FlwYkYJUExzUf8T4fL1taVXspqLFqjaI8RRBb84Lja4BLuRbbgydTOif2VTMh2SbhLMlIMGqPr77KRfrSTf9kp3HZb?purpose=fullsize)

---

## 🧠 File States

Git tracks files in 3 states:

### 1. Untracked

* not in Git yet

### 2. Modified

* changed but not staged

### 3. Staged

* ready for commit

---

## 🏗 Internal Detail

Git compares:

* working directory
* staging area (index)
* last commit

---

## 🔬 How It Works Internally

`git status` checks:

```text
Working Directory vs Index vs HEAD
```

---

## 🧩 Example Flow

```bash
touch file.txt
git status   # untracked

git add file.txt
git status   # staged

echo "hi" >> file.txt
git status   # modified
```

---

## ⚠️ Rule

> Always run `git status` before committing

---

## 🧠 Memory Trick

> git status = current truth

---

## ➡️ Next Step

👉 `08-git-add.md`
