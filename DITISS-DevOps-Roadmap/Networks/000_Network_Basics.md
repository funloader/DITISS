## 🧭 Who Owns “The Internet”?

### ✅ 1. One-Line Definition

- *The internet has no single owner; it's a global collection of interconnected networks following common standards (TCP/IP).*

### 📘 2. Short Technical Explanation

- Internet = network of networks, interconnected via ISPs, IXPs, and backbone providers.
- No central authority controls the internet; governance is distributed (IETF, ICANN, W3C).
- Data travels through fiber, copper, wireless, satellite links.
- Every online service (Google, WhatsApp, Netflix) runs on servers connected to these networks.
- Local networks (home, office, enterprise) plug into the global internet through ISPs.

### 🎤 3. Ideal Interview Answer

- “The internet is not owned by any company or government. It’s a decentralized network of networks built on open standards like TCP/IP. It works because ISPs, backbone providers, and data centers interconnect and agree to route traffic globally. Bodies like ICANN and IETF manage standards and naming, not ownership.”


### 🌍 6. Real-World Example

- When you open instagram.com, the request flows:
```
Home WiFi → ISP → regional router → national backbone → international fiber → Meta data center → back to you.
```
- No single company owns this entire path.

## 🖧 1.1 Local Networks
✅ *A local network (LAN) connects devices within a small geographic area like homes, offices, or schools.*

- LANs interconnect devices like PCs, printers, cameras, Wi-Fi routers.
- Businesses use LANs for file sharing, communication, internal apps.
- SOHO networks connect small offices/homes with minimal devices.
- Larger networks span multiple floors or buildings with switches/routers.
- LANs connect to the internet through an ISP.

🎤 A local network is a small-area network where devices share resources like printers, files, and internet access. It can range from a simple home WiFi with few devices to enterprise LANs with switches, VLANs, and multiple subnets.

🌍 Your home Wi-Fi router creates a LAN connecting your phone, laptop, and smart TV.


## 💾 1.2 Data Transmission

### The Bit

✅ *All computers store and transmit data as binary digits (0s and 1s).*

- Bits represent two states: voltage high/low, light on/off.
- ASCII maps 8 bits (1 byte) to characters.
- Transmission converts bits to signals: electrical, optical, wireless.
- All input/output devices convert human-readable data ↔ binary.

🎤 Computers only process binary. A bit is the smallest unit, and 8 bits form a byte. Data is transmitted as electrical, optical, or wireless signals. ASCII or Unicode maps binary to readable characters.

### Bandwidth & Throughput

- *Bandwidth: Maximum data capacity of a link.*
- *Throughput: Actual data transfer rate measured.*
- Bandwidth units: bps → kbps → Mbps → Gbps → Tbps.
- Throughput impacted by congestion, latency, protocol overhead, slow links.
- Throughput ≤ slowest segment on the end-to-end path.

🎤 Bandwidth is the theoretical max speed; throughput is the real-world speed. Throughput depends on factors like congestion, latency, and device hops

Your ISP gives 100 Mbps but your speed test shows 70 Mbps = throughput.

### 📡 Common Methods of Data Transmission

There are three common methods of signal transmission used in networks:

- ⚡ Electrical signals - Transmission is achieved by representing data as electrical pulses on copper wire.
- 💡 Optical signals - Transmission is achieved by converting the electrical signals into light pulses.
- 📶 Wireless signals - Transmission is achieved by using infrared, microwave, or radio waves through the air.

## 1.3 Bandwidth and Throughput

### Bandwidth 
Bandwidth is the capacity of a medium to carry data.
| ⚙️ Units of Bandwidth | 🔠 Abbreviation | 🔁 Equivalence                    |
| --------------------- | --------------- | --------------------------------- |
| Bit per second        | **bps**         | 1 bit per second                  |
| Kilobit per second    | **kbps**        | 1,000 bits per second             |
| Megabit per second    | **Mbps**        | 1,000,000 bits per second         |
| Gigabit per second    | **Gbps**        | 1,000,000,000 bits per second     |
| Terabit per second    | **Tbps**        | 1,000,000,000,000 bits per second |

## 🖥️ 2.0 Network Components, Types amd Connections

### 👥 2.1 Client and Server Roles

✅ *Clients request services; servers provide services.*

- Servers host apps/services (DNS, web, file).
- Clients consume these services.
- Roles depend on installed software, not hardware.
- One machine can be both (e.g., dev laptop running a local server).

🎤 A server provides services like web, DNS, DHCP; clients request these services. The role depends on software, not hardware.

🌍 Browser (client) → Google server → HTML page returned.

### 🔄 2.2 Peer-to-Peer (P2P) Networking

✅ *A peer-to-peer network allows devices to act as both clients and servers without centralized control.*

- Simple network model used in homes/small offices.
- Each device can share files, printers, or resources directly.
- No central server; peers communicate directly.
- Works for small scale but not scalable or secure for enterprises.

🎤 A P2P network is one where each computer can act as both client and server. It’s easy to set up and used in small environments, but lacks centralized management, security, and scalability

🌍 Two PCs sharing files over a home Wi-Fi network.

### ✅ The advantages of peer-to-peer networking:

- Easy to set up
- Less complex
- Lower cost because network devices and dedicated servers may not be required
- Can be used for simple tasks such as transferring files and sharing printers

### ⚠️ The disadvantages of peer-to-peer networking:

- No centralized administration
- Not as secure
- Not scalable
- All devices may act as both clients and servers which can slow their performance

