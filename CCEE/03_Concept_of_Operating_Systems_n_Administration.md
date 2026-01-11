> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 03

## **Session 3: Concept of Windows Server Backup (WSB)**

---

### 1. An organization wants to ensure rapid restoration of critical business data after accidental deletion or hardware failure on a Windows Server. What is the primary purpose of Windows Server Backup (WSB) in this scenario?

* [ ] Video editing and multimedia processing
* [ ] Malware detection and removal
* [ ] Data backup and recovery for Windows Server components
* [ ] File compression and archiving

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data backup and recovery for Windows Server components
💡 WSB is designed to back up and restore files, system state, applications, and entire volumes to ensure business continuity.

</details>

---

### 2. A system administrator wants to perform scheduled backups without installing third-party software. Which built-in Windows Server tool fulfills this requirement?

* [ ] Paint
* [ ] Windows Media Player
* [ ] Windows Server Backup
* [ ] Task Scheduler

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Windows Server Backup
💡 Windows Server Backup is the native Microsoft utility for backup and recovery operations on Windows Server systems.

</details>

---

### 3. Which interface options are officially supported for managing Windows Server Backup operations?

* [ ] Only command-line interface
* [ ] Only web-based console
* [ ] Graphical User Interface and command-line interface
* [ ] BIOS-level interface

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Graphical User Interface and command-line interface
💡 WSB can be managed via the MMC snap-in and through command-line tools like **wbadmin** and PowerShell.

</details>

---

### 4. A junior administrator is unable to locate Windows Server Backup on the desktop. Where should it be accessed from by default?

* [ ] Control Panel
* [ ] Taskbar
* [ ] Server Manager → Tools
* [ ] Windows Defender

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Server Manager → Tools
💡 Windows Server Backup is accessed via Server Manager under the Tools menu.

</details>

---

### 5. From which Windows Server version was Windows Server Backup introduced as a replacement for NTBackup?

* [ ] Windows Server 2000
* [ ] Windows Server 2003
* [ ] Windows Server 2008
* [ ] Windows NT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Windows Server 2008
💡 NTBackup was deprecated after Windows Server 2003, and WSB was introduced in Windows Server 2008.

</details>

---

### 6. Which set of data can be backed up using Windows Server Backup?

* [ ] Only system files
* [ ] Only registry data
* [ ] Files, system state, and full volumes
* [ ] Only device drivers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Files, system state, and full volumes
💡 WSB supports file-level, system state, and bare-metal backups.

</details>

---

### 7. By default, how frequently does Windows Server Backup schedule backups when automated scheduling is enabled?

* [ ] Once a month
* [ ] Every 2 hours
* [ ] Once daily
* [ ] Weekly

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Once daily
💡 WSB schedules backups once per day by default, though this can be customized.

</details>

---

### 8. Windows Server Backup primarily uses which backup methodology to optimize storage usage?

* [ ] Differential
* [ ] Full
* [ ] Incremental (block-level)
* [ ] Synthetic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Incremental (block-level)
💡 WSB uses block-level incremental backups after the initial full backup.

</details>

---

### 9. Which PowerShell or command-line instruction initiates a backup operation using Windows Server Backup?

* [ ] Start-WSB
* [ ] Start-Backup
* [ ] Start-WBBackup
* [ ] Begin-Backup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Start-WBBackup
💡 **Start-WBBackup** is the correct PowerShell cmdlet used to initiate WSB backups.

</details>

---

### 10. What is the role of Volume Shadow Copy Service (VSS) during a WSB backup?

* [ ] Compress backup data
* [ ] Restore registry keys
* [ ] Create a consistent snapshot of data
* [ ] Encrypt backup files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Create a consistent snapshot of data
💡 VSS ensures data consistency by capturing a snapshot even when files are in use.

</details>

---

### 11. Which backup option in WSB includes system state data necessary for Active Directory recovery?

