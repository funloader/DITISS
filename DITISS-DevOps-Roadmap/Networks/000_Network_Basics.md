### 🛜 1.1 DATA COMMUNICATIONS

✅ *Data communication is the exchange of digital data between devices using a transmission medium (copper, fiber, wireless).*

- Requires hardware + software (NICs, protocols, OS, applications).
- Communication happens over physical or wireless media.
- Effectiveness depends on Delivery, Accuracy, Timeliness, Jitter.
- Basis for all modern networking, telecommunication, internet communication.

🎤 Data communication is the process of transferring digital data between two devices over a medium like copper, fiber, or wireless. A reliable communication system ensures correct delivery, accuracy, timeliness, and minimal jitter, especially important for real-time applications like voice and video.

🧭 **The Four Fundamental Characteristics**

1️⃣ *Delivery*
- Data must reach the correct destination.
- Ensured via addressing (MAC, IP), routing, switching.

2️⃣ *Accuracy*
- Data must be error-free.
- Achieved using error detection/correction (CRC, checksums, ARQ).

3️⃣ *Timeliness*
- Data must arrive on time.
- Critical for streaming, VoIP, online gaming.
- Called real-time transmission.

4️⃣ *Jitter*
- Variation in packet arrival time.
- High jitter causes choppy audio/video.
- Managed using jitter buffers, QoS.

🌍 *Real-World Example*
In a Zoom call:
- Delivery: Packets reach your device.
- Accuracy: Error-corrected packets reconstruct voice/video properly.
- Timeliness: Must arrive instantly.
- Jitter: If packet timing varies (30ms → 50ms → 20ms), video lags or breaks.

### 1.1.1 *Components*

*A data communication system consists of five components: Message, Sender, Receiver, Transmission Medium, and Protocol.*

- Communication only works when all five components are present.
- Message = information; Sender/Receiver = endpoints; Medium = path; Protocol = rules.
- Missing any component → no meaningful communication.

🎤 A communication system has five parts: the message to be sent, the sender, the receiver, the transmission medium like copper/fiber/wireless, and the protocol that defines how data is formatted and transmitted. All of these together ensure end-to-end data transfer.

1️⃣ *Message*
- The actual data (text, audio, video, numbers, images).
- Can be analog or digital depending on application.

**Interview angle:** *What kind of data formats do networks handle ?*

2️⃣ *Sender*
- Device initiating the data transfer.
- Examples: PC, phone, CCTV camera, IoT device.

**Interview point:** *Sender converts the message into signals.*

3️⃣ *Receiver*
- Device that receives and interprets the signals.
- Examples: Server, laptop, TV, router.

**Interview point:** *Receiver must understand the same protocol as sender.*

4️⃣ *Transmission Medium*
- The physical or wireless channel.
- Examples:
  - Twisted pair (Ethernet)
  - Coaxial cable
  - Fiber-optic (long-range, high-speed)
  - Radio waves (Wi-Fi, mobile networks)

**Why important:** *Speed, distance, noise depend heavily on the medium.*

5️⃣ *Protocol*
- The set of rules managing data communication.
- Defines:
  - Format
  - Timing
  - Error control
  - Flow control
- Examples: *TCP, UDP, HTTP, FTP, SIP, DNS.*

### 🔁 1.1.2 Data Flow (Simplex, Half-Duplex, Full-Duplex)
*Data flow defines how signals travel between two devices — in one direction or both.*

📘 **2. Short Technical Explanation**
Data communication can happen in three modes:
- Simplex → *one-way only* Entire channel bandwidth is used for sending in one direction.
- Half-Duplex → *both ways, but not simultaneously* Bandwidth is shared; only one device speaks at a time.
- Full-Duplex → *both ways, at the same time* There are two main ways this is achieved:
1. Two Separate Physical Paths
  - How it works : One physical path is dedicated to **sending** & A second, separate physical path is dedicated to **receiving**
  - *No interference because transmit and receive signals never share the same medium.*
  - Examples : Ethernet (older twisted-pair & fiber links) , One wire/fiber pair for TX, another for RX
  - Advantages : Simple design, True simultaneous communication, Minimal signal processing
  - Disadvantages :  Requires extra physical resources (wires/fibers)

