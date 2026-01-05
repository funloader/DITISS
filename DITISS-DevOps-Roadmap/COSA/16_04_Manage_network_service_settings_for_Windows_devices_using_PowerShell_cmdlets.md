# Introduction

Both Windows PowerShell and PowerShell Core support cmdlets that you can use to manage all aspects related to network settings on Windows devices. Settings that you can configure with PowerShell include TCP/IP, Domain Name System (DNS), firewall, and routing table configurations. In addition to the cmdlets for managing network features and components, the Test-NetConnection cmdlet is also available. This cmdlet offers the same functionality as traditional command-line interface tools such as ping.exe and tracert.exe, which are used to identify and diagnose network connectivity and configuration settings.

In this module, you'll learn about the PowerShell modules and cmdlets used for configuring network settings for Windows devices.

### Learning objectives
After completing this module, you'll be able to:

* Identify cmdlets for managing TCP/IP settings.
* Describe how to manage local routing table settings.
* Describe how to modify DNS client configuration.
* List cmdlets for managing Windows Firewall.

### Prerequisites
Familiarity with:

* Windows networking technologies and implementation.
* Windows Server administration, maintenance, and troubleshooting.
* Windows PowerShell and its commands to perform specific tasks.

---

# Manage IP addresses in PowerShell

PowerShell includes the NETTCPIP module, which consists of TCP/IP-specific cmdlets used to manage network settings for Windows servers and devices. You can use the NETTCPIP cmdlets to add, remove, change, and validate IP address settings.

IP address management cmdlets use the noun "NetIPAddress" in their names. You can also find them by using the Get-Command command with the -Module NetTCPIP parameter.

The following table lists common cmdlets for managing IP address settings.

Table 1: Cmdlets for managing IP address settings

| Cmdlet              | Description |
|---------------------|-------------|
| New-NetIPAddress    | Creates a new IP address |
| Get-NetIPAddress    | Displays properties of an IP address |
| Set-NetIPAddress    | Modifies properties of an IP address |
| Remove-NetIPAddress | Deletes an IP address |

### Creating new IP address settings
The New-NetIPAddress cmdlet requires an IPv4 or IPv6 address and either the alias or index of a network interface. As a best practice, you should also set the default gateway and subnet mask at the same time.

The following table lists common parameters for the New-NetIPAddress cmdlet.

Table 2: Parameters for New-NetIPAddress

| Parameter | Description |
|-----------|-------------|
| `-IPAddress` | Defines the IPv4 or IPv6 address to create |
| `-InterfaceIndex` | Defines the network interface, by index, for the IP address |
| `-InterfaceAlias` | Defines the network interface, by name, for the IP address |
| `-DefaultGateway` | Defines the IPv4 or IPv6 address of the default gateway host |
| `-PrefixLength` | Defines the subnet mask for the IP address |

The following command creates a new IP address on the Ethernet interface:

```powershell
New-NetIPAddress -IPAddress 192.168.1.10 -InterfaceAlias "Ethernet" -PrefixLength 24 -DefaultGateway 192.168.1.1
```

The New-NetIPAddress cmdlet also accepts the –AddressFamily parameter, which defines either the IPv4 or IPv6 IP address family. If you don't use this parameter, the address family property is detected automatically.

---

# Manage IP routing in PowerShell

IP routing forwards data packets based on the destination IP address. This routing is based on routing tables, and while entries are made automatically, you might need to add, remove, or modify routing table entries manually. The NETTCPIP PowerShell module also includes cmdlets used to manage the routing table for Windows servers and devices.

The cmdlets for managing routing table entries have the noun “NetRoute” in the names.

The following table lists common cmdlets for managing routing table entries and settings.

Table 1: Cmdlets for managing routing table entries and settings
| Cmdlet         | Description |
|---------------:|-------------|
| New-NetRoute   | Creates an entry in the IP routing table |
| Get-NetRoute   | Retrieves an entry from the IP routing table |
| Set-NetRoute   | Modifies properties of an entry in the IP routing table |
| Remove-NetRoute| Deletes an entry from the IP routing table |
| Find-NetRoute  | Identifies the best local IP address and route to reach a remote address |

### Creating an IP routing table entry
You can use the New-NetRoute cmdlet to create routing table entries on a Windows computer. The New-NetRoute cmdlet requires you to identify the network interface and destination prefix.

The following table lists common parameters for the New-NetRoute cmdlet.

Table 2: Parameters for New-NetRoute
| Parameter         | Description                                |
|------------------|--------------------------------------------|
| -DestinationPrefix | Defines the destination prefix of an IP route |
| -InterfaceAlias    | Defines the network interface, by alias, for an IP route |
| -InterfaceIndex    | Defines the network interface, by index, for an IP route |
| -NextHop           | Defines the next hop for an IP route      |
| -RouteMetric       | Defines the route metric for an IP route |

