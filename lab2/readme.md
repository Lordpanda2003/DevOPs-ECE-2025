
# Lab 2 – DevOps Project Setup

## Objectifs

* Démarrer un projet Node.js
* Initialiser un package NPM
* Créer un script Node.js
* Créer une application web avec Express
* Ajouter un `CHANGELOG.md`
* Décrire le projet dans un `README.md`

## 1. Démarrer le projet

```bash
mkdir DevOPs-ECE-2025
cd DevOPs-ECE-2025
git init
git remote add origin git@github.com:Lordpanda2003/DevOPs-ECE-2025.git
```

Vérifier SSH avec GitHub et configurer si nécessaire.

---

## 2. Initialiser le package Node.js

```bash
npm init -y
npm run test
```

---

## 3. Créer un script Node.js

Créer `index.js` :

```js
str = "Hello Node.js!";
console.log(str);
```

Exécuter :

```bash
node index.js
npm start  # si script start défini dans package.json
```

---

## 4. Application web avec Express

Installer Express :

```bash
npm install express
```

`index.js` :

```js
const express = require("express");
const app = express();
const port = 3000;

app.get("/", (req, res) => res.send("Hello world!"));

app.listen(port, () => console.log("Server listening on port " + port));
```

Lancer :

```bash
npm start
```

---

## 5. CHANGELOG.md

```md
# Changelog

## Unreleased

### Added
- HTTP server avec Express
- Projet initialisé
```

---

