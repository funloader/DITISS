# Introduction

---
Learn about essential management and maintenance tasks for Active Directory Domain Services (AD DS) domain controllers, including their deployment, backup and recovery, and schema management. Find out about design considerations regarding the optimal number, roles, and location of domain controllers.

---


## Scenario
Contoso, Ltd. is a financial services company in Seattle with major offices located throughout the world. Most of its compute environment runs on-premises on Windows Server. This includes virtualized workloads on Windows Server 2016 hosts.

Contoso's IT staff are migrating Contoso on-premises servers to Windows Server 2025. As part of the migration, Contoso plans to expand into additional sites and use virtualization to help expedite bringing a new site online. The company is also generating larger volumes of data with plans for even more data in the future. Because of this, the company needs flexible storage options. Finally, Contoso plans to increase their use of virtualization to optimize their computing environment because many physical servers are underutilized.

As a newly hired Windows Server administrator, you're responsible for managing and maintaining Active Directory Domain Services (AD DS) operations, including domain controller deployments, and AD DS backup and recovery. You also need to identify and implement the optimal placement of such AD DS roles as operation masters or global catalog. In addition, you've been asked to implement custom schema extensions to accommodate deployment of a newly developed in-house application.

After completing this module, you'll understand how to accomplish these tasks.

### Learning objectives

After completing this module, you'll be able to:

- Deploy and maintain AD DS domain controllers.
- Describe the AD DS global catalog role and its placement considerations.
- Describe AD DS operations master roles, their placement considerations, and their management tasks.
- Describe the AD DS schema and its management tasks.

### Prerequisites
To get the best learning experience from this module, it's important that you have knowledge and experience of the following areas:

- Windows Server administration.
- Core networking technologies.
- AD DS.

---

# Deploy AD DS domain controllers

Domain controllers authenticate all users and computers in a domain. Therefore, it's critical to ensure the optimal number and placement of domain controllers in any AD DS environment, especially in larger, distributed environments such as the one that Contoso is transitioning to.

### Deploy AD DS domain controllers in an on-premises environment

The domain controller deployment process has two steps. First, you install the binaries necessary to implement the domain controller role. For this purpose, you can use Windows Admin Center or Server Manager. At the end of the initial installation process, you have installed the AD DS files, but not yet configured AD DS on the server. The second step is to configure AD DS role. The simplest way to perform this configuration is by using the Active Directory Domain Services Configuration Wizard. You start the wizard by selecting the AD DS link in Server Manager.

As part of AD DS role configuration, you need to provide answers to the questions in the following table:

# Active Directory Domain Services Deployment Questions

| **Question** | **Comments** |
|-------------|--------------|
| Are you installing a new forest, a new tree, or an additional domain controller for an existing domain? | Answering this question determines what additional information you might need, such as the parent domain name. |
| What is the Domain Name System (DNS) name for the AD DS domain? | When you create the first domain controller for a domain, you must specify the fully qualified domain name (FQDN). When you add a domain controller to an existing domain or forest, you use the existing domain name. |
| Which level will you choose for the forest functional level? | The forest functional level determines the available forest features and the supported domain controller operating system (OS). This also sets the minimum domain functional level for the domains in the forest. |
| Which level will you choose for the domain functional level? | The domain functional level determines the domain features that will be available and the supported domain controller operating systems. |
| Will the domain controller be a DNS server? | You can install the DNS role as part of the domain controller deployment. |
| Will the domain controller host the global catalog? | This option is selected by default. |
| Will the domain controller be a read-only domain controller (RODC)? | This option isn't available for the first domain controller in a forest. |
| What will be the Directory Services Restore Mode (DSRM) password? | This is necessary for restoring AD DS database objects from a backup. |
| What is the NetBIOS name for the AD DS domain? | When you create the first domain controller for a domain, you must specify the NetBIOS name for the domain. |
| Where will the database, log files, and SYSVOL folders be created? | By default, the database and log files folder is located at `C:\Windows\NTDS`. The SYSVOL folder is located at `C:\Windows\SYSVOL`. |

![Diagram](images/m7-addc-deployment-configuration-dfd90c9e.png).

### Install a domain controller on a Server Core installation of Windows Server
A Windows Server computer that is running a Server Core installation doesn't have the Server Manager graphical user interface (GUI). Therefore, you must use alternative methods to install the files for the domain controller role, and to install the domain controller role itself. You can use Windows Admin Center, Server Manager, Windows PowerShell, or Remote Server Administration Tools (RSAT) installed on any supported version of Windows Server that has the Desktop Experience feature, or any supported Windows client such as Windows 10.

