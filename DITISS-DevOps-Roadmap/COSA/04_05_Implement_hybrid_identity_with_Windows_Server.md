> [!WARNING]
> This content is currently being edited and is not yet finalized.


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

# Prepare on-premises Active Directory for directory synchronization

Before IT staff at Contoso deploys Microsoft Entra Connect, it's essential that they check the on-premises AD DS and related technologies for potential issues, and any issues that are discovered are remediated. This is especially important if they implement directory synchronization as an identity service for Microsoft 365.

### Predeployment checks

Predeployment checks should include:

* Analyzing the on-premises environment for invalid characters in AD DS object attributes, and for incorrect user principal names (UPNs).
* Performing domain email discovery and user counts.
* Identifying domain-functional levels and schema extensions, and identifying custom attributes in use.
* Identifying proxy servers used for Microsoft Exchange or Skype for Business, if you deploy Microsoft Entra Connect as a part of a Microsoft 365 deployment.
* Identifying Microsoft SharePoint domains, if you deploy Microsoft Entra Connect as part of a Microsoft 365 deployment.
* Evaluating client for SSO readiness.
* Recording network port use, and DNS records related to Office 365 (if you deploy Microsoft Entra Connect as part of an Office 365 deployment).

After you complete these checks, key remediation tasks include:

* Removing duplicate `proxyAddress` and `userPrincipalName` attributes.
* Updating blank and invalid `userPrincipalName` attributes and replacing with valid `userPrincipalName` attributes.
* Removing invalid characters in the following attributes: `givenName`, `surname (sn)`, `sAMAccountName`, `displayName`, `mail`, `proxyAddresses`, `mailNickname`, and `userPrincipalName`.

UPNs that are used for SSO can contain letters, numbers, periods, dashes, and underscores; no other character types are allowed.

If you're deploying Microsoft 365 and your deployment includes plans for SSO, you should ensure that UPN names meet this requirement before SSO is rolled out. Domains used for SSO and directory synchronization must be routable, which means that you can't use local domain names, such as Contoso.local.

### Active Directory health-check tools

To have directory synchronization work properly, you must ensure that on-premises Active Directory is well-prepared and error free. You can use the following AD DS health check tools can be used to identify and remediate issues.

**IdFix tool**

The Microsoft 365 IdFix tool enables you to identify and remediate most object synchronization errors in Active Directory, including common issues such as duplicate or malformed `proxyAddresses` and `userPrincipalName`.

You can select the OUs that you want IdFix to check, and you can fix common errors within the tool itself. Common errors might include problems such as invalid characters that might have been introduced during scripted user imports to attributes such as `proxyAddresses` and `mailNickname`.

For distinguished names that contain format and duplicate errors, IdFix might not be able to suggest an automatic remediation. Such errors can either be fixed outside IdFix or can be manually remediated within IdFix.

**ADModify.NET tool**

For errors such as format issues, you can make changes to specific attributes object-by-object by using either ADSIEdit or Advanced Mode in Active Directory Users and Computers. However, to make attribute changes to multiple objects, `ADModify.NET` is a better tool. This is because the batch mode operation provided by `ADModify.NET` is useful for making changes to attributes such as UPNs across OUs or domains.


---

# Install and configure directory synchronization with Microsoft Entra Connect

Microsoft Entra Connect requires a domain-joined computer to host the synchronization service. Most organizations deploy a dedicated synchronization server.

### Requirements
After you have set up Azure with an Active Directory tenant, you must complete the primary tasks to deploy directory synchronization using the following steps:

1. Add your AD DS domain into Azure, verify the domain, and then set the domain as the primary domain.
2. Download and install Microsoft Entra Connect.
3. Run the Microsoft Entra Connect Configuration Wizard. (Optionally, you can configure Microsoft Entra Connect to synchronize specific OUs in the on-premises AD DS environment).
4. Enable optional features such as password hash sync, password writeback, and Exchange hybrid deployment.
5. Run Microsoft Entra Connect, and let it configure the environment for directory synchronization
6. Validate the synchronization results.

After you set up Microsoft Entra Connect and perform the initial synchronization, you can reconfigure synchronization options if needed. The Microsoft Entra Connect software installation includes several applications related to directory synchronization. When you run Microsoft Entra Connect, you have the option to use Express installation settings, which sets up directory synchronization with the most commonly used settings, or you can choose to customize setup options.

