> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 03

---

### 1. In a Kubernetes cluster, which network topology best describes how nodes and pods communicate within the cluster?

* [ ] Mesh Topology
* [ ] Ring Topology
* [ ] Star (Hub-and-Spoke) Topology
* [ ] Bus Topology

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Star (Hub-and-Spoke) Topology
💡 Kubernetes uses a hub-and-spoke-like architecture where the control plane (API server, controller manager, scheduler) acts as the hub and worker nodes/pods are spokes. Communication between pods and services is centrally orchestrated via the control plane.

</details>

---

### 2. Which Kubernetes component continuously monitors the cluster to ensure the desired state is maintained?

* [ ] Kubelet
* [ ] Kube-proxy
* [ ] Kube-scheduler
* [ ] Kube-controller-manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Kube-controller-manager
💡 The controller manager runs controllers that watch the cluster state and take corrective actions to match the desired state specified in manifests (e.g., ReplicaSets ensuring pods are running).

</details>

---

### 3. What is the smallest deployable unit in Kubernetes that can contain one or more containers?

* [ ] Container
* [ ] Node
* [ ] Pod
* [ ] Deployment

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Pod
💡 A Pod is the minimal unit in Kubernetes for deployment, encapsulating one or more containers that share storage, network, and specifications.

</details>

---

### 4. If you want to expose a Kubernetes application externally using a cloud provider’s load balancer, which service type should you use?

* [ ] ClusterIP
* [ ] NodePort
* [ ] LoadBalancer
* [ ] ExternalName

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** LoadBalancer
💡 LoadBalancer service type automatically provisions an external load balancer (from cloud providers) and assigns a public IP to expose the service.

</details>

---

### 5. Which function does kube-proxy perform in a Kubernetes cluster?

* [ ] Schedule pods to nodes
* [ ] Expose services using Ingress
* [ ] Manage container lifecycle
* [ ] Handle network routing and load balancing for services

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Handle network routing and load balancing for services
💡 Kube-proxy runs on each node to maintain network rules, enabling communication to services and implementing basic load balancing for service endpoints.

</details>

---

### 6. Which Kubernetes object ensures that a specific number of pod replicas are running at all times?

* [ ] ReplicaSet
* [ ] Deployment
* [ ] DaemonSet
* [ ] StatefulSet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ReplicaSet
💡 ReplicaSet maintains a defined number of pod replicas; Deployments use ReplicaSets to manage updates and scaling.

</details>

---

### 7. What is the primary purpose of Kubernetes?

* [ ] Building container images
* [ ] Monitoring system metrics
* [ ] Orchestrating containerized applications
* [ ] Virtualizing physical servers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Orchestrating containerized applications
💡 Kubernetes automates deployment, scaling, and management of containerized applications across clusters of nodes.

</details>

---

### 8. Which Kubernetes component runs containers on each node and communicates with the control plane?

* [ ] kube-apiserver
* [ ] kubelet
* [ ] kube-proxy
* [ ] etcd

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** kubelet
💡 Kubelet runs on each node, ensuring containers described in Pods are running and reporting node status to the API server.

</details>

---

### 9. What is the default service type in Kubernetes if no type is explicitly specified?

* [ ] ClusterIP
* [ ] NodePort
* [ ] LoadBalancer
* [ ] ExternalName

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ClusterIP
💡 ClusterIP exposes the service only internally within the cluster. It is the default service type in Kubernetes.

</details>

---

### 10. Which built-in Kubernetes component handles the lifecycle of containers on nodes?

* [ ] Kubelet
* [ ] Scheduler
* [ ] API Server
* [ ] Controller Manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Kubelet
💡 Kubelet ensures containers are running as specified in Pod specs, managing container start, stop, and health checks.

</details>

---

### 11. Which Kubernetes object allows you to store sensitive data such as passwords or API keys?

* [ ] ConfigMap
* [ ] Secret
* [ ] ServiceAccount
* [ ] Namespace

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Secret
💡 Secrets store sensitive information in base64-encoded form, which can be mounted as files or environment variables inside pods.

</details>

---

### 12. Which Kubernetes resource is primarily responsible for defining networking access for pods?

* [ ] Service
* [ ] Ingress
* [ ] Pod
* [ ] Namespace

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Service
💡 Services define stable endpoints, enable pod-to-pod communication, and can expose pods internally or externally. Ingress manages HTTP/HTTPS routing.

</details>

---

### 13. Which Kubernetes controller is typically used to manage stateless applications?

