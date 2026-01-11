> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 013 


## **Session 13 & 14: Hyper-V & Storage Solutions**

---

### 1. What is the primary role of Hyper-V in a Windows Server environment?

* [ ] Providing endpoint security and malware protection
* [ ] Hosting and managing enterprise email services
* [ ] Creating and managing virtualized computing environments
* [ ] Resolving hostnames using directory services

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Creating and managing virtualized computing environments
💡 Hyper-V is Microsoft’s native hypervisor that enables hardware virtualization, allowing multiple isolated virtual machines to run on a single physical server.

</details>

---

### 2. Which virtual hard disk format introduced with Windows Server 2012 provides better resiliency and larger capacity?

* [ ] `.iso`
* [ ] `.exe`
* [ ] `.vhdx`
* [ ] `.zip`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `.vhdx`
💡 VHDX supports up to 64 TB, protection against corruption, and improved performance compared to legacy VHD.

</details>

---

### 3. To deploy virtualization capabilities on Windows Server, which feature must be installed?

* [ ] Telnet Client
* [ ] FTP Server
* [ ] Hyper-V role
* [ ] BitLocker Drive Encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hyper-V role
💡 The Hyper-V role installs the hypervisor, virtualization stack, and management tools required for VM hosting.

</details>

---

### 4. Which Windows disk configuration provides fault tolerance by maintaining identical copies of data?

* [ ] Simple volume
* [ ] Spanned volume
* [ ] Mirrored volume
* [ ] Striped volume

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mirrored volume
💡 Mirroring (RAID 1) writes identical data to two disks, ensuring availability if one disk fails.

</details>

---

### 5. Which built-in Windows Server utility is used to create, format, and manage disks and volumes?

* [ ] Task Scheduler
* [ ] Disk Management
* [ ] Resource Monitor
* [ ] Event Viewer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Disk Management
💡 Disk Management provides graphical control for partitions, volumes, and disk initialization.

</details>

---

### 6. By default, where does Hyper-V store configuration data and virtual hard disks?

* [ ] `C:\Windows\System32`
* [ ] `C:\Program Files\Hyper-V`
* [ ] `C:\Users\VMStorage`
* [ ] `C:\ProgramData\Microsoft\Windows\Hyper-V`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `C:\ProgramData\Microsoft\Windows\Hyper-V`
💡 Hyper-V stores VM configuration and related metadata in the ProgramData directory by default.

</details>

---

### 7. Which Windows Server feature reduces storage consumption by eliminating redundant data blocks?

* [ ] Encryption
* [ ] Compression
* [ ] Deduplication
* [ ] Partitioning

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Deduplication
💡 Data Deduplication identifies and stores unique data blocks only once, replacing duplicates with references.

</details>

---

### 8. Which Hyper-V virtual switch type allows virtual machines to communicate with the physical network?

* [ ] Private
* [ ] Internal
* [ ] External
* [ ] Virtual-only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** External
💡 An external switch binds to a physical NIC, enabling VM access to external networks and the internet.

</details>

---

### 9. Which RAID level provides disk striping without any fault tolerance?

* [ ] RAID 0
* [ ] RAID 1
* [ ] RAID 5
* [ ] RAID 10

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RAID 0
💡 RAID 0 improves performance via striping but offers no redundancy—failure of one disk causes total data loss.

</details>

---

### 10. Which file system is recommended for enabling Data Deduplication on Windows Server?

* [ ] FAT32
* [ ] ReFS
* [ ] NTFS
* [ ] exFAT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NTFS
💡 Data Deduplication is fully supported on NTFS volumes (with limited support scenarios for ReFS).

</details>

---

### 11. What is a key advantage of using Generation 2 virtual machines in Hyper-V?

* [ ] Legacy BIOS compatibility
* [ ] IDE-based boot support
* [ ] Secure Boot with UEFI firmware
* [ ] Parallel port device support

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Secure Boot with UEFI firmware
💡 Generation 2 VMs use UEFI, Secure Boot, and SCSI boot, enhancing security and performance.

</details>

---

