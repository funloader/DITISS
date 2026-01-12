> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---

# SET 03 – OpenDaylight & Mininet (DITISS Level)

---

### 1. An enterprise plans to deploy a software-defined networking (SDN) controller that is vendor-neutral, supports multiple southbound protocols, and allows extensible network applications. Which platform best fits this requirement?

* [ ] An open-source operating system
* [ ] A cloud service orchestration framework
* [ ] A proprietary SDN appliance
* [ ] A software-defined networking (SDN) controller platform

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A software-defined networking (SDN) controller platform
💡 SDN controllers like OpenDaylight provide centralized control, extensibility, and multi-vendor interoperability. This distinguishes them from general-purpose network OSes or cloud orchestration frameworks.

</details>

---

### 2. Which organization governs OpenDaylight as a collaborative open-source project to ensure vendor neutrality?

* [ ] Cisco
* [ ] Google
* [ ] Open Networking Foundation (ONF)
* [ ] The Linux Foundation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The Linux Foundation
💡 OpenDaylight operates under the Linux Foundation, ensuring open governance and preventing vendor lock-in.

</details>

---

### 3. You are developing a custom network application that runs natively on the OpenDaylight controller. Which programming language is most commonly used for such development?

* [ ] Python
* [ ] Ruby
* [ ] Java
* [ ] C++

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Java
💡 OpenDaylight is primarily built on Java and uses OSGi/Karaf architecture for modular application development.

</details>

---

### 4. Which of the following is **NOT** considered a core southbound or modeling component used within OpenDaylight?

* [ ] OpenFlow
* [ ] YANG
* [ ] OVSDB
* [ ] Docker

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Docker
💡 Docker is a containerization platform and not a native SDN or controller protocol/component of OpenDaylight.

</details>

---

### 5. In OpenDaylight, what is the primary purpose of the YANG modeling language?

* [ ] To virtualize network hardware
* [ ] To model network configurations, state data, and services
* [ ] To encrypt SDN controller communications
* [ ] To provide packet forwarding rules

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To model network configurations, state data, and services
💡 YANG provides a structured data modeling language used with NETCONF/RESTCONF in SDN controllers.

</details>

---

### 6. Which protocol is most commonly used by OpenDaylight for configuration and state management of network devices using YANG models?

* [ ] SNMP
* [ ] HTTP
* [ ] NETCONF
* [ ] SMTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NETCONF
💡 NETCONF works with YANG to enable transactional, model-driven configuration of network devices.

</details>

---

### 7. What is the **primary architectural goal** of OpenDaylight in SDN environments?

* [ ] To provide a cloud computing framework
* [ ] To enable centralized control and programmability
* [ ] To replace traditional routing protocols
* [ ] To enforce proprietary hardware usage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To enable centralized control and programmability
💡 OpenDaylight centralizes the control plane, enabling dynamic network behavior and automation.

</details>

---

### 8. Which OpenDaylight feature allows administrators to dynamically control packet forwarding behavior across switches?

* [ ] OpenStack
* [ ] Docker
* [ ] OpenFlow
* [ ] SNMP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OpenFlow
💡 OpenFlow enables the controller to program flow tables on switches dynamically.

</details>

---

### 9. Which of the following is **NOT** a typical enterprise or service-provider use case for OpenDaylight?

* [ ] Network orchestration and automation
* [ ] Network monitoring and analytics
* [ ] Network function virtualization (NFV)
* [ ] Game engine development

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Game engine development
💡 OpenDaylight is designed for SDN and NFV use cases, not application or game development.

</details>

---

### 10. What is the **main advantage** of adopting OpenDaylight in a multi-vendor SDN deployment?

* [ ] Proprietary licensing
* [ ] Vendor lock-in
* [ ] Flexibility, openness, and interoperability
* [ ] Limited scalability

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Flexibility, openness, and interoperability
💡 OpenDaylight promotes open standards and works across heterogeneous network environments.

</details>

---

### 11. OpenFlow was originally developed as part of SDN research at which institution?

