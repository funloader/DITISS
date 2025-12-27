# Introduction

---
### Learn about the fundamentals of Active Directory Domain Services (AD DS) in Windows Server, including forests, domains, sites, domain controllers, organizational units (OUs), users, and groups. *2 minutes read*
---

## Scenario
Contoso, Ltd. is a financial services company in Seattle with major offices located throughout the world. Most of its compute environment runs on-premises on Windows Server. This includes virtualized workloads on Windows Server 2016 hosts.

Contoso's IT staff are migrating Contoso on-premises servers to Windows Server 2025. As part of the migration, Contoso is evaluating its current AD DS environment. As a Windows Server administrator, you're responsible for managing AD DS objects, such as users, groups, and OUs.

After completing this module, you’ll understand the fundamental AD DS structure and how users, groups, and group managed service accounts, and how they relate to OUs.

### Learning objectives
After completing this module, you'll be able to:

- Describe AD DS.
- Describe users, groups, and computers.
- Identify and describe AD DS forests and domains.
- Describe OUs.
- Manage objects and their properties in AD DS.

### Prerequisites
To get the best learning experience from this module, you should have knowledge and experience of:
- Windows Server.
- Core networking technologies.

---

# Define AD DS

AD DS and its related services form the foundation for enterprise networks that run Windows operating systems. The AD DS database is the central store of all the domain objects, such as user accounts, computer accounts, and groups. AD DS provides a searchable, hierarchical directory and a method for applying configuration and security settings for objects in an enterprise.

AD DS includes both logical and physical components. You should understand how AD DS components work together so that you can manage your infrastructure efficiently. In addition, you can use AD DS options to perform actions such as:
- Installing, configuring, and updating apps.
- Managing the security infrastructure.
- Enabling Remote Access Service and DirectAccess.
- Issuing and managing digital certificates.

### What are the logical components?
AD DS logical components are structures that you use to implement an AD DS design that is appropriate for an organization. The following table describes the types of logical components that an AD DS database contains.

| Logical Component | Description |
|-------------------|-------------|
| **Partition** | A partition, or naming context, is a portion of the AD DS database. Although the database consists of one file named *Ntds.dit*, different partitions contain different data. For example, the schema partition contains a copy of the Active Directory schema. The configuration partition contains the configuration objects for the forest, and the domain partition contains the users, computers, groups, and other objects specific to the domain. Active Directory stores copies of partitions on multiple domain controllers and updates them through directory replication. |
| **Schema** | A schema is the set of definitions of the object types and attributes that you use to define the objects created in AD DS. |
| **Domain** | A domain is a logical administrative container for objects such as users and computers. A domain maps to a specific partition and you can organize the domain with parent-child relationships to other domains. |
| **Domain Tree** | A domain tree is a hierarchical collection of domains that share a common root domain and a contiguous Domain Name System (DNS) namespace. |
| **Forest** | A forest is a collection of one or more domains that have a common AD DS root, a common schema, and a common global catalog. |
| **OU (Organizational Unit)** | An OU is a container object for users, groups, and computers that provides a framework for delegating administrative rights and administration by linking Group Policy Objects (GPOs). |
| **Container** | A container is an object that provides an organizational framework for use in AD DS. You can use the default containers, or you can create custom containers. You can't link GPOs to containers. |


### What are the physical components?
Physical components in AD DS are those objects that are tangible, or that described tangible components in the real world.

A screenshot of Active Directory Sites and Services. The administrator has selected the Sites node. Displayed are two sites, Seattle and Vancouver. Also displayed are two subnets.

The following table describes some of the physical components of AD DS.

