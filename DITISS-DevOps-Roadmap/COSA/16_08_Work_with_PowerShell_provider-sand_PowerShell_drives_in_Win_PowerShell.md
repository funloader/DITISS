# Connect with data stores using PowerShell providers

## Introduction 

In this module, you'll learn about PowerShell providers, which are adapters that connect Windows PowerShell to data stores. They offer an easier-to-understand and consistent interface for working with data stores. You can also reuse scripts as you change the underlying technologies with which you're working.

### Learning objectives:
After completing this module, you'll be able to:

* Explain the purpose of PowerShell providers.
* Compare different PowerShell provider capabilities.
* Explain how to access PowerShell provider help files.
* Explain how to review a list of providers and the help options for a specific provider.

### Prerequisites
Familiarity with:

* Windows networking technologies and implementation.
* Windows Server administration, maintenance, and troubleshooting.
* Windows PowerShell and its commands to perform specific tasks.
* PowerShell cmdlets used for system administration tasks related to Active Directory, network configuration, server administration, and Windows 10 device administration.
* Windows PowerShell pipeline.

## Define Windows PowerShell providers

A PowerShell provider, or just provider, is an adapter that makes some data stores resemble hard drives within Windows PowerShell. Because most administrators are already familiar with managing hard drives using command-line commands, PowerShell providers help those administrators manage other forms of data storage using the same familiar commands.

A provider presents data as a hierarchical store. For example, items such as folders can have sub-items that appear as subfolders. Items can also have properties, and providers let you manipulate both items and their properties by using a specific set of commands.

Managing a technology by using a provider is more difficult than managing it by using technology-specific commands. Individual commands perform specific actions, and the command name describes what the command does. For example, in Internet Information Services (IIS), the Get-WebSite command retrieves IIS sites. When you use the IIS provider, you run the Get-ChildItem IIS:\Sites command instead.

The advantage of a PowerShell provider is that it's dynamic, which makes it suitable for technologies that are subject to frequent changes. For example, when managing IIS, its provider can accommodate newly introduced Microsoft and third-party IIS add-ins. Even though using a provider to manage dynamic and extensible technologies tends to be more complex, it offers a more consistent approach due to its extensibility.

Some common providers include:

* Registry. Provides access to the registry keys and values.
* Alias. Provides access to aliases for Windows PowerShell cmdlets.
* Environment. Provides access to Windows environment variables and their values.
* FileSystem. Provides access to the files and folders in the file system.
* Function. Provides access to Windows PowerShell functions loaded into memory.
* Variable. Provides access to Windows PowerShell variables and their values loaded into memory.

## Review the built-in providers in PowerShell

The generic commands that you use to work with providers offer a superset of every feature that a provider might support. For example, the **Get-ChildItem** command includes the *–UseTransaction* parameter. However, the only built-in provider that supports the Transactions capability is the Registry provider. If you try to use the *-UseTransaction* parameter in any other provider, you'll receive an error message. You'll also receive an error message whenever you use a common parameter that the provider doesn't support.

Running the **Get-PSProvider** cmdlet lists the capabilities of each provider that loads into Windows PowerShell. The capabilities of each provider will be different because each provider connects to a different underlying technology.

Some important capabilities include:

* **ShouldProcess** for providers that can support the –WhatIf and –Confirm parameters.
* **Filter** for providers that support filtering.
* **Include** for providers that can include items in the data store based on the name. Supports using wildcards.
* **Exclude** for providers that can exclude items in the data store based on the name. Supports using wildcards.
* **ExpandWildcards** for providers that support wildcards in their paths.
* **Credentials** for providers that support alternative credentials.
* **Transactions** for providers that support transacted operations.

You should always review the capabilities of a provider before you work with it. This helps you avoid unexpected errors when you try to use unsupported capabilities.

### Access provider help in PowerShell

