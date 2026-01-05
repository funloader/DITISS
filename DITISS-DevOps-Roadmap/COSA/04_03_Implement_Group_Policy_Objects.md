# Introduction
---
Learn to implement Group Policy Objects (GPOs) in Active Directory Domain Services (AD DS) in Windows Server.

---

## Scenario
Contoso, Ltd. is a financial services company in Seattle with major offices located throughout the world. Most of its compute environment runs on-premises on Windows Server. This includes virtualized workloads on Windows Server 2016 hosts.

Contoso IT staff is migrating Contoso on-premises servers to Windows Server 2022. As a Windows Server administrator at Contoso, you're responsible for configuring user and computer settings. These settings will be applied by using GPOs.

After completing this module, you’ll understand how group policies work in a Windows Server Active Directory environment.

### Learning objectives
After completing this module, you'll be able to:
- Describe GPOs.
- Describe GPO scope and inheritance.
- Describe domain-based GPOs.
- Create and configure GPOs.
- Explain GPO storage.
- Describe administrative templates and the Central Store.
- Prerequisites
- To get the best learning experience from this module, you should have knowledge and experience of:

AD DS concepts and technologies.
- Core networking technologies.
- Windows client operating systems such as Windows 10.
- Windows PowerShell basics.

---

# Define GPOs

Since early versions of Windows Server, the Group Policy feature of Windows operating systems has provided an infrastructure with which administrators can define settings centrally and then deploy them to computers across their organizations.

Consequently, IT staff at Contoso can define, enforce, and update their entire configuration by using GPO settings. By using GPO settings, they can affect an entire site or a domain within their organization, or they can narrow their focus to a single OU.

> [!TIP]
> Filtering based on security group membership and physical computer attributes also enables Contoso to define the target for their GPO settings even further.

What is Group Policy?
Group Policy is a framework in Windows operating systems with components that reside in AD DS, on domain controllers, and on each Windows Server and client. By using these components, you can manage configuration in an AD DS domain. You define Group Policy settings within a GPO. A GPO is an object that contains one or more policy settings that apply to one or more configuration settings for a user or a computer.

![Diagram](images/m8-group-policy-1-3047661e.png).

Group Policy is a powerful administrative tool. You can use GPOs to push various settings to a large number of users and computers. Because you can apply them to different levels, from the local computer to domain, you also can focus these settings precisely. Primarily, you use Group Policy to configure settings that you do not want users to configure. Additionally, you can use Group Policy to standardize desktop environments on all computers in an organizational unit (OU) or in an entire organization. You also can use Group Policy to provide additional security, to configure some advanced system settings, and for other purposes discussed in a subsequent demonstration unit.

![Diagram](images/m8-group-policy-2-07377f9d.png).

### What are GPOs?
The most granular component of Group Policy is an individual policy setting. An individual policy setting defines a specific configuration, such as a policy setting that prevents a user from accessing registry-editing tools. If you define that policy setting and then apply it to a user, that user will be unable to run tools such as Regedit.exe.

Some settings affect a user, known as user configuration settings or user policies, and some affect the computer, known as computer configuration settings or computer policies.

> [!IMPORTANT]
> Settings do not affect groups directly and apply only to user and computer objects.

Group Policy manages various policy settings, and the Group Policy framework is extensible. You can manage almost any configurable setting with Group Policy.

![Diagram](images/m8-group-policy-3-4bb956fe.png).

To define a policy setting:
1. In the Group Policy Management Editor, locate the policy setting and then select Enter. The policy setting Properties dialog box appears.
2. Change the policy state to Enabled or Disabled. Most policy settings can have three states: Not Configured, Enabled, and Disabled.
3. If required, configure additional values, and when complete, select OK.
GPOs store Group Policy settings. In a new GPO, every policy setting defaults to Not Configured. When you enable or disable a policy setting, Windows Server makes a change to the configuration of users and computers to which the GPO is applied.

> [!NOTE]
> When you return a setting to its Not Configured value, you return it to its default value.

