> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 012

## **Session 12 : Linux OS**

---

### 1. A Linux system translates human-readable domain names into IP addresses using a hierarchical naming mechanism. What does DNS stand for in this context?

* [ ] Dynamic Network Service
* [ ] Domain Network Structure
* [ ] Data Name Service
* [ ] Domain Name System

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Domain Name System
💡 DNS is a distributed, hierarchical naming system that resolves domain names into IP addresses as defined in RFC 1034/1035.

</details>

---

### 2. A system administrator wants to statically map internal hostnames to IP addresses without querying a DNS server. Which Linux file is used for this purpose?

* [ ] /etc/nsswitch.conf
* [ ] /etc/hostname
* [ ] /etc/hosts
* [ ] /etc/resolv.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/hosts
💡 The `/etc/hosts` file provides static hostname-to-IP mappings and is consulted before DNS depending on `/etc/nsswitch.conf`.

</details>

---

### 3. DNS primarily uses which well-known port for query and response communication?

* [ ] 25
* [ ] 53
* [ ] 80
* [ ] 443

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 53
💡 DNS uses UDP port 53 for standard queries and TCP port 53 for zone transfers and large responses.

</details>

---

### 4. Which command-line utility allows interactive querying of DNS servers and supports both forward and reverse lookups?

* [ ] ifconfig
* [ ] digg
* [ ] netstat
* [ ] nslookup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** nslookup
💡 `nslookup` is a legacy but widely used DNS query tool for interactive lookups.

</details>

---

### 5. Which widely adopted DNS server package is used to deploy authoritative and recursive DNS services on Linux systems?

* [ ] dnsutils
* [ ] netdns
* [ ] resolv
* [ ] bind

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** bind
💡 BIND (Berkeley Internet Name Domain) is the most commonly deployed DNS server software globally.

</details>

---

### 6. A Linux system receives its DNS resolver configuration dynamically via DHCP. Which file reflects the DNS server IP addresses currently used by the system?

* [ ] /etc/named.conf
* [ ] /etc/hosts
* [ ] /etc/dhcpd.conf
* [ ] /etc/resolv.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/resolv.conf
💡 `/etc/resolv.conf` specifies resolver settings including `nameserver` entries used for DNS queries.

</details>

---

### 7. Which DNS record type directly maps a domain name to an IPv4 address?

* [ ] PTR
* [ ] MX
* [ ] CNAME
* [ ] A

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A
💡 An **A record** maps a hostname to an IPv4 address, as defined in DNS standards.

</details>

---

## 🔸 Intermediate Level (Configuration & Operations – 14 Questions)

---

### 8. You are configuring a BIND DNS server on a Linux system. Which file serves as the primary configuration file for defining zones and global options?

* [ ] /etc/dns.conf
* [ ] /etc/bind.conf
* [ ] /etc/named.conf
* [ ] /etc/bind/named.zone

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/named.conf
💡 `named.conf` is the central configuration file used by BIND to define zones, ACLs, and options.

</details>

---

### 9. On a system using systemd, which command correctly restarts the BIND DNS service after configuration changes?

* [ ] service bind restart
* [ ] named restart
* [ ] systemctl restart dnsmasq
* [ ] systemctl restart named

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl restart named
💡 The BIND service runs as `named` under systemd-based Linux distributions.

</details>

---

### 10. Which directive is used within `named.conf` to define a DNS zone and its properties?

* [ ] domain
* [ ] forward
* [ ] include
* [ ] zone

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** zone
💡 The `zone` directive specifies zone name, type, and associated zone file.

</details>

---

### 11. In a DNS zone file, which record specifies the mail server responsible for handling emails for a domain?

* [ ] NS
* [ ] SOA
* [ ] A
* [ ] MX

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MX
💡 MX (Mail Exchange) records define mail servers and their priority for a domain.

</details>

---

### 12. Which DNS utility provides detailed query responses, supports advanced options, and is preferred for troubleshooting?