If you choose to use custom installation, at the beginning of the setup you can choose to use a custom SQL server instead of a local database. You can also choose to use an existing service account, instead of the one created by the automatic setup process. In addition, you can specify custom sync groups. By default, the Administrators, Operators, Browse, and the Password Reset groups are created by Microsoft Entra Connect, but you can choose to use your own custom groups for this purpose.

By default, Microsoft Entra Connect sets up password hash synchronization for the directory synchronization mode. If you choose custom installation, you can also choose the Federation with AD FS option, or pass-through authentication. Alternatively, you can manually configure directory synchronization if you have a non-Microsoft federation server or another existing solution deployed.

Custom Microsoft Entra Connect installation also allows you to choose the way you identify your users. By default, Setup presumes that your users are represented only once across all directories. However, if you have a scenario where user identities exist across multiple directories, you must choose the matching attribute. You can choose between the options described in the following table.

| Option | Description |
|------|-------------|
| mail attribute | This option joins users and contacts if the mail attribute has the same value in different forests. |
| ObjectSID and msExchangeMasterAccountSID | This option joins an enabled user in an account forest with a disabled user in an Exchange resource forest. In Exchange, this is also known as a linked mailbox. |
| sAMAccountName and mailNickname | This option joins additional attributes on locations in a directory where the login ID for the user is expected to be found. |
| My own attribute | This option allows you to select your own attribute. |
| Source Anchor | This is an attribute that stays immutable during the lifetime of a user object. In other words, this attribute is the primary key that links the on-premises user object with the user object in Microsoft Entra ID. Because this attribute can't be changed later, you must carefully choose an attribute to use for this purpose. A default choice is objectGUID, as this attribute doesn't change unless the user account is moved between forests and domains. |

You can configure the UserPrincipalName attribute in the same window. This is the attribute that users use when they sign in to Microsoft Entra ID. The domains used for this purpose, also known as the UPN-suffix, should be verified in Microsoft Entra ID before synchronizing the user objects.

In some cases, you might want to synchronize only a subset of your users from your local AD DS. Microsoft Entra Connect allows you to select a specific group of users that you want to synchronize to Microsoft Entra ID. You should create this group before you run Microsoft Entra Connect. After you complete the setup, you can add and remove users from this group to maintain the list of user objects that should be present in Microsoft Entra ID. You also can use OUs from your local AD DS as the scope for replication. In the final step, Microsoft Entra Connect lets you set up some optional features available in Microsoft Entra ID P1 or P2.

---

# Implement Seamless Single Sign-On

The Contoso IT team wants a way to enable users to use SSO to access both on-premises resources and resources in Azure. Microsoft Entra seamless SSO is a technology that works with Password Hash Synchronization or Pass-through Authentication.

Additionally, when Seamless SSO is enabled, users rarely need to type in their usernames, and never their passwords to sign in to Microsoft Entra ID. This feature provides Contoso's users with easy access to their cloud-based applications without requiring any additional on-premises components.

### Supported scenarios for pass-through authentication

Microsoft Entra pass-through authentication helps ensure that services which rely on Microsoft Entra ID always validate passwords against an on-premises AD DS instance.

You can configure Microsoft Entra pass-through authentication by using Microsoft Entra Connect, which uses an on-premises agent that listens for external password validation requests. You can deploy this agent to one or more servers to provide high availability. It's not necessary to deploy this server to a perimeter network because all communication is outbound only.

You should join a server that runs the pass-through authentication agent to the AD DS domain where users are located. Before you deploy Microsoft Entra pass-through authentication, you should know which authentication scenarios are supported and which aren't.

You can use pass-through authentication for the following authentication scenarios:

* User sign-ins to all web browser–based applications supported by Microsoft Entra ID.
* User sign-ins to Office applications that support modern authentication.
* User sign-ins to Microsoft Outlook clients by using legacy protocols, such as Exchange ActiveSync, Simple Mail Transfer Protocol (SMTP), Post Office Protocol (POP), and Internet Message Access Protocol (IMAP).
* User sign-ins to Skype for Business application that supports modern authentication, including online and hybrid topologies.
* Microsoft Entra domain joins for Windows 10 devices.
* App passwords for multifactor authentication.
* Unsupported scenarios

