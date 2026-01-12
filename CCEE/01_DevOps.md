> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 01

---

### 1. What is the correct full form of GIT in the context of software development?

* [ ] Gastro Intestinal Track
* [ ] Gastro International Track
* [ ] Global Information Tracker
* [ ] General Internal Tool

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Global Information Tracker
💡 GIT is a distributed version control system designed for tracking changes in source code. It is **not related to medical terminology**.

</details>

---

### 2. Which Git command is used to download a remote repository from GitHub to your local machine?

* [ ] git fork
* [ ] git commit
* [ ] git clone
* [ ] git push

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** git clone
💡 `git clone <repo-url>` creates a **local copy of a remote repository**. `git fork` is a GitHub action, not a command.

</details>

---

### 3. To stage all changes in your working directory for commit, which command should you use?

* [ ] git push -am "Message"
* [ ] git add .
* [ ] git commit add
* [ ] git commit

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** git add .
💡 The command `git add .` stages **all modified and new files** in the current directory for the next commit.

</details>

---

### 4. Which is the correct Git syntax to commit all staged changes with a message?

* [ ] git add -a "I'm coding"
* [ ] git commit -am "I'm coding"
* [ ] git message -am "I'm coding"
* [ ] None of these

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** git commit -am "I'm coding"
💡 `-a` stages **all tracked changes**, and `-m` adds a commit message. New untracked files must still be added with `git add`.

</details>

---

### 5. Which operation must come first in Git: staging with `git add` or committing with `git commit`?

* [ ] Committing with git commit
* [ ] Staging with git add
* [ ] None of these
* [ ] Either can be first

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Staging with git add
💡 Git requires you to **stage changes first** with `git add` before committing them with `git commit`.

</details>

---

### 6. How do you create a copy of a repository under your own GitHub account for personal use?

* [ ] Forking it via the GitHub interface
* [ ] git clone
* [ ] git pull-request
* [ ] git fork

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forking it via the GitHub interface
💡 Forking creates a **personal copy of the repository** on GitHub, which you can later clone locally.

</details>

---

### 7. When was Git initially created?

* [ ] 2005
* [ ] 2007
* [ ] 2004
* [ ] 2008

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 2005
💡 Git was created by **Linus Torvalds in 2005** to manage Linux kernel development efficiently.

</details>

---

### 8. Which of the following is a primary advantage of using Git?

* [ ] Collaboration-friendly
* [ ] Data redundancy and replication
* [ ] Both of the above
* [ ] None of these

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both of the above
💡 Git is **distributed**, allowing multiple developers to collaborate and providing **redundancy through local copies**.

</details>

---

### 9. Which programming language is Git primarily written in?

* [ ] C language
* [ ] HTML language
* [ ] C++ language
* [ ] Python

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** C language
💡 Git is written mainly in **C**, with some scripts in Shell and Perl. HTML is irrelevant, and C++ was not used.

</details>

---

### 10. What does the command `git push` do?

* [ ] Updates remote refs only
* [ ] Updates remote refs along with associated objects
* [ ] Updates remote refs without objects
* [ ] Does nothing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Updates remote refs along with associated objects
💡 `git push` **uploads commits from local to remote repository**, including all new objects (blobs, trees, commits).

</details>

---

### 11. What is an alternative to merging in Git?

* [ ] Basing
* [ ] Rebasing
* [ ] Both 1 and 2
* [ ] None of these

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Rebasing
💡 `git rebase` **applies changes from one branch onto another** without creating a merge commit, providing a linear history.

</details>

---

### 12. Which of the following is a graphical Git client available for Linux?

* [ ] SmartGit
* [ ] Git Cola
* [ ] Gitg
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 SmartGit, Git Cola, and Gitg are all **GUI-based Git clients for Linux**, offering visual commit and branch management.

</details>

---

### 13. What is the purpose of `git log`?

* [ ] To filter commits by author
* [ ] To filter commits by date
* [ ] To show commit content
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 `git log` can display commit **author, date, message, and changes**, with optional flags for filtering.

</details>

---

### 14. Which platforms provide Git repository hosting services?

