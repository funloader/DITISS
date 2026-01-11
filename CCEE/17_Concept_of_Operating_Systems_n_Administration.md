> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 17 


## **Session 18: Concept of Exchange server**

---

### 1. An enterprise wants a centralized platform that supports secure email, shared calendars, contacts, and task management with Active Directory integration. Which Microsoft product best fulfills this requirement?

* [ ] File Server
* [ ] SharePoint Server
* [ ] Microsoft Exchange Server
* [ ] Skype for Business Server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Microsoft Exchange Server
💡 Exchange Server is designed for enterprise-grade email communication, calendaring, contacts, and collaboration tightly integrated with Active Directory.

</details>

---

### 2. Your organization plans to deploy Microsoft Exchange Server 2019. Which underlying operating system is officially supported and required for installation?

* [ ] Linux (RHEL)
* [ ] macOS Server
* [ ] Windows Server
* [ ] Android Enterprise OS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Windows Server
💡 Exchange Server is a Microsoft enterprise application that runs exclusively on supported Windows Server editions.

</details>

---

### 3. During mail flow troubleshooting, you observe that outgoing emails are being queued before delivery to external domains. Which protocol is primarily responsible for sending emails from Exchange to the Internet?

* [ ] HTTP
* [ ] IMAP
* [ ] SMTP
* [ ] FTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SMTP
💡 SMTP (Simple Mail Transfer Protocol) is the standard protocol used by Exchange Transport services for sending emails.

</details>

---

### 4. A compliance team asks for features that help users manage meetings, block spam, and organize mail efficiently. Which Exchange feature set directly addresses this requirement?

* [ ] Document collaboration
* [ ] Email filtering and calendaring
* [ ] Spreadsheet automation
* [ ] Graphic design tools

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Email filtering and calendaring
💡 Exchange provides advanced mail filtering, scheduling, and calendaring as core messaging services.

</details>

---

### 5. An administrator wants to manage Exchange entirely via a web-based interface instead of MMC snap-ins. Which Exchange version first introduced the Exchange Admin Center (EAC)?

* [ ] Exchange 2007
* [ ] Exchange 2010
* [ ] Exchange 2013
* [ ] Exchange 2003

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Exchange 2013
💡 Exchange 2013 replaced ECP and EMC with the modern web-based Exchange Admin Center.

</details>

---

### 6. User authentication for mailbox access fails after a domain controller outage. Which tightly integrated Microsoft service is critical for Exchange authentication?

* [ ] Microsoft Teams
* [ ] OneNote
* [ ] Active Directory
* [ ] Microsoft Paint

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Active Directory
💡 Exchange relies entirely on Active Directory for authentication, authorization, and directory services.

</details>

---

### 7. A forensic investigation requires identifying where a specific user’s emails are physically stored within Exchange. Which Exchange component stores individual user messages?

* [ ] Public Folder
* [ ] Shared Drive
* [ ] Mailbox
* [ ] Calendar Object

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mailbox
💡 Each user is assigned a mailbox that stores emails, calendar items, contacts, and tasks.

</details>

---

### 8. Which Exchange Server role is directly responsible for mail routing, categorization, and delivery?

* [ ] Client Access Server
* [ ] Domain Controller
* [ ] Mailbox Server
* [ ] Edge Transport Server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mailbox Server
💡 Since Exchange 2016, the Mailbox role includes transport services handling mail flow.

</details>

---

### 9. An organization requires automatic failover between mailbox servers with minimal downtime. Which Exchange feature fulfills this requirement?

* [ ] RBAC
* [ ] Database Availability Group (DAG)
* [ ] Autodiscover
* [ ] Transport Rules

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Database Availability Group (DAG)
💡 DAG provides high availability by replicating mailbox databases across multiple servers.

</details>

---

### 10. Outlook clients outside the corporate network connect securely to Exchange without VPN. Which protocol enables this connectivity?

