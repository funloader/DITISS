# Introduction

You can use Windows PowerShell more easily and effectively by first understanding its background and intended use. In this module, you'll learn about PowerShell and its various versions. You'll also learn how to open and configure commonly used host applications such as the Windows PowerShell console and Windows PowerShell Integrated Scripting Environment (ISE). Finally, you'll learn to use Microsoft Visual Studio Code (VS Code) to develop PowerShell scripts.

### Learning objectives
After completing this module, you'll be able to:

* Describe Windows PowerShell and its major versions.
* Identify the common Windows PowerShell hosting applications.
* Describe points to consider when using PowerShell.
* Explain how to configure the Windows PowerShell console host.
* Explain how to configure the Windows PowerShell ISE host.
* Describe how to use VS Code for PowerShell scripting.

### Prerequisites
This learning path assumes you have skills and experience with the following technologies and concepts:

* Windows Server administration, maintenance, and troubleshooting
* Windows Client administration, maintenance, and troubleshooting
* Basic security best practices
* Windows networking technologies and implementation
* Core networking technologies such as IP addressing, name resolution, and Dynamic Host Configuration Protocol (DHCP)

---

# Learn about Windows PowerShell

PowerShell is an automation solution that consists of a command-line shell, a scripting language, and a configuration-management framework.

### Command-line shell

Windows PowerShell superseded the Windows command-line interface (cmd.exe) and the limited functionality of its batch file scripting language. PowerShell accepts and returns .NET objects and includes:

* A command-line history.
* Tab completion and prediction.
* Support for command and parameter aliases.
* Chaining commands that use the Pipeline feature.
* A robust in-console help system

Initially, Windows PowerShell was a platform built on the .NET Framework and only worked on Windows operating systems. However, with its recent releases, PowerShell uses the .NET Core and can run on Windows, macOS, and Linux platforms. Due to their multi-platform support, these recent releases are referred to as PowerShell (rather than Windows PowerShell).

### A scripting language

Commands provide PowerShell’s main functionality. There are many varieties of commands, including cmdlets (pronounced command-lets), functions, filters, scripts, applications, configurations, and workflows. Commands are building blocks that you piece together by using the Windows PowerShell scripting language. Using commands enables you to create custom solutions to complex administrative problems. Alternatively, you can run commands directly within the PowerShell console to complete a single task. The console is the CLI for PowerShell and is the primary way in which you'll interact with PowerShell.

Cmdlets use a Verb-Noun naming convention. For example, you can use the Get-Command cmdlet to list all cmdlets and functions that are registered in the command shell. The verb identifies the action for the cmdlet to perform, and the noun identifies the resource on which the cmdlet will perform its action.

Microsoft server applications and cloud services provide specialized cmdlets that you can use to manage those services. In fact, you can manage some features only by using PowerShell. In many cases, even when the application provides a graphical user interface (GUI) to manage a specific functionality, it relies on PowerShell to implement at least some of its features behind the scenes.

### Configuration management framework

PowerShell incorporates the PowerShell Desired State Configuration (DSC) management framework. This framework enables you to manage enterprise infrastructure with code to help with:

* Using declarative configurations and repeatable scripts for repeatable deployments.
* Enforcing configurations settings and identifying when configuration drift takes place from standard requirements.
* Deploying configuration settings using push or pull models.

Applications and services with PowerShell–based administrative functions are consistent in how they work. This attribute means that you can quickly apply the lessons you learned. Also, when you use automation scripts to administer a software application, you can reuse them among other applications.

### Windows PowerShell versions
As you learn about PowerShell, it's important to understand the various versions that you might encounter, depending upon your operating system (OS) type and edition. There are two main PowerShell platforms:

* Windows PowerShell
* PowerShell (originally referred to as PowerShell Core)

### Windows PowerShell
Windows PowerShell is available exclusively for the Windows OS. Windows PowerShell 1.0 was introduced in 2006 as a component installable on Windows XP Service Pack 2 (SP2), Windows Server 2003 SP1, and Windows Vista. It was also an optional component of Windows Server 2008. In 2009, PowerShell 2.0 was integrated into Windows 7 and Windows Server 2008 R2. All versions of Windows PowerShell up to and including 5.1, which is the version available with Windows 10, are integrated with a Windows OS.

Windows PowerShell is an OS component, so it receives the same lifecycle support and licensing agreements as its parent OS.

### PowerShell
PowerShell is shipped, installed, and configured separately from Windows PowerShell. First released as PowerShell Core 6.0 in 2018, it was the first version that offered multi-platform support, extending its availability to macOS and Linux operating systems.

