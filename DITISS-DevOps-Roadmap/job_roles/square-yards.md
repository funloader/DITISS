## Aptitude & Technical Test

### 1. What is Cloud Spanner in Google Cloud Platform?

* [ ] Data warehouse service
* [ ] Document database service
* [x] Relational database service
* [ ] Object storage service

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Relational database service
💡 Cloud Spanner is a globally distributed relational database service that combines horizontal scalability with strong consistency.

</details>

---

### 2. What is Google Cloud Identity and Access Management (IAM) used for?

* [ ] Data analysis
* [ ] Serverless computing
* [x] Managing user permissions
* [ ] Object storage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Managing user permissions
💡 IAM controls who can access which resources and what actions they can perform in GCP.

</details>

---

### 3. Google App Engine comes under which kind of service?

* [x] Compute service
* [ ] Networking service
* [ ] Storage service
* [ ] Big data service

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Compute service
💡 App Engine is a Platform-as-a-Service (PaaS) offering used to run applications without managing infrastructure.

</details>

---

### 4. Which GCP service helps create a secure environment for application deployments?

* [ ] Compute Engine
* [ ] Google App Engine
* [ ] Cloud Load Balancing
* [x] Virtual Private Cloud

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtual Private Cloud
💡 VPC provides network isolation, firewall rules, and private IP ranges for secure deployments.

</details>

---

### 5. In Docker, your image size is very large. What is the BEST practice to reduce it?

* [ ] Use multiple RUN commands
* [x] Use a minimal base image like alpine
* [ ] Add more layers
* [ ] Store logs inside image

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use a minimal base image like alpine
💡 Minimal base images significantly reduce final image size and improve security.

</details>

---

### 6. CDN comes under which kind of service?

* [ ] Compute service
* [x] Networking service
* [ ] Storage service
* [ ] Big data service

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Networking service
💡 CDN improves content delivery performance by caching data closer to users.

</details>

---

### 7. You pushed code to Git, but the CI pipeline in Jenkins didn’t trigger. What is the most likely reason?

* [ ] Jenkins server is too fast
* [x] Webhook is not configured properly
* [ ] Git repository is public
* [ ] Docker is not installed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Webhook is not configured properly
💡 Jenkins relies on webhooks or polling to detect changes in repositories.

</details>

---

### 8. Which of the following is the default Docker network driver?

* [x] Bridge
* [ ] Host
* [ ] Overlay
* [ ] ipvlan

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Bridge
💡 Bridge is the default network driver for standalone Docker containers.

</details>

---

### 9. Which command shows all open files and network sockets?

* [ ] netstat -tulnp
* [x] lsof
* [ ] ps aux
* [ ] df -h

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** lsof
💡 lsof (List Open Files) shows files and network sockets opened by processes.

</details>

---

### 10. What does the letter "A" stand for in the CIA triad of cybersecurity?

* [ ] Authorization
* [ ] Accessibility
* [ ] Authentication
* [x] Availability

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Availability
💡 CIA stands for Confidentiality, Integrity, and Availability.

</details>

---

### 11. Which type of encryption uses the same key for both encryption and decryption?

* [x] Symmetric encryption
* [ ] Asymmetric encryption
* [ ] Hybrid encryption
* [ ] Public-key encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Symmetric encryption
💡 Symmetric encryption uses one shared key for both encryption and decryption.

</details>

---

### 12. The purpose of an SSL certificate is to ____.

* [x] Authenticate the identity of the server and encrypt data during transmission
* [ ] Authenticate the identity of the client and encrypt data during transmission
* [ ] Identify potential cyber threats in the network
* [ ] Filter and block malicious websites

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticate the identity of the server and encrypt data during transmission
💡 SSL/TLS certificates secure communication and verify server identity.

</details>

---

### 13. A filesystem shows 100% usage in df -h, but du -sh / shows much less usage. What is the MOST likely reason?

* [ ] Too many small files
* [x] Deleted file still held open by a process
* [ ] Root Filesystem Full
* [ ] Swap partition full
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Deleted file still held open by a process
💡 The space remains allocated until the process releases the file descriptor.

</details>

---

### 14. Load average is 8.0 on a 4-core system. What does this indicate?

* [ ] System idle
* [ ] CPU usage 80%
* [x] 4 processes waiting for CPU
* [ ] Memory leak

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 4 processes waiting for CPU
💡 Load average higher than CPU cores means processes are waiting for CPU time.

</details>

---

### 15. chmod 4755 file means:

* [ ] SGID
* [ ] Sticky bit
* [x] SUID
* [ ] Immutable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SUID
💡 4 in 4755 sets the Set User ID (SUID) bit.

</details>

---

### 16. What is the purpose of "Facts" in Ansible?