### 12. In Hyper-V architecture, what best describes a differencing disk?

* [ ] A complete standalone virtual disk
* [ ] A read-only backup disk
* [ ] A child disk that tracks changes from a parent disk
* [ ] A physical disk mapped to the VM

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A child disk that tracks changes from a parent disk
💡 Differencing disks store only modified data while referencing the parent VHD/VHDX.

</details>

---

### 13. Which administrative interface is commonly used to automate and manage Hyper-V environments?

* [ ] netsh
* [ ] vmmanage
* [ ] PowerShell
* [ ] diskpart

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PowerShell
💡 Hyper-V PowerShell modules allow advanced automation and VM lifecycle management.

</details>

---

### 14. Which storage architecture provides block-level access using the iSCSI protocol?

* [ ] DAS
* [ ] SAN
* [ ] NAS
* [ ] SSD

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SAN
💡 Storage Area Networks deliver block-level storage, often using iSCSI or Fibre Channel.

</details>

---

### 15. In data deduplication, what does the term “chunk” represent?

* [ ] A disk partition
* [ ] A storage pool
* [ ] A duplicated data segment
* [ ] A uniquely identified block of data

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A uniquely identified block of data
💡 Deduplication breaks files into chunks and stores only unique chunks to save space.

</details>

---

### 16. What is the primary purpose of Hyper-V Integration Services?

* [ ] Managing NTFS permissions
* [ ] Enhancing guest OS performance and integration
* [ ] Encrypting virtual hard disks
* [ ] Increasing physical CPU cores

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enhancing guest OS performance and integration
💡 Integration Services improve time sync, shutdown, heartbeat, and network performance.

</details>

---

### 17. What is the maximum supported size of a VHDX file?

* [ ] 1 TB
* [ ] 2 TB
* [ ] 32 TB
* [ ] 64 TB

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 64 TB
💡 VHDX significantly expands capacity compared to legacy VHD (2 TB limit).

</details>

---

### 18. Which Hyper-V feature allows administrators to capture the state of a virtual machine at a specific point in time?

* [ ] Checkpoint
* [ ] Backup
* [ ] HyperClone
* [ ] Restore Point

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Checkpoint
💡 Checkpoints (formerly snapshots) capture VM state for testing and rollback purposes.

</details>

---

### 19. What prerequisite component is required to create a Storage Pool in Windows Server?

* [ ] Disk quota
* [ ] Dynamic disk
* [ ] Storage Spaces
* [ ] Shared folder

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Storage Spaces
💡 Storage Spaces aggregates physical disks into pools for flexible virtual storage management.

</details>

---

### 20. Which Hyper-V capability allows a VM to adjust memory usage dynamically based on workload?

* [ ] Smart Paging
* [ ] Memory Ballooning
* [ ] Dynamic Memory
* [ ] Memory Compression

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dynamic Memory
💡 Dynamic Memory optimizes RAM allocation by increasing or decreasing memory during runtime.

</details>

---

### 21. What does thin provisioning mean in virtualized storage environments?

* [ ] Allocating full disk space in advance
* [ ] Allocating storage only when data is written
* [ ] Encrypting unused disk blocks
* [ ] Creating fixed-size virtual disks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Allocating storage only when data is written
💡 Thin provisioning improves storage efficiency by avoiding upfront allocation.

</details>

---

### 22. Why is data deduplication generally not recommended for high IOPS workloads such as SQL databases?

* [ ] It improves query latency
* [ ] It is mandatory for SQL workloads
* [ ] It can introduce performance overhead
* [ ] It disables SQL Server support

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It can introduce performance overhead
💡 Deduplication adds CPU and disk overhead, negatively impacting latency-sensitive workloads.

</details>

---

### 23. What is the immediate consequence if the parent disk of a differencing disk is deleted?

* [ ] The VM continues normally
* [ ] The VM fails to boot
* [ ] The VM resets to default state
* [ ] The disk converts automatically to fixed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The VM fails to boot
💡 Differencing disks depend entirely on the parent disk for unchanged data blocks.

</details>

---

### 24. Before enabling data deduplication on a volume, which prerequisite must be satisfied?