* [ ] FTP
* [ ] Telnet
* [ ] RPC over HTTP (Outlook Anywhere)
* [ ] SFTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RPC over HTTP (Outlook Anywhere)
💡 Outlook Anywhere allows secure Outlook connectivity over HTTPS.

</details>

---

### 11. During user login audits, which service does Exchange consult to verify credentials?

* [ ] IIS
* [ ] SQL Server
* [ ] Active Directory
* [ ] DNS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Active Directory
💡 Exchange does not maintain its own authentication database; it uses AD exclusively.

</details>

---

### 12. What is the **primary operational benefit** of deploying a DAG in Exchange?

* [ ] Faster mail delivery
* [ ] Centralized logging
* [ ] High availability and disaster recovery
* [ ] Enhanced GUI performance

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** High availability and disaster recovery
💡 DAG ensures mailbox resiliency during hardware or server failures.

</details>

---

### 13. In legacy Exchange versions, administrators managed user options using ECP. What does ECP stand for?

* [ ] Exchange Command Protocol
* [ ] Exchange Control Panel
* [ ] Email Configuration Portal
* [ ] External Connection Protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Exchange Control Panel
💡 ECP was used prior to EAC for administrative and user self-service tasks.

</details>

---

### 14. Which database file format is used to store mailbox data in Exchange?

* [ ] NTFS
* [ ] EDB
* [ ] MDF
* [ ] FAT32

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** EDB
💡 Exchange mailbox databases are stored in Extensible Storage Engine (.edb) format.

</details>

---

### 15. Which tool provides full administrative control of Exchange through scripting and automation?

* [ ] Command Prompt
* [ ] PowerShell
* [ ] Control Panel
* [ ] Registry Editor

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PowerShell
💡 Exchange Management Shell is built on PowerShell and is mandatory for many admin tasks.

</details>

---

### 16. What does OWA stand for in Microsoft Exchange?

* [ ] Office Web Access
* [ ] Outlook Web Access
* [ ] Online Web Application
* [ ] Outlook Windows App

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Outlook Web Access
💡 OWA allows users to access mailboxes through a web browser.

</details>

---

### 17. Which Exchange component enables secure synchronization of emails on mobile devices?

* [ ] MDM
* [ ] Exchange ActiveSync
* [ ] Microsoft Intune
* [ ] Group Policy

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Exchange ActiveSync
💡 ActiveSync manages mobile email, policies, and remote wipe functionality.

</details>

---

### 18. Which Transport service function is critical for mail delivery?

* [ ] Message encryption
* [ ] Mail routing
* [ ] User authentication
* [ ] Database indexing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mail routing
💡 Transport services determine message paths and delivery logic.

</details>

---

### 19. To allow outbound emails to reach external domains, which connector must be configured?

* [ ] Receive Connector
* [ ] Internal Connector
* [ ] Send Connector
* [ ] DNS Connector

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Send Connector
💡 Send Connectors route outbound emails to the Internet or partner systems.

</details>

---

### 20. A newly added user’s Outlook profile configures itself automatically. Which Exchange service enables this?

* [ ] DNS Manager
* [ ] Autodiscover
* [ ] Antivirus Service
* [ ] Event Viewer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Autodiscover
💡 Autodiscover automatically configures Outlook client settings.

</details>

---

### 21. Which security model controls administrative permissions within Exchange?

* [ ] ACL
* [ ] Role-Based Access Control (RBAC)
* [ ] Group Policy
* [ ] Local Administrator

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Role-Based Access Control (RBAC)
💡 RBAC ensures least-privilege administration using predefined roles.

</details>

---

### 22. What is the maximum number of mailbox databases supported by **Exchange Server 2019 Standard Edition**?

* [ ] 5
* [ ] 10
* [ ] 50
* [ ] 100

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 5
💡 Exchange 2019 Standard Edition supports up to 5 mounted databases.

</details>

---