You can display a list of available providers by using the Get-PSProvider cmdlet. Be aware that providers can be added into Windows PowerShell when you load modules, and they don't display until loaded. For example, when you run the **Import-Module ActiveDirectory** command to load the ActiveDirectory module or use module autoloading when running an Active Directory cmdlet, a PowerShell provider for Active Directory is included.

Some providers include help files that you can review. Help files use the naming format about_ProviderName_Provider. For example, the help file for the FileSystem provider is about_FileSystem_Provider. You can review this help file's contents by running the following command:

```powershell
Get-Help about_FileSystem_Provider
```

Cmdlets that work with providers use the nouns Item and ItemProperty. To list cmdlets that work with providers, run the following cmdlets:

```powershell
Get-Command *-Item,*-ItemProperty
```

Examples for every scenario might not be in commands’ help, because the commands are designed to work with any provider. The intent of provider help is to supplement command help with more specific descriptions and examples.

---

### Summary

In this module, you learned about PowerShell providers, their capabilities, and how to access PowerShell provider help files. The following are the key takeaways:

* A PowerShell provider, or just provider, is an adapter that makes some data stores resemble hard drives within Windows PowerShell. They offer an easier-to-understand and consistent interface for working with data stores.
* The advantage of a PowerShell provider is that it's dynamic, which makes it suitable for technologies that are subject to frequent changes.
* Some common providers include Registry, Alias, Environment, FileSystem, Function, and Variable.
* The Get-PSProvider cmdlet lists the capabilities of each provider that loads into Windows PowerShell.
* Some providers include help files that you can review. Help files use the naming format about_ProviderName_Provider.

---
## Check your knowledge

---

---

### 1. Which command would you use to get help information for the Registry provider?

* [ ] `Get-Help about_Registry_Provider`
* [ ] `Get-Command Registry_Provider`
* [ ] `Get-Help Registry_Provider`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `Get-Help about_Registry_Provider`
💡 PowerShell providers have conceptual help topics that begin with **about_**. To view help for the Registry provider, you use `Get-Help about_Registry_Provider`.

</details>

---

### 2. Which of the following options is a PowerShell provider that loads automatically when you open a Windows PowerShell prompt?

* [ ] HKCU
* [ ] Alias
* [ ] ActiveDirectory

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Alias
💡 The **Alias** provider is built into PowerShell and loads automatically. `HKCU` is a registry drive, and `ActiveDirectory` requires the Active Directory module to be installed and imported.

</details>

---

# Use PowerShell drives in PowerShell

This module explains how to work with PowerShell drives.

### Learning objectives
Upon completion of this module, the learner will be able to:

* Explain the purpose and use of PowerShell drives.
* Identify the cmdlets for using PowerShell drives.
* Explain how to find, delete, and create files and directories.
* Explain how to use Windows PowerShell to manage the file system.
* Explain how to work with the registry.
* Explain how to use Windows PowerShell to manage the registry.
* Explain how to work with certificates.
* Explain how to work with other PowerShell drives.

### Prerequisites

* Familiarity with Windows networking technologies and implementation.
* Familiarity with Windows Server administration, maintenance, and troubleshooting.
* Familiarity with Windows PowerShell and its commands to perform specific tasks.
* Familiarity with PowerShell cmdlets used for system administration tasks related to Active Directory, network configuration, server administration, and Windows 10 device administration.
* Familiarity with Windows PowerShell pipeline.

## Explain PowerShell drives in PowerShell

A PowerShell drive, or drive, is a connection to a data store. Each PowerShell drive uses a single PowerShell provider to connect to a data store. The PowerShell drive has all the capabilities of the PowerShell provider that it uses to make the connection.

Names identify drives in Windows PowerShell. Drives can consist of a single letter. Single-letter drive names typically connect to a **FileSystem** drive. For example, drive C connects to the physical drive C of a computer. However, names also can consist of more than one character. For example, the drive **HKCU** connects to the **HKEY_CURRENT_USER** registry hive.