### Unsupported scenarios for pass-through authentication

Although pass-through authentication supports most common authentication scenarios, there are still some scenarios in which you can’t use this method. These scenarios include:

* User sign-ins to legacy Office client applications, excluding Outlook.

> [!NOTE]
> These legacy client apps include Office 2010 and Office 2013 without modern authentication.

* Access to calendar sharing and free/busy information in Exchange hybrid environments on Office 2010 only.
* User sign-ins to Skype for Business client applications without modern authentication.
* User sign-ins to Windows PowerShell version 1.0.
* Detection of users with leaked credentials.
* Scenarios that require Microsoft Entra Domain Services. Microsoft Entra Domain Services requires tenants to have password hash synchronization enabled, so tenants that use only pass-through authentication won’t work in these scenarios.
* Scenarios that require Microsoft Entra Connect Health. Pass-through authentication isn't integrated with Microsoft Entra Connect Health.

If you use the Apple Device Enrollment Program (Apple DEP) that uses the iOS Setup Assistant, then you can’t use modern authentication as it isn't supported. It will fail to enroll Apple DEP devices into Intune for managed domains that use pass-through authentication. Consider using the Intune Company Portal app as an alternative.

### How pass-through authentication works

Before you deploy pass-through authentication, you should understand how it works and how this method of authentication differs from AD FS. Pass-through authentication isn't just a simpler form of AD FS authentication. Both methods use the on-premises infrastructure to authenticate users when accessing resources such as Microsoft 365, but not in the same way.

Pass-through authentication uses a component called Authentication Agent to authenticate users. Microsoft Entra Connect installs the Authentication Agent during configuration.

After installation, the Authentication Agent registers itself in your Microsoft 365 tenant’s Microsoft Entra ID. During registration, Microsoft Entra ID assigns the Authentication Agent a unique digital-identity certificate. This certificate (with a key pair) enables secure communication with Microsoft Entra ID. The registration procedure also binds the Authentication Agent to your Microsoft Entra tenant.

> [!NOTE]
> Authentication requests aren't pushed to the Authentication Agent. Instead, during its initialization, the Authentication Agent connects to Microsoft Entra ID over port 443, an HTTPS channel that is secured by using mutual authentication. After establishing the connection, Microsoft Entra ID provides the Authentication Agent with access to the Azure Service Bus queue. From this queue, the Authentication Agent retrieves and manages password validation requests. Because of this, there is no inbound traffic, so it's not necessary to install the Authentication Agent in the perimeter network.


#### Example
When Contoso IT staff enable pass-through authentication on their Microsoft 365 tenant and a user tries to authenticate on Outlook Web App, the following steps occur:

1. If not already signed in, the user is redirected to the Microsoft Entra user Sign-in page. On this page, the user signs in with a username and password. Microsoft Entra ID receives the request to sign in and places the username and password in a queue. A Microsoft Entra security token service (STS) uses the Authentication Agent public key to encrypt these credentials. The STS service retrieves this public key from the certificate that the Authentication Agent receives during the registration process.

> [!NOTE]
> Although Microsoft Entra ID temporarily places user credentials in the Azure Service Bus queue, they are never stored in the cloud.

2. The Authentication Agent, which is persistently connected to the Azure Service Bus queue, notices the change in the queue and retrieves the encrypted credentials from the queue. Because the credentials are encrypted with the Authentication Agent public key, the Agent uses its private key to decrypt the data.
3. The Authentication Agent validates the username and password against the local AD DS by using standard Windows APIs. At this point, this mechanism is similar to what AD FS uses. A username can be either the on-premises default username, usually `userPrincipalName`, or another attribute configured in Microsoft Entra Connect, known as *Alternate ID*.
4. The on-premises AD DS evaluates the request and returns the appropriate response to the Authentication Agent: success, failure, password expired, or user locked out.
5. After it receives the response from AD DS, the Authentication Agent returns this response to Microsoft Entra ID.
6. Microsoft Entra ID evaluates the response and responds to the user as appropriate. For example, Microsoft Entra ID either signs in the user immediately, or requests multifactor authentication. If the user sign-in is successful, the user can access the application.

