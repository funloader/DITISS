> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 07

## **Session 8: Local policies and Group Policies**

---

---

### 1. What is the primary purpose of Group Policy in a Windows environment?

* [ ] Hardware configuration
* [ ] Application installation
* [ ] Centralized management of user and computer settings
* [ ] File compression

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Centralized management of user and computer settings
💡 Group Policy allows administrators to define security, software, and system settings centrally and enforce them on multiple computers or users in a domain or local machine. It is not meant for hardware configuration or compression.

</details>

---

### 2. Which tool is used to edit Local Group Policies on a Windows workstation?

* [ ] Task Manager
* [ ] gpedit.msc
* [ ] msconfig
* [ ] regedit

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** gpedit.msc
💡 `gpedit.msc` opens the Local Group Policy Editor, allowing configuration of policies for users and computers locally. Other tools serve different purposes: Task Manager (processes), msconfig (startup), regedit (registry).

</details>

---

### 3. To manage Group Policy across a Windows domain, which utility should an administrator use?

* [ ] Group Policy Management Console (GPMC)
* [ ] Device Manager
* [ ] File Explorer
* [ ] Event Viewer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Group Policy Management Console (GPMC)
💡 GPMC provides a centralized interface to create, edit, link, and report on GPOs in an Active Directory environment.

</details>

---

### 4. Where are Local Group Policies physically stored on a Windows machine?

* [ ] C:\Windows\System32\Config
* [ ] C:\Windows\System32\GroupPolicy
* [ ] C:\Program Files\Policies
* [ ] C:\Users\Default

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** C:\Windows\System32\GroupPolicy
💡 Local GPO settings are stored in this folder, including machine and user-specific configurations.

</details>

---

### 5. Which of the following is NOT considered a Local Policy category in Windows?

* [ ] User Rights Assignment
* [ ] Security Options
* [ ] Audit Policy
* [ ] Software Restriction Policies

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Software Restriction Policies
💡 Local Policies include User Rights Assignment, Security Options, and Audit Policy. Software Restriction Policies exist but under a different node called Security Settings → Software Restriction Policies.

</details>

---

### 6. Which command opens the Local Security Policy editor?

* [ ] lsp.msc
* [ ] secpol.msc
* [ ] locpol.msc
* [ ] policyedit.exe

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** secpol.msc
💡 `secpol.msc` opens the Local Security Policy console where security settings like account policies and audit policies can be configured.

</details>

---

### 7. Who has the authority to modify Local Group Policy settings on a Windows system?

* [ ] Any user
* [ ] Only guests
* [ ] Users in the Administrators group
* [ ] Anyone with internet access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Users in the Administrators group
💡 Only users with administrative privileges can change Local Group Policy settings; standard or guest accounts cannot.

</details>

---

### 8. An administrator wants to know the order in which Group Policies are applied in Windows. Which sequence is correct?

* [ ] Site → OU → Domain → Local
* [ ] Local → Site → Domain → OU
* [ ] OU → Domain → Site → Local
* [ ] Local → Site → Domain → OU

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Local → Site → Domain → OU
💡 Group Policies are processed starting from Local, then Site, Domain, and finally Organizational Unit (OU). Policies applied later override conflicting settings from earlier ones.

</details>

---

### 9. A domain GPO conflicts with a local policy on a workstation. What happens?

* [ ] Local policy overrides domain policy
* [ ] Domain policy overrides local policy
* [ ] Neither policy is applied
* [ ] A random policy applies

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Domain policy overrides local policy
💡 In Active Directory, domain-level policies have higher precedence over local GPOs, ensuring consistent configuration across multiple machines.

</details>

---

### 10. How can an administrator immediately enforce the latest Group Policy settings on a client computer?

* [ ] gpupdate /force
* [ ] gppolicy /update
* [ ] refresh /gp
* [ ] gpedit /refresh

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** gpupdate /force
💡 The `gpupdate /force` command reapplies all policy settings immediately, overriding the normal refresh interval.

