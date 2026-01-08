> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---

# SET 04 – Internetworking (DITISS Level)

---

### 1. Which device operates at the Network Layer and is primarily responsible for directing packets between different networks?

* [ ] Hub
* [ ] Switch
* [ ] Router
* [ ] Bridge

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Router
💡 Routers operate at the Network Layer (Layer 3) of the OSI model. They use logical IP addresses to forward packets between networks, unlike switches and hubs, which operate at Layer 2 or Layer 1.

</details>

---

### 2. In an enterprise internetwork, what is the primary function of a gateway?

* [ ] Amplify network signals
* [ ] Connect devices within the same network
* [ ] Translate between different protocols to enable communication between networks
* [ ] Filter unwanted network traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Translate between different protocols to enable communication between networks
💡 A gateway serves as an entry/exit point between networks using different protocols, enabling interoperability, whereas routers primarily forward packets.

</details>

---

### 3. A company wants to connect multiple LANs across cities using public networks. Which OSI layer’s protocol is essential for this task?

* [ ] Application Layer
* [ ] Transport Layer
* [ ] Network Layer
* [ ] Data Link Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network Layer
💡 The Network Layer (Layer 3) handles logical addressing and routing, enabling communication across multiple networks (LANs/WANs).

</details>

---

### 4. Which protocol is fundamental for internetwork communication and routing over the Internet?

* [ ] IP (Internet Protocol)
* [ ] FTP (File Transfer Protocol)
* [ ] HTTP (Hypertext Transfer Protocol)
* [ ] SMTP (Simple Mail Transfer Protocol)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IP (Internet Protocol)
💡 IP provides addressing and routing capabilities, allowing packets to traverse multiple networks to reach their destination.

</details>

---

### 5. What is a key characteristic of a LAN within an internetwork?

* [ ] Always wireless
* [ ] Connects devices over long distances
* [ ] Connects devices within a small geographical area
* [ ] Operates at the Application Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Connects devices within a small geographical area
💡 LANs are designed for localized areas such as offices or campuses. Wide Area Networks (WANs) cover larger distances.

</details>

---

### 6. Which of the following statements about NAT (Network Address Translation) is correct?

* [ ] It assigns MAC addresses to devices
* [ ] It translates private IP addresses to public IP addresses
* [ ] It segments a network into VLANs
* [ ] It encrypts data during transmission

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It translates private IP addresses to public IP addresses
💡 NAT allows multiple devices in a private network to share a single public IP address, conserving IP addresses and enhancing security.

</details>

---

### 7. Which sequence correctly represents a basic internetwork setup from external connection to end devices?

* [ ] Hub → Router → Switch
* [ ] Router → Switch → Hub
* [ ] Switch → Hub → Router
* [ ] Router → Hub → Switch

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Router → Switch → Hub
💡 Routers connect to external networks, switches manage local traffic, and hubs (if present) are legacy devices for simple connectivity.

</details>

---

### 8. How many layers are there in the OSI model?

* [ ] 5
* [ ] 7
* [ ] 10
* [ ] 3

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 7
💡 The OSI model has seven layers: Physical, Data Link, Network, Transport, Session, Presentation, and Application.

</details>

---

### 9. Which OSI layer is responsible for establishing, managing, and terminating sessions between applications?

* [ ] Session Layer
* [ ] Transport Layer
* [ ] Data Link Layer
* [ ] Network Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Session Layer
💡 The Session Layer (Layer 5) controls dialog between applications, including session establishment, maintenance, and termination.

</details>

---

### 10. Physical addressing (MAC address) occurs at which OSI layer?

* [ ] Network Layer
* [ ] Transport Layer
* [ ] Data Link Layer
* [ ] Application Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data Link Layer
💡 MAC addresses are Layer 2 addresses used for local delivery within a LAN segment.

</details>

---

### 11. Data encryption and compression are performed at which OSI layer?

* [ ] Application Layer
* [ ] Presentation Layer
* [ ] Transport Layer
* [ ] Session Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Presentation Layer
💡 The Presentation Layer (Layer 6) handles data translation, compression, and encryption to ensure compatibility between applications.

</details>

---

### 12. Which protocol operates at the Transport Layer of the OSI model?

* [ ] HTTP
* [ ] TCP
* [ ] IP
* [ ] Ethernet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TCP
💡 TCP (Transmission Control Protocol) operates at Layer 4, providing reliable data delivery, sequencing, and flow control.

</details>

---

### 13. Which OSI layer is responsible for error detection and correction in data frames?

* [ ] Application Layer
* [ ] Transport Layer
* [ ] Data Link Layer
* [ ] Network Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data Link Layer
💡 Layer 2 ensures reliable link-level delivery using error detection techniques like CRC and can request retransmission.

</details>

---

### 14. Which layer defines logical addressing and routing for packets across networks?

* [ ] Transport Layer
* [ ] Network Layer
* [ ] Session Layer
* [ ] Application Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network Layer
💡 Layer 3 provides logical IP addressing and determines optimal paths for packet delivery.

</details>

---

### 15. Segmentation and reassembly of data occurs at which OSI layer?