> [!NOTE]
> You can consider deploying Microsoft Entra seamless SSO together with pass-through authentication to make the user experience even better when accessing cloud-based resources from domain-joined computers. When you deploy this feature, your users can access cloud resources without signing in if they are already signed in on their corporate domain-joined computers with their domain credentials.

### Enable Microsoft Entra login in for Windows VM in Azure
* Subscription
* Resource Group
* Virtual Machine Name
* Region
* Availability Options
* Image

---
## Check your knowledge

---

### 1. Which of the following statements about Microsoft Entra ID is true?

A user in the Sales department based in Windsor, whose user and computer accounts reside in the Sales OU, is experiencing conflicting settings. Which GPO’s settings take precedence?

* [ ] Microsoft Entra ID implements the same authentication protocols as on-premises AD DS
* [ ] Microsoft Entra ID is the equivalent on-premises AD DS in the cloud.
* [ ] Microsoft Entra users and groups are created in a flat structure.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Microsoft Entra users and groups are created in a flat structure.
💡 Microsoft Entra users and groups are created in a flat structure, and there are no OUs or GPOs.

</details>

---

### 2. Contoso IT staff have set up Microsoft Entra Connect and are beginning to synchronize accounts. Maria in IT finds a new user account in Microsoft Entra ID that has been created by the Microsoft Entra Connect process. Which of the following accounts would Maria have found?

* [ ] Maria found an account called `MSOL_c778af008d92`.
* [ ] Marie found an account called `Sync_CONTOSO-DC1_c778af008d92@Contoso.com`.
* [ ] Maria found an account called `AAD_c778af008d92`.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Marie found an account called `Sync_CONTOSO-DC1_c778af008d92@Contoso.com`.
💡 An account with the prefix Sync is created in Microsoft Entra ID as part of the Microsoft Entra Connect setup.

</details>

---

### 3. Which of the following sign-in methods is NOT available for Contoso IT staff to combine with Seamless SSO?

A user in the Sales department based in Windsor, whose user and computer accounts reside in the Sales OU, is experiencing conflicting settings. Which GPO’s settings take precedence?

* [ ] Password Hash Synchronization.
* [ ] AD FS.
* [ ] Pass-through authentication.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** AD FS
💡 You can combine Seamless SSO with both Password Hash Synchronization and Pass-Through Authentication, but not AD FS.

</details>

---

# Describe Microsoft Entra Domain Services

The Contoso IT team deploys a number of line-of-business (LOB) applications on computers and devices that are domain members. Contoso uses AD DS–based credentials for authentication, and GPOs to manage those devices and apps. Now they're considering moving these apps to run in Azure. A key issue for you is how to provide authentication services to these apps.

To satisfy this need, the Contoso IT team can choose to:

* Implement a site-to-site virtual private network (VPN) between your local infrastructure and the Azure IaaS.
* Deploy replica domain controllers from your local AD DS as VMs in Azure.
However, these approaches can entail additional costs and administrative effort. Also, the difference between these two approaches is that with the first option, authentication traffic crosses the VPN; in the second option, replication traffic crosses the VPN and authentication traffic remains in the cloud. Microsoft provides Microsoft Entra Domain Services as an alternative to these approaches.

### What is Microsoft Entra Domain Services?

Microsoft Entra Domain Services, which runs as part of the Microsoft Entra ID P1 or P2 tier, provides domain services such as Group Policy management, domain joining, and Kerberos authentication to your Microsoft Entra tenant. These services are fully compatible with on-premises AD DS, so you can use them without deploying and managing additional domain controllers in the cloud.

Because Microsoft Entra ID can integrate with your on-premises AD DS, when you implement Microsoft Entra Connect, users can utilize organizational credentials in both on-premises AD DS and in Microsoft Entra Domain Services. Even if you don't have AD DS deployed locally, you can choose to use Microsoft Entra Domain Services as a cloud-only service. This enables you to have similar functionality of locally deployed AD DS without having to deploy a single domain controller on-premises or in the cloud.