To create a new connection, you use the **New-PSDrive** cmdlet. You must specify a unique drive name, the root location for the new drive, and the PowerShell provider that will make the connection. Depending on the PowerShell provider's capabilities, you might also specify alternative credentials and other options.

Windows PowerShell always starts a new session with the following drives:

* Registry drives **HKLM** and **HKCU**
* Local hard drives, such as drive C
* Windows PowerShell storage drives **Variable**, **Function**, and **Alias**
* Web Services for Management (WS-Management) settings drive **WSMan**
* Environment variables drive **Env**
* Certificate store drive **CERT**

You can review a list of drives by running the Get-PSDrive cmdlet.

> [!NOTE]
>  Drive names don't include a colon. Drive name examples include Variable and Alias. However, when you want to refer to a drive as a path, include a colon. For example, Variable: refers to the path to the Variable drive, just as C: refers to the path to drive C. Cmdlets such as New-PSDrive require a drive name, but when using these commands, don't include a colon in the drive name.

## Use PowerShell drive cmdlets in PowerShell

Because Windows PowerShell creates PowerShell drives for local drives (such as drive C), you might already be using some of the cmdlets associated with PowerShell drives without realizing it. PowerShell drives contain items that contain child items or item properties. The Windows PowerShell cmdlet names that work with PowerShell drive objects use the nouns Item, ChildItem, and ItemProperty.

You can use the Get-Command cmdlet with the -Noun parameter to review a list of commands that work on each PowerShell drive object. You can also use Get-Help to review the help for each command. The following table describes the verbs that are associated with common PSDrive cmdlets.

*Table 1: PSDrive cmdlet verbs*

| Verb   | Description                                                                 |
|--------|-----------------------------------------------------------------------------|
| New    | Creates a new item or item property.                                        |
| Set    | Sets the value of an item or item property.                                 |
| Get    | Displays properties of an item or child item, or value of an item property. |
| Clear  | Clears the value of an item or item property.                               |
| Copy   | Copies an item or item property from one location to another.               |
| Move   | Moves an item or item property from one location to another.                |
| Remove | Deletes an item or item property.                                            |
| Rename | Renames an item or item property.                                            |
| Invoke | Performs the default action that's associated with an item.                 |

The items in the various PowerShell drives behave differently. Although these commands work in all PowerShell drives, how the verbs act on the items in each PowerShell drive might vary. Additionally, other commands might work with those items. The other topics in this module describe how to work with specific PowerShell drives.

When you use commands that have the Item, ChildItem, and ItemProperty nouns, you typically specify a path to tell the command what item or items you want to manipulate. Most of these commands have two parameters for paths:

* *–Path.* This typically interprets the asterisk (*) and the question mark (?) as wildcard characters. In other words, the path *.txt refers to all files ending in “.txt.” This approach works correctly in the file system because the file system doesn't allow item names to contain the asterisk or question mark characters.

* *–LiteralPath.* This parameter treats all characters as literals and doesn't interpret any character as a wildcard. The literal path .txt means the item named “.txt.” This approach is useful in drives where the asterisk and question mark characters are allowed in item names, such as in the registry.

### Working with PowerShell drive locations

In addition to the commands for working with PowerShell drive items and item properties, there are also commands for working with PowerShell drive working locations. Working locations are paths within PowerShell drives to items that can have child items, such as a file system folder or registry path. The commands that manage PowerShell drive locations use the Location noun and include those described in the following table.

**Table 2: Location commands**

| Command        | Description                                              |
|----------------|----------------------------------------------------------|
| Get-Location  | Displays the current working location.                  |
| Set-Location  | Sets the current working location.                      |
| Push-Location | Adds a location to the top of a location stack.         |
| Pop-Location  | Changes the current location to the location at the top of a location stack. |

> [!NOTE]
>  The Push-Location and Pop-Location cmdlets are the equivalent of the pushd and popd commands in the Windows Command Prompt (cmd.exe) console. In PowerShell, pushd and popd are aliases for those cmdlets.

### Manage the file system in PowerShell

