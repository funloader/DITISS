# Introduction

In this module, you'll learn about the cmdlet structure and parameters for using Windows PowerShell cmdlets. You'll also learn how to use tab completion and how to display About files content.

### Learning objectives
After completing this module, you'll be able to:

* Describe cmdlet structure.
* Identify how to use Windows PowerShell parameters.
* Explain how to use tab completion.
* Explain how to display the About files content.

### Prerequisites
Familiarity with:

* Windows Server administration, maintenance, and troubleshooting
* Windows Client administration, maintenance, and troubleshooting
* Basic security best practices
* Windows networking technologies and implementation
* Core networking technologies such as IP addressing, name resolution, and Dynamic Host Configuration Protocol (DHCP)

### Discover the structure of PowerShell cmdlets

There are thousands of Windows PowerShell cmdlets built into the Windows operating systems and other Microsoft products. Memorizing the names and the syntax for all these commands isn't possible. Fortunately, cmdlet creators build cmdlets by using a common format that helps you predict both a cmdlet's name and its syntax. This common format makes it much easier to discover and use cmdlets.

> [!NOTE]
> The common format that PowerShell cmdlets use is the Verb-Noun notation.

Cmdlet verbs
The verb portion of a cmdlet name indicates what the cmdlet does. There's a set of approved verbs that cmdlet creators use, which provides consistency in cmdlet names. Common verbs include:

* Get. Retrieves a resource, such as a file or a user.
* Set. Changes the data associated with a resource, such as a file or user property.
* New. Creates a resource, such as a file or user.
* Add. Adds a resource to a container of multiple resources.
* Remove. Deletes a resource from a container of multiple resources.

> [!NOTE]
>  You can run the Get-Verb command to have the full list of approved verbs.

This list represents just some of the verbs that cmdlets use. Additionally, some verbs perform similar functions. For example, the Add verb can create a resource, similar to the New verb. Some verbs might seem similar, but have different functions. For example, the Read verb retrieves information that a resource contains, such as a text file's content, whereas the Get verb retrieves the actual file.

### Cmdlet nouns

The noun portion of a cmdlet name indicates what kinds of resources or objects the cmdlet affects. All cmdlets that operate on the same resource should use the same noun. For example, the Service noun is for cmdlets that work with Windows services and the Process noun is for managing processes on a computer.

Nouns can also have prefixes that help the grouping of related nouns into families. For example, the Active Directory nouns start with the letters AD (such as ADUser, ADGroup, and ADComputer). Microsoft SharePoint Server cmdlets begin with the prefix SP, and Microsoft Azure cmdlets begin with the prefix Az.

> [!NOTE]
> Windows PowerShell uses the generic term command to refer to cmdlets, functions, workflows, applications, and other items. These items differ in terms of creation method. However, for now, you should consider them as all working in the same way. This module uses the terms command and cmdlet interchangeably.

---

# Discover the parameters for using PowerShell cmdlets

Parameters modify the actions that a cmdlet performs. You can specify no parameters, one parameter, or many parameters for a cmdlet.

### Parameter format
Parameter names begin with a dash (-). A space separates the value that you want to pass from the parameter name. If the value that you're passing contains spaces, you need to wrap the text in quotation marks. Some parameters accept multiple values, which you must separate by commas and no spaces.

### Optional vs. required parameters
---

#### 1. Required parameters

Some cmdlets *must* be given certain parameters to work.

* `Get-Item` **requires** the `-Path` parameter.
* If you run:

```powershell
Get-Item
```

PowerShell doesn’t fail immediately. Instead, it **prompts you** to supply the missing required parameter:

```text
Supply values for the following parameters:
Path[0]:
```

### Why do you press Enter twice?

* The `-Path` parameter can accept **multiple values** (an array).
* PowerShell keeps asking for another value.
* When you press **Enter without typing anything**, you’re telling PowerShell:

  > “I’m done entering values.”

Example interaction:

```text
Path[0]: C:\
Path[1]:    ← press Enter with no value
```

Then the command runs.

---

#### 2. Optional parameters

Optional parameters are not required for the command to run.
If you don’t supply them, PowerShell uses a default behavior.

Example:

```powershell
Get-ChildItem
```

This works because `-Path` is optional and defaults to the current directory.

