> [!WARNING]
> Content under process !

# Understand the Windows PowerShell pipeline

## Introduction 

In this module, you'll learn about the Windows PowerShell pipeline and some basic techniques for running multiple commands in it. Running commands individually is both cumbersome and inefficient. Understanding how the pipeline works is fundamental to your success in using Windows PowerShell for administration.

### Learning objectives
After completing this module, you'll be able to:

* Describe the features and functionalities of the pipeline.
* Use the appropriate terminology to describe the pipeline output and pipeline objects.
* Explain how to discover and display object members.
* Describe the cmdlets used to format the pipeline output for display.

### Prerequisites
Familiarity with:

* Windows networking technologies and implementation.
* Windows Server administration, maintenance, and troubleshooting.
* Windows PowerShell and its commands to perform specific tasks.
* PowerShell cmdlets used for system administration tasks related to Active Directory, network configuration, server administration, and Windows 10 device administration.

## Review Windows PowerShell pipeline and its output

PowerShell can run commands in a pipeline, which is a chain of one or more commands in which the output from one command can pass as input to the next command. In Windows PowerShell, each command in the pipeline runs in sequence from left to right. For multiple commands, each command and its parameters are separated from the next command by a character known as a pipe (|). Specific rules dictate how output passes from one command to the next. You'll learn about those rules throughout this module.

As you interact with Windows PowerShell in the console host application, you should think of each command line as a single pipeline. You enter a command or a series of commands and then press the Enter key to run the pipeline. The output of the last command in the pipeline displays on your screen. Another shell prompt follows that output, and you can enter commands into a new pipeline at that shell prompt.

> [!NOTE]
>  You can enter one logical command line over multiple physical lines in the console. For example, enter Get-Service, and then press the Enter key. Windows PowerShell enters an extended prompt mode, which is indicated by the presence of two consecutive greater than signs (>>). This allows you to complete the command line. Select Ctrl+C to exit the command and return to the Windows PowerShell prompt.

Previously, you learned about common actions, or verbs, associated with Windows PowerShell commands. When running multiple commands as part of a single pipeline, you most commonly notice the verbs `Get` and `Set` used in combination. You use the output of a `Get-*` command as the input for a `Set-*` command. You often use these commands in combination with a filtering command, such as `Where` or `Select`. In that case, the output of `Get-*` is filtered by the Where or Select command before being piped to the `Set-*` command.

The `Where` command is an alias for `Where-Object`, and the Select command is an alias for `Select-Object`. Lesson 3, “Filter objects out of the pipeline” explains filtering in more detail.

It helps to understand the concept of PowerShell objects and pipelines by comparing them to real-world items. For example, if we consider a car as an object, we can describe attributes of the car such as engine, car color, car size, type, make and model. In PowerShell, these would be known as properties. Properties of the object could be, in turn, objects themselves. For instance, the engine property is also an object that has attributes, such as pistons, spark plugs, crankshaft, etc.

Objects have actions, corresponding to such activities as opening or closing doors, changing gears, accelerating, and applying brakes. In PowerShell, these actions are called methods.

Pipelines allow us to take the output produced by one command and pass that object into the input of another command. To make this easier to understand we can liken commands to factories, where each factory receives materials and transforms them into something else.

### Pipeline output
PowerShell commands don't generate text as output. Instead, they generate objects. Object is a generic word that describes an in-memory data structure.

You can imagine command output as something that resembles a database table or a spreadsheet. In PowerShell terminology, the table or spreadsheet consists of a collection of objects, or just a *collection* for short. Each row is a single object, and each column is a *property* of that object, that is, information about the object. For example, when you run the Get-Service command, it returns a collection of service objects. Each object has properties with names such as Name, DisplayName, and Status.

With its use of objects, PowerShell differs from other command-line shells in which the commands primarily generate text. In a text-based shell, suppose that you want to obtain a list of all the services that have been started. You might run a command to produce a text list of the services, with a different row for each service. Each row might contain the name of a service and some properties of the service, with each property separated by a comma or other character. To retrieve a particular property value, you would need to send that text output to another command that processes the text to pull out the particular value you need. That command would be created to understand the specific text format created by the first command. If the output of the first command ever changes, and the status information moves, you'll have to edit the second command to get the new position information. Text-based shells require significant text parsing skills. This makes scripting languages such as Perl popular, because they offer strong text parsing and text manipulation features.