2. Channel Division (Shared Medium)

 * A. Frequency Division Duplex (FDD / FDM-style)

  - How it works : Transmit and receive use **different frequency bands**. Both operate simultaneously
  - Examples : Cellular networks (LTE, 5G FDD), DSL (Digital Subscriber Line) internet connections
  - Advantages : Continuous two-way communication & No waiting to transmit
  - Disadvantages : Requires careful frequency planning & Needs filters to avoid interference
    
* B. Time Division Duplex (TDD / TDM-style)

  - How it works : Transmit and receive use the **same frequency**.Time is divided into **rapid alternating time slots**
  - *Appears simultaneous to users, but at any instant only one direction is active*
  - Examples : Wi-Fi, 5G TDD, Walkie-talkie systems with fast switching
  - Advantages : Efficient use of spectrum & Flexible allocation of bandwidth
  - Disadvantages : Requires tight synchronization & Slight latency due to switching
   
```

| Method         | Physical Medium | Separation Method | True Simultaneous?    |
| -------------- | --------------- | ----------------- | --------------------- |
| Separate paths | Two             | Physical          | ✅ Yes                |
| FDD            | One             | Frequency         | ✅ Yes                |
| TDD            | One             | Time              | ⚠️ Quasi-simultaneous |

```

These modes determine link capacity, performance, and use cases.

🎤 There are three data flow modes. Simplex is one-way communication like a keyboard to a monitor. Half-duplex allows both transmit and receive but not simultaneously, like walkie-talkies. Full-duplex supports simultaneous transmission and reception, such as a phone call. Modern networks mostly use full-duplex for better bandwidth utilization.



### 1.2 NETWORKS

## 🧭 Who Owns “The Internet”?

### ✅ 1. One-Line Definition

- *The internet has no single owner; it's a global collection of interconnected networks following common standards (TCP/IP).*

- Data communication can happen in three modes:
  - Simplex → one-way only
  - Half-Duplex → both ways, but not simultaneously
  - Full-Duplex → both ways, at the same time
These modes determine link capacity, performance, and use cases.

🎤 There are three data flow modes. Simplex is one-way communication like a keyboard to a monitor. Half-duplex allows both transmit and receive but not simultaneously, like walkie-talkies. Full-duplex supports simultaneous transmission and reception, such as a phone call. Modern networks mostly use full-duplex for better bandwidth utilization

- ❌ Saying “Wi-Fi is full-duplex” (it’s half-duplex by design)

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

### 🔄 2.3 Network Infrastructure
- End devices : An end device (or host) is either the source or destination of a message transmitted over the network.
  - Computers (workstations, laptops, file servers, web servers)
  - Network printers
  - Telephones and teleconferencing equipment
  - Security cameras
  - Mobile devices (such as smart phones, tablets, PDAs, and wireless debit/credit card readers and barcode scanners)
- Intermediate devices :
  - Wirless Router
  - Lan Switch
  - Router
  - Muiltilayer Switch
  - Firewall Appliance
- Network media :
  - Wireless Media
  - LAN Media
  - WAN Media
    
### 🔄 2.3 ISP Services
  - An Internet Service Provider (ISP) provides the link between the home network and the internet.
  - ISPs are connected in a hierarchical manner that ensures that internet traffic generally takes the shortest path from the source to the destination.
  - Two common methods ate cable and DSL. Other option include cellular, satellite and dail-up telephone.

---

  1️⃣ **Cable**
   - Typically offered by cable television service providers, the internet data signal is carried on the same coaxial cable that delivers cable television.
   - It provides a high bandwidth, always on, connection to the internet.
   - A special cable modem separates the internet data signal from the other signals carried on the cable and provides an Ethernet connection to a host computer or LAN.

---

  2️⃣ **DSL ( Digital Subscriber Line )**
   - Digital Subscriber Line provides a high bandwidth, always on, connection to the internet.
   - It requires a special high-speed modem that separates the DSL signal from the telephone signal and provides an Ethernet connection to a host computer or LAN.
   - DSL runs over a telephone line, with the line split into three channels.
     - One channel is used for voice telephone calls. This channel allows an individual to receive phone calls without disconnecting from the internet.
     - Second channel is a faster download channel, used to receive information from the internet.
     - Third channel is used for sending or uploading information. This channel is usually slightly slower than the download channel.
   - The quality and speed of the DSL connection depends mainly on the quality of the phone line and the distance from the central office of your phone company The farther you are from the central office, the slower the connection.

---