* [ ] Custom backup
* [ ] Bare Metal backup
* [ ] Full volume backup
* [ ] File-only backup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Bare Metal backup
💡 Bare Metal Backup includes system state, boot files, and OS components.

</details>

---

### 12. Windows Server Backup cannot directly write backups to which destination?

* [ ] Local disk
* [ ] Remote shared folder
* [ ] Tape drive
* [ ] External USB drive

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Tape drive
💡 WSB does not support tape drives; third-party solutions are required.

</details>

---

### 13. Which WSB feature enables full server recovery after catastrophic hardware failure?

* [ ] System Restore
* [ ] Bare Metal Recovery
* [ ] Event Viewer
* [ ] Hyper-V

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Bare Metal Recovery
💡 Bare Metal Recovery restores the OS, system state, and volumes to new hardware.

</details>

---

### 14. How does WSB manage retention of backups on a dedicated backup disk?

* [ ] Manual deletion only
* [ ] Unlimited retention
* [ ] FIFO (First-In-First-Out)
* [ ] Weekly rotation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** FIFO (First-In-First-Out)
💡 Older backups are automatically deleted when disk space is required.

</details>

---

### 15. Can Windows Server Backup jobs be scheduled using Task Scheduler directly?

* [ ] Yes
* [ ] No
* [ ] Only in Server Core
* [ ] Only with domain admin rights

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** No
💡 WSB has its own scheduling mechanism and does not rely on Task Scheduler.

</details>

---

### 16. Which file format is used by Windows Server Backup to store system image data?

* [ ] .wbcat
* [ ] .bak
* [ ] .zip
* [ ] .vhd

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** .vhd
💡 System images are stored as Virtual Hard Disk files.

</details>

---

### 17. What action does WSB take when the backup destination becomes full?

* [ ] Backup stops permanently
* [ ] Old backups are deleted automatically
* [ ] System crashes
* [ ] Disk is reformatted

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Old backups are deleted automatically
💡 WSB manages disk space automatically using retention policies.

</details>

---

### 18. What prerequisite must be fulfilled before using Windows Server Backup?

* [ ] Installation via Roles and Features
* [ ] Active Directory configuration
* [ ] Internet connectivity
* [ ] Domain controller privileges

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Installation via Roles and Features
💡 WSB is an optional feature that must be installed manually.

</details>

---

### 19. Which component is used to restore files from an existing WSB backup?

* [ ] Task Scheduler
* [ ] Windows Explorer
* [ ] Recovery Wizard
* [ ] Hyper-V Manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Recovery Wizard
💡 The Recovery Wizard guides administrators through restore operations.

</details>

---

### 20. Which file system is mandatory for a disk dedicated to scheduled WSB backups?

* [ ] FAT32
* [ ] exFAT
* [ ] NTFS
* [ ] ext4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NTFS
💡 NTFS is required for VSS and backup management features.

</details>

---

### 21. How is Windows Server Backup managed on Server Core installations?

* [ ] Internet Explorer
* [ ] Installing GUI
* [ ] PowerShell or wbadmin
* [ ] Remote Desktop only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PowerShell or wbadmin
💡 Server Core supports command-line management only.

</details>

---

### 22. Which command-line utility is officially used to manage Windows Server Backup?

* [ ] wsbackup.exe
* [ ] backup.cmd
* [ ] wbadmin
* [ ] backutil

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** wbadmin
💡 **wbadmin** is the native CLI tool for WSB.

</details>

---

### 23. What is mandatory to perform a Bare Metal Recovery successfully?

* [ ] Active Directory backup
* [ ] EFI partition only
* [ ] System image backup and Windows installation media
* [ ] Hyper-V snapshot

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** System image backup and Windows installation media
💡 Bare Metal Recovery requires booting from installation media to load recovery tools.

</details>

---

### 24. How does WSB efficiently manage disk space during scheduled backups?

* [ ] Manual log analysis
* [ ] Registry-based allocation
* [ ] Shadow copies with automatic disk management
* [ ] User-defined scripts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Shadow copies with automatic disk management
💡 WSB integrates VSS and automated cleanup policies.