* [ ] Deployment
* [ ] StatefulSet
* [ ] ReplicaSet
* [ ] CronJob

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Deployment
💡 Deployments manage stateless applications by creating and updating ReplicaSets, handling rolling updates and scaling.

</details>

---

### 14. Which Kubernetes object handles persistent storage provisioning for pods?

* [ ] Persistent Volume (PV)
* [ ] StatefulSet
* [ ] Deployment
* [ ] Secret

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Persistent Volume (PV)
💡 PVs provide persistent storage independent of pod lifecycle; pods access PVs via Persistent Volume Claims (PVCs).

</details>

---

### 15. What is the main purpose of a Namespace in Kubernetes?

* [ ] A way to manage and isolate resources
* [ ] A method to scale resources
* [ ] A tool to track resource usage
* [ ] A network protocol for communication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A way to manage and isolate resources
💡 Namespaces partition cluster resources, allowing multiple teams or projects to coexist without conflict.

</details>

---

### 16. Which component serves the Kubernetes API and acts as the gateway to the cluster?

* [ ] Kubelet
* [ ] API Server
* [ ] Controller Manager
* [ ] Scheduler

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** API Server
💡 The API Server handles all REST requests, validates, authenticates, and persists the state of objects in etcd.

</details>

---

### 17. Which command applies changes defined in a YAML or JSON manifest to a Kubernetes cluster?

* [ ] kubectl apply
* [ ] kubectl run
* [ ] kubectl create
* [ ] kubectl deploy

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** kubectl apply
💡 `kubectl apply` creates or updates resources declaratively from a manifest file.

</details>

---

### 18. Which Kubernetes resource allows you to store non-sensitive configuration data for pods and containers?

* [ ] ConfigMap
* [ ] Secret
* [ ] Persistent Volume
* [ ] Pod

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ConfigMap
💡 ConfigMaps store key-value pairs or configuration files that can be injected into pods as environment variables or volumes.

</details>

---

### 19. What does the `kubectl get` command do in Kubernetes?

* [ ] Fetches the status of resources
* [ ] Creates new resources
* [ ] Deletes resources
* [ ] Scales the application

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Fetches the status of resources
💡 `kubectl get` lists resources, showing their current state, replicas, and other details.

</details>

---

### 20. What is the purpose of a Kubernetes Service?

* [ ] To manage storage in the cluster
* [ ] To provide load balancing and access to pods
* [ ] To define and manage pods
* [ ] To deploy containers inside pods

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To provide load balancing and access to pods
💡 Services create a stable network endpoint for pods, abstracting underlying pod IPs and providing load balancing across them.

</details>

---

### 21. Which Terraform command is used to initialize a new or existing Terraform configuration directory?

* [ ] terraform validate
* [ ] terraform apply
* [ ] terraform init
* [ ] terraform plan

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** terraform init
💡 `terraform init` initializes the working directory, downloads required providers, and sets up backend configuration. This must be run before any plan or apply operations.

</details>

---

### 22. Considering ease of coding Infrastructure as Code (IaC), which is generally regarded as easier to write for multi-cloud deployments?

* [ ] Terraform
* [ ] CloudFormation
* [ ] Both 1 and 2
* [ ] None of these

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Terraform
💡 Terraform uses HCL, a declarative language, and supports multiple cloud providers, making it easier to code cross-cloud IaC compared to AWS-specific CloudFormation.

</details>

---

### 23. Which types of files does Terraform process to define infrastructure?

* [ ] .tf and .tf.json
* [ ] .tf only
* [ ] .tm only
* [ ] All text files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** .tf and .tf.json
💡 Terraform processes `.tf` (HCL) and `.tf.json` (JSON) configuration files to define infrastructure resources.

</details>

---

### 24. In Terraform, which files are processed last when multiple configuration files exist?

* [ ] xml
* [ ] git
* [ ] override
* [ ] json

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** override
💡 Terraform processes override files last, allowing them to modify or supersede values defined in standard `.tf` files.

</details>

---

### 25. Terraform is primarily classified as which type of language?

* [ ] Objective
* [ ] Declarative
* [ ] Descriptive
* [ ] Functional

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Declarative
💡 Terraform uses a declarative approach: users define the desired state of infrastructure, and Terraform determines how to reach that state.

</details>

---

### 26. Terraform operates based on a master-less and agent-less architecture.

* [ ] True
* [ ] False

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** True
💡 Terraform does not require a central master or agents on nodes; it interacts directly with cloud provider APIs.

</details>

---