To create a new GPO in a domain:
1. In Group Policy Management, right-click or access the context menu for the Group Policy Objects container, and then select New.
2. To modify the configuration settings in a GPO, right-click or access the context menu for the GPO, and then select Edit. This opens the Group Policy Management Editor snap-in.

The Group Policy Management Editor displays all the policy settings that are available in a GPO in an organized hierarchy that begins with the division between computer settings and user settings: the Computer Configuration node and the User Configuration node.

GPOs display in a container named Group Policy Objects. The next two levels of the hierarchy are nodes named Policies and Preferences. Progressing through the hierarchy, the Group Policy Management Editor displays folders, called nodes or policy setting groups. The policy settings are within the folders.

### What are starter GPOs?
You can use a Starter GPO as a template from which to create other GPOs within the Group Policy Management Console. Starter GPOs only have Administrative Template settings. You might use a Starter GPO to provide a starting point to create new GPOs in your domain. The Starter GPO might already have specific settings that are best practices for your environment. You can export starter GPOs to, and import them from, cabinet (.cab) files to make distribution to other environments simple and efficient.

> [!NOTE]
> The Group Policy Management Console stores Starter GPOs in a folder called StarterGPOs, which is in SYSVOL.

> [!NOTE]
> SYSVOL is a shared folder on domain controllers.

Microsoft includes pre-configured Starter GPOs for Windows client operating systems. These Starter GPOs have Administrative Template settings that reflect best practices that Microsoft recommends for the configuration of the client environment.

---

# Implement GPO scope and inheritance

Policy settings in GPOs define configuration. However, you must specify the computers or users to which the GPO applies before the configuration changes in a GPO will affect computers or users in your organization. This is called scoping a GPO. The scope of a GPO is the collection of users and computers that will apply the settings in the GPO.

> [!IMPORTANT]
> You scope a GPO by linking it to an OU that contains the target users and computers.

### Scope a GPO
You can use several methods to manage the scope of domain-based GPOs. The first is the GPO link. In AD DS, you can link GPOs to:

* Sites
* Domains
* OUs

The site, domain, or OU then becomes the maximum scope of the GPO. The configurations that the policy settings in the GPO specify will affect all computers and users within the site, domain, or OU, including those in child OUs. You can link a GPO to more than one domain, OU, or site.

> [!CAUTION]
> Linking GPOs to multiple sites in a multiple domain forest can introduce performance issues when applying the policy, and you should avoid linking GPOs to multiple sites in this situation. This is because, in a multi-forest multiple-site network, the GPOs are stored on the domain controllers in the domain where the GPOs were created. The consequence of this is that computers in other domains might need to traverse a slow wide area network (WAN) link to obtain the GPOs.

You can further narrow the scope of the GPO with one of two types of filters discussed in the following table.

| Filter   | Description |
|----------|-------------|
| Security | Specifies security groups or individual user or computer objects that relate to a GPO’s scope, indicating whether the GPO should or should not apply to them. |
| WMI      | Specifies a scope using system characteristics, such as operating system version or available free disk space. |

![Diagram](images/m8-group-policy-4-20d1e6db.png).

Use security filters and WMI filters to narrow or specify the scope within the initial scope that the GPO link created. The following is an example of a WMI filter that results in a list of computers running Windows 10.


```powershell
select * from Win32_OperatingSystem where Version like "10.%"

```
### GPO processing order

The GPOs that apply to a user, computer, or both don't apply all at once. GPOs apply in a particular order. Conflicting settings that process later might overwrite settings that process first.

Group Policy follows the following hierarchical processing order:
1. Local GPOs
2. Site-linked GPOs
3. Domain-linked GPOs
4. OU-linked GPOs
5. Child OU-linked GPOs

> [!IMPORTANT]
> In Group Policy application, the default rule is that the last policy (the most specific policy) applied prevails.

For example, a policy that restricts access to the Control Panel applied at the domain level could be reversed by a policy applied at the OU level for the objects contained in that particular OU.