* [ ] GitLab
* [ ] GitHub
* [ ] Bitbucket
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 GitHub, GitLab, and Bitbucket are popular platforms for **remote Git repository hosting** with collaboration features.

</details>

---

### 15. What does `git ls-tree` display?

* [ ] A tree object showing mode, name, and SHA-1 for each item
* [ ] A tree object showing mode and name only
* [ ] None of these
* [ ] Commit history

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A tree object showing mode, name, and SHA-1 for each item
💡 `git ls-tree` **displays a Git tree object** with details about files and subtrees, including object hashes.

</details>

---

### 16. Which of the following is **not** a Git configuration scope?

* [ ] User
* [ ] System
* [ ] Local
* [ ] Global

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** User
💡 Git has **system, global, and local configuration scopes**. `user` is not a configuration scope; it’s a setting.

</details>

---

### 17. Which vendor acquired GitHub in June 2018 for $7.5 billion?

* [ ] IBM
* [ ] Microsoft
* [ ] Google
* [ ] Oracle

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Microsoft
💡 Microsoft purchased GitHub in 2018, continuing its role as a **leading code hosting platform**.

</details>

---

### 18. Which command initializes a new Git repository in the current directory?

* [ ] git init
* [ ] git install
* [ ] git start
* [ ] git bash

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** git init
💡 `git init` creates a new **empty Git repository** in the current directory.

</details>

---

### 19. Which of the following is **not** a valid Git command?

* [ ] git clean
* [ ] git clone
* [ ] git commit
* [ ] git roll

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** git roll
💡 `git roll` does not exist; `git clean` removes untracked files, `git clone` clones repos, and `git commit` commits changes.

</details>

---

### 20. Which command is used to show a limited number of recent commits?

* [ ] git fetch
* [ ] git config
* [ ] git log -n
* [ ] git show

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** git log -n
💡 `git log -n <number>` displays only the **last n commits** from the history.

</details>

---

### 21. What is Docker?

* [ ] Programming Language
* [ ] Text Editor
* [ ] Containerization Platform
* [ ] Web Server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Containerization Platform
💡 Docker is a platform that allows developers to **package applications and dependencies into lightweight containers** that can run consistently across environments.

</details>

---

### 22. Which command is used to create a new Docker image?

* [ ] docker build
* [ ] docker pull
* [ ] docker run
* [ ] docker commit

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker build
💡 `docker build -t <image_name> .` creates a **Docker image from a Dockerfile**, compiling all instructions and dependencies.

</details>

---

### 23. What does a Dockerfile contain?

* [ ] Compiled source code
* [ ] Docker images
* [ ] Binary data
* [ ] Instructions for building a Docker image

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Instructions for building a Docker image
💡 A Dockerfile is a **text file with declarative instructions** to build a Docker image, such as base image, dependencies, and commands.

</details>

---

### 24. What is a Docker container?

* [ ] A running instance of a Docker image
* [ ] A lightweight virtual machine
* [ ] A storage volume
* [ ] A service running on Docker Swarm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A running instance of a Docker image
💡 Containers are **runtime instances of images**, isolating processes without the overhead of a full VM.

</details>

---

### 25. Which command lists all running Docker containers?

* [ ] docker list
* [ ] docker show
* [ ] docker ps
* [ ] docker display

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker ps
💡 `docker ps` shows **currently running containers**. Use `docker ps -a` to see all containers, including stopped ones.

</details>

---

### 26. Which command pulls an image from Docker Hub?

* [ ] docker get
* [ ] docker fetch
* [ ] docker pull
* [ ] docker download

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker pull
💡 `docker pull <image_name>` **downloads an image** from a remote registry such as Docker Hub to the local system.

</details>

---

### 27. How can you run a command inside an existing Docker container?

* [ ] docker exec
* [ ] docker attach
* [ ] docker run
* [ ] docker enter

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker exec
💡 `docker exec -it <container> <command>` **executes a command inside a running container** without starting a new one.

</details>

---

### 28. Which command is used to remove a Docker image?

* [ ] docker rmi
* [ ] docker remove
* [ ] docker del
* [ ] docker erase

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker rmi
💡 `docker rmi <image_name>` **removes one or more images** from the local Docker host.