* [ ] Encrypting the volume
* [ ] Using dynamic disks
* [ ] Installing the Data Deduplication role
* [ ] Formatting as FAT32

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Installing the Data Deduplication role
💡 Deduplication must be installed as a server role before configuration.

</details>

---

### 25. Which PowerShell cmdlet manually initiates a data deduplication job?

* [ ] Invoke-Dedup
* [ ] Start-Dedup
* [ ] Start-DedupJob
* [ ] Run-DedupScan

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Start-DedupJob
💡 This cmdlet triggers optimization, garbage collection, or scrubbing jobs.

</details>

---

### 26. Which Hyper-V virtual switch type allows communication only among virtual machines on the same host?

* [ ] Private
* [ ] External
* [ ] NAT
* [ ] Internal

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Private
💡 Private switches isolate VM communication entirely from the host and external networks.

</details>

---

### 27. What is a valid and practical use case for pass-through disks in Hyper-V?

* [ ] Enabling VM checkpoints
* [ ] Improving file sharing performance
* [ ] Providing direct access to physical disks
* [ ] Managing dynamic disk expansion

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Providing direct access to physical disks
💡 Pass-through disks allow VMs to bypass VHDX abstraction for specific performance needs.

</details>

---

### 28. Which Hyper-V feature ensures business continuity by maintaining a replica VM on another host?

* [ ] Live Migration
* [ ] VM Checkpoint
* [ ] VM Export
* [ ] Hyper-V Replica

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hyper-V Replica
💡 Hyper-V Replica asynchronously replicates VMs for disaster recovery.

</details>

---

### 29. In Storage Spaces, what benefit does the “Parity” layout provide?

* [ ] Maximum speed without redundancy
* [ ] Full redundancy using mirroring
* [ ] Balanced fault tolerance and storage efficiency
* [ ] Automatic volume compression

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Balanced fault tolerance and storage efficiency
💡 Parity uses parity data to protect against disk failure with better capacity utilization.

</details>

---

### 30. Which storage solution is most suitable for scalable, centralized, and fault-tolerant storage in large enterprise environments?

* [ ] DAS
* [ ] SAN
* [ ] USB storage
* [ ] RAID 0

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SAN
💡 SANs provide high availability, scalability, and centralized block-level storage for enterprises.

</details>

---

## **Session 15: Concept of File Server Resource Manager (FSRM)**

---

---

### 1. An organization wants to centrally control how storage is utilized on its Windows file servers. Which is the primary purpose of File Server Resource Manager (FSRM)?

* [ ] Firewall rule enforcement
* [ ] Disk defragmentation and optimization
* [ ] File server storage management and policy enforcement
* [ ] System state backup restoration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** File server storage management and policy enforcement
💡 FSRM is designed to manage, monitor, and control data stored on Windows file servers through quotas, file screening, and reporting.

</details>

---

### 2. An administrator wants to restrict how much disk space a department can consume on a shared folder. Which FSRM feature should be used?

* [ ] File screening
* [ ] Quota management
* [ ] Storage reports
* [ ] Event forwarding

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Quota management
💡 Quota management enforces storage limits on volumes or folders, preventing uncontrolled disk usage.

</details>

---

### 3. File Server Resource Manager is installed as a role service under which Windows Server role?

* [ ] Active Directory Domain Services
* [ ] Print and Document Services
* [ ] File and Storage Services
* [ ] Remote Access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** File and Storage Services
💡 FSRM is a role service under **File and Storage Services** in Windows Server.

</details>

---

### 4. Which management interfaces are officially supported for administering FSRM?

* [ ] Graphical User Interface (GUI) only
* [ ] Command Line Interface (CLI) only
* [ ] Web-based console only
* [ ] GUI and PowerShell

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** GUI and PowerShell
💡 FSRM can be managed using the MMC snap-in and PowerShell cmdlets for automation.

</details>

---

### 5. An administrator wants to prevent users from storing executable and multimedia files on a shared drive. Which FSRM feature enables this control?

