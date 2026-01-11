> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 14

## **Session 14 : Linux OS**

---

### 1. In an enterprise Linux environment, what is the **primary role of a Samba server** when integrated with Windows clients?

* [ ] Hosting web applications over HTTP/HTTPS
* [ ] Providing cross-platform file and printer sharing using SMB/CIFS
* [ ] Acting as a stateful firewall between network segments
* [ ] Managing email delivery using SMTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Providing cross-platform file and printer sharing using SMB/CIFS
💡 Samba implements the SMB/CIFS protocol, enabling Linux systems to interoperate seamlessly with Windows-based file and print services.

</details>

---

### 2. An administrator wants to install Samba on an **Ubuntu Server 22.04** system. Which command correctly installs the package using the native package manager?

* [ ] yum install samba
* [ ] install samba-server
* [ ] apt install samba
* [ ] get samba

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** apt install samba
💡 Debian-based systems such as Ubuntu use APT for package management; `apt install samba` installs both client and server components.

</details>

---

### 3. Which configuration file serves as the **central configuration repository** for Samba services on most Linux distributions?

* [ ] /etc/samba.conf
* [ ] /etc/smb.conf
* [ ] /usr/samba/smb.conf
* [ ] /etc/samba/settings.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/smb.conf
💡 The `smb.conf` file defines global settings, shares, security modes, and access controls for Samba.

</details>

---

### 4. DHCP is a core network service used in enterprise networks. What does **DHCP** stand for?

* [ ] Dynamic Host Configuration Protocol
* [ ] Data Host Control Protocol
* [ ] Direct Host Communication Protocol
* [ ] Dynamic Host Channel Protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Dynamic Host Configuration Protocol
💡 DHCP automates IP address allocation and related network parameters for hosts.

</details>

---

### 5. A Linux system attempts to resolve `www.cdac.in` to an IP address. Which protocol is primarily responsible for this operation?

* [ ] FTP
* [ ] SSH
* [ ] DNS
* [ ] SMTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DNS
💡 DNS resolves human-readable domain names into machine-usable IP addresses.

</details>

---

### 6. On a Linux-based DHCP server using ISC DHCP, which file typically contains the **server-side DHCP configuration**?

* [ ] /etc/network/interfaces
* [ ] /etc/dhcp/dhcpd.conf
* [ ] /etc/sysconfig/network-scripts
* [ ] /etc/dhcp.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/dhcp/dhcpd.conf
💡 This file defines subnets, IP ranges, options, and lease behavior for the DHCP server.

</details>

---

### 7. Which **well-known port** does DNS primarily use for standard query and response operations?

* [ ] 22
* [ ] 53
* [ ] 67
* [ ] 80

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 53
💡 DNS uses UDP port 53 for most queries and TCP port 53 for zone transfers and large responses.

</details>

---

### 8. In `smb.conf`, the `workgroup` parameter primarily specifies:

* [ ] The authentication backend
* [ ] The Windows workgroup or domain name
* [ ] The network interface used by Samba
* [ ] The encrypted Samba password

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The Windows workgroup or domain name
💡 This ensures Samba clients appear in the correct Windows network browsing context.

</details>

---

### 9. On a system using **systemd**, which command correctly restarts the Samba service responsible for file sharing?

* [ ] service samba restart
* [ ] restart samba
* [ ] systemctl restart smb
* [ ] init.d smb restart

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl restart smb
💡 Modern distributions manage Samba services (`smb`, `nmb`) via systemd.

</details>

---

### 10. In an ISC DHCP configuration, what does the `range` directive define?

* [ ] Duration of IP leases
* [ ] DNS name boundaries
* [ ] Pool of assignable IP addresses
* [ ] Default gateway

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Pool of assignable IP addresses
💡 The range specifies the IP addresses that can be dynamically leased to clients.

</details>

---

### 11. A network administrator wants to manually query a DNS server from the CLI. Which tool is most appropriate?

* [ ] nslookup
* [ ] ping
* [ ] ftp
* [ ] traceroute

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** nslookup
💡 `nslookup` directly queries DNS servers and displays resolution results.