* [ ] Transport Layer
* [ ] Session Layer
* [ ] Application Layer
* [ ] Data Link Layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Transport Layer
💡 Layer 4 breaks large messages into segments for transmission and reassembles them at the destination.

</details>

---

### 16. Which Ethernet standard supports speeds of 10 Gbps over twisted-pair cables?

* [ ] 1000Base-T
* [ ] 10Base-T
* [ ] 10GBase-T
* [ ] 100Base-TX

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 10GBase-T
💡 10GBase-T supports 10 Gbps over standard Cat6a or Cat7 twisted-pair cables, widely used in high-speed LANs.

</details>

---

### 17. A network administrator needs to identify a device uniquely on a LAN. Which address should they use?

* [ ] IP address
* [ ] MAC address
* [ ] Subnet mask
* [ ] Domain name

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MAC address
💡 MAC addresses are unique 48-bit identifiers assigned to network interfaces for Layer 2 communication.

</details>

---

### 18. In Ethernet networking, “Full Duplex” refers to:

* [ ] Data can only travel in one direction at a time
* [ ] Data can be sent and received simultaneously
* [ ] Data is sent only at scheduled intervals
* [ ] Data is transmitted only over fiber optic cables

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data can be sent and received simultaneously
💡 Full duplex allows bidirectional communication at the same time, unlike half-duplex, which alternates directions.

</details>

---

### 19. Which Ethernet device filters traffic and forwards frames only to the correct device based on MAC address?

* [ ] Router
* [ ] Switch
* [ ] Hub
* [ ] Gateway

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Switch
💡 Switches operate at Layer 2, using MAC address tables to forward frames selectively, reducing collisions compared to hubs.

</details>

---

### 20. For Gigabit Ethernet (1000Base-T), which cable type is most appropriate?

* [ ] Coaxial cable
* [ ] Fiber optic cable
* [ ] Twisted pair cable
* [ ] USB cable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Twisted pair cable
💡 Cat5e or Cat6 twisted-pair cables are used for 1 Gbps Ethernet connections over short distances (≤100 meters).

</details>

---

### 21. What is the primary purpose of the ARP (Address Resolution Protocol) in Ethernet?

* [ ] To map IP addresses to MAC addresses
* [ ] To route packets between networks
* [ ] To encrypt data for secure transmission
* [ ] To establish network connections

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To map IP addresses to MAC addresses
💡 ARP allows devices on a LAN to discover the physical MAC address corresponding to a known IP address for frame delivery.

</details>

---

### 22. Which of the following is NOT part of a standard Ethernet frame format?

* [ ] Start Frame Delimiter
* [ ] Data Payload
* [ ] Destination IP Address
* [ ] Frame Check Sequence

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Destination IP Address
💡 Ethernet frames use MAC addresses, not IP addresses, for Layer 2 delivery; IP addresses are used at Layer 3.

</details>

---

### 23. What is the maximum recommended length of a standard Cat5e/Cat6 cable for Gigabit Ethernet?

* [ ] 10 meters
* [ ] 50 meters
* [ ] 100 meters
* [ ] 200 meters

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 100 meters
💡 100 meters is the maximum length for twisted-pair Ethernet cabling to maintain signal integrity and throughput.

</details>

---

### 24. For long-distance Ethernet communication between buildings, which technology is preferred?

* [ ] Ethernet over Power
* [ ] Fiber Optic Ethernet
* [ ] Coaxial Ethernet
* [ ] Wireless Ethernet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Fiber Optic Ethernet
💡 Fiber optics provide high-speed, low-loss transmission over long distances, unlike copper-based Ethernet.

</details>

---

### 25. Which Wi-Fi standard supports a maximum speed of approximately 1.3 Gbps?

* [ ] Wi-Fi 3 (802.11g)
* [ ] Wi-Fi 4 (802.11n)
* [ ] Wi-Fi 5 (802.11ac)
* [ ] Wi-Fi 6 (802.11ax)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Wi-Fi 5 (802.11ac)
💡 Wi-Fi 5 introduced wider channel bandwidth (80–160 MHz) and MIMO for high-speed data transfer up to 1.3 Gbps.

</details>

---

### 26. What is the main difference between 2.4 GHz and 5 GHz Wi-Fi bands?

* [ ] 5 GHz provides greater range than 2.4 GHz
* [ ] 2.4 GHz supports faster speeds than 5 GHz
* [ ] 5 GHz supports faster speeds but has a shorter range
* [ ] 2.4 GHz is less prone to interference than 5 GHz

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 5 GHz supports faster speeds but has a shorter range
💡 Higher frequency signals (5 GHz) have less interference but shorter range and penetration compared to 2.4 GHz.

</details>

---

### 27. Which of the following is a common Wi-Fi security protocol?

* [ ] WPA2
* [ ] FTP
* [ ] TCP/IP
* [ ] HTTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** WPA2
💡 WPA2 provides encryption and authentication for Wi-Fi networks, securing data from unauthorized access.

</details>

---

### 28. What is the purpose of WPS (Wi-Fi Protected Setup)?