In PowerShell, you instruct the cmdlet to produce the collection of service objects and to then display only the Name property. The structure of the objects in memory enables PowerShell to find the information for you. This way, you don't have to worry about the exact form of the command output.

This functionality makes it possible for the Get | Set pattern to work. Because the output of a Get-* command is an object, PowerShell can find the properties needed by a Set-* command for it to work, without you having to specify them explicitly.

## Discover object members in PowerShell

Members are the various components of an object and include:

* Properties, which describe attributes of the object. Examples of properties include a service name, a process ID number, and an event log message.
* Methods, which invoke an action on an object. For example, a process object can be stopped, and an event log can be cleared.
* Events, which trigger when something happens to an object. A file might trigger an event when it is updated, or a process might trigger an event when it has output to produce.

PowerShell primarily deals with properties and methods. For most commands that you run, the default on-screen output doesn't include all of an object’s properties. Some objects have hundreds of properties, and the full list won't fit on the screen. PowerShell includes several configuration files that list the object properties that should display by default. That's why you notice three properties when you run **Get-Service**.

Use the **Get-Member** command to list all the members of an object. This command lists all the properties, even those that don't display on the screen by default. This command also lists methods and events and displays the type name of the object. For example, the objects that **Get-Service** produces have the type name **System.ServiceProcess.ServiceController**. You can use the type name when you search the internet to locate object documentation and examples. However, those examples are frequently in a programming language such as Microsoft Visual Basic or C#.

> [!NOTE]
> Get-Member has an alias: gm.

To use Get-Member, just pipe any command output to it. For example, enter the following command in the console, and then select Enter:

```powershell
Get-Service | Get-Member
```

> [!NOTE]
> The first command runs, produces its output, and then passes that output to **Get‑Member**. Use caution when you run commands that might modify the system configuration, because those commands make changes to the system. You can't use the *-WhatIf* parameter, which indicates to PowerShell to only test and display the results of the command, when you want to pipe to **Get-Member**. The *-WhatIf* parameter prevents the command from producing any output. That means **Get-Member** receives no input, and therefore doesn't display any output.

## Control the formatting of pipeline output

PowerShell provides several ways to control the formatting of pipeline output. The default formatting of the output depends on the objects that exist in the output and the configuration files that define the output. After PowerShell decides on the appropriate format, it passes the output to a set of formatting cmdlets without your input.

The formatting cmdlets are:

* Format-List
* Format-Table
* Format-Wide
* Format-Custom

You can override the default output formatting by specifying any of the preceding cmdlets as part of the pipeline.

> [!NOTE]
> The Format-Custom cmdlet requires creating custom XML configuration files that define the format. It's used infrequently and is beyond the scope of this course.

Each formatting cmdlet accepts the -Property parameter. The -Property parameter accepts a comma‑separated list of property names, and then it filters the list of properties that display and the order in which they display. Keep in mind that when you specify property names for this parameter, the original command must have returned those properties.

For example, the Get-ADUser cmdlet returns only a subset of properties, unless you specify its -Properties parameter. Therefore, if you specify the City property in the -Property parameter for a formatting cmdlet, it will display as if the property isn't set, unless you make sure that the City property is one of the properties returned for the users queried.

Some cmdlets default to passing a different set of properties for each formatting cmdlet. For example, the Get-Service cmdlet displays three properties (Status, Name, and DisplayName) in a table format by default. If you display the output of Get-Service as a list by using the Get-Service | Format-List command, six additional properties will display.

### Format-List
The Format-List cmdlet, as the name suggests, formats the output of a command as a simple list of properties, where each property displays on a new line. If the command passing output to Format-List returns multiple objects, a separate list of properties for each object displays. List formatting is particularly useful when a command returns a large number of properties that would be hard to review in table format.

> [!NOTE]
> The alias for the Format-List cmdlet is fl.

To display a simple list in the console of the default properties for the processes running on the local computer, enter the following command, and then press the Enter key:

```powershell
Get-Process | Format-List
```

### Format-Table
The Format-Table cmdlet formats output as a table, where each row represents an object, and each column represents a property. The table format is useful for displaying properties of many objects at the same time and comparing the properties of those objects.

