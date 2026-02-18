## Aptitude & Technical Test

### 1. What is Cloud Spanner in Google Cloud Platform?

* [ ] Data warehouse service
* [ ] Document database service
* [ ] Relational database service
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
* [ ] Managing user permissions
* [ ] Object storage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Managing user permissions
💡 IAM controls who can access which resources and what actions they can perform in GCP.

</details>

---

### 3. Google App Engine comes under which kind of service?

* [ ] Compute service
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
* [ ] Virtual Private Cloud

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtual Private Cloud
💡 VPC provides network isolation, firewall rules, and private IP ranges for secure deployments.

</details>

---

### 5. In Docker, your image size is very large. What is the BEST practice to reduce it?

* [ ] Use multiple RUN commands
* [ ] Use a minimal base image like alpine
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
* [ ] Networking service
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
* [ ] Webhook is not configured properly
* [ ] Git repository is public
* [ ] Docker is not installed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Webhook is not configured properly
💡 Jenkins relies on webhooks or polling to detect changes in repositories.

</details>

---

### 8. Which of the following is the default Docker network driver?

* [ ] Bridge
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
* [ ] lsof
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
* [ ] Availability

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Availability
💡 CIA stands for Confidentiality, Integrity, and Availability.

</details>

---

### 11. Which type of encryption uses the same key for both encryption and decryption?

* [ ] Symmetric encryption
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

* [ ] Authenticate the identity of the server and encrypt data during transmission
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
* [ ] Deleted file still held open by a process
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
* [ ] 4 processes waiting for CPU
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
* [ ] SUID
* [ ] Immutable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SUID
💡 4 in 4755 sets the Set User ID (SUID) bit.

</details>

---

### 16. What is the purpose of "Facts" in Ansible?

* [ ] They are hard-coded variables in the ansible.cfg file.
* [ ] They are system properties (IP address, OS version, etc.) gathered from the remote node.
* [ ] They are the logs generated after a playbook runs.
* [ ] None of the above
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** They are system properties gathered from the remote node.
💡 Ansible facts are automatically collected system information like OS, IP, memory, etc., used in playbooks.

</details>

---

### 17. In K8s,  Taint prevents scheduling unless?

* [ ] NodeSelector
* [ ] Affinity
* [ ] Toleration
* [ ] PDB

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Toleration
💡 A Pod must have a matching toleration to be scheduled on a tainted node.

</details>

---

### 18. Your company is migrating a monolithic on‑premises web application to Google Cloud. The app consists of a frontend, a backend API, and a PostgreSQL database, all running on a single large server. Management wants minimal refactoring now but expects traffic to grow significantly over the next 12 months. They also want to avoid major downtime during migration. Which approach best balances quick lift‑and‑shift with a clear path to future scalability on GCP?

* [ ] Deploy the frontend and backend onto a single GKE cluster node and keep the database on‑premises connected via Cloud VPN indefinitely.
* [ ] Containerize the frontend and backend, deploy to Cloud Run, and migrate the database to Cloud SQL for PostgreSQL, using a short cutover window.
* [ ] Migrate the entire server as a single VM to Compute Engine using Migrate to Virtual Machines, keeping all components tightly coupled on one instance.
* [ ] Rebuild the application into fully event‑driven microservices using Cloud Functions and Pub/Sub before migration.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Containerize the frontend and backend, deploy to Cloud Run, and migrate the database to Cloud SQL for PostgreSQL, using a short cutover window.
💡 Provides minimal refactoring now while enabling automatic scaling and managed database services.

</details>

---

### 19. Your startup is launching a web application on Google Cloud that needs to handle unpredictable traffic spikes during marketing campaigns. You want minimal operational overhead and automatic scaling of instances based on incoming HTTP requests. Which GCP service is the best fit for hosting this application backend?