* [ ] Quota templates
* [ ] File screens
* [ ] Storage reports
* [ ] Shadow copies

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** File screens
💡 File screening blocks or monitors specific file types based on extensions or file groups.

</details>

---

### 6. From which console is the dedicated FSRM management interface launched?

* [ ] Disk Management
* [ ] File Explorer
* [ ] Server Manager only
* [ ] File Server Resource Manager MMC snap-in

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** File Server Resource Manager MMC snap-in
💡 FSRM provides its own MMC snap-in for managing quotas, file screens, and reports.

</details>

---

### 7. Which operating system edition natively supports File Server Resource Manager?

* [ ] Windows 10 Home
* [ ] Windows 11 Pro
* [ ] Windows Server editions
* [ ] macOS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Windows Server editions
💡 FSRM is available only on Windows Server operating systems.

</details>

---

### 8. In FSRM, what is the primary purpose of a quota template?

* [ ] To create backup snapshots
* [ ] To define physical disk layouts
* [ ] To provide reusable quota configurations
* [ ] To classify file ownership

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To provide reusable quota configurations
💡 Quota templates standardize quota settings and ensure consistent policy enforcement.

</details>

---

### 9. Which FSRM feature helps administrators identify large files, duplicate files, and file ownership patterns?

* [ ] File screening
* [ ] Quota templates
* [ ] Storage reports
* [ ] DFS replication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Storage reports
💡 Storage reports analyze file usage patterns and help optimize storage resources.

</details>

---

### 10. What occurs when a user exceeds a **soft quota** defined in FSRM?

* [ ] File write operations are blocked
* [ ] Notifications or alerts are triggered
* [ ] Files are automatically deleted
* [ ] The disk is marked offline

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Notifications or alerts are triggered
💡 Soft quotas allow storage usage beyond limits but generate alerts for monitoring.

</details>

---

### 11. Which statement best describes a **hard quota** in FSRM?

* [ ] It logs usage without enforcement
* [ ] It provides unlimited storage
* [ ] It strictly prevents exceeding defined limits
* [ ] It applies only temporarily

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It strictly prevents exceeding defined limits
💡 Hard quotas enforce absolute storage limits, blocking further writes once exceeded.

</details>

---

### 12. Which predefined file screen template should be applied to block MP3 file uploads?

* [ ] Block Image Files
* [ ] Block Audio and Video Files
* [ ] Block Executable Files
* [ ] Block Office Files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Block Audio and Video Files
💡 MP3 files belong to audio categories covered under audio/video file groups.

</details>

---

### 13. Why are custom file groups created in FSRM?

* [ ] To group users by role
* [ ] To organize folder hierarchies
* [ ] To define and manage file type classifications
* [ ] To install storage drivers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To define and manage file type classifications
💡 File groups allow administrators to control file screening based on extensions.

</details>

---

### 14. What is the default response when a file screen violation occurs?

* [ ] The file is permanently deleted
* [ ] The event is logged and notifications may be sent
* [ ] The server reboots automatically
* [ ] The file is encrypted

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The event is logged and notifications may be sent
💡 FSRM logs violations and can trigger email or script-based notifications.

</details>

---

### 15. How does FSRM assist organizations in meeting regulatory or compliance requirements?

* [ ] By managing authentication policies
* [ ] By encrypting storage volumes
* [ ] By generating audit and storage usage reports
* [ ] By configuring firewall rules

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** By generating audit and storage usage reports
💡 Reports support compliance audits by providing visibility into stored data.

</details>

---

### 16. What is the key advantage of using FSRM storage reports?

* [ ] Automatic deletion of unused files
* [ ] Monitoring disk hardware health
* [ ] Analysis of storage consumption and trends
* [ ] Partition creation and resizing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Analysis of storage consumption and trends
💡 Storage reports help administrators understand how storage is being used.

</details>

---

### 17. Which FSRM capability directly prevents users from accidentally storing disallowed file types?

* [ ] Quota management
* [ ] File screening
* [ ] File replication
* [ ] Shadow copies

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** File screening
💡 File screening enforces file-type restrictions at write time.

</details>

---

