# 🛠 Mettre à jour un repository forké
> Exemple concret avec le projet **Quartz (v4)**

---

## 🎯 Objectif
Mettre à jour un **repository Git personnel forké** (comme mon site Quartz) avec les nouveautés publiées dans le **dépôt officiel**, sans perdre mes propres modifications.

---

## 📦 Exemple utilisé dans ce guide
- Dépôt personnel (`origin`) : `https://github.com/laureanaisboulay/wiki.git`
- Dépôt officiel (`upstream`) : `https://github.com/jackyzha0/quartz.git`
- Branche principale : `v4` (et non `main`)

---

## 🧭 Étapes complètes

### 1. 📂 Ouvrir un terminal dans le dossier du projet

```bash
cd "C:\Users\anais\OneDrive\Github Repository\quartz"
```

---

### 2. 🔍 Vérifier les dépôts distants

```bash
git remote -v
```

Résultat attendu :
```
origin    https://github.com/laureanaisboulay/wiki.git (fetch)
upstream  https://github.com/jackyzha0/quartz.git (fetch)
```

---

### 3. 🧩 Ajouter le dépôt officiel (si ce n’est pas encore fait)

```bash
git remote add upstream https://github.com/jackyzha0/quartz.git
```

---

### 4. 🔄 Récupérer les mises à jour du dépôt officiel

```bash
git fetch upstream
```

---

### 5. 📌 Identifier la bonne branche principale

> ⚠️ Habituellement, la branche principale d’un projet Git s’appelle `main`.  
> Mais certains projets, comme Quartz, utilisent un autre nom — ici, `v4`.

Pour le vérifier :
```bash
git branch -r
```

Exemple de résultat réaliste :
```
origin/HEAD -> origin/v4
origin/main
origin/v4
...
upstream/HEAD -> upstream/v4
upstream/v4
```

🔎 On en déduit que :
- Branche principale de mon dépôt : **origin/v4**
- Branche principale du dépôt officiel : **upstream/v4**

✅ Je dois donc suivre la branche `v4`, pas `main`.

---

### 6. 🧭 Se placer sur ma branche locale

```bash
git checkout v4
```

---

### 7. 🔧 Fusionner les changements de l’`upstream`

```bash
git merge upstream/v4
```

👉 Résoudre les conflits si nécessaire, puis :
```bash
git add fichier-concerné
git commit
```

---

### 8. 🚀 (Optionnel) Pousser les changements sur mon dépôt GitHub

```bash
git push origin v4
```

---

## ✅ Résultat

Mon dépôt personnel est à jour avec les nouveautés du dépôt officiel, tout en conservant mes modifications locales.