By default, the table includes the property names as the column headers, which are separated from the data by a row of dashes. The formatting of the table depends on the returned objects. You can modify this formatting by using a variety of parameters, such as:

*-AutoSize*. This parameter adjusts the size and number of columns based on the width of the data. In Windows PowerShell 5.0 and newer, -AutoSize is set to true by default. In older versions of Windows PowerShell, the default values might truncate data in the table.
*-HideTableHeaders*. This parameter removes the table headers from the output.
*-Wrap*. This parameter causes text that's wider than the column width to wrap to the next line.

> [!NOTE]
> The alias for the Format-Table cmdlet is ft.

To display the Name, ObjectClass, and Description properties for all Windows Server Active Directory objects as a table, with the columns set to automatically size and wrap the text, enter the following command in the console, and then press the Enter key:

```powershell
Get-ADObject -filter * -Properties * | ft -Property Name, ObjectClass, Description -AutoSize -Wrap
```
### Format-Wide

The output of the Format-Wide cmdlet is a single property in a single list displayed in multiple columns. This cmdlet functions like the /w parameter of the dir command in cmd.exe. The wide format is useful for displaying large lists of simple data, such as the names of files or processes, in a compact format.

By default, Format-Wide displays its output in two columns. You can modify the number of columns by using the *-Column* parameter. The *-AutoSize* parameter, which works the same way it does for Format‑Table, is also available. You can't use *-AutoSize* and *-Column* together, however. The *-Property* parameter is also available, but in the case of Format-Wide, it can accept only one property name.

> [!NOTE]
> The alias for the Format-Wide cmdlet is fw.

To send the DisplayName property of all the Group Policy Objects (GPOs) in the current domain as output in three columns, enter the following command in the console, and then press the Enter key:

```powershell
Get-GPO -all | fw -Property DisplayName -Column 3
```
---

### Summary
In this module, you've learned about the Windows PowerShell pipeline and some basic techniques for running multiple commands in it. The following are the key takeaways:

* PowerShell can run commands in a pipeline, which is a chain of one or more commands in which the output from one command can pass as input to the next command.
* PowerShell commands generate objects as output. Object is a generic word that describes an in-memory data structure.
* If you imagine command output as a database table or a spreadsheet, in PowerShell terminology, the table or spreadsheet consists of a collection of objects, or just a collection in short. Each row is a single object, and each column is a property of that object, that is, information about the object.
* Members are the various components of an object and include Properties, which describe attributes of the object, Methods, which invoke an action on an object, and Events, which trigger when something happens to an object.
* The default formatting of the output depends on the objects that exist in the output and the configuration files that define the output. You can override the default output formatting by specifying any of the formatting cmdlets as part of the pipeline.

---

# Select, sort, and measure objects using the pipeline

## Introduction

In this module, you'll learn to manipulate objects in the pipeline by using commands that sort, select, and measure objects. Selecting, sorting, and measuring objects is essential to successfully creating automation in Windows PowerShell.

### Learning objectives
After completing this module, you'll be able to:

* Explain how to sort objects by a specified property.
* Explain how to measure objects’ numeric properties.
* Explain how to display a subset of objects in a collection.
* Explain how to display a customized list of objects’ properties.
* Explain how to create calculated properties.

### Prerequisites
Familiarity with:

* Windows networking technologies and implementation.
* Windows Server administration, maintenance, and troubleshooting.
* Windows PowerShell and its commands to perform specific tasks.
* PowerShell cmdlets used for system administration tasks related to Active Directory, network configuration, server administration, and Windows 10 device administration.

## Sort and group objects by property in the pipeline

Some PowerShell commands produce their output in a specific order. For example, the Get-Process and Get-Service commands produce output that's sorted alphabetically by name. Get-EventLog produces output that's sorted by time. In other cases, the output might not seem to be sorted at all. Sometimes, you might want command output sorted differently from the default. The Sort-Object command, which has the alias sort, can do that for you.

### Sort-Object

The Sort-Object command accepts one or more property names to sort by. By default, the command sorts in ascending order. If you want to reverse the sort order, add the -Descending parameter. If you specify more than one property, the command sorts by the first property, then by the second property, and so on. It isn't possible in a single command to sort by one property in ascending order and another in descending order.

The following commands are examples of sorting:

```powershell
Get-Service | Sort-Object –Property Name –Descending
Get-Service | Sort Name –Desc
Get-Service | Sort Status,Name
```
By default, string properties are sorted without regard to case. That is, lowercase and uppercase letters are treated the same. The parameters of Sort-Object allow you to specify a case-sensitive sort, a specific culture’s sorting rules, and other options. As with other commands, you can review the help for Sort-Object for details and examples.

### Grouping objects by property

Sorting objects also allows you to display objects in groups. The Format-List, Format-Table, and Format-Wide formatting cmdlets have a -GroupBy parameter that accepts a property name. By using the -GroupBy parameter, you can group the output by the specified property.

For example, the following command displays the names of services running on the local computer in two two-column lists that are grouped by the Status property:

```powershell
Get-Service | Sort-Object Status,Name | fw -GroupBy Status
```

The -GroupBy parameter works similarly to the Group-Object command. The Group-Object command accepts piped input and gives you more control over the grouping of the objects. Group-Object has the alias group.

---
## Measure objects in the pipeline

The Measure-Object command can accept any kind of object in a collection. By default, the command counts the number of objects in the collection and produces a measurement object that includes the count.

> [!NOTE]
> The Measure-Object command has the alias Measure.

The -Property parameter of Measure-Object allows you to specify a single property, which must contain numeric values. You can then include the -Sum, -Average, -Minimum, and -Maximum parameters to calculate those aggregate values for the specified property.

> [!NOTE]
> PowerShell allows you to truncate a parameter name, or use only a portion of the parameter name, if the truncated name clearly identifies the parameter. You'll frequently notice the –Sum, -Minimum, and –Maximum parameters truncated to -Sum, -Min, and -Max, corresponding to the common English abbreviations for those words. However, you can't shorten ‑Average to -Avg, although beginners frequently try to. You can shorten the ‑Average parameter to -Ave, which is a valid truncation of the name.

The following command counts the number of files in a folder and displays the smallest, largest, and average file sizes:

> [!NOTE]
> Get-ChildItem -File | Measure -Property Length -Sum -Average -Minimum -Max

## Select a set of objects in the pipeline

Sometimes, you might not need to display all the objects that a command produces. For example, you've already learned that the Get-EventLog command has a parameter -Newest that produces a list of only the newest event log entries. Not all commands have the built-in ability to limit their output like that. However, the Select-Object command can limit the output from any command.

> [!NOTE]
> The Select-Object command has the alias Select.

 You can use Select-Object to select a subset of the objects that are passed to it in the pipeline. One of the ways you can select a subset of objects is by position. If you think of a collection of objects as a table or spreadsheet, selecting a subset means selecting only certain rows. Select-Object can select a specific number of rows. You can't use Select-Object to choose those rows by column or property value, only by position. You can instruct it to start from the beginning or the end of the collection. You can also instruct it to skip a certain number of rows before the selection begins. You can use the Sort-Object command to control the row order before passing the objects to Select-Object in the pipeline.

For example, to select the first 10 processes based on the least amount of virtual memory use, enter the following command in the console, and then press the Enter key:

```powershell
Get-Process | Sort-Object –Property VM | Select-Object –First 10
```

To select last 10 running services and sort them by name, enter the following command in the console, and then press the Enter key:
```powershell
Get-Service | Sort-Object –Property Name | Select-Object –Last 10
```

To select the five processes using the least amount of CPU and skip the one process using the least CPU, enter the following command in the console and press the Enter key:
```powershell
Get-Process | Sort-Object –Property CPU –Descending | Select-Object –First 5 –Skip 1
```

### Selecting unique objects
Consider a scenario in which Select-Object evaluates the properties and values when selecting the rows to return. If some members of the object collection passed to Select-Object have duplicate names and values, and you include the -Unique parameter, Select-Object returns only one of the duplicated objects.

For example, if you want to display user information for one user in each department, enter the following command in the console, and then press the Enter key:
```powershell
Get-ADUser -Filter * -Property Department | Sort-Object -Property Department | Select-Object Department -Unique
```
---
## Select object properties in the pipeline

In addition to selecting the first or last number of rows from a collection, you can use Select-Object to specify the properties to display. You use the -Property parameter followed by a comma-separated list of the properties you want to display. If you think of a collection of objects as a table or spreadsheet, you're choosing the columns to display. After you choose the properties you want, Select-Object removes all the other properties (or columns). If you want to sort by a property but not display it, you first use Sort-Object and then use Select-Object to specify the properties you want to display.

