### ✅ 1. What is an IP Address?

*One-line definition*
✅ An IP address is a logical address used to uniquely identify a device on a network.

🎤 An IP address is a numerical label assigned to every device on a network for identification and communication. It has two parts: the Network ID, which identifies the network, and the Host ID, which identifies the specific device.
- An IP address has two components:
 - 1️⃣ Network ID
   - Identifies the network segment
   - Used by routers for routing decisions
 - 2️⃣ Host ID
   - Identifies the specific device in the network
   - Must be unique within the network

**Technical explanation**
- Works at Layer 3 (Network Layer)
- Used for routing packets between networks
= Assigned to interfaces (NICs)
- Written in IPv4 (32-bit) or IPv6 (128-bit) format
Components of an IPv4 Address
 - Network ID – identifies the network
 - Host ID – identifies the specific device inside that network
Example: 192.168.1.10/24
  - Network ID = 192.168.1.0
  - Host ID = .10

*Follow-ups:*
- How does IP differ from MAC?
- Why do we need IP addressing?

### 🏷️ 2. Classes of IP Addresses (IPv4)

### 🔄 4. Types of IP Addresses
1️⃣ **Private IP**
*Used inside networks, not routable on internet.
Ranges:*
 - 10.0.0.0 – 10.255.255.255
 - 172.16.0.0 – 172.31.255.255
 - 192.168.0.0 – 192.168.255.255

2️⃣ **Public IP**
- Routable on the internet, assigned by ISP.

3️⃣ **Static IP**
- Assigned manually → used for servers, printers, routers.

4️⃣ **Dynamic IP**
- Assigned automatically by DHCP.

### ⚡ 5. Special IPs (Important for Interviews)
🔁 **Loopback IP**
 - 127.0.0.1
 - Used for *self-testing*, checking TCP/IP stack
 - Helps test network software locally
 - Used by developers & troubleshooting (``ping 127.0.0.1``)

⚠️ **APIPA (Automatic Private IP Addressing)**
 - Range: 169.254.0.0 – 169.254.255.255
 - Assigned when DHCP server is unreachable
 - Device can only communicate within local subnet
 - Common interview keyword: "DHCP fallback mechanism"

 What happens if gateway is misconfigured?

What is default route (0.0.0.0/0)?

What is the difference between DNS and Gateway?

What is subnet mask?

How does DHCP work?
