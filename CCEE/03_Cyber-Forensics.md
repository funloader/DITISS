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

### 21. Cybercrimes are offences committed where a computer system is used as a tool, target, or both. Which classification correctly represents the broad categories of cybercrime?

* [ ] Crimes against individuals only
* [ ] Crimes against organizations only
* [ ] Crimes against government only
* [ ] Crimes against individuals, organizations, and government

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Crimes against individuals, organizations, and government
💡 Cybercrimes span personal, corporate, and national security domains.

</details>

---

### 22. **Scenario:** A person gains access to a computer system without the owner’s consent. Under the IT Act, 2000 (as amended), the traditional term “hacking” has been replaced by which legally accurate expression?

* [ ] Unauthorized access
* [ ] Denial of access
* [ ] Securing access to a computer
* [ ] Ethical access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Securing access to a computer
💡 Section 43 and Section 66 use the phrase *“secures access”* to encompass broader cyber intrusions.

</details>

---

### 23. Under the IT Act, 2000, the term **“Computer Source Code”** includes which of the following?

* [ ] Program listings
* [ ] Computer commands and instructions
* [ ] Design and layout of computer programs
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Section 2(1)(u) defines source code expansively to include all logical components of software.

</details>

---

### 24. **Scenario:** An employee dishonestly downloads confidential customer data from a company server without authorization. Which section of the IT Act, 2000 specifically addresses *data theft*?

* [ ] Section 66A
* [ ] Section 66B
* [ ] Section 66C
* [ ] Section 66D

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Section 66B
💡 Section 66B deals with dishonestly receiving stolen computer resources or communication devices.

</details>

---

### 25. Which of the following best defines **Cyber Terrorism** under Section 66F of the IT Act?

* [ ] Phishing emails sent to citizens
* [ ] Online stalking or voyeurism
* [ ] Acts intended to threaten the unity, integrity, security, or sovereignty of India
* [ ] Website defacement for protest

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Acts intended to threaten the unity, integrity, security, or sovereignty of India
💡 Cyber terrorism involves intent to destabilize or intimidate the nation using cyber means.

</details>

---

### 26. **Scenario:** While installing software, a user clicks “I Agree” to the terms displayed on-screen before installation proceeds. This form of electronic agreement is classified as:

* [ ] Shrink-wrap contract
* [ ] Browse-wrap contract
* [ ] Click-wrap contract
* [ ] Oral digital contract

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Click-wrap contract
💡 Click-wrap contracts require explicit user consent and are widely enforceable in courts.

</details>

---

### 27. The Information Technology Act, 2000 introduced amendments to which of the following Indian statutes to recognize electronic records and digital evidence?

* [ ] Indian Evidence Act
* [ ] Bankers’ Books Evidence Act
* [ ] Reserve Bank of India Act
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 These amendments enabled legal recognition of electronic records and digital transactions.

</details>

---

### 28. **Scenario:** In an e-commerce transaction, two parties exchange encrypted messages using a public key published online and a private key kept secret. Which statement correctly explains this encryption model?

* [ ] A single shared secret key is used
* [ ] Each participant uses one public key only
* [ ] Each participant has a public key and a private key
* [ ] RSA is mandatory for all such communications

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Each participant has a public key and a private key
💡 Public key cryptography relies on asymmetric key pairs for confidentiality and authentication.

</details>

---

### 29. Which form of evidence, under the Indian Evidence Act (as amended by the IT Act), is considered *secondary electronic evidence*?

* [ ] Original hard disk seized from accused
* [ ] Mirror image of original disk with hash value
* [ ] Printout accompanied by Section 65B certificate
* [ ] Live RAM acquisition

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Printout accompanied by Section 65B certificate
💡 Section 65B legitimizes secondary electronic evidence if proper certification is provided.

</details>

---

### 30. **Scenario:** A company employee copies proprietary source code onto a USB drive and sells it to a competitor. Which law is *most directly* violated?

* [ ] Copyright Act, 1957
* [ ] IT Act, Section 66F
* [ ] Trade Marks Act, 1999
* [ ] Indian Penal Code – Cheating

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Copyright Act, 1957
💡 Source code is protected as a literary work under copyright law.

</details>

---

### 31. Which intellectual property right protects *inventions* that are novel, non-obvious, and industrially applicable?

* [ ] Copyright
* [ ] Trademark
* [ ] Patent
* [ ] Industrial Design

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Patent
💡 Patents protect functional and technical innovations, not ideas or expressions.

</details>

---

### 32. **Scenario:** A software company licenses its product but prohibits reverse engineering. This restriction is primarily enforced through:

* [ ] Patent law
* [ ] Copyright law
* [ ] License agreement (contract law)
* [ ] Trade secret registration

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** License agreement (contract law)
💡 Software licenses impose contractual restrictions beyond statutory IP protections.

</details>

---

### 33. Which section of the IT Act deals with *identity theft*?

* [ ] Section 66B
* [ ] Section 66C
* [ ] Section 66D
* [ ] Section 65

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Section 66C
💡 Identity theft involves fraudulent use of electronic signatures, passwords, or IDs.

</details>

---

### 34. **Scenario:** An attacker creates a fake banking website to trick users into entering credentials. Which offence is most applicable?

* [ ] Identity theft (Sec 66C)
* [ ] Cyber terrorism (Sec 66F)
* [ ] Cheating by personation using computer resource (Sec 66D)
* [ ] Unauthorized access (Sec 43)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Cheating by personation using computer resource (Sec 66D)
💡 Phishing scams fall squarely under Section 66D.

</details>

---

### 35. What is the *primary objective* of Information Security Governance?

* [ ] Deploying firewalls and antivirus
* [ ] Ensuring alignment of security with business objectives
* [ ] Preventing all cyber attacks
* [ ] Monitoring employee activity

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ensuring alignment of security with business objectives
💡 Governance focuses on strategy, risk, compliance, and accountability.

</details>

---

### 36. Which principle ensures that digital evidence has not been altered since acquisition?

* [ ] Availability
* [ ] Confidentiality
* [ ] Integrity
* [ ] Authenticity

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Integrity
💡 Hash verification is the standard method for maintaining integrity.

</details>

---

### 37. **Scenario:** An organization collects user data but uses it only for stated purposes and retains it for a limited period. Which data protection principle is being followed?

* [ ] Lawful interception
* [ ] Purpose limitation
* [ ] Data localization
* [ ] Non-repudiation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Purpose limitation
💡 Data should be collected and processed only for specific, lawful purposes.

</details>

---

### 38. Which international standard provides best practices for establishing an Information Security Management System (ISMS)?

* [ ] ISO 9001
* [ ] ISO/IEC 27001
* [ ] PCI-DSS
* [ ] COBIT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ISO/IEC 27001
💡 ISO 27001 defines a risk-based ISMS framework.

</details>

---

### 39. **Scenario:** A forensic investigator accesses evidence beyond the scope defined in a warrant. What is the most likely consequence?

* [ ] Evidence becomes inadmissible
* [ ] Investigator gains discretionary immunity
* [ ] Evidence is automatically encrypted
* [ ] Chain of custody strengthens

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Evidence becomes inadmissible
💡 Exceeding legal authority violates due process and can taint evidence.

</details>

---

### 40. Which concept ensures that a person cannot later deny having performed a digital transaction?

* [ ] Authentication
* [ ] Authorization
* [ ] Non-repudiation
* [ ] Availability

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Non-repudiation
💡 Digital signatures and logs provide proof of origin and action.

</details>

---