| Physical Component | Description |
|--------------------|-------------|
| **Domain Controller** | A domain controller contains a copy of the AD DS database. For most operations, each domain controller can process changes and replicate the changes to all the other domain controllers in the domain. |
| **Data Store** | A copy of the data store exists on each domain controller. The AD DS database uses Microsoft Jet database technology and stores the directory information in the *Ntds.dit* file and associated log files. The `C:\Windows\NTDS` folder stores these files by default. |
| **Global Catalog Server** | A global catalog server is a domain controller that hosts the global catalog, which is a partial, read-only copy of all the objects in a multiple-domain forest. A global catalog speeds up searches for objects that might be stored on domain controllers in a different domain in the forest. |
| **Read-Only Domain Controller (RODC)** | An RODC is a special read-only installation of AD DS. RODCs are common in branch offices where physical security isn't optimal, IT support is less advanced than in the main corporate centers, or line-of-business applications need to run on a domain controller. |
| **Site** | A site is a container for AD DS objects, such as computers and services that are specific to a physical location. This differs from a domain, which represents the logical structure of objects such as users, groups, and computers. |
| **Subnet** | A subnet is a portion of the network IP addresses of an organization assigned to computers in a site. A site can have more than one subnet. |

---
# Define users, groups, and computers
In addition to the high-level components and objects, AD DS contains other objects such as users, groups, and computers.

### Create user objects
In AD DS, you must provide all users that require access to network resources with a user account. With this user account, users can authenticate to the AD DS domain and access network resources.

In Windows Server, a user account is an object that contains all the information that defines a user. A user account includes:

The username.
- A user password.
- Group memberships.
- A user account also contains settings that you can configure based on your organizational requirements.

The username and password of a user account serve as the user’s sign-in credentials. A user object also includes several other attributes that describe and manage the user. You can use the following to create and manage user objects in AD DS:

- Active Directory Administrative Center.
- Active Directory Users and Computers.
- Windows Admin Center.
- Windows PowerShell.
- The `dsadd` command-line tool.

### What are managed service accounts?
Many apps contain services that you install on the server that hosts the program. These services typically run at server startup or are triggered by other events. Services often run in the background and don't require any user interaction. For a service to start up and authenticate, you use a service account. A service account might be an account that is local to the computer, such as the built-in Local Service, Network Service, or Local System accounts. You also can configure a service account to use a domain-based account located in AD DS.

To help centralize administration and to meet program requirements, many organizations choose to use a domain-based account to run program services. While this does provide some benefit over using a local account, there are a number of associated challenges, such as the following:

- Extra administration effort might be necessary to manage the service account password securely.
- It can be difficult to determine where a domain-based account is being used as a service account.
- Extra administration effort might be necessary to manage the service principal name (SPN).

Windows Server supports an AD DS object, named a managed service account, which you use to facilitate service-account management. A managed service account is an AD DS object class that enables:
- Simplified password management.
- Simplified SPN management.

### What are group managed service accounts?
Group Managed Service Accounts (gMSA) enable you to extend the capabilities of standard managed service accounts to more than one server in your domain. In server farm scenarios with Network Load Balancing (NLB) clusters or IIS servers, there often is a need to run system or program services under the same service account. Standard managed service accounts can't provide managed service account functionality to services that are running on more than one server. By gMSA, you can configure multiple servers to use the same managed service account and still retain the benefits that managed service accounts provide, like automatic password maintenance and simplified SPN management.

To support group managed service account functionality, your environment must meet the following requirement:
- You must create a KDS root key on a domain controller in the domain.
- 
To create the KDS root key, run the following command from the Active Directory Module for Windows PowerShell on a Windows Server domain controller
```
Add-KdsRootKey –EffectiveImmediately
```

You create group managed service accounts by using `New-ADServiceAccount` Windows PowerShell cmdlet with the `–PrinicipalsAllowedToRetrieveManagedPassword` parameter.

For example:
```
New-ADServiceAccount -Name LondonSQLFarm -PrincipalsAllowedToRetrieveManagedPassword SEA-SQL1, SEA-SQL2, SEA-SQL3
```

### What are delegated managed service accounts?
Windows Server 2025 introduces a new type of service account called the Delegated Managed Service Account (dMSA). The dMSA account type enables users to transition from traditional service accounts to machine accounts that have managed and fully randomized keys, while also disabling the original service account passwords. Authentication for dMSA is linked to the device identity, which means that only specified machine identities mapped in AD can access the account. By using dMSA, users can prevent the common issue of credential harvesting using a compromised account that is associated with traditional service accounts.

