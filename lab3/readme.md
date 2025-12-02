
# Lab 3 – Git Basics

## Objectifs
- Suivre le tutoriel GitHub Desktop
- Créer et cloner un dépôt
- Créer et naviguer entre les branches
- Modifier un fichier et pousser les changements
- Gérer les conflits
- Refaire le lab avec la CLI Git

## 1. Tutoriel GitHub Desktop
- Lancer GitHub Desktop et créer un dépôt tutoriel  
- Suivre les instructions pas à pas

---

## 2. Créer et cloner un dépôt
- Créer un dépôt sur GitHub (public, avec README et .gitignore Node)
- Ajouter les collaborateurs
- Cloner le dépôt avec GitHub Desktop ou `git clone https://github.com/Lordpanda2003/DevOPs-ECE-2025.git`

---

## 3. Branches
- Créer `develop` : **Current branch → New branch**
- Naviguer entre `master` et `develop`

---

## 4. Modifier et pousser
- Modifier `README.md`
- Commit et push sur `develop`  
- Les autres membres : **Fetch origin** → basculer sur `develop`

---

## 5. Gérer les conflits
- Créer des branches à partir de `develop`
- Modifier le même fichier
- Commit et push  
- Merge dans `develop`  
- Résoudre les conflits dans l’IDE puis commit

---

## 6. Refaire avec CLI Git
- Installer Git si nécessaire
- Répéter toutes les étapes en ligne de commande :
```bash
git clone <https://github.com/Lordpanda2003/DevOPs-ECE-2025.git>
git checkout -b parfait
git add README.md
git commit -m "message"
git push origin develop
git merge main
```


