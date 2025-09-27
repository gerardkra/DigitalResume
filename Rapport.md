Exactement 👍, pour que ton dépôt local pointe vers `git@github.com:gerardkra/DigitalResume.git`, il suffit de **changer l’URL du remote `origin`**.

Voici comment faire :

---

### 1️⃣ Changer le remote `origin`

```bash
git remote set-url origin git@github.com:gerardkra/DigitalResume.git
```

---

### 2️⃣ Vérifier que ça a changé

```bash
git remote -v
```

Tu devrais maintenant voir :

```
origin  git@github.com:gerardkra/DigitalResume.git (fetch)
origin  git@github.com:gerardkra/DigitalResume.git (push)
```

---

### 3️⃣ Tester avec pull ou push

```bash
git pull origin main
git push origin main
```

* Le message affichera maintenant :

```
From github.com:gerardkra/DigitalResume
```

* Git utilisera le dépôt correct pour synchroniser tes fichiers.

---