dMSAs and gMSAs are two types of managed service accounts that are used to run services and applications in Windows Server. A dMSA is managed by an administrator and is used to run a service or application on a specific server. A gMSA is managed by AD and is used to run a service or application on multiple servers. Other differences include:

- Utilizing gMSA concepts to limit scope of usage using Credential Guard to bind machine authentication.
- Credential Guard can be used to enhance security in dMSA by automatically rotating passwords and binding all service account tickets. Legacy accounts are then disabled to further improve security.
- Although gMSAs are secured with machine generate and autorotated passwords, the passwords are still not machine bound and can be stolen.

### What are group objects ?
Although it might be practical to assign permissions and rights to individual user accounts in small networks, this becomes impractical and inefficient in large enterprise networks.

For example, if several users need the same level of access to a folder, it's more efficient to create a group that contains the required user accounts, and then assign the required permissions to the group.

> [!TIP]
> As an added benefit, you can change users’ file permissions by adding or removing them from groups rather than editing the file permissions directly.

Before you implement groups in your organization, you must understand the scope of various AD DS group types. In addition, you must understand how to use group types to manage access to resources or to assign management rights and responsibilities.

### Group types
In a Windows Server enterprise network, there are two types of groups, described in the following table.

| Group Type | Description |
|------------|-------------|
| **Security** | Security groups are security-enabled and are used to assign permissions to various resources. You can use security groups in access control lists (ACLs) to help control security for resource access. If you want to manage security, the group must be a security group. |
| **Distribution** | Distribution groups are typically used by email applications and are not security-enabled. Security groups can also be used as distribution groups for email purposes. |

> [!NOTE]
> When you create a group, you choose the group type and scope. The group type determines the capabilities of the group.

### Group scopes
Windows Server supports group scoping. The scope of a group determines both the range of a group’s abilities or permissions and the group membership. There are four group scopes.

- Local. You use this type of group for standalone servers or workstations, on domain-member servers that aren't domain controllers, or on domain-member workstations. Local groups are available only on the computer where they exist. The important characteristics of a local group are:
  - You can assign abilities and permissions on local resources only, meaning on the local computer.
  - Members can be from anywhere in the AD DS forest.
- Domain-local. You use this type of group primarily to manage access to resources or to assign management rights and responsibilities. Domain-local groups exist on domain controllers in an AD DS domain, and so, the group’s scope is local to the domain in which it resides. The important characteristics of domain-local groups are:
  - You can assign abilities and permissions on domain-local resources only, which means on all computers in the local domain.
  - Members can be from anywhere in the AD DS forest.
- Global. You use this type of group primarily to consolidate users who have similar characteristics. For example, you might use global groups to join users who are part of a department or a geographic location. The important characteristics of global groups are:
  - You can assign abilities and permissions anywhere in the forest.
  - Members can be from the local domain only and can include users, computers, and global groups from the local domain.
- Universal. You use this type of group most often in multidomain networks because it combines the characteristics of both domain-local groups and global groups. Specifically, the important characteristics of universal groups are:
  - You can assign abilities and permissions anywhere in the forest similar to how you assign them for global groups.
  - Members can be from anywhere in the AD DS forest.

### What are computer objects?
Computers, like users, are security principals, in that:

- They have an account with a sign-in name and password that Windows changes automatically on a periodic basis.
- They authenticate with the domain.
- They can belong to groups and have access to resources, and you can configure them by using Group Policy.

A computer account begins its lifecycle when you create the computer object and join it to your domain.After you join the computer account to your domain, day-to-day administrative tasks include:

- Configuring computer properties.
- Moving the computer between OUs.
- Managing the computer itself.
Renaming, resetting, disabling, enabling, and eventually deleting the computer object.

### Computers container
Before you create a computer object in AD DS, you must have a place to put it. The Computers container is a built-in container in an AD DS domain. This container is the default location for the computer accounts when a computer joins the domain.

This container isn't an OU. Instead, it's an object of the Container class. Its common name is CN=Computers. There are subtle but important differences between a container and an OU. You can't create an OU within a container, so you can't subdivide the Computers container. You also can't link a Group Policy Object to a container. Therefore, we recommend that you create custom OUs to host computer objects, instead of using the Computers container.