### Install a domain controller from media
If you have a network connection between sites that is slow, unreliable, or costly, you might find it beneficial to add another domain controller at a remote location or branch office. In this scenario, to significantly reduce the amount of traffic moving over the wide area network (WAN) link, you can create an AD DS backup (perhaps to a USB drive) and take this backup to the remote location. When you're at the remote location and run Server Manager to install AD DS, you can select the Install from media option. Most of the copying occurs locally. In this scenario, the WAN link transfers only security-related traffic and AD DS changes following the backup. The WAN link also helps ensure that the new domain controller receives any changes made to the central AD DS after you created the Install from media backup.

### Branch office considerations
When you deploy a domain controller in a branch office that can't guarantee physical security, you can use additional measures to reduce the impact of a security breach. One option is to deploy an RODC. The RODC contains a read-only copy of the AD DS database, and by default, it doesn't cache any user passwords. However, you can configure the RODC to cache the passwords for users in the branch office. If an RODC is compromised, the potential loss of information risk is lower than with a full read/write domain controller.

### Upgrade domain controllers from the previous version
The process for upgrading a domain controller is the same for any version of Windows Server starting with Windows Server 2012 R2 through Windows Server 2025. You can upgrade to a Windows Server 2025 domain using either of the following methods:
- Upgrade the OS on existing domain controllers that are running Windows Server 2012 R2 or later.
- Add servers running Windows Server 2025 as domain controllers in a domain that already has domain controllers running earlier Windows Server versions.
We recommend the latter method, because when you finish you have a clean installation of both the Windows Server 2025 OS and the AD DS database. Whenever you add a new domain controller, Windows Server automatically updates the domain DNS records so clients are able to locate and use this domain controller.

### Deploy AD DS domain controllers in Azure virtual machines (VMs)
Azure provides infrastructure as a service (IaaS), which is a cloud-based virtualization platform. When deploying AD DS on Azure IaaS, you're installing the domain controller on a VM, so all the rules that apply to virtualizing a domain controller apply to deploying AD DS in Azure.

When you implement AD DS in Azure, consider the following:
- Network topology. To meet AD DS requirements, you must create an Azure Virtual Network and attach your VMs to it. If you intend to join an existing on-premises AD DS infrastructure, you can extend network connectivity to your on-premises environment. You can achieve this through hybrid connectivity methods such as a virtual private network (VPN) connection or an Azure ExpressRoute circuit, depending on the speed, reliability, and security that your organization requires.
- Site topology. As with a physical site, you should define and configure an AD DS site that corresponds to the IP address space of your Azure Virtual Network.
- IP addressing. All Azure VMs receive Dynamic Host Configuration Protocol (DHCP) addresses by default, but you can configure static addresses that will persist across restarts and shutdowns.
- DNS. Azure's built-in DNS does not meet the requirements of AD DS, such as Dynamic DNS and service (SRV) resource records. To provide DNS functionality for an AD DS environment in Azure, you can use the Windows Server DNS server role or other DNS solutions available in Azure, such as Azure private DNS zones.
- Disks. You have control of caching Azure VM disk configurations. When you install AD DS to an Azure VM, you should place the NTDS.DIT and SYSVOL files on one of its data disks, and set the Host Cache Preference setting of that disk to NONE.

### Maintain AD DS domain controllers

There are operational aspects applicable to every AD DS environment that focus on maintaining business continuity of the authentication services. This includes backup and recovery of domain controllers, and the AD DS objects they host.

### Maintain AD DS domain controller availability
Domain controllers use a multi-master replication process to copy data from one domain controller to another. As a best practice, an AD DS domain should have at least two domain controllers per AD DS site. This makes the AD DS database more available and spreads the authentication load during peak sign-in times.

> [!IMPORTANT]
> For most enterprises, consider two domain controllers per geographical region as the absolute minimum to help ensure high availability and performance.

### Plan for AD DS backup and restore
Maintaining the reliability of the Active Directory data is important. Performing regular backups can play a part in this process but knowing how to restore or recover data after a failure is vital.

### Restoring deleted AD DS objects by using Recycle Bin
Because restoring objects deleted from AD DS by using traditional backup methods involves temporary OS downtime, Windows Server offers the Active Directory Recycle Bin feature, which provides a straightforward method to restore deleted objects with no AD DS downtime. After you enable Active Directory Recycle Bin, the Deleted Objects container displays in Active Directory Administrative Center. Deleted objects persist in this container until their deleted object lifetime expires. For new AD DS deployments, that lifetime is set to 180 days, but you have the option to change it. You can choose to restore the objects either to their original location or to an alternate location within AD DS.

