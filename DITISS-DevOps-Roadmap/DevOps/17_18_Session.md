## 🧩 **Session 17 & 18: GitHub, Git & Jenkins (CI/CD Fundamentals)**

---

### 🧠 **1. Concept Overview**

* These sessions cover **version control** and **continuous integration/continuous delivery (CI/CD)**.
* **Git + GitHub** manage **source code and collaboration**.
* **Jenkins** automates **build, test, and deployment pipelines**.
* Core backbone of **DevOps automation**.

---

### 📖 **2. Key Definitions**

* **Git:** Distributed Version Control System (DVCS) used to track code changes.
* **GitHub:** Cloud-based platform for hosting Git repositories.
* **Repository (Repo):** Central place where code and history are stored.
* **Commit:** Snapshot of changes with a message.
* **Jenkins:** Open-source automation server for CI/CD pipelines.

---

### 🧩 **3. Main Content (Organized from Notes)**

---

#### 🔰 **Introduction to Git**

* Created to manage:

  * Source code versions
  * Team collaboration
* Every developer has a **local repository**.
* Supports:

  * Branching
  * Merging
  * Rollback

---

#### 🧠 **Git Core Concepts**

| Term       | Description                        |
| ---------- | ---------------------------------- |
| Repository | Storage of project files & history |
| Commit     | Saved change snapshot              |
| Branch     | Parallel line of development       |
| Merge      | Combine branches                   |
| Clone      | Copy remote repo to local          |
| Push       | Upload local commits               |
| Pull       | Fetch & merge changes              |

---

#### 💻 **Going Command Line (Git CLI)**

* Git is mostly used via **command line**.
* Common commands:

  * `git init`
  * `git status`
  * `git add`
  * `git commit`
  * `git clone`
  * `git push`
  * `git pull`

📌 *CLI usage is exam-relevant.*

---

#### 🔁 **Basic Git Workflow with GitHub**

##### 🧑‍💻 **Welcome to GitHub**

* Create GitHub account
* Create a repository (remote)

---

##### 📂 **Setup the Project Folder**

* Create local directory
* Initialize Git repository

---

##### ⚙️ **Git Configuration**

* Configure identity (one-time setup):

  * User name
  * Email address

📌 *Required for commits.*

---

##### 📥 **Clone Repository**

* Copies repository from GitHub to local system
* Command:

  * `git clone <repo_url>`

---

##### 📝 **The First Commit**

* Steps:

  1. Modify files
  2. Stage files
  3. Commit changes

📌 *Commit must have a message.*

---

##### 🚀 **Publishing Changes to GitHub**

* Upload local commits using:

  * `git push`

📌 *Push requires authentication.*

---

#### ⚙️ **Introduction to Jenkins**

* Open-source **CI/CD automation tool**
* Written in Java
* Uses **plugins** for extensibility

**Key Functions:**

* Build automation
* Test automation
* Deployment automation

---

#### 🔄 **CI/CD Pipeline Using Jenkins**

* Pipeline defines:

  * Steps of automation
* Typical stages:

  1. Code Checkout
  2. Build
  3. Test
  4. Deploy

**Pipeline Types:**

* Declarative
* Scripted

📌 *Jenkinsfile defines pipeline.*

---

### 🎯 **4. Important Facts / Points for MCQs**

* Git is **distributed**, not centralized
* GitHub hosts Git repositories
* Commit requires username & email
* Clone ≠ Fork
* Push sends code to remote repo
* Jenkins is CI/CD tool, not VCS
* Jenkins uses plugins

---

### 🧪 **5. Examples**

* GitHub → Remote repository
* `git clone` → Copy repo locally
* Jenkins → CI/CD automation
* Jenkins pipeline → Build → Test → Deploy

---

### ⚠️ **6. MCQ Pointers / Exam Traps**

* Git ≠ GitHub
* Clone ≠ Pull
* Commit ≠ Push
* Fork ≠ Clone
* Jenkins ≠ Build tool only
* Jenkins pipeline ≠ manual deployment

---

✅ **Final Exam Tip:**

> *PG-DITISS MCQs commonly test Git command differences, Git vs GitHub, Jenkins role, and CI/CD stages—focus on workflows and traps.*