# Define AD DS forests and domains

An AD DS forest is a collection of one or more AD DS trees that contain one or more AD DS domains. Domains in a forest share:

- A common root.
- A common schema.
- A global catalog.

An AD DS domain is a logical administrative container for objects such as:
- Users
- Groups
- Computers

### What is an AD DS forest?
A forest is a top-level container in AD DS. Each forest is a collection of one or more domain trees that share a common directory schema and a global catalog. A domain tree is a collection of one or more domains that share a contiguous namespace. The forest root domain is the first domain that you create in the forest.

The forest root domain contains objects that don't exist in other domains in the forest. Because you always create these objects on the first domain controller, a forest can consist of as few as one domain with a single domain controller, or it can consist of several domains across multiple domain trees.

The following graphic displays `Contoso.com` as the forest root domain. Beneath are two domains, `Adatum.com` in a separate tree, and `Seattle.Contoso.com` as a child of `Contoso.com`

![Diagram](images/m6-forest-bc4595bc.png)


The following objects exist in the forest root domain:
- The schema master role.
- The domain naming master role.
- The Enterprise Admins group.
- The Schema Admins group.

> [!NOTE]
> Although the schema and domain naming master roles are assigned initially in the root domain on the first domain controller you create, you can move them to other domain controllers anywhere in the forest.

An AD DS forest is often described as:
- A security boundary. By default, no users from outside the forest can access any resources inside the forest. In addition, all the domains in a forest automatically trust the other domains in the forest. This makes it easy to enable access to resources for all the users in a forest, regardless of the domain to which they belong.
- A replication boundary. An AD DS forest is the replication boundary for the configuration and schema partitions in the AD DS database. Therefore, organizations that want to deploy applications with incompatible schemas must deploy additional forests. The forest is also the replication boundary for the global catalog. The global catalog makes it possible to find objects from any domain in the forest.

> [!TIP]
> Typically, an organization creates only one forest.

The following objects exist in each domain (including the forest root):
- The RID master role.
- The Infrastructure master role.
- The PDC emulator master role.
- The Domain Admins group.

### What is an AD DS domain?
An AD DS domain is a logical container for managing user, computer, group, and other objects. The AD DS database stores all domain objects, and each domain controller stores a copy of the database.

The following graphic displays an AD DS domain. It contains users, computers, and groups.
![Diagram](images/m6-domain-755853b7.png).

The most commonly used objects are described in the following table:
| Object | Description |
|--------|-------------|
| **User Accounts** | User accounts contain information about users, including the information required to authenticate a user during the sign-in process and to build the user’s access token. |
| **Computer Accounts** | Each domain-joined computer has an account in AD DS. You can use computer accounts for domain-joined computers in the same way that you use user accounts for users. |
| **Groups** | Groups organize users or computers to simplify the management of permissions and Group Policy Objects (GPOs) within the domain. |

> [!NOTE]
> AD DS allows a single domain to contain nearly two billion objects. This means that most organizations need only deploy a single domain.

An AD DS domain is often described as:

- A replication boundary. When you make changes to any object in the domain, the domain controller where the change occurred replicates that change to all other domain controllers in the domain. If multiple domains exist in the forest, only subsets of the changes replicate to other domains. AD DS uses a multi-master replication model that allows every domain controller to make changes to objects in the domain.
- An administrative unit. The AD DS domain contains an Administrator account and a Domain Admins group. By default, the Administrator account is a member of the Domain Admins group, and the Domain Admins group is a member of every local Administrators group of domain-joined computers. Also, by default, the Domain Admins group members have full control over every object in the domain.

> [!NOTE]
> The Administrator account in the forest root domain has additional rights.

An AD DS domain provides:

- Authentication. Whenever a domain-joined computer starts or a user signs in to a domain-joined computer, AD DS authenticates it. Authentication verifies that computer or user has the proper identity in AD DS by verifying its credentials.
- Authorization. Windows uses authorization and access control technologies to determine whether to allow authenticated users to access resources.

> [!TIP]
> Organizations with decentralized administrative structures or multiple locations might consider implementing multiple domains in the same forest to accommodate their administrative needs.

