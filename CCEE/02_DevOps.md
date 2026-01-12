> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 02

---

### 1. What is the primary purpose of Docker Swarm in a containerized environment?

* [ ] Image version management
* [ ] Container storage optimization
* [ ] Automated container build pipeline
* [ ] Multi-host container orchestration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Multi-host container orchestration
💡 Docker Swarm is a native clustering and orchestration tool in Docker that allows multiple Docker hosts to work together as a single virtual system, managing container deployment, scaling, and networking across nodes.

</details>

---

### 2. Which command is used to initialize a node as a Docker Swarm manager?

* [ ] docker swarm start
* [ ] docker swarm create
* [ ] docker swarm manager
* [ ] docker swarm init

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker swarm init
💡 `docker swarm init` initializes the current Docker node as a manager in a Swarm cluster and outputs a join token for worker nodes.

</details>

---

### 3. Which of the following is **not** a Docker network type?

* [ ] bridge
* [ ] host
* [ ] overlay
* [ ] transit

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** transit
💡 Docker supports bridge, host, overlay, and macvlan networks, but “transit” is not a valid Docker network type.

</details>

---

### 4. How can you view the logs of a running Docker container?

* [ ] docker show-logs CONTAINER_ID/NAME
* [ ] docker view CONTAINER_ID/NAME
* [ ] docker logs CONTAINER_ID/NAME
* [ ] docker inspect CONTAINER_ID/NAME

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker logs CONTAINER_ID/NAME
💡 The `docker logs` command retrieves stdout and stderr logs from a running or stopped container.

</details>

---

### 5. Which command creates a new Docker volume?

* [ ] docker create volume
* [ ] docker volume new
* [ ] docker new volume
* [ ] docker volume create

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker volume create
💡 Docker volumes are created with `docker volume create <VOLUME_NAME>` and are used to persist data outside container lifecycles.

</details>

---

### 6. How can you inspect the detailed configuration of a Docker network?

* [ ] docker network view NETWORK_NAME
* [ ] docker network show NETWORK_NAME
* [ ] docker network detail NETWORK_NAME
* [ ] docker network inspect NETWORK_NAME

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker network inspect NETWORK_NAME
💡 `docker network inspect` provides detailed information, including connected containers, IP addresses, and driver configuration.

</details>

---

### 7. Which command stops a running Docker container gracefully?

* [ ] docker kill CONTAINER_ID/NAME
* [ ] docker pause CONTAINER_ID/NAME
* [ ] docker halt CONTAINER_ID/NAME
* [ ] docker stop CONTAINER_ID/NAME

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker stop CONTAINER_ID/NAME
💡 `docker stop` sends a SIGTERM signal allowing the container to exit gracefully, whereas `docker kill` forcefully terminates it.

</details>

---

### 8. How can you list all Docker images available on your local machine?

* [ ] docker show images
* [ ] docker list images
* [ ] docker images
* [ ] docker img

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker images
💡 `docker images` lists all local images, including repository, tag, image ID, and size.

</details>

---

### 9. Which command removes a Docker volume?

* [ ] docker remove-volume VOLUME_NAME
* [ ] docker rmvol VOLUME_NAME
* [ ] docker volume rm VOLUME_NAME
* [ ] docker delete VOLUME_NAME

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker volume rm VOLUME_NAME
💡 `docker volume rm` deletes a specified volume. Volumes must not be in use by containers at the time of deletion.

</details>

---

### 10. How do you connect an existing container to a Docker network?

* [ ] docker connect NETWORK_NAME CONTAINER_NAME
* [ ] docker attach NETWORK_NAME CONTAINER_NAME
* [ ] docker link NETWORK_NAME CONTAINER_NAME
* [ ] docker network connect NETWORK_NAME CONTAINER_NAME

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker network connect NETWORK_NAME CONTAINER_NAME
💡 This command attaches a running container to an existing Docker network without restarting it.

</details>

---

### 11. How many types of volumes are available in Docker?

* [ ] 2
* [ ] 3
* [ ] 4
* [ ] 5

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 3
💡 Docker supports three types of volumes: **named volumes**, **anonymous volumes**, and **host bind mounts**.

</details>

---

### 12. Which command displays real-time resource statistics of a running container?