### 23. Which PowerShell cmdlet is used to create a new mailbox database?

* [ ] New-MailDatabase
* [ ] Create-MailboxDB
* [ ] New-MailboxDatabase
* [ ] Add-Database

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** New-MailboxDatabase
💡 This is the official Exchange PowerShell cmdlet.

</details>

---

### 24. What is the primary security function of the Edge Transport role?

* [ ] Hosting mailboxes
* [ ] Managing Active Directory
* [ ] Protecting the organization from external threats
* [ ] Scheduling meetings

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Protecting the organization from external threats
💡 Edge Transport handles anti-spam and perimeter security.

</details>

---

### 25. What is the primary objective of an Exchange Hybrid deployment?

* [ ] Install Exchange on Linux
* [ ] Enable coexistence between on-premises and Exchange Online
* [ ] Block phishing emails
* [ ] Reduce licensing costs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enable coexistence between on-premises and Exchange Online
💡 Hybrid enables seamless mail flow, migration, and management.

</details>

---

### 26. Which file extension stores Exchange transaction logs?

* [ ] .edb
* [ ] .log
* [ ] .bak
* [ ] .tmp

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** .log
💡 Transaction logs ensure database consistency and recovery.

</details>

---

### 27. Which mechanism does Exchange use to replicate mailbox databases in a DAG?

* [ ] DFS
* [ ] File Copy
* [ ] Continuous Replication
* [ ] Volume Shadow Copy

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Continuous Replication
💡 Exchange uses log-based continuous replication for DAGs.

</details>

---

### 28. Which PowerShell cmdlet checks mailbox database replication health?

* [ ] Test-HealthDB
* [ ] Get-DatabaseStatus
* [ ] Test-ReplicationHealth
* [ ] Check-Mailbox

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Test-ReplicationHealth
💡 This cmdlet verifies DAG and database copy health.

</details>

---

### 29. Which tool is essential for migrating mailboxes to Microsoft 365 in a hybrid setup?

* [ ] Windows Migration Tool
* [ ] Azure AD Connect
* [ ] Exchange Admin Center
* [ ] Hybrid Configuration Wizard

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hybrid Configuration Wizard
💡 HCW establishes secure hybrid connectivity and migration readiness.

</details>

---

### 30. Which Exchange feature enforces restrictions on email and attachment size?

* [ ] Retention Policy
* [ ] Transport Rules
* [ ] Mailbox Quota
* [ ] Journaling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Mailbox Quota
💡 Mailbox quotas limit storage and attachment sizes per user.

</details>

---

## **Session 19 & 20: Power Shell**

---

### 1. A system administrator needs to automate repetitive configuration tasks across multiple Windows servers using a command-line environment that supports object-based output. Which Windows component best fulfills this requirement?

* [ ] Web browsing via Internet Explorer
* [ ] System administration and automation using PowerShell
* [ ] Graphic design using GDI+
* [ ] Game development using DirectX

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** System administration and automation using PowerShell
💡 PowerShell is designed specifically for task automation and configuration management using object-based pipelines.

</details>

---

### 2. While auditing a compromised system, an analyst wants to enumerate files and directories within a specific path using PowerShell. Which cmdlet supports this functionality?

* [ ] list
* [ ] open
* [ ] show
* [ ] dir

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** dir
💡 `dir` is an alias for `Get-ChildItem`, used to list files and directories in PowerShell.

</details>

---

### 3. During malware script analysis, you observe variables prefixed with a special symbol in PowerShell scripts. Which symbol denotes a variable?

* [ ] &
* [ ] %
* [ ] #
* [ ] $

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** $
💡 PowerShell variables are always prefixed with `$`, distinguishing them from literals.

</details>

---

### 4. PowerShell integrates deeply with which underlying technology to provide access to system components and APIs?

* [ ] ASP.NET
* [ ] VB.NET
* [ ] .NET Framework
* [ ] Mono

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** .NET Framework
💡 PowerShell is built on the .NET Framework, enabling access to CLR objects and assemblies.

