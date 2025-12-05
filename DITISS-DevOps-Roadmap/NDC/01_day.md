## tcpdump
*tcpdump is a command-line packet capture tool used to sniff, analyze, and troubleshoot network traffic at the packet level*
- Works at Layer 2–4 (captures frames/packets).
- Captures and displays raw network packets in real-time.
- Uses libpcap library (same as Wireshark backend).
- Supports filtering using **BPF (Berkeley Packet Filter) syntax** so you capture only what you need.

tcpdump is used for low-level network troubleshooting, security analysis, and validating traffic flows. It helps identify issues like dropped packets, ARP problems, DNS failures, routing mismatches, and suspicious traffic. It's extremely lightweight and works even on servers without GUI, which makes it ideal for Linux admins, SOC analysts, and DevOps engineers.

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

