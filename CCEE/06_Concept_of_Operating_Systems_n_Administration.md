> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 06

---

## **Session 5: Linux Essentials**

### 1. A system administrator wants to immediately shut down a Linux system without delay. Which command guarantees an immediate system halt across most modern Linux distributions?

* [ ] shutdown -h +1
* [ ] reboot
* [ ] halt
* [ ] shutdown 22:00

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** halt
💡 `halt` immediately stops all CPU functions. While `shutdown now` also works, `halt` directly halts the system and is unambiguous for immediate shutdown behavior.

</details>

---

### 2. During a Red Hat–based installation using Kickstart, where is the automatically generated Kickstart configuration file saved after a successful installation?

* [ ] /etc/kickstart.cfg
* [ ] /boot/ks.cfg
* [ ] /root/anaconda-ks.cfg
* [ ] /var/log/kickstart

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /root/anaconda-ks.cfg
💡 Anaconda installer saves the generated Kickstart file in `/root/anaconda-ks.cfg` for reuse or auditing.

</details>

---

### 3. Which Linux system file contains the mapping between usernames and their corresponding UID, GID, home directory, and default shell?

* [ ] /etc/shadow
* [ ] /etc/passwd
* [ ] /etc/group
* [ ] /etc/login.defs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/passwd
💡 `/etc/passwd` stores essential account metadata, while `/etc/shadow` stores encrypted passwords.

</details>

---

### 4. What is the primary purpose of the `useradd` command when executed by the root user?

* [ ] Modify an existing user account
* [ ] Create a new group
* [ ] Create a new user account
* [ ] Assign administrative privileges

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Create a new user account
💡 `useradd` creates a new user entry, optionally with home directory, UID, shell, and group membership.

</details>

---

### 5. Which command is most appropriate for rebooting a Linux system in a controlled manner?

* [ ] halt
* [ ] reboot
* [ ] poweroff
* [ ] exit

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** reboot
💡 `reboot` cleanly restarts the system after notifying logged-in users and stopping services.

</details>

---

### 6. Which command displays a list of users currently logged into the system?

* [ ] login
* [ ] users
* [ ] whoami
* [ ] lslogins

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** users
💡 `users` prints the usernames of all currently logged-in users.

</details>

---

### 7. Which component of the Red Hat installation process executes Kickstart-based automated installations?

* [ ] Linux Kernel
* [ ] GRUB
* [ ] Anaconda
* [ ] systemd

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Anaconda
💡 Anaconda is Red Hat’s official installer and fully supports Kickstart automation.

</details>

---

### 8. In a Kickstart configuration file, what is the function of the `%packages` section?

* [ ] Define disk partitioning
* [ ] Specify software packages and package groups
* [ ] Configure network interfaces
* [ ] Define post-installation scripts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Specify software packages and package groups
💡 `%packages` determines which RPM packages or groups are installed on the system.

</details>

---

### 9. Which Linux command is used to modify attributes such as UID, shell, or group membership of an existing user?

* [ ] useradd
* [ ] usermod
* [ ] passwd
* [ ] chage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** usermod
💡 `usermod` alters existing user account properties without recreating the account.

</details>

---

### 10. How can a system administrator schedule a system shutdown at exactly 10:00 PM?

* [ ] shutdown -h now
* [ ] shutdown 22:00
* [ ] shutdown -r 22
* [ ] shutdown -k 22

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** shutdown 22:00
💡 Time-based shutdown scheduling is supported using the HH:MM format.

</details>

---

### 11. Which shutdown option sends a warning message to logged-in users but does not actually shut down the system?

* [ ] -h
* [ ] -r
* [ ] -k
* [ ] -P

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** -k
💡 `-k` is used for testing shutdown warnings without performing shutdown.

</details>

---

### 12. What is the role of the `%post` section in a Kickstart file?

* [ ] Kernel configuration
* [ ] Post-installation automation scripts
* [ ] Bootloader setup
* [ ] Disk encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Post-installation automation scripts
💡 `%post` scripts execute after OS installation, commonly used for hardening and configuration.

</details>

---

### 13. Which command locks a user account by disabling password authentication?

* [ ] passwd -d
* [ ] usermod -L
* [ ] userdel
* [ ] chage -E

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** usermod -L
💡 The `-L` option prepends `!` to the password hash, effectively locking the account.

</details>

---

### 14. Kickstart is primarily designed for which type of Linux installation?

* [ ] Manual text-mode installation
* [ ] GUI-based installation
* [ ] Automated unattended installation
* [ ] Live OS installation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Automated unattended installation
💡 Kickstart enables repeatable, unattended OS deployments at scale.

</details>

---

### 15. Which Kickstart directive correctly configures the system timezone?