For example, Contoso IT staff can choose to create a Microsoft Entra tenant and enable Microsoft Entra Domain Services, and then deploy a virtual network (VNet) between its on-premises resources and the Microsoft Entra tenant. Contoso IT staff can enable Microsoft Entra Domain Services for this VNet so that all on-premises users and services can use domain services from Microsoft Entra ID.

Microsoft Entra Domain Services provides several benefits for organizations, such as:
* Administrators not needing to manage, update, and monitor domain controllers.
* Administrators not needing to deploy and manage Active Directory replication.
* There's no need to have Domain Admins or Enterprise Admins groups for domains that Microsoft Entra Domain Services manages.

If you choose to implement Microsoft Entra Domain Services, you must understand the service's current limitations. These include:

* Only the base computer Active Directory object is supported.
* It's not possible to extend the schema for the Microsoft Entra Domain Services domain.
* The OU structure is flat, and nested OUs aren't currently supported.
* There's a built-in GPO, which exists for computer and user accounts.
* It's not possible to target OUs with built-in GPOs. Additionally, you can't use Windows Management Instrumentation (WMI) filters or security-group filtering.

By using Microsoft Entra Domain Services, you can freely migrate applications that use LDAP, NT LAN Manager (NTLM), or the Kerberos protocols from your on-premises infrastructure to the cloud. You can also use applications such as Microsoft SQL Server or SharePoint Server on VMs, or deploy them in Azure IaaS. All this without needing domain controllers in the cloud or a VPN to local infrastructure. The following table identifies some common scenarios that utilize Microsoft Entra Domain Services.

| Advantage | Description |
|----------|-------------|
| Secure administration of Azure VMs | You can join Azure VMs to a Microsoft Entra Domain Services–managed domain, which allows you to use a single set of Active Directory credentials. This approach reduces credential management issues such as maintaining local administrator accounts on each VM or separate accounts and passwords between environments. You can manage and secure VMs that you join to a Microsoft Entra Domain Services–managed domain. You can also apply required security baselines to VMs to lock them down in accordance with corporate security guidelines. For example, you can use Group Policy Management capabilities to restrict the types of applications that can be launched on the VM. |
| On-premises applications that use LDAP bind authentication | Microsoft Entra Domain Services lets applications perform LDAP binds as part of the authentication process. Legacy on-premises applications can lift-and-shift into Azure and continue to seamlessly authenticate users without any change in configuration or user experience. |
| On-premises applications that use LDAP read to access the directory | Microsoft Entra Domain Services lets applications perform LDAP reads against the managed domain to retrieve the attribute information it needs. The application doesn't need to be rewritten, so a lift-and-shift into Azure lets users continue to use the app without realizing there's a change in where it runs. |
| On-premises service or daemon application | Some applications include multiple tiers where one tier performs authenticated calls to a backend tier such as a database. Active Directory service accounts are commonly used. When lifting applications into Azure, Microsoft Entra Domain Services allows continued use of service accounts—either synchronized from on-premises or created in a custom OU—so applications function without change. |
| Remote desktop services in Azure | Microsoft Entra Domain Services can provide managed domain services to remote desktop servers deployed in Azure. |

### Considerations
When implementing the previous scenarios, the following deployment considerations apply:

* Microsoft Entra Domain Services–managed domains use a single, flat OU structure by default. All domain-joined VMs are in a single OU. If desired, you can create custom OUs.
* Microsoft Entra Domain Services uses a built-in GPO each for the users and computers containers. For additional control, you can create custom GPOs and target them to custom OUs.
* Microsoft Entra Domain Services supports the base Active Directory computer object schema. However, you can't extend the computer object's schema.
* You can't change passwords directly in a Microsoft Entra Domain Services–managed domain. End users can change their password either using Microsoft Entra ID's self-service password change mechanism or against the on-premises directory. These changes are then automatically synchronized and available in the Microsoft Entra Domain Services–managed domain.

Also, make sure that:

* Any applications don't need to modify/write to the LDAP directory. LDAP write access to a Microsoft Entra Domain Services–managed domain isn't supported.
* The application doesn't need a custom/extended Active Directory schema. Schema extensions aren't supported in Microsoft Entra Domain Services.
* The applications use a username and password for authentication. Certificate or smart card–based authentication isn't supported by Microsoft Entra Domain Services.