</details>

---

### 29. What is Docker Compose?

* [ ] A scripting language for Docker
* [ ] A continuous integration tool for Docker
* [ ] A tool for defining and running multi-container Docker applications
* [ ] A Docker CLI plugin

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A tool for defining and running multi-container Docker applications
💡 Docker Compose allows you to **define multiple containers and their configurations** in a single YAML file and run them together.

</details>

---

### 30. Which of the following is the default registry used by Docker?

* [ ] Kubernetes Hub
* [ ] Container Store
* [ ] Docker Hub
* [ ] Image Hub

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Docker Hub
💡 Docker Hub is the **default public registry** for storing and distributing Docker images.

</details>

---

### 31. What is the primary purpose of the Docker Engine?

* [ ] To provide a graphical visualization of containers
* [ ] To build and run containers
* [ ] To manage databases inside containers
* [ ] To interface with Kubernetes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To build and run containers
💡 The Docker Engine is the **core runtime** that builds images, runs containers, and manages their lifecycle.

</details>

---

### 32. Which command logs you into Docker Hub from the CLI?

* [ ] docker login
* [ ] docker auth
* [ ] docker sign-in
* [ ] docker connect

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker login
💡 `docker login` authenticates your CLI session with a Docker registry like Docker Hub using your credentials.

</details>

---

### 33. What does the `-d` flag do in the `docker run` command?

* [ ] Deletes the container
* [ ] Displays detailed information
* [ ] Detaches the container (runs in the background)
* [ ] Downloads the latest image

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Detaches the container (runs in the background)
💡 `docker run -d` **runs the container in detached mode**, allowing it to run in the background.

</details>

---

### 34. How do you specify a Dockerfile other than the default "Dockerfile" during the build process?

* [ ] Use --filename option
* [ ] Use --source option
* [ ] Use --file option
* [ ] Use --dockerfile option

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use --file option
💡 `docker build -f <path/to/Dockerfile> .` allows you to **specify a custom Dockerfile name or location**.

</details>

---

### 35. In Docker, what is a bridge network?

* [ ] A public network accessible from outside
* [ ] A private network segment created for a specific container
* [ ] A way to connect multiple containers to the internet
* [ ] A network connecting containers to each other on the same host

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A network connecting containers to each other on the same host
💡 A bridge network **allows communication between containers on the same host** while isolating them from the external network.

</details>

---

### 36. How can you share storage volumes between containers?

* [ ] Using --volumes-from
* [ ] Using --share-storage
* [ ] Using --link
* [ ] Using --connect-volumes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Using --volumes-from
💡 `--volumes-from <container>` **mounts volumes from one container into another**, enabling shared persistent storage.

</details>

---

### 37. Which of the following is not a valid storage driver for Docker?

* [ ] aufs
* [ ] btrfs
* [ ] zfs
* [ ] ntfs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ntfs
💡 Docker supports **aufs, btrfs, zfs, overlay2**, but **NTFS is not a native Linux storage driver**.

</details>

---

### 38. What is the primary function of the `.dockerignore` file?

* [ ] To list all images to be pulled from Docker Hub
* [ ] To specify commands to run inside a container
* [ ] To prevent certain files and directories from being copied into an image
* [ ] To provide metadata about a Docker image

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To prevent certain files and directories from being copied into an image
💡 `.dockerignore` works like `.gitignore`, **reducing build context size** and excluding unnecessary files during `docker build`.

</details>

---

### 39. Which Docker command shows the history and intermediate layers of an image?

* [ ] docker inspect
* [ ] docker details
* [ ] docker history
* [ ] docker layers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker history
💡 `docker history <image>` lists **all intermediate layers and commands** used to build a Docker image.

</details>

---

### 40. In a `docker-compose.yml` file, what is the function of the `depends_on` key?

* [ ] Specifies the base images for services
* [ ] Specifies the build context for services
* [ ] Specifies the order in which services are started
* [ ] Specifies the network links between services

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Specifies the order in which services are started
💡 `depends_on` **ensures that certain services start before others**, managing startup dependencies between containers.

</details>

---