> [!NOTE]
> The latest version of PowerShell is PowerShell 7.5, available via Microsoft Update.

PowerShell and Windows PowerShell are separately installed and you can run supported commands using either environment.

Standard Windows licensing agreements don't include PowerShell. Rather, it's supported under Microsoft paid support, Microsoft Enterprise Agreements, and Microsoft Software Assurance. Community support is also available.

### Version release history
The following table provides a general timeline of the major PowerShell releases:

**Table 1: PowerShell release timelines**

| Version    | Release Date   | Notes |
|-----------:|---------------|-------|
| PowerShell 7.5 | January 2025 | Built on .NET 9.0. |
| PowerShell 7.4 | November 2023 | Built on .NET 8.0. |
| PowerShell 7.3 | November 2022 | Built on .NET 7.0. |
| PowerShell 7.2 | November 2021 | Built on .NET 6.0. |
| PowerShell 7.1 | November 2020 | Built on .NET 5.0. |
| PowerShell 7.0 | March 2020 | Built on .NET Core 3.1. |
| PowerShell 6.0 | September 2018 | Built on .NET Core 2.0. First release installable on Windows, Linux, and macOS. |
| PowerShell 5.1 | August 2016 | Released in Windows 10 Anniversary Update and Windows Server 2016; part of Windows Management Framework (WMF) 5.1. |
| PowerShell 5.0 | February 2016 | Integrated in Windows 10 version 1511; released in WMF 5.0. Installable on Windows Server 2008 R2, Server 2012, Windows 10, Windows 8.1 Enterprise/Pro, and Windows 7 SP1. |
| PowerShell 4.0 | October 2013 | Integrated in Windows 8.1 and Windows Server 2012 R2; installable on Windows 7 SP1, Server 2008 SP1, and Server 2012. |
| PowerShell 3.0 | October 2012 | Integrated in Windows 8 and Windows Server 2012; installable on Windows 7 SP1, Server 2008 SP1, and Server 2008 R2 SP1. |
| PowerShell 2.0 | July 2009 | Integrated in Windows 7 and Windows Server 2008 R2; installable on Windows XP SP3, Server 2003 SP2, and Windows Vista SP1. |
| PowerShell 1.0 | November 2006 | Installable on Windows XP SP2, Windows Server 2003 SP1, and Windows Vista; optional component of Windows Server 2008. |


> [!NOTE]
> Throughout this module, topics will relate to both the latest Windows PowerShell and PowerShell versions (5.1 and 7.5). Most cmdlets will work using either platform. However, there'll be a note if a specific feature is only supported or relates to one specific platform.

---
# Get familiar with Windows PowerShell applications

To interact with PowerShell, you use an application that embeds, or hosts, the PowerShell's engine. Some of those applications will offer a graphical user interface (GUI), such as Windows Admin Center or Exchange Admin Center in Microsoft Exchange Server. Both of them utilize PowerShell to carry out administrative tasks.

In this learning path, you'll primarily interact with Windows PowerShell through one of the two primary hosts that Microsoft provides:
* The Windows PowerShell console
* The Windows PowerShell Integrated Scripting Environment (ISE)

### Windows PowerShell console
The console uses the Windows built-in console host application. This is similar to the command-line experience that the traditional Windows Command Prompt shell (cmd.exe) offers. However, all currently supported versions of Windows provide an updated console with more functionality, including syntax coloring. The console provides the broadest Windows PowerShell functionality, with a number of significant improvements introduced in Windows PowerShell 5.1.

### Windows PowerShell ISE
The ISE is a Windows Presentation Foundation (WPF) application that provides rich editing capabilities, including IntelliSense code hinting and completion. In this course, you'll begin by using the console. This is an effective way to reinforce important foundational skills. Toward the end of the course, you'll shift to using the ISE as you begin to link multiple commands together into scripts.

Third parties offer other Windows PowerShell host applications. Several companies produce free and commercial Windows PowerShell scripting, editing, and console hosts. However, this module focuses on the host applications that the Windows OS provides.

> [!NOTE]
> Windows PowerShell ISE only supports Windows PowerShell versions up to and including 5.1. It doesn't support subsequent versions of PowerShell (6.x or 7.x). You can use Microsoft Visual Studio Code with the PowerShell extension if you are looking for a similar scripting environment as the one that Windows PowerShell ISE provides.

---

# Identify factors to install and use Windows PowerShell

As you use PowerShell to manage and automate management tasks, you take into account several considerations, including:

* Installing and using PowerShell side-by-side with Windows PowerShell.
* Running PowerShell using administrative credentials.
* Identifying and modifying the execution policy in PowerShell.