* [ ] traceroute
* [ ] whois
* [ ] ping
* [ ] dig

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** dig
💡 `dig` (Domain Information Groper) offers granular control and verbose DNS query output.

</details>

---

### 13. Which DNS record type enables reverse DNS lookups from IP address to hostname?

* [ ] A
* [ ] CNAME
* [ ] TXT
* [ ] PTR

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PTR
💡 PTR records are used within reverse lookup zones (in-addr.arpa).

</details>

---

### 14. What is the primary purpose of the `named-checkconf` utility?

* [ ] Restart the DNS service
* [ ] Validate `named.conf` syntax
* [ ] Resolve domain names
* [ ] Test zone file integrity

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Validate `named.conf` syntax
💡 `named-checkconf` verifies configuration correctness without starting the service.

</details>

---

### 15. What does the TTL field in a DNS resource record control?

* [ ] Maximum packet size
* [ ] Time before record expiration in cache
* [ ] Query timeout value
* [ ] Zone refresh interval

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Time before record expiration in cache
💡 TTL (Time To Live) defines how long a record can be cached by resolvers.

</details>

---

### 16. Which option in BIND specifies the working directory where zone files are stored?

* [ ] chroot
* [ ] rootdir
* [ ] directory
* [ ] path

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** directory
💡 The `directory` option sets the base path for relative zone file locations.

</details>

---

### 17. In BIND configuration, the `forwarders` directive is primarily used to:

* [ ] Host authoritative zones
* [ ] Redirect unresolved queries to upstream DNS servers
* [ ] Create DNS aliases
* [ ] Enable recursion

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Redirect unresolved queries to upstream DNS servers
💡 Forwarders send queries to external resolvers like ISP or public DNS servers.

</details>

---

### 18. What is the primary role of the SOA record in a DNS zone?

* [ ] Define mail routing
* [ ] Identify authoritative name servers
* [ ] Store domain aliases
* [ ] Provide zone authority and synchronization parameters

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provide zone authority and synchronization parameters
💡 SOA contains serial number, refresh, retry, and expiry values for zone transfers.

</details>

---

### 19. What function does an NS record perform in DNS?

* [ ] Maps aliases to canonical names
* [ ] Identifies authoritative name servers for a domain
* [ ] Specifies mail servers
* [ ] Defines TTL values

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Identifies authoritative name servers for a domain
💡 NS records delegate authority to specific DNS servers.

</details>

---

### 20. What is the purpose of a CNAME record?

* [ ] Maps hostname to IP
* [ ] Defines an email relay
* [ ] Maps an alias to a canonical domain name
* [ ] Creates a reverse lookup entry

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Maps an alias to a canonical domain name
💡 CNAME records allow multiple domain aliases to point to a single canonical name.

</details>

---

### 21. Which log location commonly records BIND service errors on modern Linux systems?

* [ ] /etc/named.log
* [ ] /var/bind/errors
* [ ] /var/log/named/named.log
* [ ] /var/log/syslog

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /var/log/syslog
💡 BIND logs are typically routed via syslog unless explicitly configured otherwise.

</details>

---

## 🔺 Difficult Level (Security, Architecture & Advanced Concepts – 9 Questions)

---

### 22. Which command is specifically used to validate the syntax and integrity of a DNS zone file?

* [ ] dig-checkzone
* [ ] zoneverify
* [ ] ns-check
* [ ] named-checkzone

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** named-checkzone
💡 `named-checkzone` validates zone file format and records.

</details>

---

### 23. What is the correct reverse DNS zone name for the network 192.168.1.0/24?

* [ ] 192.168.1.zone
* [ ] rev.1.168.192.in-arpa
* [ ] 192.168.1.reverse
* [ ] 1.168.192.in-addr.arpa

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1.168.192.in-addr.arpa
💡 Reverse zones invert octets and use the `in-addr.arpa` domain.

</details>

---

### 24. How does DNSSEC primarily enhance DNS security?

