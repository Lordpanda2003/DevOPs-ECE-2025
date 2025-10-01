
# 🛠 Lab 1: Implementing DevOps Practices with Node.js

Welcome to this lab on **Implementing DevOps Practices in IT Projects**.  
The goal of this lab is to learn how to start a project **following best practices**, including **clean code, documentation, and version control**.  

As an example, we will use **JavaScript with Node.js** to create a simple web server, but you may use any other programming language (Python, Java, C++, etc.) following the same principles.  

---

## 🎯 Objectives
By the end of this lab, you will be able to:  
1. Start a new project folder following best practices.  
2. Initialize a Node.js package using `npm`.  
3. Create a simple Node.js script.  
4. Build a basic web application using **Express.js**.  
5. Create and maintain a **CHANGELOG.md** file.  
6. Write a professional **README.md** file documenting the project.  

---

## 📌 Prerequisites
Before starting the lab, make sure you have:  

- **IDE / Text Editor**: VS Code, Atom, WebStorm, or your preferred editor.  
- **Git**:  
  - Windows: [https://gitforwindows.org/](https://gitforwindows.org/)  
  - Linux: [https://git-scm.com/download/linux](https://git-scm.com/download/linux)  
  - macOS: [https://git-scm.com/download/mac](https://git-scm.com/download/mac)  
- **Node.js**: [https://nodejs.org/](https://nodejs.org/)  
- **Command Line Interface**:  
  - macOS / Linux → Terminal  
  - Windows → Git Bash (avoid CMD.exe)

---

## 1️⃣ Start a Project
1. Open the terminal and navigate to your working directory:  
```bash
cd ~/path/to/your-root-project-directory
````

2. Create a project folder (use **kebab-case**, no spaces):

```bash
mkdir myschool-devops-myproject
cd myschool-devops-myproject
```

3. Initialize Git:

```bash
git init
```

4. Create a GitHub repository with the **same name**. Do **not** initialize with a README.

5. Add the remote origin:

```bash
git remote add origin git@github.com:Lordpanda2003/DevOPs-ECE-2025.git
```

---

## 2️⃣ Initialize a Node.js Package

1. Initialize `package.json`:

```bash
npm init -y
```

2. Optional: Edit `package.json` to include author, description, and other metadata.

3. Run the default test script:

```bash
npm test
# or
npm run test
```

---

## 3️⃣ Create a Node.js Script

1. Open your project folder in your editor:

```bash
code .
```

2. Create `index.js` with:

```javascript
const str = "Hello Node.js!";
console.log(str);
```

3. Run the script:

```bash
node index.js
```

4. Add a **start script** in `package.json`:

```json
"scripts": {
  "test": "echo \"Error: no test specified\" && exit 1",
  "start": "node index.js"
}
```

5. Run it via npm:

```bash
npm start
```

---

## 4️⃣ Create a Web Application Using Express

1. Install Express:

```bash
npm install express
```

2. Update `index.js` to serve a simple web page:

```javascript
const express = require("express");
const app = express();
const port = 3000;

app.get("/", (req, res) => {
  res.send("Hello world!");
});

module.exports = app.listen(port, (err) => {
  if (err) throw err;
  console.log("Server listening on port " + port);
});
```

3. Start the server:

```bash
npm start
```

4. Open your browser at `http://localhost:3000` to see "Hello world!".

---

## 5️⃣ Create a CHANGELOG.md

Document all project changes to track progress and updates. Example:

```markdown
# Changelog

## Unreleased

### Added
- Initialize Node.js project
- Create HTTP web server using Express
```

---

## 6️⃣ Create a README.md

Document your project including:

* **Short description**
* **List of functionalities**
* **Installation instructions**
* **Usage instructions**
* **Author information**

Example structure is provided in this file.

---

## 💡 Bonus Tasks

* Practice common Bash commands.
* Learn to use **Vim** (`vimtutor` in terminal).
* Try alternative programming languages to implement the same steps.

---

## 👨‍💻 Author

* Name: *MONEZE PARFAIT-JUNIOR*
* Course: *DevOps / Technology Web – ECE*
* Date: *01-10-2025*

---

✅ After completing this lab, you will have a **documented Node.js project** with a working web server and a professional structure suitable for DevOps workflows.