---

#### 3. Positional parameters (why you can skip the parameter name)

Some parameters have a **position number** assigned.

For example:

```powershell
Get-ChildItem -Path C:\
```

Because `-Path` is defined as **position 0** (the first parameter), you can omit the name:

```powershell
Get-ChildItem C:\
```

PowerShell interprets this as:

```powershell
Get-ChildItem -Path C:\
```

This is called a **positional parameter**.

---

#### 4. Important rules about positional parameters

✔ You can omit the parameter name **only if**:

* The parameter has a defined position
* You supply the values in the correct order

❌ You cannot omit the parameter name if:

* The parameter has no position
* The command has multiple parameters and the order would be ambiguous

Example where you **must** use parameter names:

```powershell
Get-ChildItem -Recurse -Filter *.txt
```

---

### Switches
Switches are a special case. They're basically parameters that accept a Boolean value (true or false). They differ from actual Boolean parameters in that the value is only set to true if the switch is included when running the command. An example is the -Recurse parameter or switch of the Get-ChildItem cmdlet. The command Get-ChildItem c:\ -Recurse returns not just the items in the C:\ directory, but also those in all of its subdirectories. Without the -Recurse switch, only the items in the C:\ directory are returned.

---

### What is a switch parameter?

A **switch** is a parameter that:

* Has **no value** after it
* Is **false by default**
* Becomes **true only when you include it**

Example switch:

```powershell
-Recurse
```

---

### How a switch works

 Without the switch

```powershell
Get-ChildItem C:\
```

Result:

* Lists **only** files and folders directly inside `C:\`
* Does **not** look inside subfolders

Here, `-Recurse = false`

---

 With the switch

```powershell
Get-ChildItem C:\ -Recurse
```

Result:

* Lists files and folders in `C:\`
* **Also lists everything in all subfolders**

Here, `-Recurse = true`

---
# Review the tab completion feature in PowerShell

Tab completion is a PowerShell feature that improves the speed and ease of finding and entering cmdlets and parameters. To use it, enter a few characters of a cmdlet or a parameter in the ISE or console, and then press the Tab key. PowerShell will automatically provide the missing part of the name for you based on the match on the characters you entered. If there are multiple matches, just press the Tab key multiple times until you are presented with the one you intended to use. This works for cmdlets and parameters, variable names, object properties, and file paths.

### Improving speed and accuracy
Tab completion enables you to enter commands much faster and makes your code less prone to errors. Some cmdlet names can be lengthy and complicated. For example, you might accidentally miss or reverse letters when entering the name such as Get-DnsServerResponseRateLimitingExceptionList.

### Discovering cmdlet and parameter names
Tab completion also helps you discover cmdlet and parameter names. For example, if you know that you want a Get cmdlet that works on an Active Directory resource, you can enter the text Get-AD in the console and press the Tab key to review the available options. For parameters, just enter a dash (-) and you can press the Tab key multiple times to review all parameters for a cmdlet.

Tab completion even works with wildcards. If you know you want a cmdlet that operates on services, but aren't sure which one you want, enter the text *-service in the console, and then press the Tab key to review all cmdlets that contain the text -service in their names.

---
# Display the About files content in PowerShell

Although much of the help content in Windows PowerShell relates to commands, there are also many help files that describe PowerShell concepts. These files include information about the PowerShell scripting language, operators, and other details. This information doesn't specifically relate to a single command, but to global shell techniques and features.

You can review a complete list of these topics by running:
```powershell
Get-Help about*
```

To view a specific topic, use:
```powershell
Get-Help about_common_parameters
```
You can also open the help topic in a separate window or online:
```powershell
Get-Help about_common_parameters -ShowWindow
Get-Help about_common_parameters -Online
```
When you use wildcard characters with the Get-Help command, About help files will appear in a list when their titles contain a match for your wildcard pattern. Typically, About help files will appear last, after any commands whose names also matched your wildcard pattern. You can also use the ‑Category parameter to specify a search for About files.

---
# Define modules in PowerShell

Modules are groups of related PowerShell capabilities that are bundled together into a single unit. For the purposes of this class, you can think of them as containers hosting multiple cmdlets. Modules help with organizing cmdlets into distributable units. Microsoft and other software companies provide modules as part of the management tools for their applications and services.

You can check the list of available modules by running the following command:
```powershell
Get-Module -ListAvailable
```
To use a module's cmdlets, the module must be loaded into the current PowerShell session. This typically takes place automatically but, depending on your configuration, might require that you load modules explicitly by running the Import-Module cmdlet. Some server products, such as Microsoft Exchange Server, provide a shortcut to what appears to be a dedicated management shell. However, this is really a normal PowerShell console session with application-specific modules already loaded.

### Autoloading
In Windows PowerShell version 3.0 and newer, modules load automatically if you run a cmdlet that is part of that module. This works if the module that contains the cmdlet is in a folder under the module load paths. By default, these folders include %systemdir%\WindowsPowerShell\v1.0\Modules and %userprofiles%\Documents\WindowsPowerShell\Modules. The list of folders is stored in the $env:PSModulePath environment variable. When you explicitly import a module by name, PowerShell checks the locations referenced by that environment variable.

For PowerShell 7, the PSModulePath includes the following locations:

* `C:\Users\<user>\Documents\PowerShell\Modules`
* `C:\Program Files\PowerShell\Modules`
* `C:\Program Files\PowerShell\7\Modules`
* `C:\Program Files\WindowsPowerShell\Modules`
* `C:\WINDOWS\System32\WindowsPowerShell\v1.0\Modules`

> [!NOTE]
> When using Windows PowerShell, the path %systemdir%\WindowsPowerShell\v1.0\Modules is commonly referred to by using the combination of the `$PSHome` environment variable (which points to %systemdir%\WindowsPowerShell\v1.0) and the Modules path (that is, by using the `$PSHome\Modules` notation). For PowerShell 7.0, the `$PSHome` environment variable refers to C:\Program Files\PowerShell\7.
---
# If you have experience using the traditional Windows Command Prompt shell (cmd.exe), you're likely also familiar with batch commands such as:

* dir for listing files and folders.
* cd for changing directories.
* mkdir for creating new directories.

In many cases, you can continue to use these commands within Windows PowerShell because, behind the scenes, these commands are running native PowerShell cmdlets. The dir command runs Get-ChildItem, the cd command runs Set-Location, and the mkdir command runs New-Item. These commands work with PowerShell because they're aliases of the cmdlets that perform the equivalent action.

Aliases and parameters
It's important to note that aliases typically don't support the parameters that the original commands use. For example, if you run the command dir /o:d in the console, you'll receive an error because Get‑ChildItem doesn't recognize the /o:d parameter. Instead, you can use the dir | sort LastAccessTime to list the contents of the current folder sorted by last accessed date and time in the ascending order.

### Get-Alias
PowerShell includes more than just aliases for legacy batch and Linux commands. It also provides other aliases, such as gci for Get-ChildItem, which you can use to replace a full command with its abbreviated notation and minimize the amount of typing required. You can discover aliases, their definitions, and the commands that they run, by using the Get-Alias cmdlet. Get‑Alias with no parameters returns all aliases defined. You can use the -Name parameter, a positional parameter, which also accepts wildcards, to find the definition for specific aliases. For example, running the command Get-Alias di* returns aliases for both diff and dir.

You can also use the Get-Alias cmdlet to discover new cmdlets. For example, you use the batch command del to delete a file or folder. You can enter the command Get-Alias del to discover that del is an alias for Remove-Item. You can even reverse the discovery process by running the command Get‑Alias -definition Remove-Item to discover that Remove-Item has several other aliases, including rd, erase, and ri.

Parameters can also have aliases. For example, the -s parameter is an alias for -Recurse in the Get‑ChildItem cmdlet. In fact, for parameters, you can use partial parameter names just like aliases, if the portion of the name you do include in the command is enough to uniquely identify that parameter.

### New-Alias
You can also use the New-Alias cmdlet to create a custom alias that you can map to any existing cmdlet. Keep in mind, however, that custom aliases aren't saved between Windows PowerShell sessions. You can use a Windows PowerShell profile to recreate the alias every time you open Windows PowerShell.

### Disadvantages of aliases
Aliases can help you enter commands more quickly, but they tend to make scripts harder to review and understand. One reason is that the verb-noun syntax clearly defines the action taking place. It creates commands that read and sound more like natural language. Aliases for parameters and partial parameter names make scripts even harder to review. In most cases, using tab completion will make command entry almost as fast as entering an alias name and, at the same time, ensure its accuracy.

### Use Show-Command and Get-Help in PowerShell

The Show-Command cmdlet opens a window that displays either a list of commands or a specific command's parameters. This window is the same one that displays when you select the Show Command Window option in the ISE.

To display a specific command's parameters, provide the name of the command as the value for the ‑Name parameter. For example, to open the Show Command Window with the command used to retrieve an Active Directory user, enter the following command in the console, and then press the Enter key:

```powershell
Show-Command –Name Get-ADUser
```
The –Name parameter is positional, so the following command produces the same result:

```powershell
Show-Command Get-ADUser
```

If you select the Show Command Window option in the ISE, and your cursor is within or immediately next to a command name within the console or scripting pane, the results are the same.

> [!NOTE]
> In these examples, Show-Command is the command that you're actually running, but Get-ADUser is the name of the command that you want to review in the dialog box.

Within the Show Command Window, each parameter set for the specified command displays on a separate tab. This makes it visually clear that you can't mix and match parameters between sets.

Once you provide values for all required parameters, you can run the command immediately by selecting Run in the Show commands window. You can also copy it to the Clipboard by selecting Copy. From the Clipboard, you can paste the command into the console, so that you can review the correct command-line syntax without running the command.

Notice that Show-Command also exposes the Windows PowerShell common parameters, which are a set of parameters that Windows PowerShell adds to all commands to provide a predefined set of core capabilities. You'll learn more about many of the common parameters in upcoming modules. However, if you want to find out about them now, run help about_common_parameters in Windows PowerShell and review the results.

### Using Get-Help

Windows PowerShell provides extensive in-product help for commands. You can access this help by using the Get-Help command. Get-Help displays all help content on the screen and lets you scroll through it. You can also use the Help function or the Man alias, which maps to the Get-Help command. All three return basically the same results. These results include a short and long description of the cmdlet, the syntax, any additional remarks from the help author, and links to related cmdlets or additional information online. The help and Man commands display content in the console one page at a time. The ISE displays the entire help content.

For example, to display the help information for the Get-ChildItem cmdlet, enter the following command in the console, and then press the Enter key:

```powershell
Get-Help Get-ChildItem
```

### Get-Help parameters
The Get-Help command accepts parameters that allow you find additional information beyond the information displayed by default. A common reason to seek additional help is to identify usage examples for a command. Windows PowerShell commands commonly include many such examples. For instance, running the command Get-Help Stop-Process –Examples will provide examples of using the Stop-Process cmdlet.

The -Full parameter provides in-depth information about a cmdlet, including:

* A description of each parameter.
* Whether each parameter has a default value (although this information isn't consistently documented across all commands).
* Whether a parameter is mandatory.
* Whether a parameter can accept a value in a specific position (in which case the position number, starting from 1, is given) or whether you must enter the parameter name (in which case named displays).
* Whether a parameter accepts pipeline input and, if so, how.


Other Get-Help parameters include:

* ‑ShowWindow. Displays the help topic in a separate window, which makes it much easier to access help while entering commands.
* ‑Online. Displays the online version of the help topic (typically the most up-to-date information) in a browser window.
* ‑Parameter ParameterName. Displays the description of a named parameter.
* ‑Category. Displays help only for certain categories of commands, such as cmdlets and functions.

### Using Get-Help to find commands
The Get-Help command can be very useful for finding commands. It accepts wildcard characters (*, ?), notably the asterisk (*) wildcard character. When you ask for help and use wildcard characters with a partial command name, Windows PowerShell will display a list of matching help topics.

By using the information you learned earlier about the verb-noun structure of cmdlets, you can use Get-Help as a tool to discover cmdlets even if you don't know their names. For example, if you want all cmdlets that operate on processes, you can enter the command Get-Help *process* in the console, and then press the Enter key. The results match the ones returned by the command Get-Command *process*, except that Get-Help displays a synopsis. This synopsis is a short description that helps you identify the command you want.

Sometimes, you might specify a wildcard search that doesn't match any command name. For example, running Get-Help *beep* won't find any commands that have beep in their name. When no results are found, the help system performs a full-text search of available command descriptions and synopses. This search locates any help files that contain beep. If there's only a single file with a match, the help system displays its content, rather than displaying a one-item list. In the case of the search term beep, Get-Help returns a list of two topics: Set-PSReadlineOption, a cmdlet, and about_Special_Characters, a conceptual help topic.

When you find the command that you need for a task, you can use its help file to learn how to use it. One way to learn is to review the examples and try to understand their usage. However, it's uncommon for examples to cover all possible variations of that's command's usage. Learning to interpret the help-file syntax can help you to identify all capabilities of a given command.

### Get-EventLog help
Use the help for Get-EventLog as an example. If you enter the command Get-Help Get-EventLog in the console and press the Enter key, the help returns the following syntax:
```powershell
Get-EventLog [-LogName] <String> [[-InstanceId] <Int64[]>] [-After <DateTime>] [-AsBaseObject] [-Before <DateTime>] [-ComputerName <String[]>] [-EntryType {Error | Information | FailureAudit | SuccessAudit | Warning}] [-Index <Int32[]>] [-Message <String>] [-Newest <Int32>] [-Source <String[]>] [-UserName <String[]>] [<CommonParameters>]