* [ ] Encrypts DNS payloads
* [ ] Improves query performance
* [ ] Authenticates DNS responses using cryptographic signatures
* [ ] Enables traffic load balancing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticates DNS responses using cryptographic signatures
💡 DNSSEC ensures integrity and authenticity, preventing cache poisoning attacks.

</details>

---

### 25. What is the function of a `view` statement in BIND?

* [ ] Defines MX records
* [ ] Lists zone sizes
* [ ] Controls zone transfers
* [ ] Provides different DNS responses based on client source

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provides different DNS responses based on client source
💡 Views enable split-DNS implementations (internal vs external clients).

</details>

---

### 26. What role does `/etc/nsswitch.conf` play in hostname resolution?

* [ ] Stores DNS server IPs
* [ ] Contains authentication secrets
* [ ] Specifies the order of name resolution methods
* [ ] Defines authoritative zones

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Specifies the order of name resolution methods
💡 It controls whether lookups use files, DNS, LDAP, etc.

</details>

---

### 27. Which DNS server type maintains the original, writable copy of a zone file?

* [ ] Forwarding
* [ ] Secondary (Slave)
* [ ] Caching
* [ ] Primary (Master)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Primary (Master)
💡 Only the primary server hosts authoritative and editable zone files.

</details>

---

### 28. What is the impact of failing to increment the serial number after modifying a zone file?

* [ ] All zones reload automatically
* [ ] Secondary servers will not receive updates
* [ ] DNS queries will fail entirely
* [ ] No operational impact

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Secondary servers will not receive updates
💡 Zone transfers depend on serial number changes to detect updates.

</details>

---

### 29. What is the primary use of dnsmasq in Linux environments?

* [ ] DNS packet debugging
* [ ] DNS over VPN tunneling
* [ ] DNS penetration testing
* [ ] Lightweight DNS and DHCP services

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Lightweight DNS and DHCP services
💡 dnsmasq is commonly used in small networks, VMs, and containers.

</details>

---

### 30. Which DNS misconfiguration presents a significant security risk and can be abused for amplification attacks?

* [ ] Excessive A records
* [ ] High TTL values
* [ ] Use of private IP addresses
* [ ] Open recursive DNS server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Open recursive DNS server
💡 Open recursion enables DNS amplification and reflection DDoS attacks.

</details>

---

## **Session 13 : Linux OS**

---

### 1. In a Linux-based enterprise network, NFS is primarily used to enable which functionality?

* [ ] Remote command execution across nodes
* [ ] Centralized authentication for Linux systems
* [ ] File sharing across networked UNIX/Linux systems
* [ ] Secure file transfer over encrypted channels

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** File sharing across networked UNIX/Linux systems
💡 NFS (Network File System) allows files to be shared and accessed transparently over a network as if they were local files.

</details>

---

### 2. Which TCP/UDP port is officially assigned to NFS services in modern Linux systems?

* [ ] 21
* [ ] 22
* [ ] 2049
* [ ] 111

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 2049
💡 Port 2049 is the default port used by NFS for client-server communication, especially in NFSv4.

</details>

---

### 3. Which FTP daemon is commonly deployed on Linux servers due to its security-focused design?

* [ ] apache
* [ ] proftpd
* [ ] samba
* [ ] bind

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** proftpd
💡 ProFTPD is a widely used FTP server offering flexible configuration and improved security controls.

</details>

---

### 4. FTP operates primarily at which layer of the OSI model?

* [ ] Transport layer
* [ ] Network layer
* [ ] Application layer
* [ ] Session layer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Application layer
💡 FTP is an application-layer protocol designed for file transfer between systems.

</details>

---

### 5. An administrator wants to install the NFS server on a Debian-based Linux distribution. Which command is appropriate?

* [ ] yum install nfs-utils
* [ ] dnf install nfs-utils
* [ ] apt install nfs-kernel-server
* [ ] zypper install nfs-server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** apt install nfs-kernel-server
💡 Debian and Ubuntu systems use APT, and `nfs-kernel-server` provides NFS server functionality.