* [ ] Allow configuration without entering a password
* [ ] Prevent unauthorized devices from connecting
* [ ] Encrypt data over wireless networks
* [ ] Extend wireless coverage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Allow configuration without entering a password
💡 WPS simplifies network setup using PINs or push-button methods but may introduce security risks if not managed.

</details>

---

### 29. Which Wi-Fi 6 (802.11ax) feature enhances performance in environments with many devices?

* [ ] Increased range
* [ ] Higher frequency band
* [ ] Higher data transfer speeds and better multi-device handling
* [ ] Support for older devices only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Higher data transfer speeds and better multi-device handling
💡 Wi-Fi 6 introduces OFDMA and MU-MIMO to support multiple devices efficiently in dense networks.

</details>

---

### 30. What is the primary function of a Wireless Access Point (WAP)?

* [ ] Connect wireless devices to a wired network
* [ ] Manage routing across multiple networks
* [ ] Filter and monitor network traffic
* [ ] Assign IP addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Connect wireless devices to a wired network
💡 WAPs bridge wireless clients to the wired LAN while forwarding traffic and sometimes enforcing security policies.

</details>

---

### 31. Which is a disadvantage of using the 5 GHz Wi-Fi band?

* [ ] Shorter range compared to 2.4 GHz
* [ ] More prone to interference
* [ ] Slower data transfer speeds
* [ ] Higher power consumption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Shorter range compared to 2.4 GHz
💡 Higher frequency signals attenuate faster, resulting in a shorter coverage area.

</details>

---

### 32. In wireless networking, what does SSID stand for?

* [ ] Service Set Identifier
* [ ] Secure Service Identifier
* [ ] Subnet Set Identifier
* [ ] Simple Set Identifier

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Service Set Identifier
💡 SSID is the network name used to identify and differentiate wireless networks.

</details>

---

### 33. Which wireless standard operates on the 6 GHz frequency band?

* [ ] Wi-Fi 6 (802.11ax)
* [ ] Wi-Fi 7 (802.11be)
* [ ] Wi-Fi 5 (802.11ac)
* [ ] Wi-Fi 4 (802.11n)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Wi-Fi 7 (802.11be)
💡 Wi-Fi 7 expands operation into 6 GHz (alongside 2.4 GHz and 5 GHz) for higher throughput and low latency.

</details>

---

### 34. What is the main purpose of a mesh network?

* [ ] Provide higher data rates
* [ ] Connect multiple WAPs to extend coverage
* [ ] Support out-of-range devices
* [ ] Encrypt data between access points

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Connect multiple WAPs to extend coverage
💡 Mesh networks use multiple interconnected nodes to provide seamless wireless coverage over a large area.

</details>

---

### 35. Which wireless protocol offers the highest throughput in the 2.4 GHz band?

* [ ] 802.11g
* [ ] 802.11n
* [ ] 802.11a
* [ ] 802.11b

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 802.11n
💡 802.11n uses MIMO and wider channels to achieve higher throughput (~600 Mbps) on the 2.4 GHz band.

</details>

---

### 36. Which modulation technique is used in 802.11ac for high data throughput?

* [ ] BPSK
* [ ] QPSK
* [ ] QAM
* [ ] DSSS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** QAM
💡 Quadrature Amplitude Modulation (QAM) increases bits per symbol, enabling higher Wi-Fi 5/6 throughput.

</details>

---

### 37. Main advantage of using 5 GHz Wi-Fi over 2.4 GHz:

* [ ] Greater coverage
* [ ] Less interference and congestion
* [ ] Supported by more devices
* [ ] Cheaper implementation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Less interference and congestion
💡 5 GHz is less crowded and suffers less interference from devices like microwaves and Bluetooth than 2.4 GHz.

</details>

---

### 38. What does “beamforming” refer to in Wi-Fi technology?

* [ ] Amplifying signal directionally
* [ ] Extending wireless coverage
* [ ] Securing Wi-Fi connections
* [ ] Using multiple frequencies simultaneously

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Amplifying signal directionally
💡 Beamforming focuses Wi-Fi signals toward specific devices to improve performance and reduce interference.

</details>

---

### 39. Which Wi-Fi technology allows long-range communication with minimal power consumption?

* [ ] 802.11ac
* [ ] 802.11ah (Wi-Fi HaLow)
* [ ] 802.11ax
* [ ] 802.11n

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 802.11ah (Wi-Fi HaLow)
💡 Wi-Fi HaLow operates in sub-GHz bands, optimized for long-range IoT devices with low power consumption.

</details>

---

### 40. Which of the following is NOT a feature of Wi-Fi 6 (802.11ax)?

* [ ] Improved performance in crowded environments
* [ ] Faster speeds on 2.4 GHz and 5 GHz bands
* [ ] Greater support for IoT devices
* [ ] Inability to operate on the 2.4 GHz band

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Inability to operate on the 2.4 GHz band
💡 Wi-Fi 6 operates on both 2.4 GHz and 5 GHz bands, offering backward compatibility and improved multi-device performance.

</details>

---