* [ ] They are hard-coded variables in the ansible.cfg file.
* [x] They are system properties (IP address, OS version, etc.) gathered from the remote node.
* [ ] They are the logs generated after a playbook runs.
* [ ] None of the above
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** They are system properties gathered from the remote node.
💡 Ansible facts are automatically collected system information like OS, IP, memory, etc., used in playbooks.

</details>

---

### 17. In Kubernetes, Taint prevents scheduling unless?

* [ ] NodeSelector
* [ ] Affinity
* [x] Toleration
* [ ] PDB

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Toleration
💡 A Pod must have a matching toleration to be scheduled on a tainted node.

</details>

---

### 18. Your company is migrating a monolithic app to GCP with minimal refactoring but future scalability. What is the best approach?

* [ ] Deploy frontend/backend on single GKE node and keep DB on-prem via VPN
* [x] Containerize frontend/backend, deploy to Cloud Run, migrate DB to Cloud SQL
* [ ] Migrate entire server as single VM to Compute Engine
* [ ] Rebuild into event-driven microservices first

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Containerize and deploy to Cloud Run with Cloud SQL
💡 Provides minimal refactoring now while enabling automatic scaling and managed database services.

</details>

---

### 19. Best GCP service for unpredictable traffic with minimal operational overhead?

* [ ] Compute Engine managed instance group
* [ ] Cloud Functions via Pub/Sub
* [x] App Engine Standard environment
* [ ] Cloud Run on GKE Autopilot

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** App Engine Standard environment
💡 Fully managed PaaS with automatic scaling based on HTTP traffic.

</details>

---

### 20. Prometheus server crashes frequently due to high memory usage. BEST first step?

* [ ] Increase CPU
* [x] Reduce scrape interval
* [ ] Increase retention time
* [ ] Enable debug logs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reduce scrape interval
💡 Lowering scrape frequency reduces time-series data ingestion and memory consumption.

</details>

---

### 21. Main purpose of a Pull Request (PR) in GitHub?

* [x] Propose changes from one branch to be reviewed and merged
* [ ] Permanently delete a branch
* [ ] Automatically deploy to production
* [ ] Fork repository

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Propose changes to be reviewed and merged
💡 PRs enable collaboration, code review, and discussion before merging changes.

</details>

---

### 22. Best AWS VPC design for microservices exposing public APIs while isolating databases?

* [ ] Microservices in one VPC, DB in another with unrestricted peering
* [x] Public services in public subnets, databases in private subnets with NAT
* [ ] All services in one public subnet
* [ ] Only private subnets accessed via VPN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Public subnets for APIs, private subnets for databases
💡 This ensures public access to APIs while keeping databases isolated from direct internet exposure.

</details>

---

### 23. Best IaC approach for AWS multi-account deployments?

* [ ] Single Terraform state for all accounts
* [x] Separate Terraform workspaces/state files with reusable modules
* [ ] Independent CloudFormation stacks only
* [ ] Manual Ansible ad-hoc commands

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Separate state files/workspaces with reusable modules
💡 Provides isolation, reproducibility, and modular infrastructure management.

</details>

---

### 24. SQL injection attempts observed but DB safe. Which control blocked it?

* [ ] Reverse proxy TCP termination
* [ ] IPS inline mode
* [x] WAF applying application-layer rules
* [ ] Stateful firewall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** WAF applying application-layer rules
💡 WAF inspects HTTP payloads and blocks SQL injection patterns.

</details>

---

### 25. iptables filters only inbound traffic and allows all outbound. Main security risk?

* [ ] QoS cannot be enforced
* [ ] VPN tunnels cannot be established
* [ ] Increased inbound SYN flood risk
* [x] None of the Above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** None of the Above
💡 The real risk is data exfiltration, which is not listed in the options.

</details>

---

### 26. Handling 20x traffic spike on GCP with minimal long-term cost?

* [ ] Move to Cloud Functions
* [x] Configure autoscaling and pre-scale managed instance group
* [ ] Single powerful VM + CDN
* [ ] Disable autoscaling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configure autoscaling with pre-scaling
💡 Autoscaling ensures capacity during spike and scales down after promotion.

</details>

---

### 27. GCP compliance: CMEK + tight access + audit visibility. Best solution?

* [x] Use CMEK with Cloud KMS + IAM least privilege + Data Access logs
* [ ] Only VPC Service Controls
* [ ] Default encryption + project audit logs
* [ ] Move to BigQuery only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CMEK + IAM + Data Access logs
💡 Meets encryption and audit requirements with minimal pipeline changes.

</details>

---

### 28. Most cost-effective Compute Engine setup for batch job tolerating preemption?

