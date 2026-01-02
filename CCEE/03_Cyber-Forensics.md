> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
# SET 03 – Advanced Cyber Law, IPR & Information Security (DITISS Level)
---

### 1. If you encounter a *sheep-dip machine* at a client site during a forensic readiness assessment, what is the most accurate inference?

* [ ] A system coordinating multiple honeypots
* [ ] A deception system meant to lure attackers
* [ ] A standalone system used exclusively to scan external media for malware
* [ ] A system that mitigates denial-of-service attacks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A standalone system used exclusively to scan external media for malware
💡 A sheep-dip system is an isolated computer used to scan removable media before introducing it into a secure network.

</details>

---

### 2. In digital forensics, what term describes the documented trail showing who handled evidence, when, and for what purpose?

* [ ] Rules of Evidence
* [ ] Evidence Integrity Policy
* [ ] Chain of Custody
* [ ] Separation of Duties

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Chain of Custody
💡 Chain of custody ensures evidence authenticity and admissibility in court.

</details>

---

### 3. What is the length (in hexadecimal characters) of an MD5 hash value?

* [ ] 16
* [ ] 32
* [ ] 64
* [ ] 128

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 32
💡 MD5 produces a 128-bit hash, represented as 32 hexadecimal characters.

</details>

---

### 4. Before a forensic examiner can testify as an expert witness in court, what must the attorney first establish?

* [ ] The infallibility of forensic tools used
* [ ] The examiner’s professional qualifications and expertise
* [ ] The examiner’s prior case success rate
* [ ] The examiner’s neutrality

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The examiner’s professional qualifications and expertise
💡 Courts require formal qualification of an expert witness before testimony.

</details>

---

### 5. **Scenario:** You are investigating a regional bank with four 30-TB SANs containing customer transaction data. What is the *most forensically sound and efficient* acquisition method?

* [ ] Compressed logical file copy
* [ ] Sparse file extraction
* [ ] Bit-stream disk-to-image acquisition
* [ ] Bit-stream disk-to-disk cloning

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Bit-stream disk-to-image acquisition
💡 Disk-to-image allows preservation, verification, and scalable analysis without altering original media.

</details>

---

### 6. Which file system is most commonly associated with legacy floppy disks?

* [ ] NTFS
* [ ] FAT32
* [ ] FAT16
* [ ] FAT12

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** FAT12
💡 FAT12 was designed for low-capacity storage such as floppy disks.

</details>

---

### 7. **Scenario:** An attacker floods a router with half-open TCP connections, preventing it from forwarding legitimate traffic. What type of attack is this?

* [ ] ARP Spoofing
* [ ] Distributed Routing Attack
* [ ] Denial-of-Service (DoS) attack
* [ ] Replay attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Denial-of-Service (DoS) attack
💡 Resource exhaustion prevents legitimate network operations.

</details>

---

### 8. When analyzing a file in a hex editor, where is the file header typically located?

* [ ] At the end of the file
* [ ] In the file allocation table
* [ ] At the beginning of the file
* [ ] Randomly distributed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** At the beginning of the file
💡 File headers contain metadata used to identify file type and structure.

</details>

---

### 9. Which statement about file deletion on FAT-based file systems is correct?

* [ ] File data is immediately overwritten
* [ ] File clusters are encrypted on deletion
* [ ] Directory entries are marked as deleted but data remains
* [ ] Deleted files are unrecoverable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Directory entries are marked as deleted but data remains
💡 This allows forensic recovery until clusters are overwritten.

</details>

---

### 10. **Scenario:** A suspect clears browser history, cookies, and deletes downloaded images. What is the *most feasible forensic step* to demonstrate policy violation?

* [ ] Request logs from visited websites
* [ ] Rely on eyewitness statements
* [ ] Examine registry and system artifacts
* [ ] Abandon the investigation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Examine registry and system artifacts
💡 Registry keys, DNS cache, pagefile, and unallocated space often retain residual evidence.

</details>

---

### 11. What type of attack is executed primarily by scripts or programs without manual intervention?

* [ ] Distributed attack
* [ ] Automated attack
* [ ] Insider attack
* [ ] Passive attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Automated attack
💡 Automation allows rapid, large-scale exploitation.

</details>

---

### 12. In hexadecimal file analysis, what does the *offset* represent?

* [ ] The byte value after the colon
* [ ] The memory address where data begins
* [ ] The file’s checksum
* [ ] The encryption key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The memory address where data begins
💡 Offsets indicate byte position relative to the start of the file.

</details>

---

### 13. How many mishandled forensic cases can permanently damage a forensic examiner’s professional credibility?

* [ ] Two
* [ ] Several
* [ ] One
* [ ] Only if proven malicious

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** One
💡 A single compromised case can undermine expert credibility in future proceedings.

</details>

---

### 14. On a Linux EXT2/EXT3/EXT4 file system, when is a file considered deleted?

* [ ] When permissions are removed
* [ ] When inode link count reaches zero
* [ ] When the superblock is updated
* [ ] When data blocks are wiped

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** When inode link count reaches zero
💡 The inode is released only after all hard links are removed.

</details>

---

### 15. **Scenario:** An employee attempts to erase CD/DVD data using a magnet. Why will this fail?

* [ ] Optical media uses logical storage
* [ ] Optical media is encrypted
* [ ] Optical media is non-magnetic
* [ ] Optical media stores data in RAM

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Optical media is non-magnetic
💡 CDs and DVDs use laser-etched pits, not magnetic domains.

</details>

---

### 16. Which legal authorization permits law enforcement to search premises for evidence?

* [ ] Subpoena
* [ ] Bench warrant
* [ ] Wiretap order
* [ ] Search warrant

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Search warrant
💡 A search warrant authorizes physical or digital searches under judicial oversight.

</details>

---

### 17. What cryptographic technique hides information within another file to avoid detection?

* [ ] Encryption
* [ ] Hashing
* [ ] Steganography
* [ ] Tokenization

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Steganography
💡 Unlike encryption, steganography conceals the *existence* of information.

</details>

---

### 18. In Windows security, which ACL identifies *who is allowed or denied* access to an object?

* [ ] SACL
* [ ] DACL
* [ ] UACL
* [ ] TACL

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DACL
💡 DACLs define access permissions; SACLs define auditing.

</details>

---

### 19. What Linux tool generates summarized audit reports from audit logs?

* [ ] auditctl
* [ ] ausearch
* [ ] aureport
* [ ] syslogd

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** aureport
💡 `aureport` produces human-readable summaries for investigators.

</details>

---

### 20. In Kerberos authentication, what does TGT stand for?

* [ ] Token Granting Ticket
* [ ] Ticket Granting Terminal
* [ ] Ticket Granting Ticket
* [ ] Trusted Grant Token

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ticket Granting Ticket
💡 The TGT allows clients to request service tickets without re-authenticating.

</details>

---