</details>

---

### 11. In the Group Policy hierarchy, which policy is applied first on a Windows machine?

* [ ] Organizational Unit (OU)
* [ ] Domain
* [ ] Local
* [ ] Site

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Local
💡 Local policies are applied first, followed by Site, Domain, and OU policies. Later policies can override earlier ones.

</details>

---

### 12. What does the Group Policy refresh interval determine?

* [ ] Boot speed
* [ ] Policy replication timing
* [ ] Frequency of policy reapplication
* [ ] Internet access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Frequency of policy reapplication
💡 Group Policy refresh interval controls how often policies are reapplied to ensure updated settings are enforced, typically every 90 minutes by default.

</details>

---

### 13. Where are domain Group Policy Objects (GPOs) physically stored?

* [ ] DNS
* [ ] Active Directory and SYSVOL
* [ ] Event Viewer
* [ ] Firewall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Active Directory and SYSVOL
💡 GPOs are stored in Active Directory for metadata and in SYSVOL for policy files/scripts, enabling replication across domain controllers.

</details>

---

### 14. What is the purpose of Administrative Templates in Group Policy?

* [ ] Managing hardware
* [ ] Defining registry-based settings
* [ ] Assigning IP addresses
* [ ] Creating user accounts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Defining registry-based settings
💡 Administrative Templates allow administrators to configure registry-based settings like control panel options, desktop settings, and system behavior through GPOs.

</details>

---

### 15. Which snap-in is primarily used for managing GPOs across an entire domain?

* [ ] Active Directory Users and Computers
* [ ] GPMC
* [ ] secpol.msc
* [ ] Event Viewer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** GPMC
💡 The Group Policy Management Console provides a centralized interface to create, link, backup, and report on GPOs at the domain level.

</details>

---

### 16. If a GPO is applied to an OU, what is its effect?

* [ ] All computers restart automatically
* [ ] Policy applies only to that OU’s objects
* [ ] It changes Group Policy order
* [ ] It disables other policies

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Policy applies only to that OU’s objects
💡 GPOs linked to an OU are applied to users and computers within that OU. Child OUs may inherit it unless inheritance is blocked.

</details>

---

### 17. What does Group Policy inheritance mean?

* [ ] Policies cannot be overridden
* [ ] Lower-level OUs inherit policies from higher-level containers
* [ ] Policies are copied between domains
* [ ] Policies are backed up automatically

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Lower-level OUs inherit policies from higher-level containers
💡 Policies applied at a higher level (domain, site) flow down to child OUs unless explicitly blocked or overridden by enforcement.

</details>

---

### 18. Which tool is used to display the Resultant Set of Policy (RSoP) for a user or computer?

* [ ] rsop.msc
* [ ] gpmc.msc
* [ ] gpedit.msc
* [ ] taskmgr.exe

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** rsop.msc
💡 `rsop.msc` shows the effective policies applied after considering all GPOs, inheritance, and security filtering.

</details>

---

### 19. In Active Directory, what is a GPO link?

* [ ] A backup of Group Policy
* [ ] A pointer from an AD container to a GPO
* [ ] A registry key
* [ ] A firewall rule

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A pointer from an AD container to a GPO
💡 Linking a GPO to a site, domain, or OU allows that container’s objects to receive the policy without duplicating the GPO itself.

</details>

---

### 20. Can Group Policies be applied selectively to a security group?

* [ ] No
* [ ] Only in Windows 7
* [ ] Yes, through security filtering
* [ ] Only on domain controllers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Yes, through security filtering
💡 Security filtering restricts GPO application to specific users or computers in a group, allowing granular control.

</details>

---

### 21. Which policy setting is used to restrict user logon hours?