Installing and using PowerShell side-by-side with Windows PowerShell
Depending on Windows operating system versions and editions, organizations might have computers running different versions of PowerShell. Sometimes, these mixed-version environments are the result of organizational policies that don't permit the installation of newer PowerShell versions. They might also be the result of software products, especially server software, being compatible with a specific PowerShell version.

If you install the latest version of PowerShell, you end up with multiple PowerShell versions installed on your system. For example, PowerShell 7 is designed to coexist with Windows PowerShell 5.1 and will install to a new directory and enable side-by-side execution with Windows PowerShell.

Installing the latest version of PowerShell results in the following when compared to Windows PowerShell:

* *Separate installation path and executable name*. Windows PowerShell 5.1 is installed in the `$env:WINDIR\System32\WindowsPowerShell\v1.0` location. PowerShell 7 is installed in the `$env:ProgramFiles\PowerShell\7` location. The new location is added to your PATH, which allows you to run both Windows PowerShell 5.1 and PowerShell 7. In Windows PowerShell, the PowerShell executable is named `powershell.exe`. In version 6 and newer, the executable is named `pwsh.exe`. The new name makes it easy to support side-by-side execution of both versions.
* *Separate PSModulePath*. By default, Windows PowerShell and PowerShell 7 store modules in different locations. PowerShell 7 combines those locations in the `$Env:PSModulePath` environment variable. When you import a module by name, PowerShell checks the location that `$Env:PSModulePath` specifies. This feature allows PowerShell 7 to load both Core and Desktop modules.
* *Separate profiles for each version*. A PowerShell profile is a script that runs when PowerShell starts. This script customizes the PowerShell environment by adding commands, aliases, functions, variables, modules, and PowerShell drives. In Windows PowerShell 5.1, the profile's location is `$HOME\Documents\WindowsPowerShell`. In PowerShell 7, the profile's location is `$HOME\Documents\PowerShell`.
* *Separate event logs*. Windows PowerShell and PowerShell 7 log events to separate Windows event logs.

When you're reviewing a PowerShell session, it's important to determine which version you're using. To determine the current version, enter `$PSVersionTable` in the PowerShell console, and then select Enter. PowerShell displays the version numbers for various components, including the main PowerShell version number.

### Running PowerShell using Administrative credentials

On 64-bit operating systems, the PowerShell host applications are available in both 64-bit (x64) and 32-bit (x86) versions. When working with Windows PowerShell, you'll use the 64-bit version that displays as Windows PowerShell or Windows PowerShell ISE in the Start menu. The 32-bit versions provide compatibility with locally installed 32-bit shell extensions. They display as Windows PowerShell (x86) or Windows PowerShell ISE (x86) in the Start menu. As soon as you open Windows PowerShell, the application window's title bars reflect the same names as in the Start menu. Be certain that you're opening the appropriate version for the task you want to perform.

On 32-bit operating systems, PowerShell’s host applications are available only in 32-bit versions. When working with Windows PowerShell, you'll notice that the icons and window title bars don't have the (x86) designation. Instead, they display simply as Windows PowerShell and Windows PowerShell ISE in the Start menu.

If you intend to use PowerShell to perform administrative tasks on computers that have User Account Control (UAC) enabled, you might have to take an extra step to run PowerShell cmdlets with full administrative credentials. To do this, right-click or activate the context menu for the application icon, and then select Run as Administrator. When you're running PowerShell with administrative credentials, the host application’s window title bar will include the Administrator prefix.

### Identifying and modifying the execution policy in PowerShell
The execution policy in PowerShell is meant to minimize the possibility of a user unintentionally running PowerShell scripts. You can think of it as a safety feature that controls the conditions under which PowerShell loads configuration files and runs scripts. This feature helps prevent the execution of malicious scripts.

> [!IMPORTANT]
> The execution policy in PowerShell isn't a security system that restricts user actions. For example, if users can't run a script, they can easily bypass a policy by entering the script contents at the command line.

To identify the effective execution policy for the current PowerShell session, use the following cmdlet:

```
Get-ExecutionPolicy

```

You can configure the following policy settings:

* **AllSigned**. Limits script execution on all signed scripts. This setting requires that all scripts are signed by a trusted publisher, including scripts that you write on the local computer. It prompts you before running scripts from publishers that you haven't yet classified as trusted or untrusted. However, verifying the signature of a script doesn't eliminate the possibility of that script being malicious. It simply provides an extra check that minimizes this possibility.
* **Default**. Sets the default execution policy, which is Restricted for Windows clients and RemoteSigned for Windows servers.
* **RemoteSigned**. This is the default execution policy for Windows server computers. Scripts can run, but the policy requires a digital signature from a trusted publisher on scripts and configuration files that have been downloaded from the internet. This setting doesn't require digital signatures on scripts that are written on the local computer.
* **Restricted**. This is the default execution policy for Windows client computers. It permits running individual commands, but it doesn't allow scripts.
* **Unrestricted**. This is the default execution policy for non-Windows computers, which you can't change. It allows unsigned scripts to run. This policy warns the user before running scripts and configuration files that aren't from the local intranet zone.
* **Undefined**. Indicates that there isn't an execution policy set in the current scope. If the execution policy in all scopes is Undefined, the effective execution policy is Restricted for Windows clients and RemoteSigned for Windows Server.

To change the execution policy in PowerShell, use the following command:

```
Set-ExecutionPolicy -ExecutionPolicy <PolicyName>

```

---

# Configure the Windows PowerShell console

When you work in the console regularly, you might want to customize its settings by specifying custom preferences. For example, font size and type, the size and position of the console window and the screen buffer, the color scheme, and keyboard shortcuts.

### Font type, color, and size
If the font size and color make it difficult for you to review content, you can change them. You might also find that the font style and size that are set in the console make it difficult to differentiate between important characters, which can make it challenging to troubleshoot long, complex lines of code. To check if this issue exists, when you first open the console, enter the following characters, and make sure that you can easily differentiate between them:

* Grave accent (`).
* Single quotation mark (').
* Open parentheses (().
* Open curly bracket ({).
* Open square bracket ([).
* Open angle bracket or less than symbol (<).

If you find it difficult to differentiate between these characters, try changing the font. To change the font, select the PowerShell icon in the console window. From the shortcut menu, select Properties, and then select the Font tab. Select a new font style and size. TrueType fonts, which the double-T symbol indicates, are considered easier to review than Raster fonts. The PowerShell Properties dialog box provides a preview pane in which you can review the results of your choice.

### Screen buffer and console window sizes
You can customize the console window's size and location. When setting the window size, you should understand the relationship between the Screen Buffer Size and Windows Size options, so that you don't accidentally miss any section of the output that appears on the console window. Screen Buffer Size is the width in number of characters, and the height in number of lines that appear in your text buffer. The Windows Size option, as the name suggests, is the width of the actual window. In most cases, you'll want to make sure that the Width option for Screen Buffer Size is equal to or smaller than the Width option for Windows Size. Doing so will prevent you from having a horizontal scroll bar on your console window. You can update these options in the Layout tab.

Set the width of both the screen buffer and console windows to be close to your actual screen's width. Doing so lets you maximize the amount of horizontal text you can display. This setting will prove useful later when you format the on-screen output that your scripts return.

The height of your screen buffer doesn't have to match your screen height. In most cases, it's much larger. If you set this value to a large number, you'll be able to scroll through large numbers of commands that are entered in a session or large amounts of output.

In the Layout tab, you can also set a specific position where the console window appears on screen. To do this, set the values for the Window Position in which the top‑left corner of the window should appear.

### Color scheme
Finally, if you want to change the default color scheme, you can select from a small range of alternative colors in the Colors tab of the console’s Properties dialog box. You can change only the primary text and the background color for the main window and any secondary pop-up windows. You can't change the color of error messages or other output from this dialog box.

After updating settings, close the dialog box. Verify that the window fits on the screen and that there isn't a horizontal scroll bar. A vertical scroll bar will still display in the console.

# Copying and pasting
The console host supports copying and pasting to and from the clipboard. It also supports using standard keyboard shortcuts, though they might not always work. This could be because of other applications that are running on the local computer and have changed settings for keyboard shortcuts. To enable this functionality, make sure that QuickEdit Mode is enabled in the console’s Properties dialog box. In the Edit Options section of the Options tab, enable keyboard shortcuts for copy and paste by selecting Enable Ctrl key shortcuts.

Within the console, select a block of text, and then select Enter to copy that text to the clipboard. Right-click or activate the context menu to paste. Starting with Windows 10 and Windows Server 2016, the Ctrl+C and Ctrl+V keyboard shortcuts also work for copy and paste.

---
# Configure the Windows PowerShell Integrated Scripting Environment (ISE)

The ISE is a graphical environment that provides a script editor, a debugger, an interactive console, and several auxiliary tools that help you discover and learn Windows PowerShell commands. This module provides a basic overview on how the ISE works. You will learn about more advanced ISE’s capabilities in the subsequent modules.

Configure the Windows PowerShell Integrated Scripting Environment (ISE)
Completed
100 XP
6 minutes
The ISE is a graphical environment that provides a script editor, a debugger, an interactive console, and several auxiliary tools that help you discover and learn Windows PowerShell commands. This module provides a basic overview on how the ISE works. You will learn about more advanced ISE’s capabilities in the subsequent modules.

### Panes
The ISE offers two main panes: a Script pane (or script editor) and the Console pane. You can position these vertically, with one above the other or horizontally, side-by-side in a two-pane view. You can also maximize one pane and switch back and forth between them. By default, a Command Add-on pane also displays. It enables you to search for or browse available commands, as well as review and fill in parameters for a command that you select. There's also a floating Command window that provides the same functionality.

### Customizing the view
The ISE provides several ways to customize the view. You can change the active font size by using the slider in the window's lower-right area. The Options dialog box lets you customize font and color selection for many different Windows PowerShell text elements, such as keywords and string values. The ISE also supports creation of visual themes. A theme is a collection of font and color settings that you can apply as a group to customize the ISE's appearance. There are several built-in themes intended for designated use cases, such as giving presentations. The ISE also gives you the option to create custom themes.

Other ISE features include:

* A built-in, extensible snippets library that you can use to store commonly used commands.
* The ability to load add-ins created by Microsoft or by third parties that provide additional functionality.
* Integration with Windows PowerShell’s debugging capabilities.

> [!NOTE]
> The PowerShell ISE is no longer in active feature development. As a shipping component of Windows, it continues to be officially supported for security and high-priority servicing fixes. We currently have no plans to remove the ISE from Windows. Windows PowerShell ISE won't work with PowerShell 6 and newer. For a similar experience, you can use Visual Studio Code (VS Code) with the PowerShell extension. You will learn more about it in the next unit of this module.

---

### Use Visual Studio Code with PowerShell

Visual Studio Code (VS Code) is a Microsoft script editor that provides a rich and interactive script editing experience. This experience is similar to the PowerShell Integrated Scripting Environment (ISE) when you use it with the PowerShell extension. VS Code supports the following PowerShell versions:

* PowerShell 7 and newer for Windows, macOS, and Linux
* PowerShell Core 6 for Windows, macOS, and Linux
* Windows PowerShell 5.1 for Windows operating systems only

### ISE Mode in Visual Studio Code
After you install VS Code and the PowerShell extension, you can replicate the ISE experience by turning on ISE Mode.

Enabling ISE Mode makes several notable changes to the way VS Code works, including:

* Mapping keyboard functions in VS Code so they match the ones used in the ISE.
* Allowing you to replicate the VS Code user interface to resemble the ISE.
* Enabling ISE-like tab completion.
* Providing several ISE themes to make the VS Code editor look like the ISE.

---
### Summary

In this module, you were introduced to Windows PowerShell and its functionalities. The following are the key takeaways:

* PowerShell is an automation solution that consists of a command-line shell, a scripting language, and a configuration-management framework.
* There are two main PowerShell platforms, Windows PowerShell and PowerShell (originally referred to as PowerShell Core), based on the operating system and edition.
* Users primarily interact with Windows PowerShell through an application that embeds, or hosts, the PowerShell's engine. Two primary hosts that Microsoft provides are the Windows PowerShell console and the Windows PowerShell Integrated Scripting Environment (ISE).
* The Windows PowerShell console host can be customized by specifying custom preferences like font size and type, the size, and position of the console window and the screen buffer, the color scheme, and keyboard shortcuts.
* The Windows PowerShell ISE allows for customizing of panes and views. It's a graphical environment that provides a script editor, a debugger, an interactive console, and several auxiliary tools.
* Visual Studio Code (VS Code) is a Microsoft script editor that provides a rich and interactive script editing experience.

---
## Check your knowledge

---

### 1. You want to start PowerShell 7 from the command line. Which command will you run?

* [ ] powershell.exe
* [ ] pwsh.exe
* [ ] powersh.exe

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** pwsh.exe  
💡 PowerShell 7 uses **pwsh.exe** as its executable, while **powershell.exe** starts Windows PowerShell 5.1.

</details>

---

### 2. Why might you decide to use the ISE versus the console host?

* [ ] Supports richer editing capabilities and can display a wider range of fonts
* [ ] Essential for running even a few commands
* [ ] Both of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Supports richer editing capabilities and can display a wider range of fonts  
💡 PowerShell ISE provides enhanced editing features such as syntax highlighting, script panes, and better font support, but it is **not required** to run basic commands.

</details>

---