* [ ] Migrate to Cloud Functions
* [x] Mix of regular and preemptible VMs with checkpointing
* [ ] Standard VMs only
* [ ] Only preemptible VMs with manual restart

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mix of regular and preemptible VMs with checkpointing
💡 Balances cost savings and reliability.

</details>

---

### 29. Reduce SSH brute-force risk after jump host compromise?

* [ ] Move SSH to high port
* [x] Use key-based SSH and disable password logins
* [ ] Port knocking
* [ ] Move jump host to DMZ

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use key-based SSH and disable passwords
💡 Eliminates password-based brute-force attacks.

</details>

---

### 30. Temporary protection against zero-day API exploit?

* [ ] Rate limiting
* [x] Add custom virtual patches on WAF
* [ ] Block all outbound traffic
* [ ] Force VPN access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Add custom virtual patches on WAF
💡 WAF rules can block exploit patterns until official patch is released.

</details>

---

### 31. How do you apply any port allow or deny rule to Compute Engine in GCP?

* [ ] Firewall Policy
* [ ] Security Groups
* [x] Target Tags
* [ ] Labels

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Target Tags
💡 GCP firewall rules are applied to VM instances using network tags (target tags).

</details>

---

### 32. Unusual outbound DNS traffic with large TXT responses. Best control to prevent data exfiltration?

* [ ] Switch DNS to TCP
* [ ] Move server behind reverse proxy
* [x] Enforce DNS query and response inspection with IDS/IPS
* [ ] Block all outbound DNS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enforce DNS inspection with IDS/IPS
💡 DNS inspection helps detect and block tunneling or data exfiltration attempts.

</details>

---

### 33. Best way to implement zero-trust model for internal GCP app?

* [ ] Move app to Cloud Run
* [x] Use Identity-Aware Proxy (IAP) with BeyondCorp Enterprise
* [ ] Implement custom authentication inside app
* [ ] Expose publicly with IP allowlists

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use IAP with BeyondCorp
💡 IAP enforces identity- and device-based access with centralized logging.

</details>

---

### 34. After enabling aggressive IPS signatures, web app issues occur. Most likely reason?

* [ ] DMZ routing table corrupted
* [ ] IPS under DDoS
* [ ] Firewall dropping SYN packets
* [x] False positives blocking legitimate traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** False positives blocking legitimate traffic
💡 Aggressive IPS signatures may incorrectly block valid application traffic.

</details>

---

### 35. Internal clients making small periodic HTTPS connections to rare foreign ASN. Best action?

* [x] Use SSL decryption and packet analysis
* [ ] Move clients to restricted VLAN
* [ ] Increase IPS severity to critical
* [ ] Block all foreign IPs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SSL decryption and packet analysis
💡 Helps detect command-and-control or covert data exfiltration over HTTPS.

</details>

---

### 36. Purpose of subnet mask 255.255.255.0?

* [ ] Indicate DNS server
* [ ] Specify default gateway
* [ ] Encrypt traffic
* [x] Define network and host portions of IP address

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Define network and host portion
💡 Subnet mask determines how IP addresses are divided between network and hosts.

</details>

---

### 37. Why separate management, storage, and data networks in data centers?

* [ ] Required by vendors
* [ ] Reduce number of switches
* [ ] Reuse same IP addresses
* [x] Isolate traffic for security, performance, troubleshooting

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Traffic isolation improves security and performance
💡 Segmentation prevents interference and enhances fault isolation.

</details>

---

### 38. Best Linux permission for sensitive file /etc/secret.conf?

* [ ] -rw-r----- owned by root:devops
* [ ] -rw-rw-rw-
* [ ] -rwxr-xr-x owned by root:root
* [x] -rw------- owned by root:root

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** -rw------- owned by root:root
💡 Only root can read/write, providing maximum restriction.

</details>

---

### 39. What does $? represent in Bash?

* [x] Exit status of the last executed command
* [ ] Current user ID
* [ ] Background job ID
* [ ] Last argument of previous command

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Exit status of last command
💡 `$?` stores the return code (0 = success, non-zero = failure).

</details>

---

### 40. What happens if MTU mismatch exists?

* [ ] Faster throughput
* [x] Fragmentation or packet drops
* [ ] TCP reset
* [ ] DNS failure

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Fragmentation or packet drops
💡 MTU mismatch can cause dropped packets or excessive fragmentation.

</details>

---

### 41. Which Kubernetes component enforces pod isolation?

* [ ] kubelet
* [ ] CRI
* [ ] CNI
* [x] Namespaces + cgroups

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Namespaces + cgroups
💡 Linux namespaces isolate resources; cgroups limit resource usage.

</details>

---

### 42. Which symbol represents a user’s home directory in Linux?

* [ ] :
* [x] ~
* [ ] $
* [ ] /

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ~
💡 The tilde (~) expands to the current user’s home directory.