* [ ] Account Lockout Policy
* [ ] User Rights Assignment
* [ ] Logon Hours
* [ ] Security Options

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Logon Hours
💡 Administrators can set allowed logon hours for user accounts via Account Properties → Logon Hours, ensuring security compliance.

</details>

---


### 22. An administrator wants to apply a GPO only to computers with specific hardware attributes, like disk size or OS version. Which feature should they use?

* [ ] Network filtering tool
* [ ] DNS management
* [ ] Conditional application of GPOs based on device attributes (WMI Filtering)
* [ ] Firewall exception rule

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Conditional application of GPOs based on device attributes (WMI Filtering)
💡 WMI filters allow administrators to target GPOs to computers that meet certain conditions, such as OS version, processor type, or installed software.

</details>

---

### 23. If a GPO is disabled at its source, what is the effect on the objects it was linked to?

* [ ] It is automatically deleted
* [ ] Settings are no longer applied
* [ ] It has no effect on objects
* [ ] It triggers event logs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Settings are no longer applied
💡 Disabling a GPO stops it from applying its settings to linked objects, though the GPO still exists and can be re-enabled later.

</details>

---

### 24. Which command can an administrator run to see all currently applied policies on a system along with inheritance details?

* [ ] gpstatus /show
* [ ] gpresult /r
* [ ] showgp /current
* [ ] gplist /active

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** gpresult /r
💡 `gpresult /r` provides a detailed report of applied GPOs, including local and domain policies, inheritance, and security filtering.

</details>

---

### 25. An organization wants user policies to depend on the computer the user logs on to (e.g., different settings in labs vs. offices). Which Group Policy feature achieves this?

* [ ] Applies user policy settings based on the user’s computer (Loopback Processing)
* [ ] Blocks domain policies
* [ ] Allows policy testing only
* [ ] Syncs GPO with firewall rules

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Applies user policy settings based on the user’s computer (Loopback Processing)
💡 Loopback processing replaces or merges user policies with those defined for the computer, enabling location-specific user configurations.

</details>

---

### 26. When multiple GPOs apply to a single object with conflicting settings, how is the final setting determined?

* [ ] Site policy wins
* [ ] First applied wins
* [ ] Last applied wins
* [ ] Randomly selected

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Last applied wins
💡 In Group Policy, the last-applied GPO (in the processing order: Local → Site → Domain → OU) overrides conflicting settings from earlier GPOs.

</details>

---

### 27. Which GPO category controls password complexity requirements for domain users?

* [ ] Account Policies
* [ ] Audit Policies
* [ ] Security Options
* [ ] Firewall Settings

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Account Policies
💡 Password policies, account lockout, and Kerberos settings are configured under Account Policies within Group Policy.

</details>

---

### 28. What is the effect of marking a GPO as “Enforced” when linked to a container?

* [ ] Deletes all conflicting GPOs
* [ ] Ensures the GPO cannot be overridden by lower-level policies
* [ ] Disables GPO inheritance
* [ ] Ignores the GPO

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ensures the GPO cannot be overridden by lower-level policies
💡 Enforcing a GPO ensures its settings apply even if child OUs have conflicting policies; it overrides “Block Inheritance.”

</details>

---

### 29. What does the “Block Inheritance” option do in Group Policy for an OU?

* [ ] Prevents child OUs from applying any GPOs
* [ ] Prevents higher-level GPOs from applying to that OU
* [ ] Deletes the GPO
* [ ] Exports GPOs to a file

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Prevents higher-level GPOs from applying to that OU
💡 Block Inheritance stops GPOs from parent containers (site/domain/OU) from affecting the OU, though enforced GPOs still apply.

</details>

---

### 30. How can an administrator create a backup of a GPO?

* [ ] By exporting the registry
* [ ] Using the GPMC backup option
* [ ] Through Group Policy Editor
* [ ] GPOs cannot be backed up

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Using the GPMC backup option
💡 GPOs can be backed up through the Group Policy Management Console, storing all policy settings, scripts, and links for recovery or migration.

