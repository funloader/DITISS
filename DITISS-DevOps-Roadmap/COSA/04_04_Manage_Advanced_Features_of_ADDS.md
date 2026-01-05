# Introduction
---
Learn about advanced Active Directory Domain Services administration tasks, including creating trust relationships, implementing Enhanced Security Administrative Environment (ESAE) forests, monitoring and troubleshooting AD DS replication, and creating custom AD DS partitions.

---
## Scenario

Contoso, Ltd. is a financial services company in Seattle with major offices located throughout the world. Most of its compute environment runs on-premises on Windows Server. This includes virtualized workloads on Windows Server 2016 hosts.

Contoso's IT staff are migrating Contoso on-premises servers to Windows Server 2025. As part of the migration, Contoso plans to expand into additional sites and use virtualization to help expedite bringing a new site online. The company is also generating larger volumes of data with plans for even more data in the future. Because of this, the company needs flexible storage options. Finally, Contoso plans to increase the use of virtualization to optimize their computing environment because many physical servers are underutilized.

As part of its technology expansion and modernization initiative, Contoso plans to consolidate its existing AD DS environment comprising several isolated AD DS forests, starting with the creation of trust relationships between them. Another major change that’s scheduled to take place in the upcoming months is a setup of an ESAE forest. Additionally, to facilitate deployment of a new in-house developed suite of applications, it’s necessary to create a custom AD DS partition.

As an experienced Windows Server administrator, you’re responsible for planning and implementing these changes. Throughout their implementation, you also need to ensure that the environment you manage remains fully operational. This includes monitoring and troubleshooting AD DS replication.

### Learning objectives
After completing this module, you'll be able to:

* Identify the purpose, types, and the process of creating trust relationships.
* Describe the purpose and the process of implementing ESAE forests.
* Monitor and troubleshoot AD DS replication.
* Identify the purpose and the process of creating custom AD DS partitions.

### Prerequisites
To get the best learning experience from this module, you should have knowledge and experience of the following areas:

* Windows Server administration.
* Core networking technologies.
* Implementing and managing AD DS.

---
# Create trust relationships

An AD DS forest represents a security boundary, providing secure authentication and authorization for its users, computers, and applications. Sometimes, it might be necessary to extend this boundary to include other AD DS domains and forests. This, for example, might result from mergers and acquisitions between organizations, or from consolidation initiatives, as is the case with Contoso.

### What is a trust relationship?
AD DS trusts enable access to resources in a multiple-domain and multiple-forest AD DS environment. In a single-domain forest, all users and resources, such as file shares, printers, or applications share the same domain, so access management is straightforward and readily available. When you have multiple domains or forests, you need trusts to provide users in one domain with secure access to resources in another domain.

In a multiple-domain AD DS forest, by default, domains form a tree-like structure with a two-way transitive trust relationship between directly adjacent domains. Trust transitivity implies that a path of trust exists between all the AD DS domains in the same forest. Additionally, you can create other types of trusts. The following table describes the main trust types.

| Trust Type | Trust Characteristics | Direction | Description |
|------------|----------------------|-----------|-------------|
| **External** | Nontransitive | One-way or two-way | Enables resource access with an individual AD DS domain in another forest. |
| **Realm** | Transitive or nontransitive | One-way or two-way | Establishes an authentication path between a Windows Server AD DS domain and a Kerberos v5 realm implemented using a directory service other than AD DS. |
| **Forest (complete or selective)** | Transitive | One-way or two-way | Allows two forests to share resources. |
| **Shortcut** | Nontransitive | One-way or two-way | Reduces the time required to authenticate between two non-adjacent domains in the same multi-domain AD DS forest. |

![Diagram](images/m9-shortcut-trust-cafa4e1c.png).

> [!NOTE]
> Forest trust relationships provide most flexibility from the authentication standpoint. They're also easier to establish, maintain, and administer than separate trust relationships between external, domain-level trusts and individual domains across the two forests.