* [ ] The Linux Foundation
* [ ] Stanford University
* [ ] Google
* [ ] Cisco

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Stanford University
💡 OpenFlow originated from Stanford and was later standardized by the Open Networking Foundation (ONF).

</details>

---

### 12. What is the **primary role** of OpenFlow in an SDN architecture?

* [ ] To provide network encryption
* [ ] To separate the control plane from the data plane
* [ ] To replace TCP/IP
* [ ] To standardize network hardware

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To separate the control plane from the data plane
💡 OpenFlow enables centralized control by moving decision-making to the SDN controller.

</details>

---

### 13. In OpenFlow-based networks, what is the function of a **flow table entry**?

* [ ] To define physical topology
* [ ] To specify packet forwarding rules
* [ ] To calculate routing metrics
* [ ] To manage power consumption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To specify packet forwarding rules
💡 Flow entries match packet headers and define actions such as forward, drop, or modify.

</details>

---

### 14. Which OpenFlow version standardized group tables and meters, enabling advanced traffic engineering features widely adopted in production SDN networks?

* [ ] OpenFlow 1.0
* [ ] OpenFlow 1.1
* [ ] OpenFlow 1.3
* [ ] OpenFlow 2.0

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OpenFlow 1.3
💡 OpenFlow 1.3 introduced standardized support for group tables and meters, allowing advanced traffic management and widely used in production. Earlier versions (1.1 and 1.2) added incremental enhancements but did not fully standardize these features.

</details>

---

### 15. What is the **default behavior** of an OpenFlow switch when it receives a packet that does not match any existing flow entry?

* [ ] Immediately drop the packet
* [ ] Forward it to the OpenFlow controller
* [ ] Broadcast it to all ports
* [ ] Encrypt and queue the packet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Forward it to the OpenFlow controller
💡 This “packet-in” message allows the controller to decide and install a new flow rule.

</details>

---

### 16. What is Mininet primarily used for in SDN research and development?

* [ ] Network monitoring
* [ ] Network emulation and testing
* [ ] Network provisioning
* [ ] Network security analysis

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network emulation and testing
💡 Mininet emulates network topologies using virtual hosts, switches, and links, enabling SDN and network experiments without physical hardware.

</details>

---

### 17. In Mininet, an "emulated network" consists of:

* [ ] Real physical devices
* [ ] Virtual routers
* [ ] Virtual hosts and switches
* [ ] Cloud-based servers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtual hosts and switches
💡 Mininet creates lightweight virtual network elements that behave like real network devices for testing purposes.

</details>

---

### 18. Which programming language is primarily used to script custom topologies and network scenarios in Mininet?

* [ ] Java
* [ ] Python
* [ ] C++
* [ ] Ruby

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Python
💡 Mininet APIs are Python-based, allowing users to define topologies, configure hosts, and interact programmatically.

</details>

---

### 19. What is the main benefit of using Mininet over a physical lab for SDN experiments?

* [ ] Real-time traffic monitoring
* [ ] Eliminates the need for physical network hardware
* [ ] Provides ultra-high-speed connections
* [ ] Primarily used for security testing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Eliminates the need for physical network hardware
💡 Mininet allows testing of SDN applications and topologies virtually, saving cost and setup time.

</details>

---

### 20. Mininet can emulate complex network topologies with many hosts and switches. Which statement about its scalability is true?

* [ ] It only supports small, simple network topologies.
* [ ] It can emulate complex topologies, limited only by the host machine’s CPU and memory.
* [ ] It runs exclusively on Windows OS.
* [ ] It is a closed-source commercial product.

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It can emulate complex topologies, limited only by the host machine’s CPU and memory.
💡 Mininet efficiently emulates hundreds of hosts and switches, but actual scalability depends on the resources of the host machine running the emulation.

</details>

---

### 21. Which controller does Mininet connect to by default if no external controller is specified?

* [ ] OpenFlow Controller
* [ ] Floodlight Controller
* [ ] Ryu Controller
* [ ] OVSController (reference OpenFlow controller)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OVSController (reference OpenFlow controller)
💡 Mininet uses a lightweight reference OpenFlow controller (OVSController) by default. If an external controller is not specified, this allows switches to function for basic testing.