* [ ] Docker statistics
* [ ] Stats
* [ ] Docker statics
* [ ] Docker stats

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Docker stats
💡 `docker stats CONTAINER_ID/NAME` provides CPU, memory, network, and I/O statistics of containers in real time.

</details>

---

### 13. Which command pauses all processes in a running container?

* [ ] Docker hold
* [ ] Docker halt
* [ ] Docker wait
* [ ] Docker pause

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Docker pause
💡 `docker pause` suspends all processes in a container by sending the SIGSTOP signal.

</details>

---

### 14. Which command terminates processes inside a running container?

* [ ] Docker terminate
* [ ] Docker delete
* [ ] Docker kill
* [ ] Docker Suspend

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Docker kill
💡 `docker kill` sends a SIGKILL signal to a container, immediately stopping all its processes.

</details>

---

### 15. How can the Docker daemon be stopped on a Linux host?

* [ ] Service kill
* [ ] Docker kill
* [ ] service docker stop
* [ ] service docker Terminate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** service docker stop
💡 This stops the Docker daemon gracefully. `docker kill` affects containers, not the daemon process.

</details>

---

### 16. How many logging levels does Docker daemon support?

* [ ] 2
* [ ] 3
* [ ] 4
* [ ] 5

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 5
💡 Docker daemon logging supports: `debug`, `info`, `warn`, `error`, and `fatal` levels.

</details>

---

### 17. How many core components does Docker architecture consist of?

* [ ] 3
* [ ] 4
* [ ] 5
* [ ] 6

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 4
💡 Docker consists of **Docker Client**, **Docker Daemon**, **Docker Objects (Images, Containers, Volumes, Networks)**, and **Docker Registry**.

</details>

---

### 18. Which component is responsible for storing Docker images?

* [ ] Docker Client
* [ ] Docker Host
* [ ] Docker Image
* [ ] Docker Registry

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Docker Registry
💡 Docker Registry stores and distributes Docker images. Docker Hub is a popular public registry.

</details>

---

### 19. To remove unused Docker volumes and free up space, which command is appropriate?

* [ ] docker volume remove_all
* [ ] docker volume delete
* [ ] docker volume rm
* [ ] docker volume prune

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker volume prune
💡 `docker volume prune` removes all unused volumes in a single command, freeing disk space.

</details>

---

### 20. Which command lists all Docker networks on the host?

* [ ] docker ls
* [ ] docker network list
* [ ] docker network ls
* [ ] network ls

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** docker network ls
💡 `docker network ls` lists all networks, including bridge, host, overlay, and custom networks.

</details>

---

### 21. What is the basic operational unit of Kubernetes?

* [ ] Task
* [ ] Nodes
* [ ] Pod
* [ ] Container

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Pod
💡 In Kubernetes, a Pod is the smallest deployable unit that can contain one or more containers with shared storage, network, and specification for running applications.

</details>

---

### 22. Kubernetes cluster data is primarily stored in _______.

* [ ] Kubelet
* [ ] Kube-apiserver
* [ ] Etcd
* [ ] None of them

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Etcd
💡 Etcd is a distributed key-value store that stores all cluster state, configuration data, and metadata in Kubernetes.

</details>

---

### 23. Kubernetes version 1.8 introduced which key feature?

* [ ] Secrets
* [ ] Taints and Tolerations
* [ ] Federated Clusters
* [ ] Cluster-level Logging

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Taints and Tolerations
💡 Taints and tolerations allow scheduling flexibility by controlling which Pods can be scheduled on which nodes.

</details>

---

### 24. What is the latest stable version of Kubernetes as of now?

* [ ] 1.1
* [ ] 2.0
* [ ] 1.19
* [ ] 1.20

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1.20
💡 Kubernetes follows semantic versioning. Version 1.20 introduced improvements like stable CronJob APIs, structured logging, and extended beta features. *(Note: Version may change over time.)*

</details>

---

### 25. Which of the following are core Kubernetes objects?

* [ ] Pods
* [ ] Volumes
* [ ] Services
* [ ] All of them

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of them
💡 Core Kubernetes objects include Pods, Services, Volumes, Deployments, ReplicaSets, and Namespaces.

</details>

---

### 26. Kubernetes network proxy (kube-proxy) runs on which node(s)?