Administrators who are familiar with using the Windows Command Prompt **(cmd.exe)** most likely know commands to manage a file system. Common cmd.exe commands include **Dir, Move, Ren, RmDir, Del, Copy, MkDir,** and **Cd**. In Windows PowerShell, these common commands are provided as aliases or functions that map to equivalent PowerShell drive cmdlets.

You can use the **Get-Alias** or **Get-Command** cmdlets to identify the cmdlets that map to these aliases and functions. Keep in mind that the aliases and functions aren't exact duplicates of the original cmd.exe commands, but instead the syntax of an alias matches the corresponding cmdlet. For example, the Dir command is an alias for the **Get-ChildItem** cmdlet. To obtain a directory listing that includes subdirectories, you run the **Get-ChildItem –Recurse** command. The parameters are the same whether you decide to use the cmdlet name or the alias. That means that you can run the **Dir –Recurse** command, but not **Dir /s** as you would when using Windows Command Prompt.

> [!NOTE]
>  Because Windows PowerShell accepts a slash (/) or backslash (\) as a path separator, Windows PowerShell interprets Dir /s to display a directory listing for the folder named s. If a folder named s exists, the command appears to work and doesn't display an error. If no such folder exists, it displays an error.

### Moving within the file system

You can move within the file system by using the **Set-Location** cmdlet. This cmdlet functions similar to the Windows Command Prompt command Cd. When using it, you can specify either an absolute or a relative path. For example, **Set-Location C:\Users** changes to the C:\Users folder. **Set-Location Temp** changes to the Temp folder that's one level down from the current directory.

### Create new files or folders

You can create new files and folders by using the **New-Item** cmdlet. You include the *-Path* parameter to define the name and location, and the *-ItemType* parameter to specify whether you want to create a file or directory.

### Delete files or folders

You can remove files or folders with the **Remove-Item** cmdlet and the positional *-Path* parameter. To delete folders that contain files, you need to include the *-Recurse* switch so that the child file items are also deleted. Otherwise, or you'll be asked to confirm the action.

### Find and enumerate files or folders

Use the **Get-Item** cmdlet and the *-Path* parameter to retrieve a single file or folder. You can also retrieve the children of an item by including the * wildcard in the path. For example, the Get-Item * command returns all files and folders in the current directory. The Get-Item * command is equivalent to the Get-ChildItem cmdlet, which returns all the children of a specified path.

You can use the **Get-ChildItem** cmdlet with the *-Recurse* switch to enumerate through child files and folders. The FileSystem provider also supports the *-Exclude, -Include,* and *-Filter* parameters. These modify the value of the *-Path* parameter and specify file and folder names to include or exclude in the retrieval process.

### Manage the registry in PowerShell

Experienced system administrators are familiar with the graphical Registry Editor, which they can use to manage registry keys, entries, and values. However, you can also manage the registry by using Windows PowerShell and the Registry provider.

You can use the New-PSDrive cmdlet to create PowerShell drives for any part of the registry. PowerShell uses the Registry provider to create two PowerShell drives automatically:

* **HKLM.** Represents the **HKEY_LOCAL_MACHINE** registry hive.

* **HKCU.** Represents the **HKEY_LOCAL_USER** registry hive.

You access registry keys by using cmdlets with the **Item** and **ChildItem** nouns, whereas you access entries and values by using cmdlets with the ItemProperty and ItemPropertyValue nouns. This is because PowerShell considers registry entries to be properties of a key item.

To return all the registry keys under the **HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion** path, run the following command:

```powershell
Get-ChildItem HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion
```

Within the registry, a registry key is equivalent to a folder within a file system that's used to organize information. The information used by apps is stored in registry values. The value name is a unique identifier for the value, and the value data is the information used by apps.

For example, to return the registry values under the HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run path, run the following command:

```powershell
Get-ItemProperty HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run
```

You can use the Get-ItemPropertyValue cmdlet to obtain the value of a specific registry entry. For example, if you want to return the path to the Windows Defender executable identified by the value WindowsDefender entry, run the following command:

```powershell
Get-ItemPropertyValue HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Run -Name WindowsDefender
```

> [!NOTE]
> The Registry provider doesn't support the Invoke-Item cmdlet. There's no default action for registry keys, entries, or values.

The Registry provider supports a dynamic parameter, -Type, for the *-ItemProperty cmdlets that are unique to the Registry provider. The following table lists valid parameter values and their equivalent registry data types.

*Table 1: Registry data types*

| Parameter value | Registry data type |
|----------------|-------------------|
| String        | REG_SZ            |
| ExpandString  | REG_EXPAND_SZ     |
| Binary        | REG_BINARY        |
| DWord         | REG_DWORD         |
| MultiString   | REG_MULTI_SZ      |
| QWord         | REG_QWORD         |
| Unknown       | Unsupported types such as REG_RESOURCE_LIST |

The Registry provider supports transactions that allow you to manage multiple commands as a single unit. The commands in a transaction will either all be committed (completed) or the results will be rolled back (undone). This feature allows you to set multiple registry values together without worrying that some of the settings will be updated successfully while others might fail. Use the *-UseTransaction* parameter to include a command in a transaction.


> [!NOTE]
>  For more information about transactions in Windows PowerShell, refer to the about_Transactions help topic.


> [!NOTE]
>  Remember to back up your registry settings before you attempt to modify registry keys and values. You can export registry settings to a file by using the reg.exe command.

### Work with certificates in PowerShell

If you've reviewed or managed security certificates on a client or server computer, you've probably used the Certificates snap-in for the Microsoft Management Console (MMC). The Certificates snap-in enables you to browse the certificates stores on local or remote computers. The Windows PowerShell Certificates provider also allows you to review and manage security certificates.

The Certificates provider creates a PowerShell drive named Cert. The Cert drive always has at least two high-level store locations that group certificates for the users and the local computer. These locations are CurrentUser and LocalMachine. The certificates specific to the user or computer are in the My subfolder, represented by the Cert:\CurrentUser\My notation.

The Certificates provider supports the Get, Set, Move, New, Remove, and Invoke verbs in combination with the Item and ChildItem nouns. (Note that the ItemProperty noun is not supported.) All *-Location commands are also supported.

The Invoke-Item cmdlet in combination with the Certificates provider opens the MMC with the Certificates snap-in automatically loaded.

The Get-ChildItem command has various dynamic parameters that are unique to the Certificate provider. These parameters include:

* *-CodeSigningCert.* Gets certificates that can be used for code signing.
* *-DocumentEncryptionCert.* Gets certificates for document encryption.
* *-DnsName.* Gets certificates with the domain name in the DNSNameList property of the certificate. This parameter accepts wildcards.
* *-EKU.* Gets certificates with the specified text in the EnhancedKeyUsageList property. This parameter supports wildcards.
* *-ExpiringInDays.* Gets certificates that are expiring within the specified number of days.
* *-SSLServerAuthentication.* Gets only Secure Sockets Layer (SSL) server certificates.

There are also many certificate management cmdlets in the pki module that don't require you to use the Cert drive. For example, to create a self-signed certificate for the server `webapp.contoso.com`, use the following code:

```powershell
New-SelfSignedCertificate -DnsName "webapp.contoso.com" -CertStoreLocation "Cert:\LocalMachine\My"
```

> [!NOTE]
> For a list of certificate management cmdlets in the **pki** module, run **Get-Command -Module pki**.

### Work with other PowerShell drives in PowerShell

In addition to the file system drives, the registry drives, and the **Cert** drive, Windows PowerShell includes other drives:

* **Alias.** Review and manage Windows PowerShell aliases.
* **Env.** Review and manage Windows environment variables.
* **Function.** Review and manage Windows PowerShell functions.
* **Variable.** Review and manage Windows PowerShell variables.
* **WSMan.** Review and manage WS-Management configurations.