* [ ] Compute Engine managed instance group
* [ ] Cloud Functions triggered by Pub/Sub messages
* [ ] App Engine Standard environment
* [ ] Cloud Run on GKE Autopilot

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** App Engine Standard environment
💡 Fully managed PaaS with automatic scaling based on HTTP traffic.

</details>

---

### 20. Prometheus server crashes frequently due to high memory usage. What is the BEST first step?

* [ ] Increase CPU
* [ ] Reduce scrape interval
* [ ] Increase retention time
* [ ] Enable debug logs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reduce scrape interval
💡 Lowering scrape frequency reduces time-series data ingestion and memory consumption.

</details>

---

### 21. In a CI/CD pipeline using GitHub as the version control system, what is the main purpose of a pull request (PR)?

* [ ] To propose changes from one branch to be reviewed, discussed, and potentially merged into another branch.
* [ ] To permanently delete a branch and its commit history from the repository.
* [ ] To automatically deploy code directly to production without human review.
* [ ] To create a copy of the repository under your own account for independent development.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To propose changes from one branch to be reviewed, discussed, and potentially merged into another branch.
💡 PRs enable collaboration, code review, and discussion before merging changes.

</details>

---

### 22. In an AWS Virtual Private Cloud (VPC), which design best supports a microservices application that exposes public APIs while keeping databases and internal services isolated?

* [ ] Place microservices in one VPC and databases in another VPC with unrestricted VPC peering
* [ ] Place public-facing services in public subnets and databases in private subnets with NAT gateways
* [ ] Place all services and databases in a single public subnet with strict security groups
* [ ] Use only private subnets and access the application via VPN without any public endpoints

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Place public-facing services in public subnets and databases in private subnets with NAT gateways
💡 This ensures public access to APIs while keeping databases isolated from direct internet exposure.

</details>

---

### 23. A DevOps team wants to implement infrastructure-as-code for deploying AWS networking, EC2 instances, and IAM roles repeatedly across multiple accounts. Which approach best balances reproducibility and cross-account separation?

* [ ] Use a single Terraform state file shared across all accounts and environments
* [ ] Create separate Terraform workspaces or state files per account and environment, with reusable modules
* [ ] Use only AWS CloudFormation stacks defined independently in each account, without shared modules
* [ ] Use Ansible ad-hoc commands manually for each account without maintaining state

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Create separate Terraform workspaces or state files per account and environment, with reusable modules
💡 Provides isolation, reproducibility, and modular infrastructure management.

</details>

---

### 24. Your company’s public web server sits in a DMZ and is fronted by a reverse proxy and a WAF. You notice repeated HTTP POSTs containing SQL keywords aimed at the login form, but the database remains uncompromised. Which control is most likely blocking these attacks?

* [ ] The reverse proxy performing TCP termination
* [ ] The IPS running in inline mode between DMZ and LAN
* [ ] The WAF applying application-layer rules
* [ ] The stateful firewall enforcing default deny on outbound traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** WAF applying application-layer rules
💡 WAF inspects HTTP payloads and blocks SQL injection patterns.

</details>

---

### 25. A security engineer notices that iptables on a Linux bastion host only has rules filtering inbound traffic, and all outbound traffic is allowed. What is the main security risk of this configuration?

* [ ] QoS policies cannot be enforced on outbound connections
* [ ] VPN tunnels cannot be established from the host
* [ ] Increased inbound SYN flood risk
* [ ] None of the Above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** None of the Above
💡 The real risk is data exfiltration, which is not listed in the options.

</details>

---

### 26. A retail company runs a seasonal promotion and anticipates a 20x traffic spike to its e‑commerce API over a weekend. The API is currently deployed on a managed instance group of Compute Engine VMs behind an external HTTP(S) Load Balancer. The promotion cannot tolerate more than a few seconds of additional latency or any significant errors. How should you prepare the environment on GCP to handle the spike while keeping costs reasonable after the promotion ends?

