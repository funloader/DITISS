## 📡 tcpdump
*tcpdump is a command-line packet capture tool used to sniff, analyze, and troubleshoot network traffic at the packet level*
- Works at Layer 2–4 (captures frames/packets).
- Captures and displays raw network packets in real-time.
- Uses libpcap library (same as Wireshark backend).
- Supports filtering using **BPF (Berkeley Packet Filter) syntax** so you capture only what you need.

🎯 **Why is tcpdump used ?**


tcpdump is used for low-level network troubleshooting, security analysis, and validating traffic flows. It helps identify issues like dropped packets, ARP problems, DNS failures, routing mismatches, and suspicious traffic. It's extremely lightweight and works even on servers without GUI, which makes it ideal for Linux admins, SOC analysts, and DevOps engineers.

### 🧩 What Problems Does tcpdump Solve?

🔧 **Troubleshooting**
- DNS resolution issues
- ARP conflicts
- DHCP failures
- Packet drops / latency
- Firewall or ACL blocking
- Incorrect routing

🛡 **Security Analysis**
- Detect malware C2 traffic
- Identify port scans
- Validate IDS alerts
- Analyze suspicious IPs
- Inspect clear-text protocols (HTTP, FTP, Telnet)

🏗 **System Administration**
- Verify if packets even reach the server
- Check network interfaces for anomalies
- Capture logs before/after configuration changes

- 1st IDS
Why used tcpdump ?
What problem its solves?
How to use it ?
Lab 14 Tcpdump installation, verification and basic usage of tcpdump

⚙️ **How to Use tcpdump**

1️⃣ Install tcpdump (Linux) 
``` 
sudo apt install tcpdump -y
```

2️⃣Verify Installation
```
tcpdump --version
tcpdump -h
```
- Check Available Interfaces ``tcpdump -D``
- Capture packets on a specific interface ``tcpdump -i ens33``
- Capture only 10 packets ``tcpdump -i ens33 -c 10``
- Capture traffic from a specific source IP ``tcpdump src host 192.168.1.10``
- Capture traffic from a specific destination IP ``tcpdump dst host 192.168.1.10``
- Capture traffic from a specific network ``tcpdump net 192.168.1.0/24``
- Capture traffic to a specific port (e.g., 80) ``tcpdump port 80``
- Write packets to a file (PCAP) ``tcpdump -i ens33 -w capture.pcap``
- Read saved capture ``tcpdump -r capture.pcap``
- Verbose output ``tcpdump -vvv -i ens33``
- Capture only ICMP (Ping) ``sudo tcpdump -i ens33 icmp``
- Capture 1 packet and display full hex dump ``tcpdump -xx -c 1``
- Capture 1 packet, show full hex dump, and limit capture size to 6 bytes
``tcpdump -xx -c 1 -s 6``