</details>

---

### 22. Which Mininet command is used to start a network emulation session with a specified topology?

* [ ] start_network
* [ ] create_topology
* [ ] mn
* [ ] run_simulation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** mn
💡 The `mn` command is the primary entry point to create and launch Mininet network topologies via CLI.

</details>

---

### 23. What is the purpose of the command `sudo mn -c` in Mininet?

* [ ] To create a new topology
* [ ] To clean up previously created Mininet networks
* [ ] To compile Mininet from source
* [ ] To connect to the network controller

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To clean up previously created Mininet networks
💡 This command ensures that stale network processes and interfaces are removed before a new emulation starts.

</details>

---

### 24. What type of networking technology is typically used to interconnect emulated hosts and switches in Mininet?

* [ ] Ethernet
* [ ] Token Ring
* [ ] ATM (Asynchronous Transfer Mode)
* [ ] Fiber Channel

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ethernet
💡 Mininet emulates Ethernet links between virtual hosts and switches, reflecting standard LAN behavior.

</details>

---

### 25. In Mininet, what does the term "host" refer to?

* [ ] A physical computer on the network
* [ ] A virtual machine running Mininet
* [ ] An endpoint device in the emulated network
* [ ] A network switch

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** An endpoint device in the emulated network
💡 Hosts are emulated endpoints (like PCs or servers) used to test connectivity and network applications.

</details>

---

### 26. You have written a custom Mininet topology script called `mytopo.py`. Which command should you use to launch it from the CLI?

* [ ] sudo mn
* [ ] sudo python mytopo.py
* [ ] mn create
* [ ] run_simulation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** sudo python mytopo.py
💡 Custom topology scripts in Mininet are Python files. Using `sudo python` runs the script with root privileges, which are required to create virtual network interfaces and switches.

</details>

---

### 27. How does Mininet relate to SDN (Software-Defined Networking)?

* [ ] It is an SDN controller
* [ ] It is an SDN switch
* [ ] It is a network emulation platform commonly used for SDN testing
* [ ] It is a routing protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It is a network emulation platform commonly used for SDN testing
💡 Mininet provides a lightweight virtual SDN testbed for evaluating controllers, switches, and applications.

</details>

---

### 28. Which of the following commands is **NOT** a standard Mininet CLI command?

* [ ] pingall
* [ ] addSwitch
* [ ] h1 ifconfig
* [ ] show_topology

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** show_topology
💡 Commands like `pingall`, `addSwitch`, and `h1 ifconfig` are valid; `show_topology` does not exist in standard Mininet CLI.

</details>

---

### 29. You start a Mininet network, but `h1` cannot ping `h2`. What is the **first step** in troubleshooting the emulation?

* [ ] Restart your computer
* [ ] Check if `sudo mn -c` has been run to clean up stale network processes
* [ ] Update the SDN controller software
* [ ] Reinstall Mininet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Check if `sudo mn -c` has been run to clean up stale network processes
💡 Mininet may leave residual virtual network interfaces or processes after a previous session. Running `sudo mn -c` ensures a clean environment before starting a new topology.

</details>

---

### 30. In SDN architecture, what is the role of the **control plane**?

* [ ] Forwarding packets directly between hosts
* [ ] Managing routing, flow rules, and network policies centrally
* [ ] Monitoring physical layer signals
* [ ] Running virtual machines

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Managing routing, flow rules, and network policies centrally
💡 The control plane in SDN separates network intelligence from the forwarding devices and programs network behavior centrally.

</details>

---

### 31. In an SDN deployment, which aspect ensures that critical services remain available and maintain consistent quality of service (QoS) even if some network components fail?

* [ ] Scalability
* [ ] Reliability
* [ ] Consistency
* [ ] Vendor neutrality

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reliability
💡 Reliability ensures networks continue functioning correctly and maintain QoS under failures or high load, enabling resilient service delivery.

</details>

---

### 32. In SDN, consistency ensures that network-wide policies are applied uniformly. Which of the following best illustrates this concept?