* [ ] Migrate the API to Cloud Functions and rely on its automatic scaling without load balancers.
* [ ] Configure autoscaling on the managed instance group based on CPU utilization, set appropriate min and max instances, and warm up capacity using pre‑scaling before the event.
* [ ] Move the API to a single powerful VM instance and put Cloud CDN in front of it for all responses.
* [ ] Increase the machine type for all existing VMs to a much larger size and disable autoscaling to keep the environment stable during the promotion.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configure autoscaling on the managed instance group based on CPU utilization, set appropriate min and max instances, and warm up capacity using pre‑scaling before the event.
💡 Autoscaling ensures capacity during spike and scales down after promotion.

</details>

---

### 27. Your organization stores sensitive customer data in Cloud Storage buckets and processes it using Dataflow jobs. A new compliance requirement mandates that all data must be encrypted with customer‑managed keys and access must be tightly controlled, including visibility into who accessed which objects. Which combination of GCP features best addresses these requirements with minimal changes to your existing pipelines?

* [] Configure Cloud Storage buckets to use CMEK from Cloud Key Management Service (KMS), set IAM policies with least privilege, and enable Data Access audit logs.
* [ ] Rely on VPC Service Controls alone to enforce perimeter security without changing encryption settings or logging.
* [ ] Use default Google‑managed encryption keys for Cloud Storage and enable Cloud Audit Logs only at the project level.
* [ ] Move all data to BigQuery and enable customer‑managed encryption keys there, without changing IAM settings or audit logging.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configure Cloud Storage buckets to use CMEK from Cloud Key Management Service (KMS), set IAM policies with least privilege, and enable Data Access audit logs.
💡 Meets encryption and audit requirements with minimal pipeline changes.

</details>

---

### 28. A financial services company runs a critical risk calculation engine on Compute Engine. The workload is batch‑oriented and runs nightly, requiring a large amount of CPU and memory for about 2 hours. The team wants to reduce costs without extending the job duration significantly and can tolerate occasional job preemptions as long as the job can resume. Which Compute Engine configuration is most cost‑effective while meeting these needs?

* [ ] Migrate the workload entirely to Cloud Functions, splitting the logic into many small functions.
* [ ] Use a mix of regular and preemptible VMs in a managed instance group and design the job to checkpoint progress so it can resume if preemptions occur.
* [ ] Run the workload on standard on‑demand VMs with no changes to the current setup.
* [ ] Use solely preemptible VMs and restart the entire job manually if preempted.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mix of regular and preemptible VMs with checkpointing
💡 Balances cost savings and reliability.

</details>

---

### 29. An administrator configures iptables to allow SSH only from a specific management subnet and drops all other inbound SSH attempts. However, a brute-force attack is still observed coming from that subnet after a jump host there was compromised. Which additional control best reduces this risk?

* [ ] Moving SSH to a non-standard high port
* [ ] Using key-based SSH authentication and disabling password logins
* [ ] Implementing port knocking for SSH
* [ ] Placing the jump host into the DMZ

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Using key-based SSH authentication and disabling password logins
💡 Eliminates password-based brute-force attacks.

</details>

---

### 30. Your company hosts a public API in a DMZ behind a stateful firewall and an IPS. A new zero-day exploit in the API framework is being actively abused in the wild. Patches are not yet available. Which additional control provides the most targeted temporary protection?

* [ ] Rate limiting API requests on the perimeter router
* [ ] Adding custom virtual patches on the WAF
* [ ] Blocking all outbound traffic from the DMZ
* [ ] Forcing clients to connect via a site-to-site VPN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Add custom virtual patches on WAF
💡 WAF rules can block exploit patterns until official patch is released.

</details>

---

### 31. How do you apply any port allow or deny rule to Compute Engine in GCP?

* [ ] Firewall Policy
* [ ] Security Groups
* [ ] Target Tags
* [ ] Labels

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Target Tags
💡 GCP firewall rules are applied to VM instances using network tags (target tags).