</details>

---

## **Session 9: Implement Network Connectivity and Remote Access Solutions**

---

### 1. A company wants all devices on its network to automatically obtain IP addresses without manual configuration. Which protocol should be used?

* [ ] DNS
* [ ] FTP
* [ ] DHCP
* [ ] HTTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DHCP
💡 Dynamic Host Configuration Protocol (DHCP) automatically assigns IP addresses, subnet masks, default gateways, and DNS servers to network devices, reducing manual configuration errors.

</details>

---

### 2. An employee needs to securely connect to the office network over the internet. What does VPN stand for?

* [ ] Virtual Private Network
* [ ] Very Protected Network
* [ ] Verified Public Network
* [ ] Virtual Public Node

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtual Private Network
💡 A VPN creates an encrypted tunnel over public networks, allowing secure communication between remote clients and a private network.

</details>

---

### 3. While configuring a secure web server, which port should be opened for HTTPS by default?

* [ ] 80
* [ ] 21
* [ ] 23
* [ ] 443

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 443
💡 HTTPS uses port 443 by default, providing encrypted communication via TLS/SSL. Port 80 is for HTTP (unencrypted).

</details>

---

### 4. A network administrator wants to verify if a remote server is reachable from a Windows PC. Which command-line tool should be used?

* [ ] ping
* [ ] notepad
* [ ] calc
* [ ] winver

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ping
💡 The `ping` command sends ICMP Echo Requests to a target IP or hostname to check connectivity and round-trip response time.

</details>

---

### 5. Which protocol is used to securely access and manage a remote computer over a network?

* [ ] HTTP
* [ ] SSH
* [ ] SMTP
* [ ] POP3

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SSH
💡 Secure Shell (SSH) provides encrypted remote login and command execution on remote systems, commonly used for server administration.

</details>

---

### 6. A network engineer is configuring a Class C network. What is the default subnet mask?

* [ ] 255.0.0.0
* [ ] 255.255.0.0
* [ ] 255.255.255.0
* [ ] 255.255.255.255

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 255.255.255.0
💡 Class C IP addresses (192.0.0.0–223.255.255.255) have a default subnet mask of 255.255.255.0, allowing 256 IP addresses per network.

</details>

---

### 7. An employee wants to access their office desktop from home. Which Windows feature allows this?

* [ ] Remote Desktop
* [ ] Task Scheduler
* [ ] BitLocker
* [ ] Device Manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Remote Desktop
💡 Remote Desktop allows users to securely connect to a Windows computer from another location over a network using RDP.

</details>

---

### 8. A system administrator needs to remotely manage multiple Windows servers from a workstation. Which Windows feature should be installed?

* [ ] Device Manager
* [ ] Remote Assistance
* [ ] Remote Server Administration Tools (RSAT)
* [ ] Event Viewer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Remote Server Administration Tools (RSAT)
💡 RSAT allows administrators to remotely manage roles and features on Windows servers without logging in directly, improving operational efficiency.

</details>

---

### 9. An organization wants to provide employees remote network access. Which device allows clients to securely connect and authenticate to the corporate network?

* [ ] Monitor power usage
* [ ] Provide internet connectivity only
* [ ] Remote Access Server (RAS)
* [ ] Block unauthorized websites

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Remote Access Server (RAS)
💡 RAS enables remote users to connect over dial-up, VPN, or other protocols, providing authentication, IP allocation, and network access control.

</details>

---

### 10. Which technology ensures confidentiality and integrity of IP packets across a public network?

* [ ] File compression
* [ ] Hardware acceleration
* [ ] Encryption and authentication (IPsec)
* [ ] IP allocation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Encryption and authentication (IPsec)
💡 IPsec secures network traffic using encryption and authentication, protecting data against interception and tampering over untrusted networks.

</details>

---

### 11. A company wants VPN access using SSL/TLS to bypass restrictive firewalls. Which VPN type should they use?

