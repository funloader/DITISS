> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 20

## **Session 20 : Linux OS**

---

### 1. Which of the following best defines a virtual machine (VM)?

* [ ] A physical computer with additional memory
* [ ] A software-based emulation of a complete computer system
* [ ] A type of malicious software that replicates itself
* [ ] A security application for protecting a host OS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A software-based emulation of a complete computer system
💡 A VM simulates a physical computer, including CPU, memory, storage, and peripherals, allowing multiple OS instances to run on the same physical host.

</details>

---

### 2. Which software is specifically designed to create and manage virtual machines?

* [ ] Photoshop
* [ ] Oracle VirtualBox
* [ ] VLC Media Player
* [ ] Adobe Reader

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Oracle VirtualBox
💡 VirtualBox is a hypervisor that enables users to create, configure, and manage VMs on a host OS.

</details>

---

### 3. In virtualization, which term refers to the software layer that manages guest OS instances on a host?

* [ ] Guest OS
* [ ] Master OS
* [ ] Hypervisor
* [ ] Emulator

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hypervisor
💡 A hypervisor (Type 1 or Type 2) manages multiple VMs, allocating CPU, memory, and I/O resources while isolating guests from each other.

</details>

---

### 4. If a VM is configured to communicate only with its host machine, which network mode is used?

* [ ] NAT
* [ ] Bridged
* [ ] Host-only
* [ ] Public

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Host-only
💡 Host-only networking restricts the VM’s connectivity to the host, providing isolation from external networks while allowing VM-host communication.

</details>

---

### 5. What is the primary role of a hypervisor in virtualization?

* [ ] Scanning for viruses
* [ ] Managing virtual machines and allocating resources
* [ ] Troubleshooting network issues
* [ ] Hosting websites

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Managing virtual machines and allocating resources
💡 Hypervisors provide an abstraction layer that allows multiple VMs to share hardware resources efficiently.

</details>

---

### 6. Which of the following is an example of a Type 1 (bare-metal) hypervisor?

* [ ] VMware Workstation
* [ ] Oracle VirtualBox
* [ ] Hyper-V
* [ ] VMware ESXi

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VMware ESXi
💡 Type 1 hypervisors run directly on physical hardware without requiring a host OS, offering better performance and isolation.

</details>

---

### 7. What is the main purpose of taking a snapshot of a VM?

* [ ] Improve the VM’s performance
* [ ] Encrypt the VM’s storage
* [ ] Revert the VM to a previous state
* [ ] Create a new user account in the VM

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Revert the VM to a previous state
💡 Snapshots capture the VM’s entire state (disk, memory, configuration), enabling rollback after testing or updates.

</details>

---

### 8. In Oracle VirtualBox, what is the default network mode assigned to a new VM?

* [ ] Bridged
* [ ] NAT
* [ ] Host-only
* [ ] Internal

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NAT
💡 NAT (Network Address Translation) allows the VM to access external networks using the host’s IP, without exposing the VM directly.

</details>

---

### 9. Which command in KVM lists all active and inactive virtual machines?

* [ ] listvm
* [ ] virsh list --all
* [ ] kvm-show
* [ ] qemu-display

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** virsh list --all
💡 The `virsh` utility interacts with libvirt to manage VMs. `--all` lists both running and shut-off VMs.

</details>

---

### 10. How does “Bridged Networking” affect a VM’s network connectivity?

* [ ] Isolates it from the host
* [ ] Shares the host’s IP address
* [ ] Assigns it a unique IP on the physical LAN
* [ ] Prevents internet access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Assigns it a unique IP on the physical LAN
💡 Bridged networking connects the VM directly to the physical network, making it appear as an independent machine.

</details>

---

### 11. What is the purpose of the `virt-manager` tool in Linux?

* [ ] Install web servers
* [ ] Manage virtual machines via libvirt
* [ ] Create VPN tunnels
* [ ] Encrypt disks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Manage virtual machines via libvirt
💡 `virt-manager` provides a GUI to create, configure, and monitor VMs using the libvirt API in Linux environments.

</details>

---

### 12. Which virtualization technique allows dynamic sharing of memory among VMs?

* [ ] Dynamic VNet
* [ ] Memory slicing
* [ ] Ballooning
* [ ] Fragmentation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ballooning
💡 Memory ballooning lets the hypervisor reclaim unused memory from one VM and allocate it to another, optimizing resource utilization.

</details>

---

### 13. Which tool is typically used to configure VM networking in VMware vSphere environments?

* [ ] vSphere Client
* [ ] CMD
* [ ] FileZilla
* [ ] Top

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** vSphere Client
💡 The vSphere Client allows administrators to configure VM networks, switches, and adapters in VMware infrastructure.

</details>

---

### 14. In KVM, what is the main function of the `virt-install` command?

* [ ] Monitor VM performance
* [ ] Import existing VM configurations
* [ ] Create a new virtual machine
* [ ] Update hypervisor software

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Create a new virtual machine
💡 `virt-install` is a command-line tool to create VMs, specifying CPU, RAM, disk, and network settings.

</details>

---

### 15. What is the risk of cloning a VM without changing its MAC address?

* [ ] The VM runs faster
* [ ] Network conflicts may occur
* [ ] MAC filtering improves
* [ ] The VM becomes read-only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network conflicts may occur
💡 Duplicate MAC addresses in the same network can cause IP conflicts and disrupted communication.

</details>

---

### 16. What distinguishes full virtualization from para-virtualization?

* [ ] Full virtualization requires a modified guest OS
* [ ] Para-virtualization is faster by bypassing some hardware emulation
* [ ] Full virtualization only runs on VM-aware hardware
* [ ] Para-virtualization does not require a hypervisor

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Para-virtualization is faster by bypassing some hardware emulation
💡 Para-virtualization modifies the guest OS to interact directly with the hypervisor, reducing overhead.

