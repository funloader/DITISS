# Cyber Forensics Sample Questions – Lab Guide
---

> [!TIP]
> Sample Question for End Module


## **1. Show the last 20 access logs of your website (Debian/Linux)**

**Command:**

```bash
sudo tail -n 20 /var/log/apache2/access.log
```

```bash
sudo tail -n 20 /var/log/nginx/access.log
```

**Explanation:**

* `tail -n 20` shows the last 20 lines.
* `/var/log/apache2/access.log` is the default Apache access log file.
* Use `nginx` path if using Nginx: `/var/log/nginx/access.log`.

---

## **2. Show the last 10 authentication log entries of your user (Debian/Linux)**

**Command:**

```bash
sudo tail -n 10 /var/log/auth.log
```

**Explanation:**

* Authentication events include login attempts, sudo usage, and SSH access.
* Useful to detect unauthorized login attempts.

---

## **3. Show the last 3 entries of the package manager (Debian/Linux)**

**Command:**

```bash
tail -n 3 /var/log/dpkg.log
```

or for `apt`:

```bash
grep " install " /var/log/apt/history.log | tail -n 3
```

**Explanation:**

* Shows recent package installations.
* Important for tracking software changes on the system.

---

## **4. Show the timestamp when your system was halted last time (Debian/Linux)**

**Command:**

```bash
last -x | grep shutdown | head -n 1
```

**Explanation:**

* `last -x` shows system boots, shutdowns, and runlevel changes.
* `grep shutdown` filters shutdown events.

---

## **5. Show the last 5 logs of USB drives attached (Windows)**

**Command (PowerShell):**

```powershell
Get-EventLog -LogName System | Where-Object {$_.Message -like "*USB*"} | Select-Object -Last 5
```

**Explanation:**

* Fetches the last 5 USB connection events from the System event log.
* Useful for tracking removable media usage.

---

## **6. Show the log of connected WiFi and its passwords (Windows)**

**Command (PowerShell):**

```powershell
netsh wlan show profiles
```

Then for each profile:

```powershell
netsh wlan show profile name="PROFILE_NAME" key=clear
```

**Explanation:**

* Lists all saved WiFi networks and passwords.
* Look for `Key Content` to see the password.

---

## **7. Show the log of LogOn and LogOff of your machine (Windows)**

**Command (PowerShell):**

```powershell
Get-EventLog -LogName Security | Where-Object {$_.EventID -eq 4624 -or $_.EventID -eq 4634} | Select-Object -Last 10
```

**Explanation:**

* EventID `4624` = successful logon, `4634` = logoff.
* Shows recent login/logout activity for auditing purposes.

---

## **8. Show the current open ports and their communication on the system**

**Linux:**

```bash
sudo netstat -tulnp
```

**Windows (PowerShell):**

```powershell
netstat -ano
```

**Explanation:**

* Lists all open TCP/UDP ports along with process IDs.
* Essential for network forensics and intrusion detection.

---

## **9. Show the ports where the state is ESTABLISHED**

**Linux:**

```bash
sudo netstat -tulnp | grep ESTABLISHED
```

**Windows (PowerShell):**

```powershell
netstat -ano | findstr ESTABLISHED
```

**Explanation:**

* Filters only active connections, showing live communications.

---

## **10. Hide the message ‘Exam is Fun’ behind a JPG file and show the hash value**

**Linux:**

```bash
echo "Exam is Fun" > message.txt
cat original.jpg message.txt > hidden.jpg
sha256sum hidden.jpg
```

**Windows (PowerShell):**

```powershell
echo "Exam is Fun" > message.txt
copy /b original.jpg + message.txt hidden.jpg
Get-FileHash hidden.jpg -Algorithm SHA256
```

**Explanation:**

* Concatenates a text message to an image (basic steganography).
* `sha256sum` / `Get-FileHash` calculates the hash to verify integrity.

---

## **11. Attach a virtual HDD of 1GB with Linux machine and perform zeroization**

**Step 1: Create a virtual disk**

```bash
dd if=/dev/zero of=/mnt/virtual_disk.img bs=1M count=1024
```

**Step 2: Attach it (example with loopback)**

```bash
sudo losetup /dev/loop0 /mnt/virtual_disk.img
```

**Step 3: Zeroise the disk**

```bash
sudo dd if=/dev/zero of=/dev/loop0 bs=1M
```

**Explanation:**

* `dd if=/dev/zero` writes zeros to the entire disk for secure wipe.
* Loopback device allows treating the file as a block device.

---

✅ **Tips for Students:**

* Always take hashes before and after modifications.
* Maintain logs in a **chain-of-custody template**.
* Double-check paths (`/var/log/...`) depending on your Linux distro.
* In Windows, run **PowerShell as Administrator** for full access.

---