</details>

---

### 43. Users experience intermittent logouts after enabling cross-zone load balancing on ALB. Best fix?

* [ ] Increase ALB idle timeout
* [ ] Disable cross-zone load balancing
* [x] Enable ALB sticky sessions
* [ ] Use NLB instead

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enable sticky sessions
💡 Session affinity ensures users consistently hit the same backend.

</details>

---

### 44. Best way to enforce prefix-based least-privilege access in S3?

* [ ] Enable Object Lock
* [ ] Grant s3:* on bucket
* [ ] Public read + encryption keys
* [x] IAM policy with s3:prefix condition and limit GetObject to appX/*

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IAM policy with prefix condition
💡 Limits access to specific object prefixes within the same bucket.

</details>

---

### 45. Inspect scheduling issues for Pod my-pod?

* [ ] kubectl get events --field-selector involvedObject.name=my-pod
* [ ] kubectl logs my-pod
* [x] kubectl describe pod my-pod
* [ ] kubectl get pod my-pod -o wide

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** kubectl describe pod my-pod
💡 Shows events, scheduling failures, and detailed status.

</details>

---

### 46. Your Pods are not starting, and you suspect an issue with the default scheduler decisions. Which kubectl command best helps you inspect the current events and scheduling-related issues for a specific Pod named my-pod in the default namespace?

* [ ] kubectl exec -it my-pod -- /bin/sh
* [x] kubectl exec -it my-pod -c sidecar -- /bin/sh
* [ ] kubectl run -it sidecar --image=debug-image -- /bin/sh
* [ ] kubectl attach -it my-pod -c sidecar

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** kubectl exec -it my-pod -c sidecar -- /bin/sh
💡 The -c flag targets a specific container inside the pod.

</details>

---

### 47. You are debugging network connectivity from inside a Pod named api-pod and want to verify DNS resolution and outbound HTTP access using kubectl without manually starting a separate debug Pod manifest. Which kubectl command is most suitable?

* [ ] kubectl run -it net-debug --image=busybox --rm --restart=Never -- nslookup kubernetes.default
* [ ] kubectl proxy
* [ ] kubectl port-forward pod/api-pod 8080:80
* [x] kubectl exec -it api-pod -- nslookup kubernetes.default

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** kubectl exec -it api-pod -- nslookup kubernetes.default
💡 Executes command directly inside the running Pod.

</details>

---

### 48. You want to temporarily scale down a Deployment named worker to zero replicas for maintenance, but you also want to remember its previous replica count for later restoration. Which kubectl command combination uses built-in features to make this easier?

* [ ] kubectl get deployment worker -o yaml > backup.yaml && kubectl scale deployment worker --replicas=0
* [ ] kubectl annotate deployment worker previous-replicas=3 && kubectl scale deployment worker --replicas=0
* [ ] kubectl scale deployment worker --replicas=0 && kubectl rollout history deployment/worker
* [x] kubectl scale deployment worker --current-replicas=3 --replicas=0

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** kubectl scale deployment worker --current-replicas=3 --replicas=0
💡 Ensures scaling happens only if current replica count matches expected value.

</details>

---

### 49. You edited a Terraform variable default value, but on the next apply Terraform still uses the old value from a previous run. Which command lets you see exactly what input values Terraform will use, including those coming from tfvars files and the environment?

* [ ] terraform plan -var
* [x] terraform console
* [ ] terraform show
* [ ] terraform plan -input=false -refresh=false

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** terraform console
💡 Allows inspection of variable values from tfvars, environment, and defaults.

</details>

---

### 50. An administrator configures sudo with the following line: aliceALL=(root)NOPASSWD:/usr/bin/rsync∗. What subtle security issue does this introduce?

* [ ] The NOPASSWD option prevents logging of Alice’s sudo commands, making auditing impossible.
* [x] Alice can use rsync’s options to copy or overwrite arbitrary root-owned files, effectively gaining root-level file access.
* [ ] The line only allows Alice to sync files within her home directory, so there is no security issue
* [ ] Alice can run rsync as root, but only with read-only permissions enforced by sudo.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Alice can use rsync’s options to copy or overwrite arbitrary root-owned files, effectively gaining root-level file access.
💡 rsync options can be abused to gain effective root-level file access.

</details>

---

### 51. You have a stopped container named "web" and want to create a new image from its current filesystem state. Which Podman command best achieves this?

* [ ] podman save web -o mywebimage.tar
* [ ] podman export web -o mywebimage.tar
* [x] podman commit web mywebimage:latest
* [ ] podman build -t mywebimage:latest web

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** podman commit web mywebimage:latest
💡 commit creates a new image from the container’s current filesystem state.

</details>

---