* [ ] clock
* [ ] timezone
* [ ] zonetime
* [ ] timedate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** timezone
💡 Example: `timezone Asia/Kolkata --isUtc`

</details>

---

### 16. What is the primary purpose of the `groupadd` command?

* [ ] Assign a group to a user
* [ ] Modify an existing group
* [ ] Create a new group
* [ ] Delete a group

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Create a new group
💡 `groupadd` creates a new entry in `/etc/group`.

</details>

---

### 17. Which command allows switching to another user account while retaining the current shell environment?

* [ ] login
* [ ] su
* [ ] sudo
* [ ] newgrp

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** su
💡 `su` switches user identity; `sudo` executes a single command as another user.

</details>

---

### 18. Which Kickstart directive securely defines the root user’s password?

* [ ] root
* [ ] passwd
* [ ] rootpw
* [ ] user root

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** rootpw
💡 `rootpw --iscrypted <hash>` is recommended for security.

</details>

---

### 19. When the root user runs `passwd username`, what is the effect?

* [ ] Deletes the user account
* [ ] Changes the user’s password
* [ ] Displays password policy
* [ ] Locks the account

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Changes the user’s password
💡 Root can reset any user password without knowing the old one.

</details>

---

### 20. What information does the `id` command display?

* [ ] Network configuration
* [ ] UID, GID, and group memberships
* [ ] Password expiration details
* [ ] Kernel version

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** UID, GID, and group memberships
💡 Useful for verifying user identity and privilege assignments.

</details>

---

### 21. Which command permanently removes a user along with their home directory?

* [ ] passwd -d
* [ ] userdel -r
* [ ] rm /etc/passwd
* [ ] usermod -d

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** userdel -r
💡 The `-r` option removes the home directory and mail spool.

</details>

---

### 22. Which Linux file securely stores encrypted user password hashes?

* [ ] /etc/passwd
* [ ] /etc/shadow
* [ ] /etc/group
* [ ] /etc/login.defs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/shadow
💡 `/etc/shadow` is readable only by root to prevent password disclosure.

</details>

---

### 23. What is the purpose of the `%pre` section in a Kickstart configuration?

* [ ] Enable services
* [ ] Execute scripts before installation begins
* [ ] Configure timezone
* [ ] Create user accounts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Execute scripts before installation begins
💡 `%pre` is often used for dynamic disk detection and logic-based installs.

</details>

---

### 24. Why is Kickstart especially beneficial for large-scale Linux deployments?

* [ ] Enables dual booting
* [ ] Reduces manual errors and deployment time
* [ ] Automatically upgrades kernels
* [ ] Improves GUI performance

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reduces manual errors and deployment time
💡 Automation ensures consistency and scalability.

</details>

---

### 25. What is the effect of the command `sudo usermod -aG wheel user1`?

* [ ] Grants root access directly
* [ ] Adds user1 to the wheel group
* [ ] Locks user1’s account
* [ ] Removes user1 from sudo access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Adds user1 to the wheel group
💡 Members of `wheel` can gain sudo privileges depending on sudoers configuration.

</details>

---

### 26. How is a remote Kickstart file specified at boot time?