</details>

---

### 25. Which component is most critical for restoring system state successfully?

* [ ] Task Scheduler
* [ ] DNS
* [ ] Volume Shadow Copy Service (VSS)
* [ ] GPU

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Volume Shadow Copy Service (VSS)
💡 VSS ensures consistency of system components during backup and restore.

</details>

---

### 26. How does WSB minimize redundant data storage across backups?

* [ ] ZIP compression
* [ ] Shadow duplication
* [ ] Block-level backup
* [ ] File copying

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Block-level backup
💡 Only changed blocks are backed up after the initial full backup.

</details>

---

### 27. Can multiple scheduled backup jobs be configured simultaneously on the same Windows Server?

* [ ] Yes
* [ ] No
* [ ] Only on domain controllers
* [ ] Only via registry editing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** No
💡 WSB allows only one scheduled backup policy per server.

</details>

---

### 28. Which file format does WSB use to store full system images?

* [ ] .img
* [ ] .vhd / .vhdx
* [ ] .iso
* [ ] .exe

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** .vhd / .vhdx
💡 Virtual Hard Disk formats are used for system image backups.

</details>

---

### 29. What is a known limitation of Windows Server Backup related to network storage?

* [ ] Cannot use USB drives
* [ ] Only supports cloud storage
* [ ] Scheduled backups cannot target network shares
* [ ] Requires SSD storage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Scheduled backups cannot target network shares
💡 Network shares can be used only for manual backups.

</details>

---

### 30. Which tool combination is most appropriate to verify the success and integrity of a WSB backup?

* [ ] Event Viewer only
* [ ] Check Disk (chkdsk)
* [ ] Windows Server Backup logs and wbadmin
* [ ] Task Manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Windows Server Backup logs and wbadmin
💡 Logs and **wbadmin get versions** provide backup verification details.

</details>

---

## **Session 4 & 5: Implementation, planning and maintaining of active directory infrastructure**

---

### 1. In a Windows Server environment, the AD DS role primarily enables which enterprise-level capability?

* [ ] Centralized patch management across servers
* [ ] Centralized authentication, authorization, and directory services
* [ ] Network traffic inspection and intrusion detection
* [ ] Automated virtual machine provisioning

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Centralized authentication, authorization, and directory services
💡 AD DS provides centralized identity management, authentication (Kerberos), authorization, and directory-based resource management in Windows domains.

</details>

---

### 2. A system administrator wants to logically group users and computers to apply security policies efficiently. Which Active Directory component best fulfills this requirement?

* [ ] Forest
* [ ] Domain
* [ ] Organizational Unit (OU)
* [ ] Site

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Organizational Unit (OU)
💡 OUs are logical containers designed specifically to organize objects and apply Group Policy independently of domain boundaries.

</details>

---

### 3. Which Microsoft Management Console (MMC) snap-in is most appropriate for creating, deleting, and modifying users, groups, and computer accounts?

* [ ] Server Manager
* [ ] Event Viewer
* [ ] Active Directory Users and Computers
* [ ] Group Policy Management

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Active Directory Users and Computers
💡 ADUC is the primary GUI tool for day-to-day management of AD objects.

</details>

---

### 4. In Active Directory terminology, what best defines a **domain**?

* [ ] A physical network boundary
* [ ] A logical security and administrative boundary
* [ ] A replication site
* [ ] A DNS forward lookup zone only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A logical security and administrative boundary
💡 A domain defines authentication scope, security policies, and administrative control within AD.

</details>

---

### 5. Which statement correctly describes an **Active Directory forest**?

* [ ] It represents a single domain with multiple sites
* [ ] It is a collection of domains sharing a common schema and trust
* [ ] It is used exclusively for DNS zone replication
* [ ] It defines the physical network topology

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It is a collection of domains sharing a common schema and trust
💡 A forest is the highest logical container in AD and establishes schema, configuration, and global catalog boundaries.