</details>

---

### 12. In DHCP terminology, what does a **lease** represent?

* [ ] Permanent IP binding
* [ ] Temporary allocation of an IP address
* [ ] DNS zone record
* [ ] Network interface alias

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Temporary allocation of an IP address
💡 DHCP leases are time-bound assignments that must be renewed.

</details>

---

### 13. Which Samba utility is used to **create or manage Samba-specific user credentials**?

* [ ] smbpasswd
* [ ] smbd
* [ ] samba-useradd
* [ ] useradd-smb

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** smbpasswd
💡 Samba maintains its own authentication database separate from system users.

</details>

---

### 14. The `hosts allow` directive in `smb.conf` is primarily used to:

* [ ] Configure DNS permissions
* [ ] Control DHCP scope access
* [ ] Restrict access to Samba shares based on IP or subnet
* [ ] Define Samba listening ports

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Restrict access to Samba shares based on IP or subnet
💡 This directive enforces network-level access control.

</details>

---

### 15. How can an administrator confirm that a DHCP server has successfully issued IP leases?

* [ ] systemctl status dhcp
* [ ] cat /var/lib/dhcp/dhcpd.leases
* [ ] dhcp show
* [ ] show dhcp-leases

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** cat /var/lib/dhcp/dhcpd.leases
💡 This file records all active and expired DHCP leases.

</details>

---

### 16. Which DNS record type maps a **hostname directly to an IPv4 address**?

* [ ] MX
* [ ] A
* [ ] CNAME
* [ ] PTR

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A
💡 An A record resolves a domain name to an IPv4 address.

</details>

---

### 17. What is the purpose of the `option domain-name-servers` directive in DHCP?

* [ ] Configure Samba name resolution
* [ ] Assign DNS server IPs to clients
* [ ] Set client hostnames
* [ ] Enable NetBIOS over TCP/IP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Assign DNS server IPs to clients
💡 This ensures clients know which DNS servers to query.

</details>

---

### 18. On a BIND-based DNS server, which command reloads configuration **without stopping the service**?

* [ ] named-reload
* [ ] systemctl reload bind9
* [ ] service named restart
* [ ] reload-dns

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl reload bind9
💡 Reloading applies configuration changes while minimizing service disruption.

</details>

---

### 19. How can available Samba shares on a local server be enumerated from the CLI?

* [ ] show samba
* [ ] smbclient -L localhost
* [ ] listshares samba
* [ ] ls /samba

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** smbclient -L localhost
💡 This command lists exported shares using SMB protocol negotiation.

</details>

---

### 20. Which file statically maps hostnames to IP addresses on a Linux system?

* [ ] /etc/hostname
* [ ] /etc/networks
* [ ] /etc/hosts
* [ ] /etc/named.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/hosts
💡 Local name resolution occurs before querying DNS.

</details>

---

### 21. Which command-line utility is widely used to **analyze DNS propagation and records**?

* [ ] dig
* [ ] ipconfig
* [ ] nsstatus
* [ ] dnslookup

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** dig
💡 `dig` provides detailed DNS query diagnostics and responses.

</details>

---

### 22. What is the primary purpose of a **reverse DNS zone**?

* [ ] Map domain names to IP addresses
* [ ] Map IP addresses back to domain names
* [ ] Block DNS amplification attacks
* [ ] Validate DNSSEC signatures

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Map IP addresses back to domain names
💡 Reverse zones use PTR records for IP-to-hostname resolution.

</details>

---

### 23. In a Linux DNS server environment, what is the role of the `named` daemon?

* [ ] Samba authentication handler
* [ ] DHCP lease manager
* [ ] Core DNS service daemon for BIND
* [ ] FTP connection controller

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Core DNS service daemon for BIND
💡 `named` processes DNS queries and manages zones.

</details>

---

### 24. Which file is commonly used to define **local DNS zones** in BIND on Debian-based systems?

* [ ] /etc/bind/named.conf.local
* [ ] /etc/bind/zone.conf
* [ ] /etc/bind/dns.conf
* [ ] /var/named/dns.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/bind/named.conf.local
💡 Local authoritative zones are declared here.