If you link several GPOs to an OU, their processing occurs in the order that the administrator specifies on the OU’s Linked Group Policy Objects tab in the Group Policy Management Console. By default, processing is enabled for all GPO links. You can disable a container’s GPO link to block the application of a GPO completely for a given domain or OU. For example, if you made a recent change to a GPO and it's causing production issues, you can disable the link or links until the issue resolves.

> [!NOTE]
> Note that if the GPO is linked to other containers, they'll continue to process the GPO if their links are enabled.

You also can disable the user or computer configuration of a particular GPO independently from either the user or computer. If one section of a policy is known to be empty, disabling the other section can speed up policy processing slightly. For example, if you have a policy that only delivers user desktop configuration, you could disable the computer section of the policy.

### GPO inheritance

You can configure a policy setting in more than one GPO, which might result in GPOs conflicting with each other. In this case, the precedence of the GPOs determines which policy setting the client applies. A GPO with higher precedence prevails over a GPO with lower precedence. Precedence is determined numerically. Each GPO has a precedence value. The lower the number, the higher the precedence. Therefore, a GPO that has a precedence of one prevails over all other GPOs.

The default behavior of Group Policy is that GPOs linked to a higher-level container are inherited by lower-level containers. When a computer starts up or a user signs in, the Group Policy Client Extensions examines the location of the computer or user object in AD DS and evaluates the GPOs with scopes that include the computer or user. Then, the client-side extensions apply policy settings from these GPOs. Policies apply sequentially, beginning with the policies that link to the site, followed by those that link to the domain, followed by those that link to OUs. This sequential application of GPOs creates an effect called policy inheritance. Policies are inherited, which means that the Resultant Set of Policies (RSoPs) for a user or computer will be the cumulative effect of site, domain, and OU policies.

### Block Inheritance

You can configure a domain or OU to prevent the inheritance of policy settings. This is known as blocking inheritance. To block inheritance, right-click or access the context menu for the domain or OU in the GPMC console tree, and then select Block Inheritance.

![Diagram](images/m8-group-policy-5-f65ab601.png).

The Block Inheritance option is a property of a container, so it blocks all Group Policy settings from GPOs that link to parents in the Group Policy hierarchy.

> [!CAUTION]
> The Block Inheritance option is a property of a container, so it blocks all Group Policy settings from GPOs that link to parents in the Group Policy hierarchy.

> [!TIP]
> With security group filtering, you can carefully scope a GPO so that it applies to only the correct users and computers in the first place, making it unnecessary to use the Block Inheritance option.

### Enforce a GPO link
Additionally, you can set a GPO link to be enforced. To enforce a GPO link, right-click or access the context menu for the GPO link in the console tree, and then select Enforced from the shortcut menu.

![Diagram](images/m8-group-policy-6-69631719.png).

> [!IMPORTANT]
> An enforced link applies to child containers even when those containers are set to Block Inheritance. The Enforced option causes the policy to apply to all objects within its scope.

Enforcement is useful when you must configure a GPO that defines a configuration that's mandated by your corporate IT security and usage policies. Therefore, you want to ensure that other GPOs that are linked to the same or lower levels don't override those settings. You can do this by enforcing the GPO’s link.

### Evaluating precedence
To facilitate evaluation of GPO precedence, you can simply select an OU or domain, and then select the Group Policy Inheritance tab. This tab displays the resulting precedence of GPOs, accounting for GPO link, link order, inheritance blocking, and link enforcement.

![Diagram](images/m8-group-policy-7-48f33863.png).

> [!IMPORTANT]
> This tab doesn't account for policies that are linked to a site, for GPO security, or WMI filtering.

---

# Define domain-based GPOs
You can create domain-based GPOs in AD DS and store them on domain controllers. You can use these GPOs to manage configuration centrally for the domain’s users and computers. When you install AD DS, Windows Server creates two default GPOs:

* Default Domain Policy
* Default Domain Controllers Policy

> [!NOTE]
> Windows computers also have local GPOs, which are primarily used when computers aren't connected to domain environments.