There are many providers included with other modules that can create PowerShell drives. For example, the process of installing management tools for Windows Server roles often includes additional drives such as:

* **AD**. This drive is created by the ActiveDirectory provider, which is part of the ActiveDirectory module included with the Remote Server Administration Tools (RSAT). The ActiveDirectory provider supports reviewing and managing AD DS database contents, such as user and computer accounts.
* **IIS**. This drive is created by the WebAdministration provider, which is part of the WebAdministration module that's included with IIS management tools. The WebAdministration provider allows you to review and manage application pools, websites, web applications, and virtual directories.


> [!NOTE]
>  The ActiveDirectory module includes many cmdlets for managing Active Directory objects. To review the cmdlets in the ActiveDirectory module, run Get-Command -Module ActiveDirectory.

> [!NOTE]
>  The WebAdministration module includes many cmdlets for managing IIS. To review the cmdlets in the WebAdministration module, run Get-Command -Module WebAdministration.

These additional drives support using most of the standard provider verbs and nouns. There might also be specific cmdlets that can perform the same functions. For instance, you can use the Get-Alias cmdlet or the following provider-based command to return a list of all aliases in the current Windows PowerShell session:

```powershell
Get-Item -Path Alias:
```

In some cases, there are no equivalent cmdlets for a provider-based command. For example, there's no Remove-Alias cmdlet that deletes an alias, but you can use either of the following commands to delete an alias named MyAlias:

```powershell
Remove-Item -Path Alias:MyAlias
```

```powershell
Clear-Item -Path Alias:MyAlias
```

As with the other providers covered by earlier topics, the providers used to create these drives can have dynamic parameters or properties associated with them. The Alias provider, for example, includes the dynamic parameter -Options, which you can use to specify the Options property of an alias.

To understand what you can do with an item that's accessible through a drive, you should review the help for the provider that's used to create the drive. In the help, you can identify any dynamic parameters or properties. You can identify the provider used to create a drive by using the Get-PSDrive cmdlet. You can use the Get-Help cmdlet to review the help available for the provider. For example, you could use the command to review help for the Alias provider:

```powershell
Get-Help About_Alias_Provider
```
### Summary

In this module, you learned how to work with PowerShell drives that are the primary interface for working with the underlying data. The following are the key takeaways:

* A PowerShell drive, or drive, is a connection to a data store. Each PowerShell drive uses a single PowerShell provider to connect to a data store. The PowerShell drive has all the capabilities of the PowerShell provider that it uses to make the connection.
* To create a new connection, use the New-PSDrive cmdlet.
* To review a list of drives, use the Get-PSDrive cmdlet.
* PowerShell drives contain items that contain child items or item properties. The Windows PowerShell cmdlet names that work with PowerShell drive objects use the nouns Item, ChildItem, and ItemProperty.
* In Windows PowerShell, the common cmd.exe commands such as **Dir, Move, Ren, RmDir, Del, Copy, MkDir,** and **Cd** are provided as aliases or functions that map to equivalent PowerShell drive cmdlets.
* To create PowerShell drives for any part of the registry, use the New-PSDrive cmdlet.
* The Windows PowerShell Certificates provider also allows you to review and manage security certificates. The Certificates provider creates a PowerShell drive named Cert.
* Other PowerShell drives include Alias, Env, Function, Variable, and WSMan.

---
## Check your knowledge

---

### 1. Which of the following PowerShell drives is created by the Registry provider?

* [ ] AD
* [ ] HKCU
* [ ] C

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HKCU
💡 The Registry provider creates drives such as **HKCU** (HKEY_CURRENT_USER) and **HKLM** (HKEY_LOCAL_MACHINE).

</details>

---

### 2. Which provider is used to create PowerShell drives that are mapped to a network share?

* [ ] FileSystem
* [ ] Function
* [ ] Variable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** FileSystem
💡 The **FileSystem** provider is used to create PowerShell drives mapped to file system locations, including network shares.

</details>

---