> [!IMPORTANT]
> You can't use Active Directory Recycle Bin to revert changes to existing objects. In such cases, you must use the traditional methods of backing up and restoring AD DS.

### AD DS backup and restore
To restore AD DS, a backup must explicitly include system state data. System state is a collection of critical OS and server role files that include the AD DS database and the registry.

> [!IMPORTANT]
> A full server backup that is used for full server recovery doesn't support this scenario.

To perform an AD DS restore, you must have full access to the files on the domain controller. This requires restarting the domain controller in DSRM. If you're restarting a domain controller locally, open the advanced startup options and choose the DSRM from the menu.

When you start a domain controller in DSRM, you sign in as Administrator with the DSRM password. You then can use Windows Server Backup to restore the directory database. After completing the restore process, you must restart the server you're recovering. The domain controller ensures that its database is consistent with the rest of the domain by pulling from its replication partners the changes to the directory that have occurred since the date of the backup.

### Nonauthoritative restore
By default, you restore an AD DS backup as of a known good date. Essentially, you roll the domain controller back in time. When AD DS restarts on the domain controller, the domain controller contacts its replication partners and requests all subsequent updates. In other words, the domain controller catches up with the rest of the domain by using standard replication mechanisms.

This type of restore is useful when the directory on a domain controller has been damaged or corrupted, but the problem has not spread to other domain controllers. However, in some scenarios, this approach is not suitable. For example, this won't enable you to recover an object you deleted after the backup took place, if that deletion has replicated to other domain controllers. If you restore a known good version of AD DS and restart the domain controller, the deletion that happened after the backup took place will simply replicate back to the domain controller.

### Authoritative restore
An authoritative restore allows you to restore a known good copy of AD DS objects, which replaces the current version of these objects in the AD DS database. In an authoritative restore, you start with the same sequence of steps as the nonauthoritative restore. However, before you restart the domain controller, you mark the restored objects that you want to persist as authoritative, so they'll replicate from the restored domain controller outbound to its replication partners.

### Manage the AD DS Global Catalog role
As part of planning for domain controller deployments, it's important to identify the optimal number and placement of the global catalog role. This becomes relevant when expanding AD DS environment to other locations, as is the case with Contoso's planned expansion.

### Manage the AD DS global catalog role
The global catalog is a partial, read-only, searchable copy of all the objects in a forest. The global catalog can help speed up searches for objects that might be stored on domain controllers in a different domain in the forest.

Within a single domain, the AD DS database on each domain controller contains all the information about every object in that domain. However, only a subset of this information replicates to the global catalog servers in other domains in the forest. Within a domain, a query for an object is directed to one of the domain controllers in that domain. However, that query doesn't return results about objects in other domains within the forest. For a query to include results from other forest domains, you must query a domain controller that is also a global catalog server.

The *global catalog* doesn't contain all the attributes for each object. Instead, it maintains the subset of attributes that are most likely to be useful in cross-domain searches. These attributes include, for example, givenName, displayName, and mail. You can change the set of attributes replicated to the global catalog by modifying the AD DS schema.

In a multiple-domain forest, searching the global catalog can be useful in many situations. For example, when a server that's running Microsoft Exchange Server receives an incoming email, it must search for the recipient’s account so it can decide how to route the message. By automatically querying the global catalog, the server can find the recipient in a multiple-domain environment. Additionally, when users sign in to their Active Directory accounts, the domain controller that performs the authentication must contact the global catalog to check for universal group memberships before authenticating the users.

In a single domain, you should configure all the domain controllers to have a copy of the global catalog. In multiple-domain and multiple-site forests, it might sometimes make sense to limit the number of domain controllers hosting the global catalog role to reduce the volume of replication traffic, although this is an uncommon scenario. Note, however, that this will introduce dependency on connectivity to other sites when performing global catalog queries.

> [!TIP]
> Consider configuring every domain controller as a global catalog unless you must reduce replication traffic volume.

### Manage AD DS operations masters
AD DS uses a multiple-master process to copy data between domain controllers, and automatically implements a conflict resolution algorithm that remediates simultaneous, conflicting updates. These provisions allow for a distributed management model, where multiple users and applications can concurrently apply changes to AD DS objects on different domain controllers. Such a model is necessary to support any AD DS environment with two or more domain controllers. However, it's critical for larger, distributed environments such as Contoso's. It's important to remember though, that certain operations can be performed only by a specific role, on a specific domain controller.