### Default Domain Policy
The Default Domain Policy GPO is linked to the domain, and it applies to Authenticated Users. This GPO doesn't have any WMI filters. Therefore, it affects all users and computers in the domain. This GPO contains policy settings that specify password, account lockout, and Kerberos version 5 authentication protocol policies.

These settings are of critical importance to the AD DS environment, and thus, make the Default Domain Policy a critical component of Group Policy. You shouldn't add unrelated policy settings to this GPO. If you need to configure other settings to apply broadly in your domain, create additional GPOs that link to the domain.

### Default Domain Controllers Policy
The Default Domain Controllers Policy GPO links to the OU of the domain controllers. Because computer accounts for domain controllers are kept exclusively in the Domain Controllers OU, and other computer accounts should be kept in other OUs, this GPO affects only domain controllers or other computer objects that are in the Domain Controllers OU.

You should modify GPOs linked to the Domain Controllers OU to implement your auditing policies and to assign user rights that are required on domain controllers.

---

# Create and configure a domain-based GPO
You manage GPOs by using two primary tools:

* The Group Policy Management console
* The Group Policy Management Editor

You can also use **Windows PowerShell cmdlets** to manage GPOs and their settings, including those described in the following table.

| Cmdlet              | Description |
|---------------------|-------------|
| `New-GPO`           | Creates a new GPO. |
| `New-GPLink`        | Links a GPO to a site, domain, or OU. |
| `Get-GPInheritance` | Gets Group Policy inheritance information for a specified domain or OU. |
| `Set-GPInheritance` | Blocks or unblocks inheritance for a specified domain or organizational unit. |
| `Get-GPO`           | Gets one GPO or all the GPOs in a domain. |

### What can you manage with GPOs?
There are two major categories of policy settings: computer settings, which are contained in the Computer Configuration node, and user settings, which are contained in the User Configuration node:

* The Computer Configuration node contains the settings that apply to computers, regardless of who logs on to them. Computer settings apply when the operating system starts, during background refreshes, and every 90 to 120 minutes thereafter.
* The User Configuration node contains settings that apply when a user logs on to a computer, during background refreshes, and every 90 to 120 minutes thereafter.

Within the **Computer Configuration** and **User Configuration** nodes are the **Policies** and **Preferences** nodes.

The Policies nodes in Computer Configuration and User Configuration have a hierarchy of folders that contain policy settings. Because there are thousands of settings, the scope of this course doesn't include individual settings. However, it's worth reviewing the types of settings that you can configure.

### Apply security settings

In the Windows Server operating system, GPOs include a large number of security-related settings that you can apply to both users and computers. For example, you can enforce settings for the domain password policy, for Windows Defender Firewall, and you can configure auditing and other security settings. You also can configure full sets of user-rights assignments.

### Manage desktop and application settings

You can use Group Policy to provide a consistent desktop and application environment for all users in your organization. By using GPOs, you can configure each setting that affects the representation of the user environment. You also can configure settings for some applications that support GPOs.

### Deploy software
With Group Policy, you can deploy software to users and computers. You can use Group Policy to deploy all software that is available in the .msi format. Additionally, you can enforce automatic software installation, or you can let your users decide whether they want the software to deploy to their computers.

> [!IMPORTANT]
> Deploying large software packages with GPOs might not be the most efficient way to distribute an application to your organization’s computers. In some circumstances, it might be more effective to distribute applications as part of the desktop computer image.

### Manage Folder Redirection
With the Folder Redirection option, it is easier to back up users’ data files. By redirecting folders, you also ensure that users have access to their data regardless of the computer to which they sign in. Additionally, you can centralize all users’ data to one place on a network server, while still providing a user experience that is similar to storing these folders on their computers. For example, you can configure Folder Redirection to redirect users’ Documents folders to a shared folder on a network server.

### Configuring network settings
By using Group Policy, you can configure various network settings on client computers. For example, you can enforce settings for wireless networks to allow users to connect only to specific Wi-Fi network SSIDs and with predefined authentication and encryption settings. You also can deploy policies that apply to wired network settings, and some Windows Server roles use Group Policy to configure the client side of services, such as DirectAccess.

