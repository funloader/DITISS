# Introduction

---
In this module, learn how to configure a Microsoft Azure environment so that Windows Server infrastructure as a service (IaaS) workloads that require Active Directory are supported. Also learn how to integrate an on-premises AD DS environment into Azure.

---

### Scenario

Contoso is a medium-size financial services company in London with a branch office in New York. Most of its compute environment runs on-premises on Windows Server. This includes virtualized workloads on Windows Server 2016 hosts. Contoso's IT staff are in the process of migrating Contoso servers to Windows Server 2025.

Contoso’s IT director realizes that Contoso has an outdated operational model with limited automation and reliance on dated technology. The Contoso IT Engineering team has started exploring Azure capabilities. They want to determine whether Azure services might assist with modernizing the current operational model through automation and virtualization.

As part of the initial design, the Contoso IT team asked you, their lead system engineer and server administrator, to set up a proof of concept environment. This environment must verify whether Azure services can help to modernize the IT infrastructure and meet business goals.

With more services available online and in the cloud, organizations like Contoso are finding that they need to define and manage cloud identities. Contoso can use cloud identities to authenticate and authorize their users when they try to access company resources.

Microsoft provides a cloud-based directory service in the Azure platform called Microsoft Entra ID (Microsoft Entra ID). Microsoft Entra ID is a multitenant, cloud-based directory, and identity management service. It provides identity and access services for resources that exist in the cloud. Microsoft Entra ID can also provide for single-sign on (SSO) access to cloud software as a service (SaaS) applications.

Contoso could also choose to use Microsoft Entra Domain Services. Microsoft Entra Domain Services provides managed domain services such as domain join, group policy, Lightweight Directory Access Protocol (LDAP), and Kerberos authentication or NTLM authentication that is fully compatible with Windows Server AD DS. Contoso could integrate Microsoft Entra Domain Services with their Microsoft Entra tenant. This makes it possible for users to sign in using their existing credentials.

In this module, you learn how to select a Microsoft Entra integration model, and plan for integration. You'll also prepare and install AD DS synchronization. You learn how to implement SSO, and enable Microsoft Entra sign-in for an Azure virtual machine (VM). Finally, you learn to plan and implement Microsoft Entra Domain Services.

### Learning objectives
After completing this module, you'll be able to:

* Select a Microsoft Entra integration model.
* Plan for Microsoft Entra integration.
* Prepare on-premises AD DS for directory synchronization.
* Install and configure directory synchronization using Microsoft Entra Connect.
* Implement Seamless SSO.
* Enable Microsoft Entra sign-in for an Azure Windows VM.
* Describe Microsoft Entra Domain Services.
* Implement and configure Microsoft Entra Domain Services.
* Manage Windows Server in a Microsoft Entra Domain Services instance.
* Join a Windows Server VM to a managed domain.

### Prerequisites
To get the best learning experience from this module, it's important that you have knowledge and experience of the following areas:

* Managing Windows Server operating system and Windows Server workloads in on-premises scenarios, including AD DS, DNS, Distributed File System (DFS), Microsoft Hyper-V, and file and storage services.
* Common Windows Server management tools.
* Core Microsoft compute, storage, networking, and virtualization technologies.
* Implementing and managing IaaS services in Microsoft Azure.
* Microsoft Entra ID.
* Security-related technologies (firewalls, encryption, multifactor authentication).
* Windows PowerShell scripting.
* Automation and monitoring.

---

# Select a Microsoft Entra integration model

Microsoft Entra ID is a directory service designed for cloud-based and web-based applications, which shares some functionalities with traditional AD DS deployments. The Contoso IT team can implement Microsoft Entra ID and synchronize its on-premises identities to the cloud. These steps would enable Contoso staff to use SSO to access both on-premises resources and those related resources in their Azure tenant.

The IT team can use Microsoft Entra ID to increase employee productivity, streamline IT processes, and improve security for adopting various cloud services. Contoso employees can access online applications by using a single user account. Contoso can also perform central user management by using well-known Windows PowerShell cmdlets. It's also worth noting that because Microsoft Entra ID is highly scalable and highly available by design, the IT team won't have to maintain related infrastructure or worry about disaster recovery.

