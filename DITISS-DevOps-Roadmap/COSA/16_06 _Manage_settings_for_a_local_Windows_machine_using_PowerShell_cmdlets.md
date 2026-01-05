# Introduction

In addition to network service and configuration settings, PowerShell is commonly used to configure and manage settings on a local Windows machine. PowerShell cmdlets can help to perform GUI-based operations more quickly or provide a basis to run multiple commands within a script.

In this module, you'll learn about common PowerShell cmdlets that can be used to perform tasks on a Windows 10 computer.

### Learning objectives
After completing this module, you'll be able to:

* Describe the cmdlets for managing Windows 10 devices.
* Describe the cmdlets for managing local permissions with Windows PowerShell.

### Prerequisites
Familiarity with:

* Windows networking technologies and implementation.
* Windows Server administration, maintenance, and troubleshooting.
* Windows PowerShell and its commands to perform specific tasks.

---
# Manage Windows 10 using PowerShell

You most likely use the Windows 10 GUI interface to change configuration settings and perform management tasks on Windows 10 workstations. However, you might be able to perform some tasks quicker by opening a PowerShell console and running a cmdlet.

The Microsoft.PowerShell.Management module includes many built-in cmdlets that can be used to obtain information and perform specific operations on a local computer. To review the cmdlets included in this module, you can enter the following:

```powershell
Get-command -module Microsoft.PowerShell.Management
```

The following table lists some of the more common cmdlets included in the Microsoft.PowerShell.Management module.

Table 1: Cmdlets included in the Microsoft.PowerShell.Management module

| Cmdlet             | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Get-ComputerInfo   | Retrieves all system and operating system properties from the computer     |
| Get-Service        | Retrieves a list of all services on the computer                            |
| Get-EventLog       | Retrieves events and event logs from local and remote computers (only available in Windows PowerShell 5.1) |
| Get-Process        | Retrieves a list of all active processes on a local or remote computer     |
| Stop-Service       | Stops one or more running services                                          |
| Stop-Process       | Stops one or more running processes                                         |
| Stop-Computer      | Shuts down local and remote computers                                       |
| Clear-EventLog     | Deletes all of the entries from the specified event logs on the local computer or on remote computers |
| Clear-RecycleBin   | Deletes the content of a computer's recycle bin                             |
| Restart-Computer   | Restarts the operating system on local and remote computers                |
| Restart-Service    | Stops and then starts one or more services                                  |

### Running management cmdlets
The following cmdlets are examples of how to use some of the management cmdlets in Windows 10:

* To retrieve detailed information about the local computer, run the following command:

```powershell
Get-ComputerInfo
```
* To retrieve the latest five error entries from the Application log, run the following command:

```powershell
Get-EventLog -LogName Application -Newest 5 -EntryType Error
```
* To clear the Application log on the local computer, run the following command:

```powershell
Clear-EventLog -LogName Application
```
---
# Manage permissions with PowerShell

The Microsoft.PowerShell.Security module includes many built-in cmdlets that you can use to manage the basic security features on a Windows computer. To review the cmdlets included in this module, you can enter the following command:

```powershell
Get-command -module Microsoft.PowerShell.Security
```

To manage access permissions on a file or folder, you use the following cmdlets included in the Microsoft.PowerShell.Security module.

Table 1: Cmdlets included in the Microsoft.PowerShell.Security module

| Cmdlet  | Description |
|--------|-------------|
| Get-Acl | Gets objects that represent the security descriptor of a file or resource. The security descriptor includes the access control lists (ACLs) that define permissions for users and groups. |
| Set-Acl | Changes the security descriptor of a specified item (such as a file, folder, or registry key) to match the values in a supplied security descriptor. |

### Retrieving access permissions
The Get-Acl cmdlet displays the security descriptor for an object. For example, you can retrieve the security descriptor for a folder named C:\Folder1. By default, the output displays in a table format. If you pipe the output to a list format, you can review all the information included in the security descriptor.

```powershell
Get-Acl -Path C:\Folder1|Format-List
```

By using the following command, you can retrieve a more verbose list of the access property with the file system rights, access control type, and inheritance settings for the specified object:

```powershell
(Get-Acl -Path C:\Folder1).Access
```

You can also retrieve only specific Access properties formatted in a table format, as the following example depicts:

```powershell
(Get-Acl -Path C:\Folder1).Access|Format-Table IdentityReference, FileSystemRights, AccessControlType, IsInherited
```

### Updating file and folder access permissions
The Set-Acl cmdlet is used to apply changes to the ACL on a specific object. The process for modifying file or folder permissions consists of the following steps:

1. Use Get-Acl to retrieve the existing ACL rules for the object.
2. Create a new FileSystemAccessRule to be applied to the object.
3. Add the new rule to the existing ACL permission set.
4. Use Set-Acl to apply the new ACL to the existing file or folder.

The following example assigns the Modify permission to C:\Folder1 for a local user named User1.

The first step is to declare a variable that includes the existing ACL rules for Folder1.

```powershell
$ACL = Get-Acl -Path C:\Folder1
```

The second step is to create a new FileSystemAccessRule variable which specifies the access specifications to be applied:
```powershell
$AccessRule = New-Object System.Security.AccessControl.FileSystemAccessRule("User1","Modify","Allow")
```

The third step is to add the new access rule to the existing ACL rules for Folder1:
```powershell
$ACL.SetAccessRule($AccessRule)
```

The third step is to add the new access rule to the existing ACL rules for Folder1:
```powershell
$ACL.SetAccessRule($AccessRule)
```

Finally, you need to apply the new ACL to Folder1:
```powershell
$ACL | Set-Acl -Path C:\Folder1
```

> [!NOTE]
> You can also configure an access rule to remove Folder1 permissions for User1 by simply changing step 3 to $ACL.RemoveAccessRule($AccessRule).

### Copying a security descriptor to a new object
If you want to copy the exact security descriptor to a new object, you can use a combination of the Get-Acl and Set-Acl commands as follows:

```powershell
Get-Acl -Path C:\Folder1|Set-ACL -Path C:\Folder2
```

These commands copy the values from the security descriptor of C:\Folder1 to the security descriptor of Folder2. When the commands complete, the security descriptors for both folders are identical.

---
### Summary

In addition to network service and configuration settings, PowerShell is commonly used to configure and manage settings on a local Windows machine. In this module, you've learned about common PowerShell cmdlets that can be used to perform management tasks with greater efficiency on a Windows 10 computer. The following are the key takeaways:

* The **Microsoft.PowerShell.Management** module includes many built-in cmdlets that can be used to obtain information and perform specific operations on a local computer.
* The **Microsoft.PowerShell.Security** module includes many built-in cmdlets that you can use to manage the basic security features on a Windows computer.

---
## Check your knowledge

---

### 1. You need to use PowerShell to review system and operating system properties of the local computer. Which cmdlet should you use?

* [ ] Get-Contact
* [ ] Get-Content
* [ ] Get-ComputerInfo

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Get-ComputerInfo  
💡 This cmdlet displays detailed system and operating system information for the local computer, including OS version, hardware details, and configuration data.

</details>

---

### 2. You want to check the level of access a user has to `C:\Folder1`. Which cmdlet in the Microsoft.PowerShell.Security module would you use?

* [ ] Set-Acl
* [ ] Get-Credential
* [ ] Get-Acl

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Get-Acl  
💡 This cmdlet retrieves the access control list (ACL) for a file or folder, allowing you to view permissions assigned to users and groups.

</details>

---