</details>

---

### 6. Which service is **critically required** for Active Directory name resolution and authentication to function correctly?

* [ ] DHCP
* [ ] IIS
* [ ] DNS
* [ ] WINS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DNS
💡 AD DS is tightly integrated with DNS; domain controllers dynamically register service records required for client authentication.

</details>

---

### 7. Before a Windows Server can function as a Domain Controller, which role must be installed?

* [ ] DNS Server role
* [ ] Active Directory Domain Services role
* [ ] Network Policy Server role
* [ ] File and Storage Services role

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Active Directory Domain Services role
💡 Installing the AD DS role is mandatory before promoting a server to a Domain Controller.

</details>

---

### 8. In a multi-domain forest, which component allows users to search for objects across all domains efficiently?

* [ ] Domain Naming Master
* [ ] Global Catalog
* [ ] Infrastructure Master
* [ ] Trust Relationship

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Global Catalog
💡 The Global Catalog stores partial replicas of all objects across the forest, enabling forest-wide searches.

</details>

---

### 9. FSMO roles exist in Active Directory primarily to:

* [ ] Improve replication speed
* [ ] Handle operations that must not be multi-master
* [ ] Replace backup domain controllers
* [ ] Manage DNS zone transfers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Handle operations that must not be multi-master
💡 FSMO roles prevent conflicts for operations that require a single authoritative DC.

</details>

---

### 10. How many FSMO roles are defined in a Windows Active Directory forest?

* [ ] 3
* [ ] 4
* [ ] 5
* [ ] 7

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 5
💡 Two forest-wide (Schema Master, Domain Naming Master) and three domain-wide roles.

</details>

---

### 11. Which of the following is **NOT** an FSMO role?

* [ ] RID Master
* [ ] PDC Emulator
* [ ] Infrastructure Master
* [ ] Group Policy Master

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Group Policy Master
💡 There is no FSMO role named Group Policy Master.

</details>

---

### 12. Why is replication essential in an AD DS environment?

* [ ] To compress the NTDS.dit database
* [ ] To synchronize directory data across domain controllers
* [ ] To speed up Kerberos authentication
* [ ] To generate backup copies of GPOs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To synchronize directory data across domain controllers
💡 Replication ensures consistency of directory data throughout the domain and forest.

</details>

---

### 13. Which replication model does Active Directory primarily follow?

* [ ] Single-master
* [ ] Master-slave
* [ ] Multi-master peer-to-peer
* [ ] Event-driven one-way

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Multi-master peer-to-peer
💡 Most AD objects can be modified on any DC and replicated to others.

</details>

---

### 14. Which protocol underpins most directory queries and object management operations in AD DS?

* [ ] SMTP
* [ ] LDAP
* [ ] FTP
* [ ] SNMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** LDAP
💡 LDAP is the core protocol for accessing and managing directory services.

</details>

---

### 15. Which naming format uniquely identifies an Active Directory domain?

* [ ] NetBIOS name
* [ ] Fully Qualified Domain Name (FQDN)
* [ ] URL
* [ ] IPv6 address

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Fully Qualified Domain Name (FQDN)
💡 AD domains rely on DNS-based FQDNs (e.g., corp.example.com).

</details>

---

### 16. A system administrator wants to apply a GPO without affecting the entire domain. What is the best approach?

* [ ] Create a new forest
* [ ] Use an OU and link the GPO
* [ ] Modify the schema
* [ ] Enable site-based replication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use an OU and link the GPO
💡 OUs provide granular policy application.

</details>

---

### 17. Which PowerShell cmdlet is used to create a new AD user object?

* [ ] Set-ADUser
* [ ] New-ADUser
* [ ] Add-DomainUser
* [ ] Create-ADAccount

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** New-ADUser
💡 `New-ADUser` is part of the ActiveDirectory module.

</details>

---

### 18. Before demoting a Domain Controller that holds FSMO roles, what must be ensured?