As a component of Azure, Microsoft Entra ID can support multifactor authentication as part of an overall access strategy for cloud services, thus providing an additional layer of security. Role-based access control (RBAC), self-service password, group management, and device registration provide enterprise-ready identity management solutions. Microsoft Entra ID also provides advanced identity protection in addition to enhanced reporting and alerting that can help you recognize threats more efficiently.

# Overview of Microsoft Entra ID

Microsoft Entra ID is part of the platform as a service (PaaS) offering and operates as a Microsoft-managed directory service in the cloud. It's not a part of the core infrastructure that customers own and manage, nor is it an IaaS offering. While this implies that you have less control over its implementation, it also means that you don't have to dedicate resources to its deployment or maintenance.

With Microsoft Entra ID, you also have access to a set of features that aren't natively available in AD DS, such as support for multifactor authentication, identity protection, and self-service password reset. You can use Microsoft Entra ID to provide more secure access to cloud-based resources for organizations and individuals by:

* Configuring access to applications.
* Configuring SSO to cloud-based SaaS applications.
* Managing users and groups.
* Provisioning users.
* Enabling federation between organizations.
* Providing an identity management solution.
* Identifying irregular sign-in activity.
* Configuring multifactor authentication.
* Extending existing on-premises Active Directory implementations to Microsoft Entra ID.
* Configuring Application Proxy for cloud and local applications.
* Configuring conditional access for users and devices.

### Microsoft Entra tenants
Unlike on-premises AD DS, Microsoft Entra ID is multitenant by design and is implemented specifically to ensure isolation between its individual directory instances. It's the world’s largest multitenant directory, hosting over a million directory services instances, with billions of authentication requests per week. The term tenant in this context typically represents a company or organization that signed up for a subscription to a Microsoft cloud-based service such as Microsoft 365, Microsoft Intune, or Azure, each of which uses Microsoft Entra ID.

However, from the technical standpoint, the term tenant represents an individual Microsoft Entra instance. Within an Azure subscription, you can create multiple Microsoft Entra tenants. Having multiple Microsoft Entra tenants might be convenient if you want to test Microsoft Entra functionality in one tenant without affecting the others.

> [!NOTE]
> At any given time, an Azure subscription must be associated with one, and only one Microsoft Entra tenant. However, you can associate the same Microsoft Entra tenant with multiple Azure subscriptions.

 Each Microsoft Entra tenant is assigned the default DNS domain name that consists of a unique prefix. The prefix is derived from the name of the Microsoft account you use to create an Azure subscription, or provided explicitly when creating a Microsoft Entra tenant, and is followed by the `onmicrosoft.com` suffix. Adding at least one custom domain name to the same Microsoft Entra tenant is possible and common. This name utilizes the DNS domain namespace that the corresponding company or organization owns; for example, `Contoso.com`. The Microsoft Entra tenant serves as the security boundary and a container for Microsoft Entra objects such as users, groups, and applications.

### Characteristics of Microsoft Entra ID
Although Microsoft Entra ID has many similarities to AD DS, there are also many differences. It's important to realize that using Microsoft Entra ID isn't the same as deploying an AD DS domain controller on an Azure VM and then adding it to your on-premises domain.

When comparing Microsoft Entra ID with AD DS, it's important to note the Microsoft Entra characteristics that differ from AD DS:

* Microsoft Entra ID is primarily an identity solution, and it's designed for internet-based applications by using HTTP (port 80) and HTTPS (port 443) communications.
* Microsoft Entra ID is a multitenant directory service.
* Microsoft Entra users and groups are created in a flat structure, and there are no organizational units (OUs) or Group Policy Objects (GPOs).
* You can't query Microsoft Entra ID by using LDAP; instead, Microsoft Entra ID uses the REST API over HTTP and HTTPS.
* Microsoft Entra ID doesn't use Kerberos authentication; instead, it uses HTTP and HTTPS protocols such as Security Assertion Markup Language (SAML), Web Services Federation (WS-Federation), and OpenID Connect for authentication. It also uses Open Authorization (OAuth) for authorization.
* Microsoft Entra ID includes federation services, and many third-party services are federated with and trust Microsoft Entra ID.

### Microsoft Entra integration options
Small organizations that don't have an on-premises directory such as AD DS can fully rely on Microsoft Entra ID as an authentication and authorization service. However, the number of these organizations is still small, so most companies search for a way to integrate on-premises AD DS with Microsoft Entra ID. Microsoft offers cloud-scale identity and access management via Microsoft Entra ID, which provides several options for integrating AD DS with Azure. These options are described in the following table.