</details>

---

### 6. Which configuration file explicitly defines which directories are shared via NFS and with whom?

* [ ] /etc/nfs.conf
* [ ] /etc/exports
* [ ] /etc/nfsd.conf
* [ ] /etc/share.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/exports
💡 `/etc/exports` controls NFS share definitions, access permissions, and client restrictions.

</details>

---

### 7. By convention, which directory is used as the default FTP document root on many Linux distributions?

* [ ] /srv/ftp
* [ ] /var/ftp
* [ ] /ftp/files
* [ ] /home/ftp

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /srv/ftp
💡 The Filesystem Hierarchy Standard (FHS) recommends `/srv/ftp` for FTP-served data.

</details>

---

### 8. On a systemd-based Linux system, which command correctly starts the NFS server service?

* [ ] service nfs start
* [ ] systemctl start nfs-server
* [ ] systemctl start nfsd
* [ ] nfs-server start

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl start nfs-server
💡 `nfs-server` is the standard systemd service name for NFS servers.

</details>

---

### 9. What is the primary role of the `/etc/exports` file in NFS administration?

* [ ] Listing authenticated FTP users
* [ ] Configuring shared directories and access rules
* [ ] Defining NFS mount points on clients
* [ ] Managing disk quotas

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configuring shared directories and access rules
💡 It specifies exported directories, permitted clients, and access options.

</details>

---

### 10. After modifying `/etc/exports`, which command ensures changes are applied without rebooting?

* [ ] exportfs -a
* [ ] systemctl restart nfs
* [ ] nfs-reload
* [ ] exportsync

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** exportfs -a
💡 This command re-exports all directories defined in `/etc/exports`.

</details>

---

### 11. In an NFS export entry, what does the `rw` option specify?

* [ ] Remote writable only
* [ ] Read-only access
* [ ] Read-write access
* [ ] Recursive write permissions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Read-write access
💡 `rw` allows clients both read and write permissions on the exported directory.

</details>

---

### 12. Which background service is essential for RPC-based NFS operations to function correctly?

* [ ] rpcbind
* [ ] crond
* [ ] apache2
* [ ] telnet

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** rpcbind
💡 rpcbind maps RPC program numbers to network ports and is required for NFS.

</details>

---

### 13. Which file is the primary configuration file for the vsftpd FTP server?

* [ ] /etc/ftp.conf
* [ ] /etc/vsftpd/vsftpd.conf
* [ ] /etc/vsftpd.conf
* [ ] /etc/ftpd.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/vsftpd/vsftpd.conf
💡 This file governs authentication, access controls, logging, and security settings.

</details>

---

### 14. How does an administrator enable anonymous FTP access in vsftpd?

* [ ] Set anonymous_enable=YES
* [ ] Set anon_access=true
* [ ] Allow /etc/anon
* [ ] Use ftp_anon=1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Set anonymous_enable=YES
💡 This directive explicitly enables anonymous login support.

</details>

---

### 15. What is the function of the `exportfs -r` command?

* [ ] Remove an existing NFS export
* [ ] Restart the FTP service
* [ ] Re-export all NFS shares
* [ ] Reload firewall rules

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Re-export all NFS shares
💡 It refreshes all exports without stopping the NFS service.

</details>

---

### 16. Which port is used by FTP for control (command) communication?

* [ ] 20
* [ ] 21
* [ ] 22
* [ ] 23

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 21
💡 Port 21 handles command and authentication traffic in FTP.

</details>

---

### 17. Which FTP variant transmits credentials and data in clear text?

* [ ] FTPS
* [ ] SFTP
* [ ] Plain FTP
* [ ] HTTPS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Plain FTP
💡 Plain FTP does not provide encryption, making it insecure on untrusted networks.

</details>

---

### 18. What is the effect of enabling `no_root_squash` in an NFS export?

