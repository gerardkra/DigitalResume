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



Ok, je vois 😅 il y a eu plusieurs étapes et maintenant GitHub Pages ne trouve toujours pas ton site. Pas de panique, on va repartir **de zéro en ligne**, étape par étape, pour que ton site HTML/CSS soit publié correctement.

---

### 1️⃣ Vérifier la structure du dépôt

Pour GitHub Pages, tu dois avoir dans ton dépôt :

```
index.html
style.css
images/ (ton dossier d’images)
CV_KRA_Gerard.pdf (si tu veux)
README.md (optionnel)
```

> Tous ces fichiers doivent être **dans le dossier que tu choisis comme source GitHub Pages**, soit la racine `/` du dépôt ou `/Resume` si tu choisis ce dossier.

---

### 2️⃣ Publier le site depuis GitHub

1. Va sur ton dépôt :

```
https://github.com/gerardkra/DigitalResume
```

2. Clique sur **Settings → Pages** (ou Paramètres → Pages).

3. Dans **Source**, sélectionne :

   * Branch : `main`
   * Folder : `/ (root)`
   * **OU**, si tu veux utiliser `Resume/`, choisis `Folder: /Resume` si l’option est disponible.

4. Clique sur **Save**.

5. GitHub Pages affichera un message comme :

```
Your site is ready to be published at https://gerardkra.github.io/DigitalResume/
```

---

### 3️⃣ Vérifier les fichiers

* Assure-toi que **index.html** est bien présent à la racine (ou dans `Resume/` si tu as choisi ce dossier).
* GitHub Pages **ne publie jamais les fichiers dans un sous-dossier non sélectionné**.

---

### 4️⃣ Si tu vois toujours README.md

* Cela veut dire que GitHub Pages regarde **la racine**, mais ton `index.html` est toujours dans un sous-dossier.
* Solution : **déplacer tous les fichiers du dossier `Resume/` à la racine**, puis refaire le commit et push :

```text
index.html
style.css
images/
CV_KRA_Gerard.pdf
```

* Après ça, retourne dans **Settings → Pages**, sélectionne branch `main` et folder `/ (root)` → Save.

---