* [ ] PPTP
* [ ] L2TP
* [ ] SSTP
* [ ] IPSec

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SSTP
💡 Secure Socket Tunneling Protocol (SSTP) uses SSL/TLS over TCP port 443, making it firewall-friendly and providing strong encryption.

</details>

---

### 12. Which network device connects multiple subnets and directs traffic based on IP addresses?

* [ ] Switch
* [ ] Router
* [ ] Access Point
* [ ] Repeater

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Router
💡 Routers operate at Layer 3, forwarding packets between different networks based on IP addresses and routing tables.

</details>

---

### 13. A network engineer wants to view all IP, gateway, DNS, and MAC information on a Windows computer. Which command should be used?

* [ ] netconfig
* [ ] ipconfig /all
* [ ] winipcfg
* [ ] ping -d

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ipconfig /all
💡 `ipconfig /all` provides detailed network configuration, including all interfaces, IP addresses, DNS servers, and MAC addresses.

</details>

---

### 14. Which port does Remote Desktop Protocol (RDP) use by default?

* [ ] TCP 3389
* [ ] UDP 80
* [ ] TCP 22
* [ ] UDP 443

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TCP 3389
💡 RDP uses TCP port 3389 to establish encrypted remote desktop sessions between clients and Windows systems.

</details>

---

### 15. A VPN server needs to authenticate users centrally. Which authentication protocol is commonly used?

* [ ] RADIUS
* [ ] DHCP
* [ ] DNS
* [ ] FTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RADIUS
💡 Remote Authentication Dial-In User Service (RADIUS) centralizes authentication, authorization, and accounting for VPN and network access.

</details>

---

### 16. An organization wants internal users to access the internet using private IPs while mapping them to a single public IP. Which technology enables this?

* [ ] Block incoming connections
* [ ] Network Address Translation (NAT)
* [ ] Encrypt data in transit
* [ ] Generate MAC addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network Address Translation (NAT)
💡 NAT translates private IP addresses to public IPs for internet access, conserving IPs and adding a layer of network security.

</details>

---

### 17. A system administrator wants to monitor CPU, memory, and network bandwidth usage in real-time. Which Windows tool is suitable?

* [ ] Event Viewer
* [ ] Task Scheduler
* [ ] Resource Monitor
* [ ] Disk Cleanup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Resource Monitor
💡 Resource Monitor provides detailed, real-time monitoring of system and network performance metrics in Windows.

</details>

---

### 18. Which Windows service allows users to connect remotely via dial-up or VPN?

* [ ] Remote Procedure Call
* [ ] Routing and Remote Access Service (RRAS)
* [ ] Windows Firewall
* [ ] Task Manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Routing and Remote Access Service (RRAS)
💡 RRAS provides VPN, dial-up, and NAT services, enabling secure remote access to Windows networks.

</details>

---

### 19. A company wants remote users to access the VPN while still using their local internet connection. What is this technique called?

* [ ] To split the screen in remote desktop
* [ ] To reduce bandwidth for remote users
* [ ] Split tunneling
* [ ] To connect two VPNs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Split tunneling
💡 Split tunneling allows traffic to be routed via the VPN for internal resources while letting other traffic use the local internet, optimizing bandwidth and speed.

</details>

---

### 20. A network engineer wants to determine the path taken by packets from a PC to a remote server. Which command is used?

* [ ] Deletes IP configuration
* [ ] Configures DNS
* [ ] Traces the route packets take to a destination
* [ ] Backs up routing tables

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Traces the route packets take to a destination (`tracert`)
💡 `tracert` displays each hop and latency along the path to the target, helping diagnose routing or network issues.

</details>

---

### 21. Which IP protocol supports a vastly larger address space to accommodate growing global internet demand?

* [ ] IPv4
* [ ] IPv5
* [ ] IPv6
* [ ] ARP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IPv6
💡 IPv6 provides 128-bit addresses, vastly expanding the address space compared to IPv4 (32-bit), and supports improved routing and auto-configuration.