* [ ] Ensuring uniform configuration and avoiding access control violations
* [ ] Scaling the network to hundreds of hosts
* [ ] Adding new switches without downtime
* [ ] Encrypting data traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ensuring uniform configuration and avoiding access control violations
💡 Consistency ensures that all devices in the network reflect the intended configuration and policy, preventing misconfigurations, access violations, or conflicting rules.

</details>

---

### 33. A common **virtual networking use case** in SDN is:

* [ ] Running game engines over SDN
* [ ] Virtual Customer Edge (vCE) for remote branch connectivity
* [ ] Encrypting physical cables
* [ ] Manual CLI configuration of each host

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtual Customer Edge (vCE) for remote branch connectivity
💡 vCE enables organizations to connect remote sites using virtualized network functions instead of physical devices.

</details>

---

### 34. Which SDN application allows administrators to specify high-level network goals (like "ensure all web servers can reach the database servers") and automatically enforces them across the network?

* [ ] Firewall CLI scripts
* [ ] OpenDaylight Application Intents
* [ ] Manual VLAN configuration
* [ ] TCP congestion control

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OpenDaylight Application Intents
💡 OpenDaylight Application Intents translate high-level goals into specific flow rules and configurations across network devices, automating policy enforcement.

</details>

---

### 35. What is the purpose of **Service Function Chaining (SFC)** in SDN?

* [ ] To chain physical servers for processing
* [ ] To define an ordered sequence of network services (firewall, DPI, NAT) applied to traffic
* [ ] To replace TCP/IP routing
* [ ] To launch Mininet topologies automatically

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To define an ordered sequence of network services (firewall, DPI, NAT) applied to traffic
💡 SFC allows dynamic insertion of services in the data path without changing the physical topology.

</details>

---

### 36. LISP Flow Mapping in SDN is primarily used to:

* [ ] Encrypt traffic end-to-end
* [ ] Decouple device identity from network location
* [ ] Replace OpenFlow
* [ ] Manage wireless access points

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Decouple device identity from network location
💡 LISP allows flexible routing and mobility by separating endpoint identity from its current network attachment point.

</details>

---

### 37. In OpenDaylight, **MD-SAL (Model-Driven Service Abstraction Layer)** provides:

* [ ] Direct CLI access to switches only
* [ ] A framework for modular applications interacting with the controller’s datastore
* [ ] Only graphical dashboards
* [ ] Encryption for the control plane

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A framework for modular applications interacting with the controller’s datastore
💡 MD-SAL enables applications to access network state, push configurations, and interact with multiple protocols through a consistent API.

</details>

---

### 38. Virtual Tenant Networks (VTNs) in OpenDaylight allow:

* [ ] Multiple tenants to share the same physical infrastructure while isolating their traffic
* [ ] Encrypting Ethernet links
* [ ] Replacing OpenFlow switches
* [ ] Directly programming physical routers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Multiple tenants to share the same physical infrastructure while isolating their traffic
💡 VTNs provide multi-tenant isolation in data centers or cloud networks, enabling separate logical networks over shared hardware.

</details>

---

### 39. The **OpenFlow plugin** in OpenDaylight primarily allows:

* [ ] Controller-to-switch communication using OpenFlow protocol
* [ ] Creating virtual machines
* [ ] Encrypting all network traffic
* [ ] Replacing physical switches with routers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Controller-to-switch communication using OpenFlow protocol
💡 The plugin enables the OpenDaylight controller to manage OpenFlow-enabled switches dynamically, installing flow rules and collecting statistics.

</details>

---

### 40. Which Mininet lab activity is typically used to **verify L2Switch application behavior** in an emulated SDN network?

* [ ] Running `pingall` between hosts
* [ ] Installing OpenDaylight controller
* [ ] Configuring AAA policies
* [ ] Creating Virtual Tenant Networks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Running `pingall` between hosts
💡 L2Switch forwards packets at layer 2. Using `pingall` ensures that all hosts can reach each other, confirming correct flow installation by the controller.

</details>

---

