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