</details>

---

### 22. An organization needs VPN access that can bypass strict firewalls and provides strong encryption using HTTPS. Which VPN protocol best meets this requirement?

* [ ] PPTP
* [ ] Uses port 80
* [ ] SSTP
* [ ] No authentication needed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SSTP
💡 Secure Socket Tunneling Protocol (SSTP) uses SSL/TLS over TCP port 443, offering strong encryption and firewall-friendly connectivity, unlike PPTP which is less secure.

</details>

---

### 23. A network admin wants RRAS to select the optimal path when multiple routes exist to a destination. Which feature should be used?

* [ ] Port forwarding
* [ ] Demand-dial routing
* [ ] Static routing
* [ ] Multilink routing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Demand-dial routing
💡 Demand-dial routing allows RRAS to dynamically select routes based on metrics and availability, optimizing network traffic over multiple connections.

</details>

---

### 24. A company wants to restrict VPN access for employees to official working hours only. How can this be implemented?

* [ ] Modify local policy
* [ ] Set time-based firewall rules
* [ ] Configure user logon hours in Active Directory
* [ ] Change DNS settings

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configure user logon hours in Active Directory
💡 Active Directory allows administrators to enforce logon hours for user accounts, restricting VPN or network access outside designated times.

</details>

---

### 25. An administrator wants to create, manage, and monitor VPN and dial-up connections on Windows Server. Which tool is most appropriate?

* [ ] Network and Sharing Center
* [ ] RRAS Console
* [ ] Device Manager
* [ ] Server Manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RRAS Console
💡 The RRAS Console allows configuration of VPN, dial-up, NAT, and routing services on Windows Server with centralized management.

</details>

---

### 26. Which tunneling protocol encrypts data but relies on external security mechanisms like IPSec for authentication?

* [ ] L2TP
* [ ] PPTP
* [ ] IPSec
* [ ] OpenVPN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** L2TP
💡 Layer 2 Tunneling Protocol (L2TP) provides tunneling but does not encrypt data by itself; it is commonly combined with IPSec to ensure security.

</details>

---

### 27. What is a primary drawback of a full-tunnel VPN configuration compared to split-tunnel?

* [ ] Insecure data
* [ ] Increased latency and bandwidth usage
* [ ] Doesn’t encrypt data
* [ ] No access to internal resources

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Increased latency and bandwidth usage
💡 Full-tunnel VPN routes all traffic through the VPN server, increasing latency and consuming bandwidth for internet-bound traffic, unlike split-tunneling.

</details>

---

### 28. Which configuration allows RRAS to act as a NAT device, providing internet access to internal clients?

* [ ] DHCP Relay
* [ ] NAT routing protocol
* [ ] IP Helper
* [ ] IGMP Proxy

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NAT routing protocol
💡 RRAS can function as a NAT device by enabling NAT routing, translating private IPs to public IPs for internet access.

</details>

---

### 29. A company wants to ensure DNS queries over a VPN are encrypted and cannot be intercepted. Which approach should be used?

* [ ] Disable DNS
* [ ] Use plaintext queries
* [ ] Implement DNS over HTTPS (DoH)
* [ ] Block port 53

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Implement DNS over HTTPS (DoH)
💡 DNS over HTTPS encrypts DNS queries, protecting them from eavesdropping and ensuring confidentiality over untrusted networks.

</details>

---

### 30. To allow remote users to connect via RDP from external networks, what must be configured on the firewall?

* [ ] Open port 3389
* [ ] Block port 443
* [ ] Enable NAT loopback
* [ ] Disable VPN access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Open port 3389
💡 RDP uses TCP port 3389 by default; the firewall must allow inbound traffic on this port for external remote desktop access. Proper security measures like VPN or RD Gateway are recommended.

</details>

---