Get-EventLog [-AsString] [-ComputerName <String[]>] [-List] [<CommonParameters>]
```
The two blocks of text are parameter sets, each of which represents a way in which you can run the command. Notice that each parameter set has many parameters, and they both have several parameters in common. You can't mix and match parameters between sets. That is, if you decide to use the –List parameter, you can't also use –LogName, because these parameters don't appear together in the same parameter set.

The –LogName parameter name is enclosed in square brackets, meaning it's a positional parameter. You can't run the command without a log name. However, you don't have to enter the –LogName parameter name. You do need to pass the log name string as the first parameter, because that's the position in the help file where the –LogName parameter appears. Therefore, the following two commands provide the same results:

```powershell
Get-EventLog –LogName Application
Get-EventLog Application
```

### Omitting parameter names
Be cautious when omitting parameter names, for a few reasons. You can't omit every parameter. For example, the ‑ComputerName parameter can't have the parameter name omitted. Additionally, you can quickly lose track of where things go. When you provide parameter names, the parameters can appear in any order, as the following command depicts:

```powershell
Get-EventLog –ComputerName LON-DC1 –LogName Application –Newest 10
```

However, when you omit parameter names, you must ensure to enter parameters in the correct order. For example, the following command won't work because the log name value doesn't appear in the correct position:

```powershell
Get-EventLog –ComputerName LON-DC1 Application
```

### Specifying multiple values
Some parameters accept more than one value. In the SYNTAX section, a double-square-bracket notation in the parameter value type designates these parameters. For example:

```powershell
-ComputerName <string[]>
```

The above syntax indicates that the –ComputerName parameter can accept one or more string values. One way to specify multiple values is by using a comma-separated list. You don't have to enclose the values in quotation marks, unless the values themselves contain a comma or white space, such as a space or tab character. For example, use the following command to specify multiple computer names:

```powershell
Get-EventLog –LogName Application –ComputerName LON-CL1,LON-DC1
```

You can find more information about each parameter by reviewing the command’s full help. For example, run Get-Help Get-EventLog –Full to review the full help for Get-EventLog, and notice the additional information that displays. For example, you can confirm that the –LogName parameter is mandatory and appears in the first position.

**Best Practice:** If you're just getting started with Windows PowerShell, try to provide full parameter names instead of passing parameter values by position. Full parameter names make commands easier to review and troubleshoot, and they make it easier to notice mistakes if you're entering the command incorrectly.

### Updating help
Windows PowerShell 3.0 and newer versions don't ship with help files. Instead, help files are available as an online service. Microsoft-authored commands have their help files hosted on Microsoft-owned web servers. Non-Microsoft commands are sometimes available online, as long as the author or vendor builds the module correctly and provides an online location for the help files. By using the online model, authors who write commands, including Microsoft authors, can make corrections and improvements to their help files over time, and then deliver them without having to create an entire product update.

Run Update-Help to scan your computer for all installed modules, retrieve online help locations for each, and try to download their respective help files. You must run this command as a member of the local Administrators group, because Windows PowerShell core command help is stored in the %systemdir% folder. Error messages will be displayed if help isn't downloadable. In such cases, Windows PowerShell will still create a default help display for the commands.

Windows PowerShell defaults to downloading help files in your system’s configured language. If help isn't available in that language, Windows PowerShell defaults to the en-US (US English) language. You can override this behavior by using a parameter of Update-Help to specify the UICulture for which you want to retrieve help.

By default, Update-Help will check for help files once every 24 hours, even if you run the command multiple times in a row. To override this behavior, include the –Force parameter.

The companion to Update-Help is Save-Help. It downloads the help content and saves it to a location that you specify. This feature allows you to copy that content to computers that aren't connected to the internet. Update-Help offers a parameter to specify an alternative source location. This feature makes it possible to update help on computers that aren't connected to the internet.

Prior to Windows PowerShell 4.0, Update-Help and Save-Help download help only for the cmdlets installed on the local computer (where you run the command from). In Windows PowerShell 4.0 and newer, you can use Save-Help for modules installed on remote computers.


---
### Summary

In this module, you've learned about the cmdlet structure and the parameters for using Windows PowerShell cmdlets. You've also learned how to use tab completion and how to display About files content. The following are the key takeaways:

* The common structure cmdlet creators use, is the Verb-Noun format. This helps you predict both a cmdlet's name and its syntax, thus making it much easier to discover and use cmdlets.
* Parameters modify the actions that a cmdlet performs. You can specify no parameters, one parameter, or many parameters for a cmdlet.
* Tab completion is a PowerShell feature that improves the speed and ease of finding and entering cmdlets and parameters.
* In addition to the help content relating to commands, About help files contain documentation about the PowerShell scripting language, operators, and other details. This information doesn't specifically relate to a single command, but to global shell techniques and features.
* Modules are groups of related PowerShell capabilities that are bundled together into a single unit. Modules help with organizing cmdlets into distributable units.
* Finding the cmdlet that you need from the extensive built-in help of Windows PowerShell can be a challenge. Using the –Module parameter and Get Help can make this task easier.
* Batch commands used in the traditional Windows Command Prompt shell (cmd.exe) can also be used within Windows PowerShell. This is because these batch commands are aliases of the cmdlets that perform the equivalent action.
* The Show-Command cmdlet opens a window that displays either a list of commands or a specific command's parameters. To display a specific command's parameters, provide the name of the command as the value for the ‑Name parameter.
* The Get-Help command can help you access the extensive in-product help for commands that Windows PowerShell provides.
* Learning to interpret the help-file syntax can help you to identify all capabilities of a given command.
* Windows PowerShell 3.0 and newer versions don't ship with help files. Instead, help files are available as an online service. Run Update-Help to scan your computer for all installed modules, retrieve online help locations for each, and try to download their respective help files.

---
## Check your knowledge

---

### 1. Which of these options is the common structure that PowerShell cmdlets use?

* [ ] Noun-Verb  
* [ ] Verb-Noun  
* [ ] There's no specific structure that PowerShell cmdlets use  

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Verb-Noun  
💡 PowerShell cmdlets follow a consistent **Verb-Noun** naming convention (for example, `Get-Process`, `Set-Service`) to improve readability and discoverability.

</details>

---

### 2. Which key can you use to complete or suggest parameters for a PowerShell command?

* [ ] Enter key  
* [ ] Tab key  
* [ ] End key  

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Tab key  
💡 The **Tab** key is used for tab completion in PowerShell, allowing you to cycle through available commands, parameters, and values.

</details>

---

### 3. How would you search for a cmdlet that retrieves a computer's properties from Active Directory?

* [ ] Get-ComputerInfo
* [ ] Get-Help Get-AD*
* [ ] Get-Command -ParameterName Auth*

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Get-Help Get-AD*  
💡 This command lists all cmdlets that start with `Get-AD`, which are used to retrieve Active Directory objects and their properties.

</details>

---

### 4. Which of the following are groups of related PowerShell capabilities that are bundled together into a single unit?

* [ ] Parameters
* [ ] Aliases
* [ ] Modules

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Modules  
💡 PowerShell **modules** package related cmdlets, providers, functions, and scripts into a single, reusable unit.

</details>

---