</details>

---

### 32. A security engineer notices unusual spikes in outbound DNS traffic from a DMZ web server. Packet captures show large TXT record responses. The firewall allows DNS only to the corporate resolvers. Which control best helps prevent potential data exfiltration via DNS?

* [ ] Switching DNS to use TCP instead of UDP
* [ ] Moving the web server behind a reverse proxy
* [ ] Enforcing DNS query and response inspection with IDS/IPS
* [ ] Blocking all outbound DNS from the DMZ

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enforce DNS inspection with IDS/IPS
💡 DNS inspection helps detect and block tunneling or data exfiltration attempts.

</details>

---

### 33. Your security team wants to implement a zero‑trust model for an internal web application hosted on GCP. Employees should only be able to access the app if they meet certain device and identity conditions, and access should be logged. The app currently runs on Compute Engine behind an internal HTTP(S) Load Balancer. What is the best way to implement this model with minimal changes to the application?

* [ ] Move the app to Cloud Run, which automatically provides zero‑trust access controls.
* [ ] Use Identity‑Aware Proxy (IAP) in combination with BeyondCorp Enterprise to enforce identity and device‑based access policies and log access.
* [ ] Implement your own authentication and authorization layer inside the application, integrating with an external identity provider.
* [ ] Expose the app publicly and protect it with Cloud Armor IP allowlists only.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use IAP with BeyondCorp
💡 IAP enforces identity- and device-based access with centralized logging.

</details>

---

### 34. You are tuning an inline IPS placed between the Internet and your DMZ. After enabling aggressive signatures, your customer-facing web application experied

* [ ] The DMZ routing table has become corrupted
* [ ] The IPS is under a DDoS attack and shutting down
* [ ] The firewall in front of the IPS is dropping all SYN packets
* [ ] False positives in IPS signatures are blocking legitimate traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** False positives in IPS signatures are blocking legitimate traffic
💡 Aggressive IPS signatures may incorrectly block valid application traffic.

</details>

---

### 35. During a threat hunting exercise, you discover that several internal clients are making outbound HTTPS connections to a rare foreign ASN at regular intervals, but only a few kilobytes are exchanged each time. Traditional firewall rules allow outbound.

* [ ] Using SSL decryption and packet analysis on those flows
* [ ] Moving the clients into a more restricted VLAN
* [ ] Increasing the IPS signature severity to "critical"
* [ ] Configuring strict egress firewall rules blocking all foreign IPs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SSL decryption and packet analysis
💡 Helps detect command-and-control or covert data exfiltration over HTTPS.

</details>

---

### 36. Purpose of subnet mask 255.255.255.0?

* [ ] To indicate the DNS server used by the clients
* [ ] To specify the default gateway address for the network
* [ ] To encrypt traffic between two hosts
* [ ] To define which portion of an IP address represents the network and which represents the host

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Define network and host portion
💡 Subnet mask determines how IP addresses are divided between network and hosts.

</details>

---

### 37. In data center design for DevOps and HPC, why is separation of management, storage, and data networks a common best practice?

* [ ] It is required by all network hardware vendors to maintain warranty.
* [ ] It reduces the number of switches required in the data center.
* [ ] It allows reuse of the same IP addresses on all networks without conflicts.
* [ ] It isolates different traffic types to improve security, performance, and troubleshooting.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Traffic isolation improves security and performance
💡 Segmentation prevents interference and enhances fault isolation.

</details>

---

### 38. In Linux permissions, which setting best restricts access to a sensitive configuration file such as /etc/secret.conf?

* [ ] -rw-r----- owned by root:devops
* [ ] -rw-rw-rw-
* [ ] -rwxr-xr-x owned by root:root
* [ ] -rw------- owned by root:root

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** -rw------- owned by root:root
💡 Only root can read/write, providing maximum restriction.

</details>

---

### 39. What does $? represent in Bash?