### Troubleshooting the application of GPOs?
Group Policy inheritance, filters, and exceptions are complex, and it can often be difficult to determine which policy settings will apply. RSoP is the net effect of GPOs applied to a user or computer, considering GPO links, exceptions such as Enforced and Block Inheritance, and the application of security and WMI filters.

RSoP also is a collection of tools that you can use to evaluate, model, and troubleshoot the application of Group Policy settings. RSoP can query a local or remote computer and report the exact settings that applied to the computer and to any user who has logged on to the computer. RSoP also can model the policy settings that are anticipated to be applied to a user or computer under a variety of scenarios, including moving the object between OUs or sites, or changing the object’s group membership. With these capabilities, RSoP can help you manage and troubleshoot conflicting policies. The following tools exist for performing RSoP analysis:
* The Group Policy Results Wizard.
* The Group Policy Modeling Wizard.
* GPResult.exe.

### How to create, configure, and apply GPOs. The main steps in the process are:

1. Open the Group Policy Management console.
2. Navigate to the Group Policy Objects container.
3. Create a new GPO.
4. Open the GPO for editing and modify some user settings.
5. Link the GPO to the Contoso.com domain.
6. Sign in to a client computer as an administrator and enable Remote Event Log Management and WMI through the firewall.
7. Sign in as a standard user and review the effect of the GPO on the local computer.
8. Create a new GPO, edit its settings, and link it to an OU. Review the inheritance settings.
9. Change the security filtering settings so that the policy only applies to a group, and not Authenticated Users.
10. Verify the effect of the change of inheritance and security filtering.

---
# Define GPO storage

Group Policy settings present as GPOs in AD DS user interface tools, but a GPO actually includes two components.

### What are Group Policy containers and templates?

These two components are described in the following table.

| Component | Description |
|----------|-------------|
| **Group Policy container** | Located in Active Directory, the Group Policy Objects container stores GPO metadata. It does not contain actual settings, but information such as when the GPO was created, how many times user and computer settings were modified, the GPO version, and its GUID, which is used to link Group Policy settings to a Group Policy template. |
| **Group Policy template** | A collection of files stored in the SYSVOL of each domain controller at `%SystemRoot%\SYSVOL\Domain\Policies\GPOGUID`, where `GPOGUID` is the globally unique identifier of the Group Policy container. The Group Policy template contains the actual Group Policy settings. |

> [!NOTE]
> Similar to all AD DS objects, each Group Policy container includes a GUID attribute that uniquely identifies the object within AD DS.

When you change the settings of a GPO, the changes are saved to the SYSVOL share. By default, the domain controller that holds the PDC Emulator operations master role is used. Changes made are then replicated to other domain controllers.

> [!TIP]
> By default, when Group Policy refresh occurs, the client-side extensions apply settings in a GPO only if the GPO has been updated.

The Group Policy client can identify an updated GPO by its version number, as the following describes:

* Each GPO has a version number that increments each time you make a change.
* The version number is stored as a Group Policy container attribute and in a text file, GPT.ini, in the Group Policy template folder.
* The Group Policy client knows the version number of each GPO it has previously applied.
* If, during the Group Policy refresh, the Group Policy client discovers that the version number of the Group Policy container has changed, Windows Server will inform the client-side extensions that the GPO is updated.

### GPO replication

The Group Policy container and the Group Policy template both replicate between all domain controllers in the local domain in AD DS. However, these two items use different replication mechanisms.

* The Group Policy container in AD DS replicates by using the Directory Replication Agent (DRA). The DRA uses a topology that the Knowledge Consistency Checker generates, which you can define or refine manually. The result is that the Group Policy container replicates within seconds to all domain controllers in a site and replicates between sites based on your intersite replication configuration.
* The Group Policy template in the SYSVOL replicates by using the Distributed File System Replication (DFS-R).

> [!CAUTION]
> Because the Group Policy container and Group Policy template replicate separately, it is possible for them to become out-of-sync for a brief time. Typically, when this happens, the Group Policy container will replicate to a domain controller first.

