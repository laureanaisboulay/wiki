# 🚀 Déploiement propre d’un site Quartz 4 sur GitHub

Objectif : Créer un dépôt GitHub **sans héritage de commits** ni de contributeurs externes, avec **Quartz 4** comme moteur de publication.

---

## 🧭 Étapes complètes

### ✅ 1. Télécharger Quartz proprement (sans Git)

- Aller sur : [https://github.com/jackyzha0/quartz](https://github.com/jackyzha0/quartz)
- Cliquer sur **Code** → **Download ZIP**
- Extraire l’archive `.zip` dans un dossier de travail :
  ```
  C:\Users\anais\Projets\quartz-routine
  ```

---

### ✅ 2. Nettoyer les fichiers liés au dépôt original

Supprimer les fichiers suivants (facultatif mais recommandé) :
- `README.md`
- `LICENSE`
- `CODE_OF_CONDUCT.md`
- `.github/` *(ou au moins les sous-fichiers liés au sponsor)*

---

### ✅ 3. Créer un dépôt GitHub

- Aller sur [https://github.com](https://github.com)
- **Créer un nouveau repository**
  - Nom : `quartz-routine`
  - Visibilité : `Public`
  - ✅ Cochez **“Add a README”** *(GitHub en a besoin pour initialiser le dépôt)*
- Cliquer sur **Create repository**

---

### ✅ 4. Initialiser Git dans le dossier local

Dans PowerShell (depuis le dossier extrait `quartz-routine`) :

```bash
git init
git add .
git commit -m "Initialisation propre de Quartz"
```

---

### ✅ 5. Lier au dépôt GitHub et pousser

```bash
git remote add origin https://github.com/laureanaisboulay/wiki/
git branch -M main
git push -u origin main
```

*(Remplacez `votre-utilisateur` par votre nom GitHub exact)*

---

### ✅ 6. Lancer le site en local pour tester

#### 🧰 A. Installer les dépendances

```bash
npm install
```

#### 🚀 B. Construire et lancer le site localement

```bash
npx quartz build --serve
```

Cela va :

- Générer le site dans le dossier `public/`
- Lancer un serveur local accessible à l’adresse :
```
http://localhost:8080
```

#### 🧪 C. Ouvrir dans le navigateur

Accédez à : [http://localhost:8080](http://localhost:8080)

---

💡 Si vous modifiez des fichiers `.md`, relancez la commande `npx quartz build --serve` pour voir les changements.

---

## 🎯 Résultat

- Le dépôt GitHub est **propre**
- Aucune trace d’auteur externe (ex : Jacky Zhao)
- Le projet est prêt à être **mis en ligne avec GitHub Pages**

---

*Procédure écrite sur mesure pour Mademoiselle Anaïs, avec élégance et rigueur 🛠️✨*