### 18. What filesystem requirement must be met before applying FSRM quotas?

* [ ] Folder must be shared
* [ ] Folder must be empty
* [ ] Volume must be NTFS
* [ ] Volume must be FAT32

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Volume must be NTFS
💡 FSRM relies on NTFS features such as file attributes and security descriptors.

</details>

---

### 19. Which command-line technology is officially supported for configuring FSRM?

* [ ] netsh
* [ ] fsutil
* [ ] PowerShell
* [ ] scconfig

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PowerShell
💡 Microsoft provides dedicated PowerShell cmdlets for FSRM administration.

</details>

---

### 20. What must be installed before any FSRM functionality can be used?

* [ ] Hyper-V role
* [ ] Internet Information Services
* [ ] File Server Resource Manager role service
* [ ] Windows Update Agent

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** File Server Resource Manager role service
💡 FSRM must be installed explicitly via Server Manager.

</details>

---

### 21. What type of event can trigger an email alert in FSRM?

* [ ] File system formatting
* [ ] CPU overheating
* [ ] Quota or file screen violations
* [ ] DNS zone modifications

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Quota or file screen violations
💡 Notifications are tied to storage policy enforcement events.

</details>

---

### 22. How does FSRM leverage Active Directory in enterprise environments?

* [ ] Through DNS replication
* [ ] By applying policies via Group Policy
* [ ] By enabling SMB encryption
* [ ] It does not directly integrate with Active Directory

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It does not directly integrate with Active Directory
💡 FSRM operates independently but can be managed centrally in domain environments.

</details>

---

### 23. To ensure a file screen is enforced correctly, which path must be specified?

* [ ] File screen template path
* [ ] Network drive mappings
* [ ] Absolute or relative folder paths
* [ ] User profile directories only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Absolute or relative folder paths
💡 File screens are applied directly to folders or volumes.

</details>

---

### 24. What is the effect of configuring a **passive file screen**?

* [ ] Blocks all restricted file operations
* [ ] Allows files but generates notifications
* [ ] Encrypts disallowed files
* [ ] Converts files to read-only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Allows files but generates notifications
💡 Passive screening monitors violations without blocking file writes.

</details>

---

### 25. How can FSRM help detect misuse or abuse of file server resources?

* [ ] By monitoring login attempts
* [ ] By tracking storage consumption and file types
* [ ] By auditing firewall traffic
* [ ] By preventing unauthorized reboots

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** By tracking storage consumption and file types
💡 Reports and quotas reveal abnormal storage behavior.

</details>

---

### 26. What is the default storage location for FSRM-generated reports?

* [ ] C:\Program Files\FSRM\Logs
* [ ] C:\Reports\Storage
* [ ] C:\StorageReports\
* [ ] C:\Windows\System32

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** C:\StorageReports\
💡 FSRM stores generated reports in this directory by default.

</details>

---

### 27. Which FSRM component enables execution of custom scripts when quota thresholds are crossed?

* [ ] Storage Reports
* [ ] File Classification
* [ ] Notification settings in quota templates
* [ ] File screen exceptions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Notification settings in quota templates
💡 Notifications can trigger scripts, emails, or event logs.

</details>

---

### 28. What happens when an existing quota template is modified?

* [ ] New quotas are automatically created
* [ ] Existing quotas remain unchanged
* [ ] Existing quotas can optionally be updated
* [ ] All quotas reset to default values

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Existing quotas can optionally be updated
💡 Administrators choose whether to propagate template changes.

</details>

---

### 29. Which scripting language is natively supported for custom FSRM automation?

* [ ] Python
* [ ] Java
* [ ] PowerShell
* [ ] Perl

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PowerShell
💡 PowerShell is Microsoft’s supported automation framework.

</details>

---

### 30. How does FSRM handle overlapping file screens applied to parent and child folders?

* [ ] Only the most restrictive screen is enforced
* [ ] Settings are merged automatically
* [ ] All file screens are disabled
* [ ] One screen is chosen randomly

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Only the most restrictive screen is enforced
💡 FSRM prioritizes enforcement to ensure policy consistency.

</details>

---