</details>

---

### 5. Which of the following follows the approved **Verb-Noun** naming convention and is a valid PowerShell cmdlet?

* [ ] Copy-Content
* [ ] Delete-Dir
* [ ] Print-File
* [ ] Remove-Item

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Remove-Item
💡 PowerShell enforces standardized verb-noun cmdlet naming; `Remove-Item` complies fully.

</details>

---

### 6. An incident responder unfamiliar with a cmdlet wants to understand its syntax and usage. Which cmdlet should be used?

* [ ] Lists services
* [ ] Displays help for cmdlets
* [ ] Opens browser
* [ ] Installs software

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Displays help for cmdlets
💡 `Get-Help` provides syntax, parameters, and examples for PowerShell cmdlets.

</details>

---

### 7. From a language classification perspective, PowerShell is best described as a:

* [ ] Markup language
* [ ] Functional language
* [ ] Scripting language
* [ ] Assembly language

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Scripting language
💡 PowerShell is a task automation and scripting language optimized for administrative control.

</details>

---

### 8. A forensic investigator wants to list all currently running processes to identify suspicious activity. Which cmdlet should be used?

* [ ] Show-Process
* [ ] List-Tasks
* [ ] Get-Process
* [ ] Process-View

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Get-Process
💡 `Get-Process` retrieves information about processes currently running on the system.

</details>

---

### 9. Before executing scripts downloaded from the internet, a security analyst modifies PowerShell settings to prevent unauthorized execution. Which cmdlet is responsible?

* [ ] Controls command output
* [ ] Changes security settings for running scripts
* [ ] Opens the registry
* [ ] Installs updates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Changes security settings for running scripts
💡 `Set-ExecutionPolicy` controls script execution restrictions for security enforcement.

</details>

---

### 10. You need to filter service objects where the status is "Running". Which cmdlet is most appropriate?

* [ ] With the Select keyword
* [ ] With the Where-Object cmdlet
* [ ] With grep
* [ ] With cut

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** With the Where-Object cmdlet
💡 `Where-Object` filters objects based on property conditions in the pipeline.

</details>

---

### 11. What is the primary purpose of the Get-Service cmdlet?

* [ ] Starts a service
* [ ] Stops a service
* [ ] Lists services
* [ ] Deletes services

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Lists services
💡 `Get-Service` retrieves the status and configuration of Windows services.

</details>

---

### 12. While analyzing log files, which cmdlet reads file contents line by line?

* [ ] Get-File
* [ ] Read-Text
* [ ] Get-Content
* [ ] Show-File

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Get-Content
💡 `Get-Content` reads the contents of files, commonly used for logs and text analysis.

</details>

---

### 13. A script must create a directory during execution. Which cmdlet supports this requirement?

* [ ] Make-Dir
* [ ] New-Directory
* [ ] New-Item
* [ ] Create-Folder

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** New-Item
💡 `New-Item` is used to create files, directories, registry keys, and more.

</details>

---

### 14. Which syntax correctly assigns the value 10 to a variable?

* [ ] var = 10
* [ ] $x = 10
* [ ] x := 10
* [ ] let x = 10

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** $x = 10
💡 PowerShell uses `$variable = value` syntax for assignment.

</details>

---

### 15. What is the primary function of the pipeline (`|`) in PowerShell?

* [ ] Separates lines
* [ ] Chains cmdlets
* [ ] Comments code
* [ ] Ends a statement

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Chains cmdlets
💡 The pipeline passes object output from one cmdlet as input to another.

</details>

---

### 16. What is the default extension for PowerShell script files?

* [ ] .bat
* [ ] .ps1
* [ ] .exe
* [ ] .cmd

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** .ps1
💡 `.ps1` identifies executable PowerShell script files.

</details>

---

### 17. Which cmdlet is used to rename an existing file?