* [ ] Root access is completely blocked
* [ ] Root user is mapped to nobody
* [ ] Root user retains full privileges
* [ ] Root access becomes read-only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Root user retains full privileges
💡 This option disables UID mapping, posing serious security risks.

</details>

---

### 19. Which utility displays NFS exports available from a remote server?

* [ ] netstat
* [ ] showmount
* [ ] rpcinfo
* [ ] mountinfo

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** showmount
💡 `showmount -e` lists directories exported by an NFS server.

</details>

---

### 20. Which command mounts an NFS share on a Linux client?

* [ ] nfs -mount
* [ ] mount -t nfs
* [ ] nfsclient
* [ ] mountfs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** mount -t nfs
💡 Specifies NFS as the filesystem type during mount.

</details>

---

### 21. Which vsftpd directive confines local users to their home directories?

* [ ] local_root
* [ ] chroot_local_user
* [ ] restrict_user
* [ ] ftp_home_dir

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** chroot_local_user
💡 Prevents users from navigating outside their home directories.

</details>

### 22. Which `/etc/exports` entry correctly restricts access to a specific subnet?

* [ ] subnet_access=on
* [ ] allow=192.168.1.0/24
* [ ] /share 192.168.1.0/24(rw)
* [ ] export_to=192.168.1.0

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /share 192.168.1.0/24(rw)
💡 NFS restricts access by specifying client networks directly in export entries.

</details>

---

### 23. Why is `no_root_squash` considered a major security risk?

* [ ] Root access becomes read-only
* [ ] Root gains unrestricted access to server files
* [ ] Root access is disabled
* [ ] Root UID is anonymized

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Root gains unrestricted access to server files
💡 This can allow full compromise of shared data if a client is breached.

</details>

---

### 24. Which command lists all NFS shares exported by the local server?

* [ ] showmount -e
* [ ] listnfs
* [ ] exports -l
* [ ] mountlist

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** showmount -e
💡 Displays exported file systems and permitted clients.

</details>

---

### 25. Which mechanism secures FTP traffic using SSL/TLS encryption?

* [ ] openssl
* [ ] FTPS
* [ ] tlsftp
* [ ] sftp

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** FTPS
💡 FTPS is FTP over SSL/TLS, providing encrypted authentication and data transfer.

</details>

---

### 26. What fundamentally differentiates SFTP from traditional FTP?

* [ ] FTP is faster
* [ ] SFTP operates over SSH and is encrypted
* [ ] SFTP requires a graphical interface
* [ ] FTP offers better encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SFTP operates over SSH and is encrypted
💡 SFTP leverages SSH for secure file transfer.

</details>

---

### 27. Which kernel component is mandatory for NFS client functionality?

* [ ] nfs_client
* [ ] nfsd
* [ ] nfs
* [ ] nfsv4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** nfs
💡 The `nfs` module enables client-side NFS operations.

</details>

---

### 28. Which file prevents specific users from logging in via FTP in vsftpd?

* [ ] /etc/ftpaccess
* [ ] /etc/anonftp.conf
* [ ] /etc/vsftpd/ftpusers
* [ ] /etc/vsftpd/anon.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/vsftpd/ftpusers
💡 Users listed here are explicitly denied FTP access.

</details>

---

### 29. In secure FTP configurations, what is the purpose of a match-style conditional block?

* [ ] Apply settings globally
* [ ] Apply rules based on user or IP
* [ ] Limit bandwidth usage
* [ ] Encrypt FTP sessions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Apply rules based on user or IP
💡 Conditional rules allow granular access control.

</details>

---

### 30. How can detailed FTP activity logging be enabled in vsftpd?

* [ ] Set log_enable=YES
* [ ] Create /var/log/ftp
* [ ] Use ftp_log=true
* [ ] Enable system journaling

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Set log_enable=YES
💡 Enables transfer and session logging for audit and forensic purposes.

</details>

---