* [ ] Master Node
* [ ] Worker Node
* [ ] CIDR Node
* [ ] Both Master & Worker Nodes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Worker Node
💡 kube-proxy runs on each worker node, managing networking rules to allow communication between Pods and Services.

</details>

---

### 27. _______ runs on each node and ensures containers in a Pod are running.

* [ ] Etcd
* [ ] Pod
* [ ] Kubelet
* [ ] Scheduler

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Kubelet
💡 Kubelet is the agent running on each node, monitoring and managing containers according to PodSpecs from the API server.

</details>

---

### 28. Replication Controllers and Deployment Controllers are part of:

* [ ] Etcd manager
* [ ] Kubeadm
* [ ] API Controller Manager
* [ ] Master Controller Manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Master Controller Manager
💡 The Controller Manager runs controllers that regulate the state of the cluster, including ReplicationControllers, DeploymentControllers, and others.

</details>

---

### 29. Kubernetes is primarily written in which programming language?

* [ ] C++
* [ ] Python
* [ ] Go
* [ ] Java

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Go
💡 Kubernetes is developed in Go (Golang) for efficiency, concurrency, and portability across platforms.

</details>

---

### 30. Which of the following is a Kubernetes Controller?

* [ ] ReplicaSet
* [ ] Deployment
* [ ] Rolling Updates
* [ ] Both ReplicaSet & Deployment

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both ReplicaSet & Deployment
💡 Both ReplicaSet and Deployment are controllers responsible for maintaining desired state, scaling, and rolling updates of Pods.

</details>

---

### 31. Kubernetes is developed by:

* [ ] IBM
* [ ] Microsoft
* [ ] Google
* [ ] None of them

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Google
💡 Kubernetes was originally designed and developed by Google and later donated to the Cloud Native Computing Foundation (CNCF).

</details>

---

### 32. ________ are Kubernetes controllers.

* [ ] ReplicaSet
* [ ] Deployment
* [ ] Namespace
* [ ] Both ReplicaSet & Deployment

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both ReplicaSet & Deployment
💡 Controllers ensure that the cluster’s desired state matches the actual state by creating, updating, or deleting Pods as needed.

</details>

---

### 33. CronJobs in Kubernetes run in:

* [ ] UTC only
* [ ] GMT only
* [ ] Local time zone
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** UTC only
💡 Kubernetes CronJobs follow UTC time by default, irrespective of the node’s local timezone.

</details>

---

### 34. Kubernetes is a type of cluster management software.

* [ ] True
* [ ] False

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** True
💡 Kubernetes provides cluster orchestration for containerized applications, automating deployment, scaling, and management.

</details>

---

### 35. Which of the following are key features of Kubernetes?

* [ ] Containerized infrastructure
* [ ] Auto-scalable infrastructure
* [ ] Higher density of resource utilization
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Kubernetes enables container orchestration, automated scaling, high resource efficiency, and self-healing workloads.

</details>

---

### 36. Which of the following are components of the Kubernetes Master Node?

* [ ] Scheduler
* [ ] Controller Manager
* [ ] API Server & etcd
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Master node components include the API server, Controller Manager, Scheduler, and etcd for cluster management.

</details>

---

### 37. Kubernetes is:

* [ ] Portable platform
* [ ] Extensible platform
* [ ] Open-source platform
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Kubernetes is an open-source, portable, and extensible platform for managing containerized workloads across clusters.

</details>

---

### 38. Which of the following are Kubernetes Node Components?

* [ ] Docker
* [ ] Kubelet Service
* [ ] Kubernetes Proxy Service
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Node components include the container runtime (Docker), kubelet, and kube-proxy to manage Pods, networking, and resources.

</details>

---

### 39. Kubernetes images are key building blocks of containerized infrastructure.

* [ ] True
* [ ] False

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** True
💡 Images contain the application code, runtime, libraries, and dependencies required to run containers in Kubernetes Pods.

</details>

---

### 40. Kubernetes API currently supports _______ type of selectors.

* [ ] Set-based selectors
* [ ] Equality-based selectors
* [ ] Both Set-based & Equality-based selectors
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both Set-based & Equality-based selectors
💡 Kubernetes selectors allow selecting resources based on labels, supporting equality (`key=value`) and set-based operations (`in`, `notin`).

</details>

---