![Diagram](images/m9-forest-trust-5cc921f4.png).

### Create and configure forest trust relationships

If the AD DS environment contains multiple forests, it's possible to set up one-way or two-way trust relationships between any pair of forests. With a one-way forest trust, you can grant users in the trusted forest access to resources in the trusting forest. With a two-way forest trust, it becomes possible to grant users on each side of the trust access to resources in the other forest.

When creating a trust, you specify the root domain of each forest. However, because forest trusts are transitive for all domains in each forest, you effectively establish a trust between each pair of domains across both forests. However, unlike trusts between multiple domains in the same forest, forest trusts aren't transitive across multiple forests. Forest trusts can only be created between two forests and can't be implicitly extended to a third forest. This means that if you create a forest trust between Forest 1 and Forest 2 and you create a forest trust between Forest 2 and Forest 3, Forest 1 doesn't implicitly trust Forest 3.

Forest trusts are useful in scenarios that involve cross-organization collaboration, mergers and acquisitions, or within a single organization that has more than one forest in which to isolate Active Directory data and services. Forest trusts are also useful for application service providers, for collaborative business extranets, and for organizations that want a solution for administrative autonomy.

Before you can implement a forest trust, you need to ensure that DNS name resolution exists between the forests. To implement such name resolution, you can use several different DNS resolution techniques, such as secondary zones, stub zones, or conditional forwarding.

### Configuring advanced AD DS trust settings

In some cases, you might want to limit the scope of trust relationships to minimize the possibility of unauthorized access to resources in your forest. Several technologies can help you accomplish this goal.

### SID filtering

By default, when you establish a forest or domain trust, you can enable a domain quarantine, also known as SID filtering. When a user authenticates in a trusted domain, the user presents an authorization request that includes the SID attributes of all groups to which the user belongs. Additionally, the user's authorization request includes the SID-History attribute of the user and the user's groups. SID filtering blocks the use of SIDs present in SID-History that don't originate from the trusted domain. This prevents a potential exploit that involves tempering with the SID-History attribute to gain unauthorized access to resources in the trusted domain.

### Selective authentication
When you create a forest trust, you can manage the scope of authentication of trusted security principals. There are two modes of authentication for an external or forest trust:

* Forest-wide authentication.
* Selective authentication.

Choosing the forest-wide authentication enables all users in the trusted forest to authenticate for services and access on all computers in the trusting forest. Therefore, it's possible for resource administrators in the trusting forest to grant users from the trusted forest permissions to resources in the local forest. Additionally, all users from a trusted forest are considered Authenticated Users in the trusting forest. Effectively, any resource that grants permissions to Authenticated Users becomes accessible by users in the trusted forest.

If you choose selective authentication, users in the trusted forest aren't considered Authenticated Users in the trusting forest. Instead, you have to explicitly designate computers that they are able to authenticate to by granting them the Allowed to Authenticate permission on those computers. For example, imagine that you have a forest trust with a partner organization's forest. You want to ensure that only users from the partner organization's marketing group can access shared folders on a specific file server. To do so, you can configure selective authentication for the trust relationship and then grant the trusted users the right to authenticate only to that one file server.

> [!NOTE]
> When using selective authentication, in addition to the right to authenticate, users from the trusted forest still need file-system and folder-level permissions on the shared folders to access their content.


### how to Configure prerequisites for trust relationships & Create a trust relationship.
The main steps in the process are:

1. Create two AD DS forests. Deploy two domain controllers, with each one in a separate forest. Make sure that their names don't match.
2. Configure DNS conditional forwarding. Configure DNS conditional forwarding on each AD DS Domain controller to provide DNS name resolution across forests.
3. Create a forest trust relationship from the first forest to the second one. Use Active Directory Domains and Trusts to establish one-way trust relationship from the first forest to the second forest.
4. Create a forest trust relationship from the second forest to the first one. Use Active Directory Domains and Trusts to establish one-way trust relationship from the second forest to the first forest.

---