### What are AD DS operations masters?
AD DS operation master roles are responsible for performing operations that aren't suitable for a multiple-master model. A domain controller that has one of these roles is an operations master. An operations master role is also known as a Flexible Single Master Operation (FSMO) role. There are five operations master roles:
- Schema master
- Domain-naming master
- Infrastructure master
- RID master
- PDC emulator master
By default, the first domain controller installed in a forest hosts all five roles. However, you can transfer these roles after deploying additional domain controllers. When performing operations master-specific changes, you must connect to the domain controller with the role. The five operations master roles have the following distribution:

- Each forest has one schema master and one domain naming master.
- Each AD DS domain has one relative ID (RID) master, one infrastructure master, and one primary domain controller (PDC) emulator.
You can place all five on a single domain controller, or distribute them across several domain controllers.

### Forest operations masters
A forest has the following operations master roles:
- Domain naming master. This is the domain controller that you must contact when you add or remove a domain or make domain name changes.

> [!IMPORTANT]
> If the domain naming master is unavailable, you won't be able to add domains to the forest.

Schema master. This is the domain controller in which you make all schema changes.

> [!NOTE]
> The Windows PowerShell command `Get-ADForest`, from the Active Directory module for Windows PowerShell, displays the forest properties, including the current domain naming master and schema master.

### Domain operations masters
A domain has the following operations master roles:
- RID master. Whenever you create a security principal such as a user, computer, or group in AD DS, the domain controller where you created the object assigns the object a unique identifying number known as a security ID (SID). To ensure that no two domain controllers assign the same SID to two different objects, the RID master allocates blocks of RIDs to each domain controller within the domain to use when building SIDs.

> [!IMPORTANT]
> If the RID master is unavailable, you might experience difficulties adding security principals to the domain. Also, as domain controllers use their existing RIDs, they eventually run out of them and are unable to create new objects.

> [!IMPORTANT]
> If the infrastructure master is unavailable, domain controllers that aren't global catalogs won't be able to perform translation of SIDs security principal names.

> [!IMPORTANT]
> The infrastructure master role shouldn't reside on the domain controller that's hosting the global catalog role unless every domain controller in the forest is configured to serve as a global catalog. In this case, the infrastructure master role isn't necessary because every domain controller knows about every object in the forest.

- PDC emulator master. The domain controller that is the PDC emulator master serves as the time source for the domain. The PDC emulator master in each domain in a forest synchronizes their time with the PDC emulator master in the forest root domain. You set the PDC emulator master in the forest root domain to synchronize with a reliable external time source. Additionally, by default, changes to Group Policy Objects (GPOs) are by default written to the PDC Emulator master. The PDC emulator master is also the domain controller that receives urgent password changes. If a user's password changes, the domain controller with the PDC emulator master role receives this information immediately. This means that if the user tries to sign in, the domain controller in the user's current location contacts the domain controller with the PDC emulator master role to check for recent changes. This occurs even if a domain controller in a different location that hadn't yet received the new password information authenticated the user.

> [!IMPORTANT]
> If the PDC emulator master is unavailable, users might have trouble signing in until their password changes have replicated to all the domain controllers.

>  [!NOTE]
> The Windows PowerShell command `Get-ADDomain`, from the Active Directory module for Windows PowerShell, displays the domain properties, including the current RID master, infrastructure master, and PDC emulator master.

### Manage AD DS operations masters
In an AD DS environment where you distribute operations master roles among domain controllers, you might need to move a role from one domain controller to another. When you perform a move in a planned manner between two online domain controllers, the move is known as transferring the role. In emergencies, if the current role holder isn't available, the move is known as seizing the role. When you transfer a role, the latest data from the domain controller in that role replicates to the target server.

> [!IMPORTANT]
> You should seize a role only as a last resort when there's no chance for recovering the current role holder.

### Transfer operations master roles
You can transfer operations master roles by using the AD DS snap-ins that the following table lists.

# FSMO Roles and Management Snap-ins

| **Role** | **Snap-in** |
|--------|-------------|
| Schema Master | Active Directory Schema |
| Domain Naming Master | Active Directory Domains and Trusts |
| Infrastructure Master | Active Directory Users and Computers |
| RID Master | Active Directory Users and Computers |
| PDC Emulator Master | Active Directory Users and Computers |