</details>

---

### 25. In Samba, what does `security = user` enforce?

* [ ] Root-only access
* [ ] Unrestricted access
* [ ] Individual user authentication
* [ ] Anonymous guest access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Individual user authentication
💡 Each client must authenticate with valid credentials.

</details>

---

### 26. A Samba server needs to authenticate users against an **Active Directory domain**. Which setting enables this?

* [ ] security = ads
* [ ] workgroup = Domain
* [ ] Enable SMBv2
* [ ] Default smb.conf only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** security = ads
💡 ADS mode integrates Samba with Kerberos and AD services.

</details>

---

### 27. Which DNS record type is used to **route email to mail servers**?

* [ ] CNAME
* [ ] PTR
* [ ] MX
* [ ] A

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MX
💡 Mail Exchange records define email routing priority.

</details>

---

### 28. In ISC DHCP, what does the `authoritative` directive indicate?

* [ ] Primary DNS server
* [ ] This server is the official DHCP server for the subnet
* [ ] Root privileges are mandatory
* [ ] Lease database reset is enabled

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** This server is the official DHCP server for the subnet
💡 It forces clients to accept this server’s configuration.

</details>

---

### 29. Which file is most directly used to analyze **Samba daemon activity and errors**?

* [ ] /var/log/samba/log.smbd
* [ ] /etc/samba/logs
* [ ] /var/log/messages
* [ ] journalctl samba

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /var/log/samba/log.smbd
💡 This log captures service-level events and errors for smbd.

</details>

---

### 30. Which tool provides real-time insight into **current Samba connections and locked files**?

* [ ] smbstatus
* [ ] ping
* [ ] nmap
* [ ] mount

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** smbstatus
💡 `smbstatus` is essential for troubleshooting active SMB sessions.

</details>

---

## **Session 15 : Linux OS**


---

### 1. In a Red Hat–based Linux system, an administrator wants to modify the global Apache configuration affecting all virtual hosts. Which is the most appropriate default configuration file to edit?

* [ ] /etc/apache2/httpd.conf
* [ ] /etc/apache2/apache.conf
* [ ] /etc/http/httpd.conf
* [ ] /etc/httpd/httpd.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/httpd/httpd.conf
💡 On RHEL/CentOS systems, `/etc/httpd/httpd.conf` is the primary Apache configuration file, unlike Debian-based systems which use `/etc/apache2/`.

</details>

---

### 2. A system administrator is troubleshooting an Apache service failure on a systemd-based Ubuntu server. Which command correctly starts the Apache service?

* [ ] apachectl start
* [ ] service apache start
* [ ] systemctl start apache2
* [ ] start apache2

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl start apache2
💡 Ubuntu uses systemd with the service name `apache2`; `systemctl` is the correct modern service manager.

</details>

---

### 3. A security audit report indicates that a web application is accessible over plain HTTP. Which default port confirms this finding?

* [ ] 80
* [ ] 8080
* [ ] 443
* [ ] 21

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 80
💡 Port 80 is the IANA-assigned default port for HTTP traffic without encryption.

</details>

---

### 4. An Apache server is incorrectly serving files from `/tmp` instead of the intended web directory. Which directive likely needs correction?

* [ ] ServerName
* [ ] ErrorLog
* [ ] DocumentRoot
* [ ] Listen

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DocumentRoot
💡 `DocumentRoot` defines the base directory from which Apache serves web content.

</details>

---

### 5. While investigating a suspected web attack, which Apache log file is most useful to analyze client request patterns?

* [ ] apache.log
* [ ] server.log
* [ ] access.log
* [ ] webserver.log

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** access.log
💡 `access.log` records all incoming HTTP requests, making it crucial for forensic and traffic analysis.

</details>

---

### 6. To harden a website with HTTPS, which Apache module must be enabled?

* [ ] mod_proxy
* [ ] mod_ssl
* [ ] mod_rewrite
* [ ] mod_secure

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** mod_ssl
💡 `mod_ssl` provides SSL/TLS support in Apache for secure HTTPS communication.

