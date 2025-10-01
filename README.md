
# 🔧 Projet DevOps - ECE

Bienvenue dans ce dépôt GitHub dédié à la matière **DevOps** à l’ECE.  
Ce projet est structuré en **plusieurs Labs et exercices pratiques** et servira de support collaboratif pour apprendre les **principes et outils DevOps**.  

---

## 📌 Table des matières
- [🎯 Objectifs du projet](#-objectifs-du-projet)
- [📂 Organisation du dépôt](#-organisation-du-dépôt)
- [🚀 Utilisation du projet](#-utilisation-du-projet)
- [🌱 Branches par utilisateur](#-branches-par-utilisateur)
- [👨‍🏫 Rôle du professeur](#-rôle-du-professeur)
- [🤝 Contribution](#-contribution)
- [📜 Licence](#-licence)

---

## 🎯 Objectifs du projet
- Comprendre et pratiquer les **principes DevOps** : CI/CD, gestion de configuration, conteneurisation, surveillance.  
- Mettre en place des **pipelines automatisés** pour le build, test et déploiement.  
- Travailler en **collaboration avec Git et GitHub**, avec branches par étudiant.  
- Construire un dépôt clair, maintenable et prêt pour des exercices pratiques.  

---

## 📂 Organisation du dépôt
Le dépôt est organisé par Labs et exercices :  

```

📦 projet-devops
┣ 📂 lab1/       → Introduction à Git et GitHub
┣ 📂 lab2/       → Docker et conteneurisation
┣ 📂 lab3/       → CI/CD avec GitHub Actions
┣ 📂 lab4/       → Gestion de configuration (Ansible / Terraform)
┣ 📂 lab5/       → Monitoring et logging
┣ 📂 lab6/       → Projet final intégrateur DevOps
┣ 📜 README.md   → Documentation du projet
┗ 📜 .gitignore  → Fichiers ignorés par Git

````

Chaque Lab contient :  
- L’**énoncé ou consigne**.  
- Le **code source ou scripts** associés.  
- Des **ressources et références** supplémentaires.  

---

## 🚀 Utilisation du projet

### 1️⃣ Cloner le dépôt
```bash
git clone https://github.com/Lordpanda2003/DevOPs-ECE-2025.git
cd DevOPs-ECE-2025
````

### 2️⃣ Naviguer dans les Labs

```bash
cd lab2
```

Ouvrir les fichiers dans votre éditeur de code préféré.

### 3️⃣ Exécuter les Labs

Certains Labs contiennent des **scripts ou pipelines** :

```bash
# Exemple : lancer un conteneur Docker
docker build -t mon-lab .
docker run -it mon-lab
```

```bash
# Exemple : lancer un workflow GitHub Actions localement (avec act)
act -j nom_du_job
```

---

## 🌱 Branches par utilisateur

Pour le travail collaboratif, chaque utilisateur a sa propre branche :

* `PARFAIT-JUNIOR`
* `MOHAMED BARRO`

Le code validé est ensuite fusionné dans la branche principale (`main`) via **Pull Requests (PR)**.

---

## 👨‍🏫 Rôle du professeur

* Il peut **accéder à toutes les branches**.
* Il supervise le **workflow DevOps** et l’exactitude des pipelines.

---

## 🤝 Contribution

1. Créez votre branche si elle n’existe pas :

```bash
git checkout -b student-nom
```

2. Développez vos Labs dans votre branche.
3. Ouvrez une **Pull Request** vers `main` pour proposer vos modifications.
4. Attendez l’**approbation du professeur** avant fusion.

---

## 📜 Licence

📌 Projet pédagogique pour la matière **DevOps – ECE**.
Usage limité à un contexte **académique et collaboratif**.

---

✨ Bon travail et profitez de l’approche DevOps collaborative !