* [ ] Rename-File
* [ ] Change-Item
* [ ] Rename-Item
* [ ] Update-File

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Rename-Item
💡 `Rename-Item` modifies the name of files, folders, or other items.

</details>

---

### 18. Which cmdlet helps enumerate all available commands in PowerShell?

* [ ] Get-Cmdlet
* [ ] Get-Command
* [ ] List-Command
* [ ] Show-All

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Get-Command
💡 `Get-Command` lists cmdlets, functions, aliases, and scripts.

</details>

---

### 19. How do you comment a single line in PowerShell scripts?

* [ ] //
* [ ] --
* [ ] #
* [ ] ;;

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** #
💡 The `#` symbol denotes single-line comments in PowerShell.

</details>

---

### 20. A suspicious process must be terminated during live response. Which cmdlet is appropriate?

* [ ] Kill-Process
* [ ] Stop-Item
* [ ] End-Process
* [ ] Stop-Process

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Stop-Process
💡 `Stop-Process` safely terminates running processes.

</details>

---

### 21. What does the Out-File cmdlet do?

* [ ] Opens a file
* [ ] Outputs to a file
* [ ] Converts file format
* [ ] Displays file size

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Outputs to a file
💡 `Out-File` sends output to a file instead of the console.

</details>

---

### 22. Which PowerShell feature allows long-running commands to execute asynchronously?

* [ ] Threads
* [ ] Background jobs
* [ ] Pipelines
* [ ] Sessions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Background jobs
💡 Background jobs (`Start-Job`) enable non-blocking execution.

</details>

---

### 23. Which parameter ensures recursive deletion of directories?

* [ ] -Full
* [ ] -DeleteAll
* [ ] -Recurse
* [ ] -Recursive

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** -Recurse
💡 `-Recurse` allows deletion of all child items.

</details>

---

### 24. What is a PSDrive in PowerShell?

* [ ] A mounted USB
* [ ] A logical drive letter
* [ ] A data provider mapped like a file system
* [ ] A virtual hard disk

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A data provider mapped like a file system
💡 PSDrives abstract data stores like registry, certificates, or file systems.

</details>

---

### 25. How do you correctly define a function in PowerShell?

* [ ] def functionname()
* [ ] func name {}
* [ ] function name {}
* [ ] define name()

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** function name {}
💡 PowerShell functions use the `function` keyword with script blocks.

</details>

---

### 26. What information does `$PSVersionTable` provide?

* [ ] Shows OS version
* [ ] Lists installed cmdlets
* [ ] Displays PowerShell version info
* [ ] Starts the shell

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Displays PowerShell version info
💡 `$PSVersionTable` shows PowerShell engine and platform details.

</details>

---

### 27. What is the primary purpose of Invoke-Command?

* [ ] Calling a DLL
* [ ] Executing a command remotely
* [ ] Installing a module
* [ ] Parsing input

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Executing a command remotely
💡 `Invoke-Command` supports PowerShell Remoting across systems.

</details>

---

### 28. How can a module be loaded into the current PowerShell session?

* [ ] Import-File
* [ ] Load-Module
* [ ] Import-Module
* [ ] Add-Cmdlet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Import-Module
💡 `Import-Module` loads cmdlets and functions from modules.

</details>

---

### 29. Which cmdlet allows the creation of a user-defined shortcut for an existing command?

* [ ] Set-Alias
* [ ] Define-Cmdlet
* [ ] Register-Command
* [ ] Add-Command

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Set-Alias
💡 `Set-Alias` maps a custom name to an existing cmdlet or command.

</details>

---

### 30. Which cmdlet converts PowerShell objects into JSON format for API communication?

* [ ] ConvertTo-XML
* [ ] ConvertTo-JSON
* [ ] Convert-Object
* [ ] Format-JSON

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ConvertTo-JSON
💡 `ConvertTo-JSON` serializes objects for REST APIs and data exchange.

</details>

---