Systems that obtained their ordered list of GPOs from that domain controller will identify the new Group Policy container. Those systems will then attempt to download the Group Policy template, and they'll notice that the version numbers are not the same. A policy processing error will record in the event logs.

If the reverse happens, and the GPO replicates to a domain controller before the Group Policy container, clients that obtain their ordered list of GPOs from that domain controller won't be notified of the new GPO until the Group Policy container has replicated.

---

# Define administrative templates

Administrative template files provide most of the available GPO settings, which modify specific registry keys. The use of administrative templates is known as a registry-based policy, because all the settings you configure in administrative templates result in changes to the registry. For many apps, using a registry-based policy is the simplest and best way to support the centralized management of policy settings.

### Overview of administrative templates
You can use administrative templates to control the environment of an operating system and the user experience. There are two sets of administrative templates:

* Computer-related settings
* User-related settings

![Diagram](images/m8-group-policy-8-34180b69.png).

When you configure settings in the Administrative Templates node of the GPO, you make modifications to the registry. Administrative templates have the following characteristics:

* They have subnodes that correspond to specific areas of the environment, such as network, system, and Windows components.
* The settings in the computer section of the Administrative Templates node edit the HKEY_LOCAL_MACHINE hive in the registry.
* The settings in the user section of the Administrative Templates node edit the HKEY_CURRENT_USER hive in the registry.
* Some settings exist for both user and computer.

> [!IMPORTANT]
> In the case of conflicting settings, the computer setting prevails.

* Some settings are available only to certain versions of Windows operating systems. For example, you can apply several new settings only to Windows 10.

> [!TIP]
> To check which Windows versions are supported, select the setting you want, and then select the Extended tab.

The following table details the organization of the **Administrative Templates** node.

| Administrative Template Section | Settings |
|--------------------------------|----------|
| **Computer Configuration** | Control Panel, Network, Printers, Server, Start Menu and Taskbar, System, Windows Components, All Settings |
| **User Configuration** | Control Panel, Desktop, Network, Shared Folders, Start Menu and Taskbar, System, Windows Components, All Se

Most of the nodes contain multiple subfolders that enable you to organize settings into logical groupings. Even with this organization, finding the setting that you need might be a daunting task.

> [!TIP]
> The All Settings node contains an alphabetically sorted list of all settings contained in all the other nodes.

### What are .admx and .adml files?
All the settings in the Administrative Templates node of a GPO are stored in files. All currently supported operating systems store the settings in .admx files.

These settings use a standards-based XML file format known as .admx files. By default, Windows stores .admx files in the Windows\PolicyDefinitions folder, but you can store them in a central location.

The .admx files are language neutral. The plain language descriptions of the settings are not part of the .admx files. Instead, they're stored in language-specific .adml files. This means that administrators can review the same GPO and observe the policy descriptions in their own language because they can each use their own language-specific .adml files.

The PolicyDefinitions folder stores .adml files subfolders. Each language has its own folder. For example, the en-US folder stores the English files, and the es-ES folder stores the Spanish files. By default, only the .adml language files for the language of the installed operating system are present.

### What is the Central Store?
In domain-based enterprises, you can create a Central Store location for .admx files, which anyone with permissions to create or edit GPOs can access. The Group Policy Management Editor automatically reads and displays administrative templates policy settings from .admx files in the Central Store, and then ignores the .admx files stored locally. If the domain controller or Central Store is not available, the Group Policy Management Editor uses the local store.

The advantages of creating a Central Store are:
* You ensure that whenever someone edits a GPO, the settings in the Administrative Templates node are always the same.
* When Microsoft releases new administrative templates for new operating systems or apps, such as Office, you only need to update the administrative templates files in one location.

You must create the Central Store manually, and then update it manually on a domain controller. The domain controllers then use AD DS replication and DFS-R to replicate the data.

To create a Central Store for .admx and .adml files, create a folder and name it PolicyDefinitions in the \\FQDN\SYSVOL\FQDN\Policies location, where FQDN is the domain name for your AD DS domain.