</details>

---

### 17. Which VMware virtual network type allows VMs to communicate exclusively among themselves?

* [ ] NAT
* [ ] Bridged
* [ ] Host-only
* [ ] Internal

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Internal
💡 Internal networks in VMware isolate VMs from the host and external networks while allowing inter-VM communication.

</details>

---

### 18. Which Linux command creates a new virtual bridge for VM networking?

* [ ] brctl addbr
* [ ] netctl new
* [ ] ipconfig create
* [ ] ifconfig makebridge

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** brctl addbr
💡 `brctl addbr <bridge_name>` creates a software bridge in Linux to connect VMs to physical or virtual networks.

</details>

---

### 19. In virtualization, what is a vNIC?

* [ ] Physical network card
* [ ] Virtual network interface card
* [ ] A special filesystem
* [ ] Cloud-hosted disk

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtual network interface card
💡 A vNIC emulates a network interface inside a VM, enabling network communication similar to a physical NIC.

</details>

---

### 20. How is bandwidth typically controlled in VM networks?

* [ ] Firewalls
* [ ] Rate limiting or QoS
* [ ] BIOS settings
* [ ] Port forwarding

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Rate limiting or QoS
💡 Network bandwidth for VMs can be managed using Quality of Service policies or rate limiting on virtual switches.

</details>

---

### 21. In VMware, what does “vSwitch” refer to?

* [ ] A virtual router
* [ ] A physical network device
* [ ] A virtual switch enabling VM communication
* [ ] A disk image management tool

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A virtual switch enabling VM communication
💡 A vSwitch operates at Layer 2 in the virtual network, connecting VMs to each other or to physical NICs.

</details>

---

### 22. What is the primary advantage of SR-IOV (Single Root I/O Virtualization) in VM networking?

* [ ] Encrypts network packets between VMs
* [ ] Allows VMs to bypass the hypervisor for direct network I/O
* [ ] Automatically installs virtual software routers
* [ ] Manages NAT tables for multiple VMs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Allows VMs to bypass the hypervisor for direct network I/O
💡 SR-IOV creates multiple virtual functions (VFs) of a single physical NIC, enabling high-performance, low-latency network access for VMs without hypervisor overhead.

</details>

---

### 23. In a libvirt XML configuration, which section defines VM networking settings such as vNIC type and source bridge?

* [ ] `<os>`
* [ ] `<devices>`
* [ ] `<memory>`
* [ ] `<features>`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `<devices>`
💡 The `<devices>` section in libvirt XML lists all hardware devices, including `<interface>` elements that configure VM network interfaces and connect them to bridges, NAT, or VLANs.

</details>

---

### 24. What is the potential effect of MAC address spoofing in a virtual machine environment?

* [ ] Enhanced network security
* [ ] Improved DNS resolution
* [ ] IP duplication errors and possible network conflicts
* [ ] Automatic disk encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IP duplication errors and possible network conflicts
💡 Spoofing a MAC address can cause two devices to have the same MAC on the network, leading to collisions, connectivity issues, or access bypass.

</details>

---

### 25. In KVM, which default networking mode uses the `virbr0` bridge for VM connectivity?

* [ ] Bridged
* [ ] NAT
* [ ] Routed
* [ ] Host-only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NAT
💡 By default, libvirt creates the `virbr0` bridge for NAT networking, allowing VMs to access external networks while isolating them from inbound connections.

</details>

---

### 26. What is a possible consequence of not assigning static MAC addresses to VMs in a clustered environment?

* [ ] Faster boot times
* [ ] IP address conflicts among VMs
* [ ] Higher throughput for network-intensive applications
* [ ] Port forwarding failures on the host

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IP address conflicts among VMs
💡 Dynamic MAC allocation can change on reboot, causing DHCP servers to assign duplicate IPs, especially in clusters with multiple VMs on the same network.

</details>

---

### 27. How do VLANs improve virtual machine network configurations?

* [ ] Increase virtual RAM
* [ ] Isolate network segments on a shared physical switch
* [ ] Automatically clone VMs for redundancy
* [ ] Encrypt data in transit

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Isolate network segments on a shared physical switch
💡 VLANs allow multiple VMs to share the same physical network interface while logically separating traffic, enhancing security and management.

</details>

---

### 28. For Linux VMs, which type of virtual NIC provides the best performance?

* [ ] rtl8139
* [ ] e1000
* [ ] virtio
* [ ] ne2000

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** virtio
💡 Virtio is a paravirtualized driver that minimizes emulation overhead, providing high-performance networking and disk I/O in Linux guests.

</details>

---

### 29. In a KVM setup, what is the correct procedure to attach a VM to an existing Linux bridge?

* [ ] Modify the `brctl` configuration file
* [ ] Edit the VM’s XML configuration and restart libvirt
* [ ] Use iptables rules to redirect traffic
* [ ] Reinstall the VM with a new bridge

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Edit the VM’s XML configuration and restart libvirt
💡 Attaching a VM to a bridge requires specifying the bridge name in the `<interface>` section of the XML configuration and reloading the VM or libvirt service.

</details>

---

### 30. Which technology allows creating overlay networks for VMs across multiple physical hosts?

* [ ] iptables
* [ ] Docker
* [ ] VXLAN
* [ ] Nmap

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VXLAN
💡 VXLAN encapsulates Layer 2 frames within Layer 3 packets, allowing VMs on different hosts to appear on the same virtual LAN, supporting scalable multi-host VM networks.

</details>

---