# Implement ESAE forests

As IT environments expand beyond the boundaries of internal networks, the role of identity as a security perimeter becomes increasingly important. One way to enhance its security capabilities is to implement the ESAE forest model, which is what Contoso is planning to do in the upcoming months.

### What is ESAE forest?

ESAE forests represent an architectural approach in which a dedicated administrative Active Directory forest hosts privileged accounts, privileged groups, and privileged access workstations. This ESAE forest is configured with a one-way trust relationship with a production forest. A one-way trust relationship means that accounts from the ESAE forest can be used in the production forest, however, accounts in the production forest can't be used in the ESAE forest. A production forest is a forest in which administrators perform an organization’s day-to-day activities. The production forest is then configured so that administrative tasks in the production forest can be performed only by using accounts that the ESAE forest hosts.

![Diagram](images/m9-esae-forests-1edb7143.png).

ESAE forests have the following benefits:

* Locked-down accounts. Standard nonprivileged user accounts in the ESAE forest can be configured as highly privileged in the production forest. For example, a standard user account in the ESAE forest is a member of the Domain Admins group in a domain in the production forest. It's possible to lock down the standard user account hosted in the ESAE forest so that it can't sign in to hosts in the ESAE forest and can only be used to sign in to hosts in the production forest. This design is more secure if an account is compromised while it is used in the production forest, because the malicious hacker can't use that account to perform administrative tasks in the ESAE forest.
* Selective authentication. ESAE forest design allows organizations to leverage the trust relationship’s selective authentication feature. For example, sign-ins from the ESAE forest will be restricted to specific hosts in the production forest. This is another method that helps limit credential exposure. For example, you can limit credential exposure when you configure selective authentication so that privileged accounts in the production forest can only be used on privileged access workstations or jump servers.
* Simple way to improve security. ESAE forest design provides substantive improvement in the security of existing production forests without requiring complete rebuilding of the production environment. The ESAE forest approach has a small hardware/software footprint and affects only IT Operations team users. In this design, standard user accounts remain hosted in the production forest. Only privileged administrative accounts are hosted in the ESAE forest. Because they're hosted in a separate forest, privileged administrative accounts can be subject to more stringent security requirements than standard user accounts in the production forest.

### What is the clean-source principle?

The clean-source principle specifies that all security dependencies are as trustworthy as the item being secured. In the context of ESAE forests, the clean-source principle involves ensuring that all of the security accounts and workstations that are used to perform administrative tasks are trustworthy.

The clean-source principle is an important aspect of security because, if a malicious hacker can control a security dependency, the hacker also can control the item being secured. One reason for using the ESAE forest design approach is that it helps secure the privileged accounts that manage the production environment.

When securing the ESAE forest, ensure that ESAE domain controllers are running on a secure virtualization fabric and that security technologies such as device guard, credential guard, and BitLocker are in use. The clean-source principle also applies to installation media. If installation media is infected, then all software and operating systems that are deployed from that installation media are untrustworthy and at risk for control by the hacker. Software obtained from vendors through physical media needs to be validated. Software downloaded from the Internet should be checked against vendor-provided file hashes to ensure that it hasn't been tampered with by unauthorized third parties.

> [!TIP]
> You can use the certutil.exe command, built into the Windows operating system, to compare a downloaded file with the hash file that the vendor provided.

### Implementing ESAE forests
You should consider several factors when implementing an ESAE forest. An ESAE forest should have the following properties:
* Limit the function of the ESAE forest to hosting accounts of administrative users for the production forest. To keep the hacker surface minimized, don't deploy applications or additional resources in the ESAE forest.
* The ESAE forest should be a single-domain Active Directory forest. There's no need for multiple domains in an ESAE forest. The ESAE forest hosts only a few accounts to which strict security policies must be applied.
* Only use one-way trusts. You should only configure a one-way trust where the production forest trusts the ESAE forest. This means that accounts from the ESAE forest can be used in the production forest, however, accounts from the production forest can't be used in the ESAE forest. Accounts used for administrative tasks in the production forest should be standard user accounts in the ESAE forest. If an account is compromised in the production forest, it can't be used to elevate privileges in the ESAE forest.