The following command creates an IP routing table entry:

```powershell
New-NetRoute -DestinationPrefix 0.0.0.0/24 -InterfaceAlias "Ethernet" -DefaultGateway 192.168.1.1
```

---
# Manage DNS clients in PowerShell

PowerShell offers cmdlets for managing DNS client settings, DNS name query resolution, and for securing DNS clients.

DNS client management cmdlets are part of the DNSClient PowerShell module and have the text “DnsClient” in the noun part of the name.

The following table lists common cmdlets for modifying DNS client settings.

Table 1: Cmdlets for modifying DNS client settings
| Cmdlet                      | Description                                           |
|-----------------------------|-------------------------------------------------------|
| Get-DnsClient               | Gets details about a network interface               |
| Set-DnsClient               | Sets DNS client configuration settings for a network interface |
| Get-DnsClientServerAddress  | Gets the DNS server address settings for a network interface |
| Set-DnsClientServerAddress  | Sets the DNS server address for a network interface  |

> [!NOTE]
> Set-DnsClient requires an interface that an alias or index references.

The following command sets the connection-specific suffix for an interface:

```powershell
Set-DnsClient -InterfaceAlias Ethernet -ConnectionSpecificSuffix "adatum.com"
```

---
# Manage Windows Firewall settings in PowerShell

PowerShell supports the NetSecurity module that contains cmdlets to manage local Network Security configurations such as Windows firewall rules and IP security settings.

To manage firewall settings, use cmdlets that have the text “NetFirewall” in their names. For firewall rule management, use cmdlets that contain the noun “NetFirewallRule.”

The following table lists common cmdlets for managing firewall settings and rules.

Table 1: Cmdlets for managing firewall settings and rules

| Cmdlet                  | Description                              |
|-------------------------|------------------------------------------|
| New-NetFirewallRule      | Creates a new firewall rule              |
| Set-NetFirewallRule      | Sets properties for a firewall rule     |
| Get-NetFirewallRule      | Gets properties for a firewall rule     |
| Remove-NetFirewallRule   | Deletes a firewall rule                  |
| Rename-NetFirewallRule   | Renames a firewall rule                  |
| Copy-NetFirewallRule     | Makes a copy of a firewall rule         |
| Enable-NetFirewallRule   | Enables a firewall rule                  |
| Disable-NetFirewallRule  | Disables a firewall rule                 |
| Get-NetFirewallProfile   | Gets properties for a firewall profile  |
| Set-NetFirewallProfile   | Sets properties for a firewall profile  |

You can use the Get-NetFirewallRule cmdlet to retrieve settings for firewall rules. You can enable and disable rules by using one of the following cmdlets:

* The Set-NetFirewallRule cmdlet with the -Enabled parameter
* The Enable-NetFirewallRule or Disable-NetFirewallRule cmdlets.
The following commands both enable firewall rules in the group Remote Access:

```powershell
Enable-NetFirewallRule -DisplayGroup "Remote Access"
```
and
```powershell
Set-NetFirewallRule -DisplayGroup "Remote Access" -Enabled True
```

--- 

### Summary

In this module, you've learned about the PowerShell modules and cmdlets used for configuring network settings for Windows devices. The following are the key takeaways:

PowerShell includes the NetTCPIP module, which consists of TCP/IP-specific cmdlets used to manage network settings for Windows servers and devices. You can use these cmdlets to add, remove, change, and validate IP address settings.
The NetTCPIP PowerShell module also includes cmdlets used to manage the routing table for Windows servers and devices. They have the noun “NetRoute” in their names.
The DNSClient PowerShell module offers cmdlets for managing DNS client settings, DNS name query resolution, and for securing DNS clients. They have the text “DnsClient” in the noun part of the name.
PowerShell supports the NetSecurity module that contains cmdlets to manage local Network Security configurations such as Windows firewall rules and IP security settings.

--- 
## Check your knowledge

---

### 1. Which parameter can you use with *-NetIPAddress cmdlets to identify a network interface?

* [ ] -DefaultGateway
* [ ] -IPAddress
* [ ] -InterfaceAlias

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** -InterfaceAlias  
💡 This parameter allows you to specify the network interface by name or alias when working with *-NetIPAddress cmdlets, making it easier to target a specific network adapter.

</details>

---

### 2. You need to manage firewall settings and rules with PowerShell. Which PowerShell module contains the required cmdlets?

* [ ] DNSClient module
* [ ] NetTCPIP module
* [ ] NetSecurity module

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NetSecurity module  
💡 The NetSecurity module contains cmdlets such as *Get-NetFirewallRule*, *New-NetFirewallRule*, and *Set-NetFirewallRule*, which are used to manage firewall rules and settings on Windows systems.

</details>

---