For example, to create a Central Store for the Seattle.Contoso.com domain, create a PolicyDefinitions folder in the following location:
```powershell
\\Seattle.Contoso.com\SYSVOL\Seattle.Contoso.com\policies

```

An administrator must copy all files and subfolders of the PolicyDefinitions folder, which on a Windows computer resides in the Windows folder. The PolicyDefinitions folder stores all .admx files, and subfolders store .adml files for all languages enabled on the client computer. For example, on a Windows Server computer that has English enabled, C:\Windows\PolicyDefinitions will contain the .admx files and in the subfolder en-US, the .adml files will contain English-based descriptions for the settings defined in the .admx files.

> [!IMPORTANT]
> You must update the PolicyDefinitions folder for each feature update and for other software, such as Windows 10 Version 2004 and Microsoft Office 2019 .admx files.

---
## Check your knowledge

---

### 1. In Adatum.com, there are two sites: London and Windsor. A single GPO (called *London settings*) is linked to London and another (*Windsor settings*) is linked to Windsor. In addition, there are two GPOs linked to the Adatum.com domain: the **Default Domain GPO (Enforced)** and **Adatum Folder Redirection**. The Sales OU has a linked GPO called *Sales Desktop settings*.

A user in the Sales department based in Windsor, whose user and computer accounts reside in the Sales OU, is experiencing conflicting settings. Which GPO’s settings take precedence?

* [ ] The Windsor settings GPO
* [ ] The Sales Desktop settings GPO
* [ ] The Default Domain GPO

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The Default Domain GPO
💡 Because the Default Domain GPO is **Enforced**, its settings cannot be overridden by conflicting settings in Site- or OU-linked GPOs. Enforced GPOs always take precedence downward in the hierarchy.

</details>

---

### 2. Which of the following options contains the actual Group Policy settings?

* [ ] The Group Policy container
* [ ] The Group Policy template

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The Group Policy template
💡 The Group Policy template (GPT), stored in SYSVOL, contains the actual policy settings. The Group Policy container (GPC) only stores metadata such as version numbers and GUIDs.

</details>

---

### 3. The IT department in Adatum is deploying a new version of Microsoft Office in their on-premises environment. The administrator wants to configure Office settings using GPOs. What should they do?

* [ ] Download and install new .adml files and then configure settings in the Administrative Templates node
* [ ] Copy the contents of the Windows\PolicyDefinitions folder to the Central Store
* [ ] Download and install new administrative template files and then configure the desired settings in the Administrative Templates node

<details>
<summary><strong>Show Answer</strong></summary>


### 4. In the `Contoso.com` domain, in the Marketing OU, an administrator creates a GPO called Folder Redirection. The administrator wants the policy to apply to all users in the Marketing OU, except for the Marketing managers. What should the administrator do to prevent the Folder Redirection GPO from applying to the managers, but allow all other GPOs linked to the Marketing OU to apply to the managers?

- [ ] Create a WMI filter that identifies the managers' computers and use that filter to Deny the application of the GPO to the managers.
- [ ] Move the marketing manager user accounts to their own child OU in Marketing, and then implement Block Inheritance on the child OU.
- [ ] Create a global security group called Marketing Managers and add the marketing manager user accounts to the group. Then configure GPO security filtering to Deny the Apply Policy permission to this group.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Create a global security group called Marketing Managers and add the marketing manager user accounts to the group. Then configure GPO security filtering to Deny the Apply Policy permission to this group.  
💡 You can use security filtering to allow or deny the application of a GPO to specific users or groups.
</details>

---

### Summary
Contoso, Ltd. is a financial services company in Seattle with major offices located throughout the world. Most of its compute environment runs on-premises on Windows Server. This includes virtualized workloads on Windows Server 2016 hosts.

Contoso IT staff is migrating Contoso on-premises servers to Windows Server 2022. As a Windows Server administrator at Contoso, you're responsible for configuring user and computer settings. These settings are applied by using GPOs.

After completing this module, you’ll understand how group policies work in a Windows Server Active Directory environment.

---