* [ ] Exit status of the last executed command
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
* [ ] Fragmentation or packet drops
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
* [ ] Namespaces + cgroups

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Namespaces + cgroups
💡 Linux namespaces isolate resources; cgroups limit resource usage.

</details>

---

### 42. Which symbol represents a user’s home directory in Linux?

* [ ] :
* [ ] ~
* [ ] $
* [ ] /

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ~
💡 The tilde (~) expands to the current user’s home directory.

</details>

---

### 43. You run a stateful web application on Amazon EC2 instances behind an Application Load Balancer (ALB). Some users report intermittent logouts and lost shopping cart data after you enabled cross-zone load balancing. Which configuration change best addresses this while keeping the app architecture largely the same?

* [ ] Increase the ALB idle timeout so that long-lived connections are not closed prematurely by the load balancer.
* [ ] Disable cross-zone load balancing so that each client always hits the same Availability Zone as before.
* [ ] Enable ALB sticky sessions (session affinity) based on application cookies and ensure the cookie is set on all responses.
* [ ] Use a Network Load Balancer (NLB) instead of an ALB so that TCP connections are preserved across AZs.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enable sticky sessions
💡 Session affinity ensures users consistently hit the same backend.

</details>

---

### 44. You have an Amazon S3 bucket that stores log files from multiple applications. Different teams need access only to logs that start with their app-specific prefix, for example appA/ or appB/. Which approach most cleanly enforces least-privilege access without creating multiple buckets?

* [ ] Enable S3 Object Lock in compliance mode and then use retention periods to restrict who can read each prefix.
* [ ] Create multiple IAM users, each with an inline policy granting s3:* on the entire bucket ARN, and rely on teams to only access their own prefix.
* [ ] Apply a bucket policy that grants public read access to all objects, and use object-level encryption keys to control which team can actually read the decrypted data.
* [ ] Attach an IAM policy to each team’s role that uses a condition on s3:prefix in s3:ListBucket and limits s3:GetObject to arn:aws:s3:::bucket-name/appX/*.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IAM policy with prefix condition
💡 Limits access to specific object prefixes within the same bucket.

</details>

---

### 45. Your Pods are not starting, and you suspect an issue with the default scheduler decisions. Which kubectl command best helps you inspect the current events and scheduling-related issues for a specific Pod named my-pod in the default namespace?

* [ ] kubectl get events --field-selector involvedObject.name=my-pod
* [ ] kubectl logs my-pod
* [ ] kubectl describe pod my-pod
* [ ] kubectl get pod my-pod -o wide

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** kubectl describe pod my-pod
💡 Shows events, scheduling failures, and detailed status.

</details>

---

### 46. Your Pods are not starting, and you suspect an issue with the default scheduler decisions. Which kubectl command best helps you inspect the current events and scheduling-related issues for a specific Pod named my-pod in the default namespace?

* [ ] kubectl exec -it my-pod -- /bin/sh
* [ ] kubectl exec -it my-pod -c sidecar -- /bin/sh
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
* [ ] kubectl exec -it api-pod -- nslookup kubernetes.default

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
* [ ] kubectl scale deployment worker --current-replicas=3 --replicas=0

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** kubectl scale deployment worker --current-replicas=3 --replicas=0
💡 Ensures scaling happens only if current replica count matches expected value.

</details>

---

### 49. You edited a Terraform variable default value, but on the next apply Terraform still uses the old value from a previous run. Which command lets you see exactly what input values Terraform will use, including those coming from tfvars files and the environment?

* [ ] terraform plan -var
* [ ] terraform console
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
* [ ] Alice can use rsync’s options to copy or overwrite arbitrary root-owned files, effectively gaining root-level file access.
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
* [ ] podman commit web mywebimage:latest
* [ ] podman build -t mywebimage:latest web

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** podman commit web mywebimage:latest
💡 commit creates a new image from the container’s current filesystem state.

</details>

---