* [ ] kickstart=/dev/sda
* [ ] ks=file:///ks.cfg
* [ ] ks=[http://server/ks.cfg](http://server/ks.cfg)
* [ ] loadkick=remote

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ks=[http://server/ks.cfg](http://server/ks.cfg)
💡 Network-based Kickstart files are common in PXE deployments.

</details>

---

### 27. What happens if a `%post` script fails during Kickstart execution?

* [ ] Installation aborts immediately
* [ ] Bootloader fails
* [ ] OS installs, but post-script actions fail
* [ ] System enters rescue mode

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OS installs, but post-script actions fail
💡 `%post` failures do not stop OS installation unless explicitly handled.

</details>

---

### 28. Which Kickstart directive correctly configures SELinux in permissive mode?

* [ ] selinux permissive
* [ ] setenforce 0
* [ ] selinux --permissive
* [ ] selinux=permissive

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** selinux --permissive
💡 This is the correct Kickstart syntax for SELinux configuration.

</details>

---

### 29. Which `useradd` option assigns a specific UID to a new user?

* [ ] -u
* [ ] -g
* [ ] -U
* [ ] -id

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** -u
💡 Useful for identity consistency across distributed systems.

</details>

---

### 30. Which utility is commonly used to generate encrypted passwords for Kickstart files?

* [ ] mkpasswd
* [ ] cryptsetup
* [ ] openssl
* [ ] grub-mkpasswd

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** openssl
💡 Example: `openssl passwd -6` generates SHA-512 hashes recommended for Kickstart.

</details>

---

## **Session 6 : Linux Essentials**

--- 
### 1. A system administrator wants to harden a Linux server by allowing only secure remote shell access without changing default configurations. Which TCP port must be explicitly permitted on the firewall to allow SSH access?

* [ ] 21
* [ ] 22
* [ ] 23
* [ ] 80

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 22
💡 SSH (Secure Shell) uses TCP port **22** by default, as defined in RFC 4253.

</details>

---

### 2. During network configuration validation, which of the following entries would be accepted as a syntactically valid IPv4 address by the TCP/IP stack?

* [ ] 192.168.1.1
* [ ] 500.500.500.500
* [ ] 192.168.999.999
* [ ] 1234:abcd::1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 192.168.1.1
💡 IPv4 addresses consist of four octets ranging from 0–255 in dotted-decimal notation.

</details>

---

### 3. A penetration tester wants to securely log into a remote Linux system using an encrypted channel. Which command-line utility is specifically designed for this purpose?

* [ ] ftp
* [ ] ssh
* [ ] telnet
* [ ] connect

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ssh
💡 SSH provides encrypted remote login and command execution, unlike FTP or Telnet.

</details>

---

### 4. In remote desktop technologies, what does **VNC** officially stand for?

* [ ] Virtual Network Connector
* [ ] Virtual Network Computing
* [ ] Virtual Node Controller
* [ ] Verified Network Configuration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Virtual Network Computing
💡 VNC enables graphical desktop sharing using the RFB protocol.

</details>

---

### 5. On a system using systemd, which component is responsible for accepting incoming SSH connections once OpenSSH is installed?

* [ ] sshd
* [ ] ssh
* [ ] openssh-client
* [ ] ssh-agent

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** sshd
💡 `sshd` is the OpenSSH **daemon** that listens for incoming SSH connections.

</details>

---

### 6. IPv6 addresses are represented using which numerical format?

* [ ] Decimal
* [ ] Hexadecimal
* [ ] Binary
* [ ] Octal

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hexadecimal
💡 IPv6 uses hexadecimal digits separated by colons, allowing compact representation.

</details>

---

### 7. Which file on a Linux system stores fingerprints of previously connected SSH servers to prevent man-in-the-middle attacks?

* [ ] ~/.ssh/config
* [ ] ~/.ssh/known_hosts
* [ ] /etc/hosts
* [ ] /etc/ssh/ssh_config

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ~/.ssh/known_hosts
💡 This file stores host key fingerprints for server authenticity verification.

</details>

---

### 8. A developer tests a locally running web application without accessing the external network. Which IPv4 address ensures traffic never leaves the host?

* [ ] 192.168.1.1
* [ ] 255.255.255.0
* [ ] 127.0.0.1
* [ ] 0.0.0.0

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 127.0.0.1
💡 The loopback address routes traffic internally within the host.

</details>

---

### 9. Which OpenSSH configuration file controls **server-side security policies** such as authentication methods and permitted users?

* [ ] /etc/ssh/sshd_config
* [ ] ~/.ssh/config
* [ ] /etc/ssh/ssh_config
* [ ] /usr/ssh/ssh.conf

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /etc/ssh/sshd_config
💡 This file defines SSH daemon behavior on the server.

</details>

---

### 10. A security analyst wants to implement password-less SSH authentication using asymmetric cryptography. Which tool generates the required key pair?

* [ ] keygen
* [ ] ssh-keygen
* [ ] ssh-init
* [ ] ssh-auth

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ssh-keygen
💡 `ssh-keygen` creates RSA, ECDSA, or ED25519 key pairs.

</details>

---

### 11. To access a remote desktop environment over VNC, which component must be installed on the **client system**?

* [ ] Server key
* [ ] VNC viewer
* [ ] SSH agent
* [ ] Authentication script

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VNC viewer
💡 The viewer initiates the connection to a VNC server.

</details>

---

### 12. A subnet mask of 255.255.255.0 corresponds to which CIDR notation?

* [ ] /8
* [ ] /16
* [ ] /24
* [ ] /32

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** /24
💡 24 bits are allocated to the network portion in this subnet.

</details>

---

### 13. Which of the following represents a valid IPv6 address as per RFC 4291?

* [ ] 192.168.0.1
* [ ] 2001:0db8:85a3::8a2e:0370:7334
* [ ] 10.0.0.256
* [ ] 172.300.0.1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 2001:0db8:85a3::8a2e:0370:7334
💡 This uses correct hexadecimal notation and zero compression.

</details>

---

### 14. Which command securely transfers a file from a local system to a remote server using SSH?

* [ ] scp
* [ ] ftp
* [ ] cp
* [ ] mv

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** scp
💡 SCP uses SSH for encrypted file transfer.

</details>

---

### 15. VNC communication primarily relies on which transport protocol?

* [ ] TCP
* [ ] UDP
* [ ] ICMP
* [ ] FTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TCP
💡 VNC requires reliable, ordered data delivery.

</details>

---

### 16. What is the **most significant architectural difference** between IPv4 and IPv6?

* [ ] IPv6 supports only private addressing
* [ ] IPv6 uses dotted decimal notation
* [ ] IPv6 has a larger address space
* [ ] IPv4 supports more security features

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IPv6 has a larger address space
💡 IPv6 uses 128-bit addressing compared to IPv4’s 32-bit.

</details>

---

### 17. By default, a VNC server listens on which TCP port number?

* [ ] 21
* [ ] 22
* [ ] 5900
* [ ] 3389

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 5900
💡 Port 5900 corresponds to display :0 in VNC.

</details>

---

### 18. Which SSH server configuration directive disables password-based login to enforce key-based authentication?

* [ ] PasswordAuthentication no
* [ ] UsePassword no
* [ ] DisablePassword yes
* [ ] AuthMode=key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PasswordAuthentication no
💡 This directive is defined in `sshd_config`.

</details>

---

### 19. Which authentication mechanism allows users to log in securely without transmitting passwords over the network?

* [ ] PAM
* [ ] LDAP
* [ ] Public key authentication
* [ ] VNC password

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Public key authentication
💡 It relies on asymmetric cryptography and challenge-response.

</details>

---

### 20. Which Linux utility is commonly used to monitor real-time bandwidth usage by IP address?

* [ ] ipconfig
* [ ] iftop
* [ ] top
* [ ] systemctl

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** iftop
💡 `iftop` displays network traffic statistics per host.

</details>

---

### 21. In enterprise networking, what does the term **dual stack** imply?

* [ ] Running both TCP and UDP
* [ ] Running IPv4 and IPv6 simultaneously
* [ ] Two servers with identical IPs
* [ ] Nested SSH sessions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Running IPv4 and IPv6 simultaneously
💡 Dual stack ensures compatibility during IPv6 migration.

</details>

---

### 22. Which IPv6 prefix range is reserved for link-local communication within the same network segment?

* [ ] fe80::/10
* [ ] ff00::/8
* [ ] 2001::/16
* [ ] fc00::/7

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** fe80::/10
💡 Link-local addresses are auto-configured and non-routable.

</details>

---

### 23. Which DNS record type resolves a hostname directly to an IPv6 address?

* [ ] A
* [ ] AAAA
* [ ] CNAME
* [ ] PTR

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** AAAA
💡 AAAA records map hostnames to 128-bit IPv6 addresses.

</details>

---

### 24. In a corporate identity management system, which protocol is commonly used for centralized authentication and directory services?

* [ ] LDAP
* [ ] FTP
* [ ] VNC
* [ ] SMB

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** LDAP
💡 LDAP integrates with SSH, PAM, and enterprise IAM systems.

</details>

---

### 25. Which SSH configuration file allows **per-user client-side customization** such as aliases and ports?

* [ ] /etc/ssh/sshd_config
* [ ] ~/.ssh/config
* [ ] /root/ssh_config
* [ ] /ssh/settings.cfg

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ~/.ssh/config
💡 This file overrides system-wide client settings.

</details>

---

### 26. When using SSH with X11 forwarding, what is the primary role of the `xauth` utility?

* [ ] Encrypt VNC passwords
* [ ] Forward keyboard mappings
* [ ] Authenticate graphical sessions
* [ ] Generate SSH keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticate graphical sessions
💡 `xauth` manages MIT-MAGIC-COOKIE authentication for X11.

</details>

---

### 27. Which IPv6 address type is functionally equivalent to IPv4 private address ranges (RFC 1918)?

* [ ] Link-local
* [ ] Global unicast
* [ ] Unique local address
* [ ] Anycast

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Unique local address
💡 ULAs (fc00::/7) are intended for internal networking.

</details>

---

### 28. Which OpenSSH feature significantly improves performance by reusing a single TCP connection for multiple SSH sessions?

* [ ] TCPKeepAlive
* [ ] SSH multiplexing
* [ ] Port forwarding
* [ ] Persistent sockets

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SSH multiplexing
💡 Enabled via `ControlMaster`, reducing connection overhead.

</details>

---

### 29. When tunneling VNC securely through SSH, which firewall port must be open on the **server**?

* [ ] 22
* [ ] 80
* [ ] 443
* [ ] 3389

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 22
💡 VNC traffic is encapsulated within the SSH tunnel.

</details>

---

### 30. In SSH authentication architecture, what is the primary role of PAM (Pluggable Authentication Modules)?

* [ ] Manages hardware settings
* [ ] Handles public key exchange
* [ ] Provides pluggable authentication
* [ ] Encrypts SSH sessions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provides pluggable authentication
💡 PAM allows SSH to integrate with multiple authentication backends.

</details>

---