</details>

---

### 7. On a Debian-based system, an administrator wants to deploy a new website following best practices. Which file location should be used for site-specific configuration?

* [ ] httpd.conf
* [ ] apache.conf
* [ ] sites-enabled/default
* [ ] sites-available/default.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** sites-available/default.conf
💡 Debian-based systems store site definitions in `sites-available`, which are then enabled via symbolic links.

</details>

---

### 8. A newly created virtual host is not live on an Ubuntu server. Which command explicitly enables it?

* [ ] apachectl enable site
* [ ] a2ensite
* [ ] systemctl enable apache2
* [ ] httpd-ctl enable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** a2ensite
💡 `a2ensite` creates a symbolic link from `sites-available` to `sites-enabled`.

</details>

---

### 9. A security administrator wants to restrict file execution and directory browsing for `/var/www/secure`. Which Apache directive provides this control?

* [ ] DNS configuration
* [ ] IP address filtering
* [ ] Access and options for a specific directory
* [ ] Apache port configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Access and options for a specific directory
💡 The `<Directory>` directive controls permissions and behavior for filesystem directories.

</details>

---

### 10. Why are `.htaccess` files often disabled in high-performance production servers?

* [ ] They break SSL
* [ ] They increase filesystem lookup overhead
* [ ] They disable virtual hosting
* [ ] They expose system passwords

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** They increase filesystem lookup overhead
💡 Apache checks `.htaccess` files on every request, impacting performance.

</details>

---

### 11. A hosting provider runs multiple websites on one IP address. Which Apache feature enables this setup?

* [ ] Serving multiple domains from one server
* [ ] Restricting root access
* [ ] Enabling FTP service
* [ ] Blocking IP addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Serving multiple domains from one server
💡 Name-based Virtual Hosting allows hosting multiple domains on a single server.

</details>

---

### 12. Before restarting Apache after configuration changes, which command ensures syntax correctness?

* [ ] apache2test
* [ ] apachectl -s
* [ ] apachectl configtest
* [ ] apache-check

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** apachectl configtest
💡 This command validates Apache configuration without restarting the service.

</details>

---

### 13. A misconfigured Apache server responds with the wrong hostname. Which directive explicitly defines the server’s domain?

* [ ] ServerAdmin
* [ ] ServerDomain
* [ ] ServerName
* [ ] DomainName

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ServerName
💡 `ServerName` sets the canonical hostname Apache uses to identify itself.

</details>

---

### 14. An organization deploys Apache as a reverse proxy in front of application servers. Which directive performs request forwarding?

* [ ] Enables SSL
* [ ] Configures proxy forwarding
* [ ] Sets up a DNS alias
* [ ] Redirects HTTPS to HTTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Configures proxy forwarding
💡 `ProxyPass` maps incoming URLs to backend servers.

</details>

---

### 15. In Squid proxy architecture, where are global access and caching rules defined?

* [ ] /etc/squid/squid.conf
* [ ] /etc/proxy/squid.cfg
* [ ] /var/squid.conf
* [ ] /usr/squid/proxy.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/squid/squid.conf
💡 This is the primary Squid configuration file across Linux distributions.

</details>

---

### 16. What is the operational impact of the directive `http_port 3128` in Squid?

* [ ] Sets the admin port
* [ ] Listens on port 3128 for proxy requests
* [ ] Defines logging output
* [ ] Enables authentication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Listens on port 3128 for proxy requests
💡 Port 3128 is Squid’s default listening port for client proxy connections.

</details>

---

### 17. After updating ACL rules, which command correctly restarts Squid on systemd systems?

* [ ] service squid reload
* [ ] squid restart
* [ ] systemctl restart squid
* [ ] squidctl reload

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** systemctl restart squid
💡 Systemd-based distributions require `systemctl` for service control.

</details>

---

### 18. In Squid, ACLs are foundational for security. What do they define?

* [ ] Access control lists
* [ ] Authentication method
* [ ] Logging options
* [ ] Proxy cache size

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Access control lists
💡 ACLs define who can access what resources through the proxy.

