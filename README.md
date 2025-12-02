
# Projet DevOps – ECE

Ce dépôt regroupe l’ensemble des travaux pratiques réalisés dans le cadre du cours de DevOps à l’ECE. Il sert de support pour apprendre et mettre en œuvre les principaux outils et méthodes liés au DevOps, de manière progressive et collaborative.

## Objectifs du projet

* Comprendre les bases du DevOps et appliquer les bonnes pratiques.
* Mettre en place des pipelines automatisés (CI/CD).
* Manipuler des outils de conteneurisation, d’orchestration et de gestion de configuration.
* Travailler en équipe avec Git et GitHub, en utilisant des branches dédiées.

## Structure du dépôt

Le projet est divisé en plusieurs Labs, chacun associé à un thème précis :

Chaque Lab contient :

* la consigne ou l’énoncé,
* les scripts et fichiers nécessaires,
* des ressources d’appui si nécessaire.

## Utilisation

### Cloner le dépôt

```
git clone https://github.com/Lordpanda2003/DevOPs-ECE-2025.git
cd DevOPs-ECE-2025
```

### Naviguer et exécuter un Lab

```
cd lab2
```

Certains Labs contiennent des scripts ou conteneurs à exécuter :

```
docker build -t mon-lab .
docker run -it mon-lab
```

## Collaboration

Chaque étudiant travaille sur sa propre branche :

* PARFAIT-JUNIOR
* MOHAMED-BARRO

Les modifications sont intégrées via des Pull Requests vers la branche principale.

### Créer ou utiliser votre branche

```
git checkout -b nom-etudiant
```

Après les modifications :

```
git push origin nom-etudiant
```