### 27. Which Terraform command deletes all resources managed by a configuration?

* [ ] terraform undo
* [ ] terraform remove
* [ ] terraform destroy
* [ ] terraform delete

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** terraform destroy
💡 `terraform destroy` safely deletes all infrastructure resources that were created via Terraform configuration.

</details>

---

### 28. When was Terraform first released?

* [ ] July 28, 2014
* [ ] May 16, 2011
* [ ] March 15, 2010
* [ ] July 24, 2013

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** July 28, 2014
💡 Terraform was developed by HashiCorp and officially released on July 28, 2014.

</details>

---

### 29. Terraform is primarily categorized as which of the following?

* [ ] IAC (Infrastructure as Code)
* [ ] PaaS
* [ ] IaaS
* [ ] SaaS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IAC (Infrastructure as Code)
💡 Terraform allows infrastructure to be defined, provisioned, and managed via code.

</details>

---

### 30. Which organization developed Terraform?

* [ ] Google
* [ ] Amazon
* [ ] HashiCorp
* [ ] Adobe

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HashiCorp
💡 HashiCorp is the company behind Terraform, Vault, Consul, and other DevOps tools.

</details>

---

### 31. Terraform is written in which programming language?

* [ ] Go
* [ ] Angular
* [ ] C
* [ ] Java

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Go
💡 Terraform is implemented in Go, providing portability and efficient compilation for multi-platform deployment.

</details>

---

### 32. Under which license is Terraform released?

* [ ] Open-source
* [ ] Mozilla Public License v2.0
* [ ] Apache License 2.0
* [ ] GPL

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mozilla Public License v2.0
💡 Terraform is open-source and licensed under MPL v2.0, allowing free use and modification with attribution.

</details>

---

### 33. In Terraform, what is the purpose of a `data` block?

* [ ] To define input variables for a Terraform module
* [ ] To create reusable modules
* [ ] To query and fetch information from remote systems or APIs
* [ ] To specify dependencies between resources

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To query and fetch information from remote systems or APIs
💡 Data blocks allow Terraform to read existing infrastructure or external information without creating resources.

</details>

---

### 34. Which language is used to write Terraform configuration files?

* [ ] YAML
* [ ] JSON
* [ ] HCL (HashiCorp Configuration Language)
* [ ] XML

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HCL (HashiCorp Configuration Language)
💡 HCL is a declarative, human-readable language designed for Terraform configurations.

</details>

---

### 35. Which command in Terraform generates an execution plan showing what actions Terraform will perform?

* [ ] terraform apply
* [ ] terraform validate
* [ ] terraform plan
* [ ] terraform init

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** terraform plan
💡 `terraform plan` previews changes without making modifications, helping prevent unintended infrastructure changes.

</details>

---

### 36. Which command applies the Terraform configuration to create or update resources?

* [ ] terraform update
* [ ] terraform apply
* [ ] terraform execute
* [ ] terraform deploy

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** terraform apply
💡 `terraform apply` provisions or modifies resources to match the desired state defined in configuration files.

</details>

---

### 37. What is the purpose of the `terraform.tfstate` file?

* [ ] Stores sensitive information like API keys
* [ ] Tracks the current state of infrastructure
* [ ] Log file for Terraform commands
* [ ] Contains the configuration files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Tracks the current state of infrastructure
💡 Terraform uses the state file to map configuration resources to real-world infrastructure, enabling incremental updates.

</details>

---

### 38. What does a Terraform provider define?

* [ ] Configuration settings for a specific infrastructure type
* [ ] Execution order of resources
* [ ] A way to organize modules
* [ ] Authentication details for Terraform Cloud

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configuration settings for a specific infrastructure type
💡 Providers allow Terraform to interact with cloud platforms, SaaS providers, or other APIs.

</details>

---

### 39. Which command is used to destroy Terraform-managed infrastructure?

* [ ] terraform clean
* [ ] terraform destroy
* [ ] terraform delete
* [ ] terraform remove

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** terraform destroy
💡 `terraform destroy` safely deletes all resources created by Terraform in the current state.

</details>

---

### 40. How can sensitive information in Terraform configurations be secured?

* [ ] Using the `terraform secrets` command
* [ ] Through the `secrets` block
* [ ] By encrypting the Terraform state file
* [ ] By storing secrets in `terraform.tfvars`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** By encrypting the Terraform state file
💡 Terraform recommends encrypting remote state storage (e.g., S3 with KMS) to secure sensitive data. Sensitive variables can also be marked as `sensitive = true`.

</details>

---