* [ ] DNS scavenging is enabled
* [ ] FSMO roles are transferred or seized
* [ ] All users are logged off
* [ ] SYSVOL replication is disabled

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** FSMO roles are transferred or seized
💡 Losing FSMO roles can disrupt domain functionality.

</details>

---

### 19. What is the default site name created when AD DS is first installed?

* [ ] Primary-Site
* [ ] Default-Site-First-Name
* [ ] Root-Site
* [ ] AD-Site-01

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Default-Site-First-Name
💡 This default site represents the initial physical topology.

</details>

---

### 20. Which utility is most suitable for diagnosing AD replication issues?

* [ ] gpupdate
* [ ] dcpromo
* [ ] repadmin
* [ ] netdom

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** repadmin
💡 `repadmin` provides detailed replication health and status.

</details>

---

### 21. Which feature allows a computer account to be reused securely when rejoining a domain?

* [ ] SID filtering
* [ ] Computer account pre-staging
* [ ] Trust delegation
* [ ] Secure channel reset

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Computer account pre-staging
💡 Pre-staging helps control domain joins and reuse existing accounts.

</details>

---

### 22. What critical responsibility does the Schema Master FSMO role perform?

* [ ] Managing DNS zone updates
* [ ] Controlling changes to the AD schema
* [ ] Assigning RIDs
* [ ] Handling time synchronization

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Controlling changes to the AD schema
💡 Schema changes affect all objects and must be tightly controlled.

</details>

---

### 23. If the RID Master remains unavailable for an extended period, what operational issue will arise?

* [ ] Users cannot log in
* [ ] New security principals cannot be created
* [ ] GPO processing fails
* [ ] DNS replication stops

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** New security principals cannot be created
💡 Without RIDs, new users, groups, or computers cannot be created.

</details>

---

### 24. By default, how frequently does **intra-site replication** occur?

* [ ] Every 15 minutes
* [ ] Every 60 minutes
* [ ] Every 180 minutes
* [ ] Only during maintenance windows

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Every 15 minutes
💡 Intra-site replication is frequent and optimized for LAN environments.

</details>

---

### 25. In Active Directory, what is a **tombstone object**?

* [ ] A permanently deleted object
* [ ] A cached DNS record
* [ ] A logically deleted object retained for replication
* [ ] A corrupted directory entry

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A logically deleted object retained for replication
💡 Tombstoning ensures deletions replicate correctly across DCs.

</details>

---

### 26. Which command prepares the forest schema for a new Windows Server version?

* [ ] dcpromo /upgrade
* [ ] adprep /forestprep
* [ ] repadmin /syncall
* [ ] netdom /prepare

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** adprep /forestprep
💡 This updates the schema to support new AD features.

</details>

---

### 27. What is the theoretical maximum number of domains in a single Active Directory forest?

* [ ] 100
* [ ] 255
* [ ] 1000
* [ ] No enforced hard limit

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** No enforced hard limit
💡 Practical limits exist, but AD does not define a strict maximum.

</details>

---

### 28. Which tool is used to **seize** FSMO roles when the original role holder is permanently unavailable?

* [ ] netsh
* [ ] adprep
* [ ] ntdsutil
* [ ] dcdiag

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ntdsutil
💡 `ntdsutil` allows forced seizure of FSMO roles.

</details>

---

### 29. How can a Domain Controller be deployed to limit credential exposure at branch offices?

* [ ] Disable Kerberos
* [ ] Install as a Read-Only Domain Controller (RODC)
* [ ] Stop SYSVOL replication
* [ ] Use local user accounts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Install as a Read-Only Domain Controller (RODC)
💡 RODCs enhance security in untrusted locations.

</details>

---

### 30. In AD replication topology, what is the purpose of a **site link bridge**?

* [ ] To connect separate forests
* [ ] To represent physical WAN links
* [ ] To enable transitive replication between site links
* [ ] To map DNS zones across sites

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To enable transitive replication between site links
💡 Site link bridges allow replication across multiple site links when enabled.

</details>

---