### Seize operations master roles
You cannot use AD DS snap-ins to seize operations master roles. Instead, you must use either the ntdsutil.exe command-line tool or Windows PowerShell to seize roles.

> [!NOTE]
> You can also use these tools to transfer roles.

The syntax for transferring a role and seizing a role is similar within Windows PowerShell, as the following syntax line demonstrates:
```
Move-ADDirectoryServerOperationsMasterRole -Identity "<servername>" -OperationsMasterRole "<rolenamelist>" -Force
```

For the preceding syntax, the noteworthy definitions are as follows:

- servername. The name of the target domain controller to which you're transferring one or more roles.
- rolenamelist. A comma-separated list of AD DS role names to move to the target server.
- -Force. An optional parameter that you include to seize a role instead of transferring it.

### Demonstration
The following video demonstrates how to:
- Identify placement of operations master roles.
- Transfer operations master roles between domain controllers.

The main steps in the process are:
1. Create AD DS environment. Create a single domain AD DS forest containing two domain controllers.
2. Check the placement of operations master roles. Identify which of the two domain controllers hosts the operations master roles.
3. Transfer operations master roles between domain controllers by using the GUI tools. Use the GUI tools to transfer the operations masters roles from the domain controller you identified in the previous step to the other one.
4. Transfer operations master roles between domain controllers by using command-line tools. Use the command-line tools to transfer the operations masters roles back to the first domain controller.

5. ## Check your knowledge

### 1. What tool allows the transfer of the Infrastructure Master operations master role?

- [ ] `Active Directory Users and Computers`
- [ ] `Active Directory Domains and Trusts`
- [ ] `Active Directory Schema`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `Active Directory Users and Computers`  
💡 You can use Active Directory Users and Computers to transfer all the domain-level masters roles.
</details>

### Manage AD DS schema
Many applications and services utilize data that's stored in an AD DS database. Some of them, such as Contoso's newly developed in-house application that you need to implement, require that data to be in a specific format. This, in turn, might require extending AD DS schema.

### What is a schema?
AD DS stores and retrieves information from a wide variety of applications and services. It does this, in part, by standardizing how the AD DS directory stores data. By standardizing data storage, AD DS can retrieve, update, and replicate data while helping to maintain data integrity.

An AD DS schema is the component that defines all the object classes and attributes that AD DS uses to store data. All domains in a forest contain a copy of the schema that applies to that forest. Any change in the schema replicates to every domain controller in the forest via their replication partners. However, changes originate at the schema master.

### Objects
AD DS uses objects as units of storage. The schema defines all object types. Each time the directory manages data, the directory queries the schema for an appropriate object definition. Based on the object definition in the schema, the directory creates the object and stores the data.

Object definitions specify both the types of data that the objects can store and the data syntax. You can only create objects that the schema defines. Because objects store data in a rigidly defined format, AD DS can store, retrieve, and validate the data that it manages, regardless of which application supplies it.

### Relationships among objects, rules, attributes, and classes
AD DS schema objects consist of attributes, which are grouped together into classes. Each class has rules that define which attributes are mandatory and which are optional. For example, the user class consists of more than 400 possible attributes, including cn (the common name attribute), givenName, displayName, objectSID, and manager. Of these attributes, the cn and objectSID attributes are mandatory.

The user class is an example of a structural class. A structural class is the only type of class that can have objects in an AD DS database. To modify the schema, you can create an auxiliary class with its own attributes, and then reference it in the definition of a structural class.
![Diagram](images/m7-addc-schema-e20bdbe5.png).

> [!IMPORTANT]
> AD DS schema doesn't support deletions.

You should change the schema only when necessary because the schema controls the storage of information. Additionally, any changes made to the schema affect every domain controller. Before you change the schema, you should review the changes and implement them only after you've performed testing. This helps ensure that the changes Won't adversely affect the rest of the forest or any applications that use AD DS.
![Diagram](images/m7-update-schema-12083aa2.png).

## Check your knowledge

### 1. Which tool can you use to trigger an AD DS schema update?

- [ ] `ADSIEDIT.MSC`
- [ ] `Active Directory Schema console`
- [ ] `Active Directory Users and Computers console`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `ADSIEDIT.MSC`  
💡 In the ADSI.MSC console, you can right-click or access the context menu on the Schema container, and then select Update Schema now. This will trigger an update.
</details>

### Summary

Using the knowledge acquired in this module, you deployed AD DS domain controllers in the manner that ensured the optimal placement of operation masters and global catalog roles. You also applied custom AD DS schema extensions to accommodate deployment of a new in-house developed application.