| Option | Description |
|-------|-------------|
| **Extending on-premises AD DS to Azure** | With this option, you host VMs in Azure that are promoted to domain controllers in your on-premises AD DS. |
| **Synchronizing on-premises AD DS with Microsoft Entra ID** | Directory synchronization propagates user, group, and contact information to Microsoft Entra ID and keeps it synchronized. Users use different passwords for cloud and on-premises resources, and authentication is handled separately. |
| **Synchronizing AD DS with Microsoft Entra ID using password hash synchronization** | On-premises AD DS synchronizes objects and password hashes to Microsoft Entra ID. Users can access Microsoft Entra ID–aware applications using the same password as their on-premises sign-in, providing a unified sign-in experience. |
| **Implementing SSO between on-premises AD DS and Microsoft Entra ID** | Supports the widest range of integration features and allows users to sign in to Azure after authenticating with on-premises AD DS. This is implemented using federation with AD FS and Web Application Proxy, or alternatively by using pass-through authentication, which offers similar results with less infrastructure complexity. |

The Microsoft Entra directory isn't an extension of an on-premises directory. Rather, it's a copy that contains the same objects and identities. Changes made to these items on-premises are copied to Microsoft Entra ID, but changes made in Microsoft Entra ID aren't replicated back to the on-premises domain.

> [!TIP]
> You can also use Microsoft Entra ID without using an on-premises directory. In this case, Microsoft Entra ID acts as the primary source of all identity information, rather than containing data replicated from an on-premises directory.
 ---
# Plan for Microsoft Entra integration

When IT staff at Contoso implements a cloud service or an application in their IT environment, they typically want to use a single identity store for their local and cloud-based applications. By using directory synchronization, they can connect their on-premises AD DS with Microsoft Entra ID.

### What is directory synchronization?

Directory synchronization enables synchronization between on-premises AD DS and Microsoft Entra ID for users, groups, and contacts. In its simplest form, you install a Directory synchronization component on a server in your on-premises domain. You then provide an account with Domain Admin and Enterprise Admin access to on-premises AD DS, and another account with administrator access to Microsoft Entra ID, and let it run.

User accounts, groups, and contacts that you select from AD DS are then replicated into Microsoft Entra ID. Users can then use those accounts to sign in to and access Azure services that rely on Microsoft Entra ID for authentication.

Unless you activate Password Synchronization, users will have a separate password from their on-premises environment to sign in to an Azure resource. Even if you implement Password Sync, users are still prompted for their credentials when they access the Azure resource on domain-joined computers. The advantage with Password Sync is that to sign in to the Azure resource, users can use the same user name and password as their domain login. Don't confuse this with SSO. The behavior provided with Password Sync is called same sign-in.

With Azure, the synchronization flow is one-way from local AD DS to Azure. However, with Microsoft Entra ID P1 or P2 features, some attributes replicate in the other direction. For example, you can configure Azure to write passwords back to an on-premises AD DS, and to groups and devices from Microsoft Entra ID. If you don't want to synchronize your entire on-premises AD DS, directory synchronization for Microsoft Entra ID supports limited filtering and customization of attribute flow based on the following values:

* OU
* Domain
* User attributes
* Applications

### Microsoft Entra Connect

You can use Microsoft Entra Connect (Microsoft Entra Connect) to perform synchronization between on-premises AD DS and Microsoft Entra ID. Microsoft Entra Connect is a wizard-based tool designed to enable connectivity between an on-premises identity infrastructure and Azure. Using the wizard, you can choose your topology and requirements and then the wizard deploys and configures all the required components for you. Depending on the requirements selected, this can include:
* Azure Active Directory Sync (Azure AD Sync)
* Exchange Hybrid deployment
* Password change writeback
* AD FS and AD FS proxy servers or Web Application Proxy
* Microsoft Graph PowerShell module

> [!NOTE]
> Most organizations deploy a dedicated synchronization server to host Microsoft Entra Connect.

When you run Microsoft Entra Connect, the following occurs:

* New users, groups, and contact objects in on-premises AD DS are added to Microsoft Entra ID. However, licenses for cloud services such as Microsoft 365 aren't automatically assigned to these objects.
* Attributes of existing users, groups, or contact objects that are modified in on-premises AD DS are modified in Microsoft Entra ID. However, not all on-premises AD DS attributes are synchronized to Microsoft Entra ID. You can configure a set of attributes that synchronize to Microsoft Entra ID by using Synchronization Manager component of Microsoft Entra Connect.
* Existing users, groups, and contact objects that are deleted from the on-premises AD DS are deleted from Microsoft Entra ID.
* Existing user objects that are disabled on-premises are disabled in Azure. However, licenses aren't automatically unassigned.

Microsoft Entra ID requires that you have a single source of authority for every object. Therefore, it's important to understand that in a Microsoft Entra Connect scenario, when you're running Active Directory synchronization you're mastering objects from within your on-premises AD DS, using tools such as Active Directory Users and Computers or Windows PowerShell. However, the source of authority is the on-premises AD DS. After the first synchronization cycle is complete, the source of authority is transferred from the cloud to the on-premises AD DS. All subsequent changes to cloud objects (except for licensing) are mastered from the on-premises AD DS tools. The corresponding cloud objects are read-only, and Microsoft Entra administrators can't edit cloud objects if the source of authority is on-premises AD DS, unless you implement some of the technologies that allow writeback.

### Permissions and accounts required to run Microsoft Entra Connect 

To implement Microsoft Entra Connect, you must have an account with required permissions assigned on both the local AD DS and Microsoft Entra ID. Installing and configuring Microsoft Entra Connect requires the following accounts:

* An Azure account with Global Administrator permission in the Azure tenant (such as an organizational account), that is not the account that was used to set up the account itself.
* An on-premises account with Enterprise Administrator permissions in the on-premises AD DS. In the Microsoft Entra Connect Wizard, you can choose to use an existing account for this purpose, or let the wizard create an account for you.

Microsoft Entra Connect uses an Azure Global Administrator account to provision and update objects when the Microsoft Entra Connect Configuration Wizard is run. You should create a dedicated service account in Azure for directory synchronization to use, because you can't use the Azure tenant administrator account. This restriction is because the account that you used to set up Azure might not have a domain name suffix that matches the domain name. The account needs to be a member of the Global Administrators role group.

In the on-premises environment, the account that is used to install and configure Microsoft Entra Connect must have the following permissions:

* Enterprise Administrator permissions in AD DS. This permission is required to create the synchronization user account in Active Directory.
* Local machine administrator permissions. This permission is required to install the Microsoft Entra Connect software.

The account you use to install AD Connect is automatically added to the ADSyncAdmins group when you install the product. You must sign out and sign in again to use the Synchronization Service Manager interface, because the account won't pick up the group security identifier (SID) until the next time the account is used to sign in.

![Diagram](images/m12-accounts.png).

The Enterprise Administrator account is only required when you install and configure Microsoft Entra Connect, but its credential isn't stored or saved by the configuration wizard. Therefore, you should create a special Microsoft Entra Connect administrator account for installing and configuring Microsoft Entra Connect, and assign this account to the Enterprise Administrators group when Microsoft Entra Connect is set up. However, this Microsoft Entra Connect Administrator account should be removed from the Enterprise Administrators group after Microsoft Entra Connect setup is complete. The following table details the accounts created during Microsoft Entra Connect configuration.

| Account    | Description |
|-----------|-------------|
| MSOL_<id> | This account is created during Microsoft Entra Connect installation and is configured to synchronize to the Azure tenant. The account has directory-replication permissions in the on-premises AD DS and write permission on certain attributes to enable hybrid deployment. |
| AAD_<id>  | This is the service account for the synchronization engine. It's created with a randomly generated complex password automatically configured to never expire. When the directory synchronization service runs, it uses the service account credentials to read from the local Active Directory and then write the contents of the synchronization database to Azure. This is done using the tenant administrator credentials that you enter in the Microsoft Entra Connect Configuration Wizard. |

> [!CAUTION]
> You shouldn't change the service account for Microsoft Entra Connect after you install Microsoft Entra Connect, because Microsoft Entra Connect always attempts to run using the account created during setup. If you change the account, Microsoft Entra Connect stops running and the scheduled synchronizations no longer occur.

> [!WARNING]
> Content under process !