The ESAE forest servers need to be configured in the following ways:

* Installation media should be validated.
* Servers should run the most recent version of the Windows Server operating system.
* Servers should be updated automatically with security updates.
* Security Compliance Manager baselines should be used as the starting point for server configuration.
* Servers should be configured with Secure Boot, BitLocker volume encryption, Credential Guard, and Device Guard.
* Servers should be configured to block USB storage.
* Servers should be on isolated networks. Inbound and outbound Internet connections should be blocked.

---

# Monitor and troubleshoot AD DS

Performance and operational issues are common in real-world environments. To analyze, evaluate, and remediate such issues affecting AD DS domain controller is a fundamental skill of any IT professional responsible for ensuring stability and availability of an AD DS environment.

### Monitor AD DS operational status

Insufficient system resources can lead to poor domain controller system performance. The four key system resources are the central processing unit (CPU), disk subsystem, memory, and network. Identifying and remediating bottlenecks involves close examination of system logs and performance counters to determine which resource is currently constrained. After augmenting that resource, performance will improve, but it might reach a plateau if it hits a new bottleneck in another system resource.

You can use several tools in Windows Server for various types of monitoring. Most of these tools are available by default as Windows Server components, and you can use them for real-time and historical monitoring of AD DS and other services. The most commonly used tools are Task Manager, Resource Monitor, Event Viewer, and Performance Monitor. With Performance Monitor, you can review current performance statistics or historical data gathered by using data collector sets.

There are many counters that you can review and analyze to address your specific requirements, including processor-, memory-, disk-, and network-specific counters. On a domain controller, you also should monitor NT Directory Service (NTDS) object counters.

* Security System-Wide Statistics\Kerberos Authentications/sec. This counter tracks the number of Kerberos authentications per second.
* Security System-Wide Statistics\NTLM Authentications. This counter tracks the number of Windows Network LAN Manager (NTLM) authentications processed per second.

If you use System Center Operations Manager in your environment, you also have the option to deploy the Active Directory Domain Services Management Pack for Operations Manager to monitor and analyze operations of your domain controllers. This management pack contains many alerts, views, tasks, and reports for various AD DS functions.

### Tools for monitoring and troubleshooting replication

In any AD DS domain environment containing multiple domain controllers, it's essential to monitor AD DS replication and, in case of any issues, troubleshoot and resolve them. Performance monitor allows you to capture and analyze Directory Replication Agent (DRA) counters, including:

* NTDS\DRA Inbound Bytes Total/sec. This counter depicts the total number of bytes replicated into the AD DS database.
* NTDS\DRA Inbound Object. This counter depicts the number of Active Directory objects received from neighbors through inbound replication.
* NTDS\DRA Outbound Bytes Total/sec. This counter depicts the total number of bytes replicated out.
* NTDS\DRA Pending Replication Synchronizations. This is the number of directory synchronizations that are in this server's queue, waiting for processing.

Two additional tools are useful for reporting and analyzing replication: the Replication Diagnostics Tool (Repadmin.exe) and the Domain Controller Diagnostics Tool (Dcdiag.exe).

### Repadmin.exe

Repadmin.exe is a command-line tool that enables you to report the status of replication on each domain controller. The information that Repadmin.exe produces can help you spot a potential replication problem in the forest. You can review levels of detail down to the replication metadata for specific objects and attributes, enabling you to identify where and when a problematic change was made to AD DS. You can even use Repadmin.exe to manage the replication topology and force replication between domain controllers.

Repadmin.exe supports several commands that perform specific tasks. You can learn about each command by running `repadmin /?` from the Command Prompt. Most commands take a DC_LIST parameter, which is simply a network label (DNS, NetBIOS name, or IP address) of a domain controller. Some of the replication monitoring tasks that you can perform by using Repadmin.exe include:

* Displaying the replication partners for a domain controller. To display the replication connections of a domain controller, enter `repadmin /showrepl DC_LIST . By default, Repadmin.exe lists intersite connections only. Add the /repsto argument also to list intersite connections.
* Displaying connection objects for a domain controller. Enter `repadmin /showconn DC_LIST` to list the connection objects for a domain controller.
* Displaying metadata about an object, its attributes, and replication. You can learn much about replication by examining an object on two different domain controllers to find out which attributes have or haven't replicated. Enter `repadmin /showobjmeta DC_LIST Object`, where DC_LIST indicates the domain controller or controllers to query. You can use an asterisk to indicate all domain controllers. The Object represents the GUID of an object, which is its unique identifier.

### Dcdiag.exe

Dcdiag.exe performs several tests and reports on the overall health of replication and operational status for AD DS. Run by itself, Dcdiag.exe performs summary tests and then reports the results. At the other extreme, Dcdiag.exe /c runs a comprehensive list of tests. You can redirect the output to files of various types, including XML. You also can specify one or more tests to perform by using the `/test:Test Name` parameter. Tests that relate directly to replication include:
* DFSREvent. Reports any operation errors in the Distributed File System (DFS).
* Intersite. Checks for failures that would prevent or delay intrasite replication.
* KccEvent. Identifies errors in the Knowledge Consistency Checker.
* Replications. Checks for timely replication between domain controllers.
* Topology. Checks that the replication topology is connected fully for all domain controllers.
* VerifyReplicas. Verifies that all application directory partitions are instantiated fully on all domain controllers that host replicas.

### Monitoring replication with Microsoft System Center Operations Manager

Active Directory Domain Services Management Pack for Operations Manager includes replication monitoring functionality that collects AD DS replication alerts along with performance data representing replication latency, and the volume of both inbound and outbound replication traffic. The management pack offers replication topology dashboards that display site links, connection objects, and broken connection objects. It also allows you to generate reports on replication connection objects, replication site links, replication bandwidth, and replication latency.

### Windows PowerShell AD DS replication cmdlets

Windows Server supports Windows PowerShell cmdlets that facilitate monitoring AD DS replication and reviewing its configuration. The following list describes some of them.

* `Get-ADReplicationConnection`. Provides a specific AD DS replication connection or a set of AD DS replication connection objects based on a specified filter
* `Get-ADReplicationFailure`. Provides a description of an AD DS replication failure
* `Get-ADReplicationPartnerMetadata`. Provides replication metadata for a set of one or more replication partners
* `Get-ADReplicationSite`. Provides a specific AD DS replication site or a set of replication site objects based on a specified filter
* `Get-ADReplicationSiteLink`. Provides a specific Active Directory site link or a set of site links based on a specified filter
* `Get-ADReplicationSiteLinkBridge`. Provides a specific Active Directory site link bridge or a set of site link bridge objects based on a specified filter
* `Get-ADReplicationSubnet`. Provides an Active Directory subnet or a set of Active Directory subnets based on a specified filter.

---
# Create custom AD DS partitions

---
Custom applications might need to store their data in the AD DS database. Some of them rely on schema extensions for this purpose, however, there are also others, which require creating custom AD DS partitions. This happens to be the case with the new, Contoso's in-house developed suite of applications that you need to help deploy.

### What are AD DS partitions?

A partition, or naming context, is a portion of the AD DS database. Although the database is one file named NTDS.dit, different partitions contain different data. Each partition is a unit of replication, and each partition has its own replication topology. The default partitions include:

* Configuration partition. The configuration partition is created automatically when you create the first domain controller in a forest. The configuration partition contains information about the forest-wide AD DS structure, including which domains and sites exist and which domain controllers exist in each domain. This partition replicates to all domain controllers in the forest.
* Schema partition. The schema partition contains definitions of all the objects and attributes that you can create in the data store, and the rules for creating and manipulating them. Schema information replicates to all domain controllers in the forest.
* Domain partition. When you create a new domain, AD DS automatically creates an instance of the domain partition. That partition is subsequently automatically replicated to every new domain controller in the same domain. The domain partition contains information about all domain-specific objects, including users, groups, computers, organizational units (OUs), and domain-related system settings.
* Application partition. The application partition stores nondomain, application-related information that tends to be updated at a higher frequency or have a customizable lifetime, such as a Domain Name System (DNS) partition when Active Directory–integrated DNS is enabled. You typically have the flexibility to designate the scope of replication of application partitions, by designating which domain controllers in a forest will host its copies.

> [!NOTE]
> By default, when you configure a domain controller to host Active Directory integrated DNS zones, two separate application partitions, domainDnsZones and forestDnsZones, are created. The domainDnsZones partition contains domain-specific DNS records and its replication scope consists of other AD DS domain controllers that host the DNS Server role.

### Create AD DS partitions
You can create and manage AD DS partitions by using the NtdsUtil.exe command-line tool. NtdsUtil.exe also allows you to perform several other AD DS-related management tasks, such as:
* NTDS database maintenance, including creating snapshots, relocating database, files, and offline defragmentation.
* Cleaning up domain-controller metadata following its unrecoverable failure.
* Resetting the password used to sign in to the Directory Services Restore Mode (DSRM).

### How to create a custom AD DS partition. 
The main steps in the process are:

1. Create AD DS environment. Create a single-domain AD DS forest containing two domain controllers.
2. Create a custom AD DS partition. Use command-line tools to create a custom application partition.
3. Verify that a custom AD DS partition exists. Use command-line tools to verify existence of a custom application partition.
4. Delete a custom AD DS partition. Use command-line tools to delete a custom application partition.

---

### Summary
Using the knowledge acquired in this module, you created trust relationships between the Contoso’s AD DS existing forests, implemented the ESAE forest, and created a custom AD DS partition to facilitate deployment of a new in-house developed suite of applications. Throughout these changes, you ensured that the AD DS replication remained fully operational.

---
## Check your knowledge
---

### 1. Which tool can be used to create, list, and delete a custom application partition?

* [ ] ntdsutil
* [ ] netdom
* [ ] disk part

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ntdsutil
💡 You can use ntdsutil to create, list, and delete a custom application partition.

</details>

---

### **2. What functionality does the transitivity of a two-way forest trust provide?**

* [ ] If you create a forest trust between Forest 1 and Forest 2 and you create a forest trust between Forest 2 and Forest 3, Forest 1 implicitly trusts Forest 3.
* [ ] All domains in both trusted forests trust each other.
* [ ] All users in the trusted forest can authenticate for services and access on all computers in the trusting forest.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All domains in both trusted forests trust each other.

💡 A **two-way forest trust** is **transitive within the scope of the two forests**, meaning every domain in one forest trusts every domain in the other forest. This trust does **not** extend transitively to additional forests.

</details>

---

### **3. How should a trust between an ESAE forest and a production forest be configured?**

* [ ] One-way with forest-wide authentication and the ESAE forest trusting the production forest
* [ ] One-way with selective authentication and the production forest trusting the ESAE forest
* [ ] One-way with forest-wide authentication and the production forest trusting the ESAE forest

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** One-way with selective authentication and the production forest trusting the ESAE forest

💡 In the **ESAE (Red Forest) model**, the production forest **trusts** the ESAE forest using a **one-way trust** with **selective authentication** to limit where privileged ESAE accounts can authenticate, reducing attack surface and credential exposure.

</details>

---

### **4. Which of the following tools can be used to monitor and troubleshoot AD DS replication?**

* [ ] Nltest.exe
* [ ] Dcdiag.exe
* [ ] Netdom.exe

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dcdiag.exe

💡 **Dcdiag.exe** performs health checks on domain controllers, including **replication status and errors**, making it the primary tool for diagnosing AD DS replication issues.

</details>

---