</details>

---

### 19. Which port should be checked during a network audit to identify an exposed Squid proxy?

* [ ] 80
* [ ] 3128
* [ ] 443
* [ ] 8888

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 3128
💡 Squid uses port 3128 by default for proxy services.

</details>

---

### 20. A penetration tester uploads a malicious `.htaccess` file. Which Apache directive allowed this behavior?

* [ ] Disables all override settings
* [ ] Disallows directory overrides
* [ ] Enables .htaccess to override config
* [ ] Enables virtual hosting

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enables .htaccess to override config
💡 `AllowOverride All` permits `.htaccess` to modify Apache behavior.

</details>

---

### 21. Which is the **correct and secure** method to enable HTTPS in Apache?

* [ ] Enable mod_rewrite
* [ ] Install an FTP module
* [ ] Enable mod_ssl and configure certificates
* [ ] Configure NFS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enable mod_ssl and configure certificates
💡 HTTPS requires SSL/TLS certificates and the `mod_ssl` module.

</details>

---

### 22. What does the directive `SSLEngine on` achieve inside an Apache VirtualHost?

* [ ] Disables HTTP
* [ ] Enables SSL/TLS for HTTPS
* [ ] Starts Apache automatically
* [ ] Encrypts email traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Enables SSL/TLS for HTTPS
💡 It activates SSL processing for that VirtualHost.

</details>

---

### 23. For hosting multiple secure domains, what is the recommended Apache configuration?

* [ ] Use the same cert for all domains
* [ ] Use port 8080
* [ ] Create a separate `<VirtualHost *:443>` block for each domain
* [ ] Use one global SSL directive

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Create a separate `<VirtualHost *:443>` block for each domain
💡 This allows proper certificate and hostname mapping, often with SNI.

</details>

---

### 24. A directory listing exposes sensitive files. Which directive prevents this when no index file exists?

* [ ] Set DirectoryIndex to None
* [ ] Use Options -Indexes
* [ ] Set AllowOverride None
* [ ] Use DenyAll

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Use Options -Indexes
💡 This disables automatic directory listing in Apache.

</details>

---

### 25. Which file securely stores hashed credentials for Apache basic authentication?

* [ ] /etc/passwd
* [ ] .htpasswd
* [ ] /etc/shadow
* [ ] user.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** .htpasswd
💡 `.htpasswd` contains hashed usernames and passwords for Apache authentication.

</details>

---

### 26. What security effect does the HTTP header `Cache-Control: no-store` enforce?

* [ ] Enable permanent caching
* [ ] Disable logging
* [ ] Prevent caching by browser or proxy
* [ ] Clear server logs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Prevent caching by browser or proxy
💡 Ensures sensitive data is not stored on client or intermediary systems.

</details>

---

### 27. Why is transparent proxying used in enterprise Squid deployments?

* [ ] To bypass firewall rules
* [ ] To cache encrypted traffic
* [ ] To intercept traffic without client-side configuration
* [ ] To mask server IP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To intercept traffic without client-side configuration
💡 Clients are unaware of the proxy, simplifying deployment.

</details>

---

### 28. What role does `refresh_pattern` play in Squid caching logic?

* [ ] Controls access logging
* [ ] Defines rules for refreshing cached content
* [ ] Filters HTTP methods
* [ ] Sets admin credentials

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Defines rules for refreshing cached content
💡 It controls cache validation and freshness decisions.

</details>

---

### 29. Which Squid directive ensures a secure default-deny access policy?

* [ ] deny all
* [ ] http_access allow localhost
* [ ] http_access deny all
* [ ] acl allow all

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** http_access deny all
💡 Best practice is to explicitly deny all traffic after allowed rules.

</details>

---

### 30. Which configuration best mitigates DNS spoofing risks in Apache hosting environments?

* [ ] Using wildcard virtual hosts
* [ ] Using IP-based virtual hosting
* [ ] Enabling HostNameLookups
* [ ] Using SNI and strict server name configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Using SNI and strict server name configuration
💡 Ensures correct certificate and host matching, reducing spoofing risks.

</details>

---