The following command displays a table containing the name, process ID, virtual memory size, paged memory size, and CPU usage for all the processes running on the local computer:

```powershell
Get-Process | Select-Object –Property Name,ID,VM,PM,CPU | Format-Table
```

The -Property parameter works with the -First or -Last parameter. The following command returns the name and CPU usage for the 10 processes with the largest amount of CPU usage:
```powershell
Get-Process | Sort-Object –Property CPU –Descending | Select-Object –Property Name,CPU –First 10
```

Take care when specifying property names. Sometimes, the default screen display that PowerShell creates doesn't use the real property names in the table column headers. For example, the output of Get-Process includes a column labeled CPU(s). However, the System.Diagnostics.Process object type doesn't have a property that has that name. The actual property name is CPU. You can check this by piping the output of Get-Process to Get-Member.

> Best Practice: Always review the property names in the output of Get-Member before you use those property names in another command. By doing this, you can help to ensure that you use the actual property names and not ones created for display purposes.

---
## Create and format calculated properties in the pipeline

Select-Object can create custom, or calculated, properties. Each of these properties has a label, or name, that Windows PowerShell displays in the same way it displays any built-in property name. Each calculated property also has an expression that defines the contents of the property. You create each calculated property by entering the values in a hash table.

### What are hash tables?
A hash table is known in some other programming and scripting languages as an associative array or dictionary. One hash table can contain multiple items, and each item consists of a key and a value, or a name-value pair. Windows PowerShell uses hash tables many times and for many purposes. When you create your own hash table, you can specify your own keys.

### Select-Object hash tables
When you use a hash table to create calculated properties by using Select-Object, you must use the following keys that Windows PowerShell expects:

* label, l, name, or n. This specifies the label, or name, of the calculated property. Because the lowercase l resembles the number 1 in some fonts, try to use either name, n, or label.
* expression or e. This specifies the expression that sets the value of the calculated property.
This means that each hash table contains only one name-value pair. However, you can use more than one hash table to create multiple calculated properties.

For example, suppose that you want to display a list of processes that includes the name, ID, virtual memory use, and paged memory use of each process. You want to use the column labels VirtualMemory and PagedMemory for the last two properties, and you want those values displayed in bytes. To do so, enter the following command in the console, and then press the Enter key:

```powershell
Get-Process |
Select-Object Name,ID,@{n='VirtualMemory';e={$PSItem.VM}},@{n='PagedMemory';e={$PSItem.PM}}
```

> [!NOTE]
> You can enter the command exactly as displayed and press the Enter key after the vertical pipe character. When you do so, you enter the extended prompt mode. After you enter the rest of the command, press the Enter key on a blank line to run the command.

The previous command includes two hash tables, and each one creates a calculated property. The hash table might be easier to interpret if you create it a bit differently, as the following code depicts:

```powershell
@{
 n='VirtualMemory';
 e={ $PSItem.VM }
 }
```

The previous example uses a semicolon to separate the two key-value pairs, and it uses the keys n and e. Windows PowerShell expects these keys. The label (or name) is a string, and therefore enclosed in single quotation marks. Windows PowerShell accepts either quotation marks (" ") or single quotation marks (' ') for this purpose. The expression is a small piece of executable code called a script block and is contained within braces ({ }).

> [!NOTE]
> `$PSItem` is a special variable created by Windows PowerShell. It represents whatever object was piped into the Select-Object command. In the previous example, that's a Process object. The period after $PSItem lets you access a single member of the object. In this example, one calculated property uses the VM property, and the other uses the PM property.

> [!NOTE]
> Windows PowerShell 1.0 and Windows PowerShell 2.0 used `$_` instead of `$PSItem`. That older syntax is compatible in Windows PowerShell 3.0 and newer, and many experienced users continue to use it out of habit.

A comma separates each property, such as Name, ID, and each calculated propert from the others in the list.

### Formatting calculated properties
You might want to modify the previous command to display the memory values in megabytes (MB). PowerShell understands the abbreviations KB, MB, GB, TB, and PB as representing kilobytes, megabytes, gigabytes, terabytes, and petabytes, respectively. Therefore, you might modify your command as follows:

```powershell
Get-Process |
Select-Object Name,
              ID,
              @{n='VirtualMemory(MB)';e={$PSItem.VM / 1MB}},
              @{n='PagedMemory(MB)';e={$PSItem.PM / 1MB}}

```
In addition to the revised formatting that makes the command easier to review, this example changes the column labels to include the MB designation. It also changes the expressions to include a division operation, dividing each memory value by 1 MB. However, the resulting values have several decimal places, which is visually suboptimal.

To improve the output, make the following change:

```powershell
Get-Process |
Select-Object Name,
              ID,
              @{n='VirtualMemory(MB)';e={'{0:N2}' –f ($PSItem.VM / 1MB) -as [Double] }},
              @{n='PagedMemory(MB)';e={'{0:N2}' –f ($PSItem.PM / 1MB) -as [Double] }}

```
This example uses the Windows PowerShell -f formatting operator. When used with a string, the -f formatting operator instructs Windows PowerShell to replace one or more placeholders in the string with the specified values that follow the operator.

In this example, the string that precedes the -f operator instructs Windows PowerShell what data to display. The string '{0:N2}' signifies displaying the first data item as a number with two decimal places. The original mathematical expression comes after the operator. It's in parentheses to make sure that it runs as a single unit. You can enter this command exactly as displayed, press the Enter key on a blank line, and then review the results.

The syntax in the previous example might seem confusing because it contains a lot of punctuation symbols. Start with the basic expression:

```powershell
'{0:N2}' –f ($PSItem.VM / 1MB)
```

The previous expression divides the VM property by 1 MB and then formats the result as a number with up to two decimal places. That expression is then placed into the hash table:

```powershell
@{n='VirtualMemory(MB)';e={'{0:N2}' –f ($PSItem.VM / 1MB) }}
```

That hash table creates the custom property named VirtualMemory(MB).

> [!NOTE]
> You can learn more about the -f operator by running Help About_Operators in Windows PowerShell.

---
### Summary

In this module, you've learned to manipulate objects in the pipeline by using commands that sort, select, and measure objects. This is needed for successfully creating automation in Windows PowerShell. The following are the key takeaways:

* The Sort-Object command can help you sort command output differently from the default. It accepts one or more property names to sort by.
* The Measure-Object command, by default, counts the number of objects in the collection and produces a measurement object that includes the count.
* The Select-Object command can limit the output from any command when you don't need to display all the objects that a command produces.
* Select-Object can also display specific properties if you use the -Property parameter followed by a comma-separated list of the properties you want to display.
* Select-Object can create custom, or calculated, properties. Each of these properties has a label, or name, that Windows PowerShell displays in the same way it displays any built-in property name.
---
# Filter objects out of the pipeline






---
## Check your knowledge

---

### 1. What is a pipeline when using PowerShell?

* [ ] A generic word that describes an in-memory data structure
* [ ] A collection of objects
* [ ] A chain of one or more commands in which the output from one command can pass as input to the next command

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A chain of one or more commands in which the output from one command can pass as input to the next command  
💡 PowerShell pipelines allow cmdlets to pass objects directly to one another, enabling powerful and efficient command chaining.

</details>

---

### 2. Which formatting cmdlet would a user pipe into a PowerShell command to display the output where each property displays on a new line?

* [ ] Format-Wide
* [ ] Format-Table
* [ ] Format-List

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Format-List  
💡 The `Format-List` cmdlet displays each object property on its own line, making it ideal for viewing detailed information.

</details>

---

### 3. What is the default behavior of the Sort-Object cmdlet?

* [ ] Case-insensitive sort in the descending order
* [ ] Case-sensitive sort in the descending order
* [ ] Case-insensitive sort in the ascending order

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Case-insensitive sort in the ascending order  
💡 By default, `Sort-Object` sorts data in ascending order and does not distinguish between uppercase and lowercase characters.

</details>

---

### 4. Which of the following cmdlets allows a user to specify which properties of an object passed to it by a pipeline should be displayed in its output?

* [ ] Measure-Object
* [ ] Sort-Object
* [ ] Select-Object

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Select-Object  
💡 The `Select-Object` cmdlet lets you choose specific properties to include in the output, making it useful for filtering and shaping data.

</details>

---
