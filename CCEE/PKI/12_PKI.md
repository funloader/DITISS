> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
# Session 12 – Authentication Protocols, FIDO & Zero Trust 40 MCQs

---

### 1. Which of the following is considered a **passive security attack**?

* [ ] Man-in-the-middle
* [ ] Eavesdropping
* [ ] Denial of Service (DoS)
* [ ] Phishing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Eavesdropping
💡 Passive attacks monitor or listen to communications without altering them, such as eavesdropping or traffic analysis.

</details>

---

### 2. FIDO authentication primarily relies on:

* [ ] Passwords only
* [ ] Biometric or hardware-based keys
* [ ] OTP sent via SMS
* [ ] Knowledge-based questions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Biometric or hardware-based keys
💡 FIDO uses public-key cryptography with biometric sensors or hardware tokens for secure passwordless authentication.

</details>

---

### 3. Zero Trust Architecture assumes:

* [ ] All users and devices inside the network are trusted
* [ ] No user or device is trusted by default
* [ ] Only internal employees are trusted
* [ ] VPN is sufficient for network security

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** No user or device is trusted by default
💡 Zero Trust requires verification of every request, regardless of location.

</details>

---

### 4. Which protocol is commonly used in FIDO authentication?

* [ ] FIDO U2F
* [ ] SAML
* [ ] OAuth 1.0
* [ ] LDAP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** FIDO U2F
💡 FIDO U2F (Universal 2nd Factor) is a widely used protocol for secure key-based authentication.

</details>

---

### 5. In Zero Trust Architecture, access decisions are based on:

* [ ] User identity, device health, and contextual information
* [ ] Location only
* [ ] Password correctness only
* [ ] Trusted internal IP addresses

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** User identity, device health, and contextual information
💡 Zero Trust enforces continuous verification using multiple contextual factors.

</details>

---

### 6. FIDO2 consists of which two components?

* [ ] WebAuthn and CTAP
* [ ] SAML and OAuth
* [ ] PKCS#11 and LDAP
* [ ] SSL and TLS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** WebAuthn and CTAP
💡 FIDO2 enables passwordless authentication via Web Authentication API (WebAuthn) and Client to Authenticator Protocol (CTAP).

</details>

---

### 7. Which of the following is a key benefit of FIDO authentication?

* [ ] Eliminates phishing attacks
* [ ] Requires multiple passwords
* [ ] Uses only knowledge-based authentication
* [ ] Increases administrative overhead

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Eliminates phishing attacks
💡 FIDO’s public-key cryptography prevents password theft and phishing.

</details>

---

### 8. Zero Trust relies heavily on:

* [ ] Micro-segmentation of networks
* [ ] Open internal network access
* [ ] Password-only authentication
* [ ] Firewall rules only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Micro-segmentation of networks
💡 Micro-segmentation isolates workloads and enforces access controls to minimize attack surface.

</details>

---

### 9. FIDO authentication reduces dependency on:

* [ ] Passwords
* [ ] Biometrics
* [ ] Hardware tokens
* [ ] Certificates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Passwords
💡 FIDO allows passwordless authentication using cryptographic keys stored on secure devices.

</details>

---

### 10. Which is a **key principle of Zero Trust**?

* [ ] Verify explicitly
* [ ] Trust all internal traffic
* [ ] Authenticate once per session
* [ ] Ignore device compliance

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Verify explicitly
💡 Zero Trust requires continuous verification of users, devices, and sessions.

</details>

---

### 11. FIDO uses which type of cryptography?

* [ ] Asymmetric public/private key
* [ ] Symmetric key only
* [ ] Hash-based message authentication only
* [ ] OTP-based cryptography

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Asymmetric public/private key
💡 FIDO generates unique key pairs for authentication, ensuring private keys never leave the device.

</details>

---

### 12. Which Zero Trust component enforces access policies based on context?

* [ ] Policy Enforcement Point (PEP)
* [ ] Certificate Authority
* [ ] LDAP server
* [ ] Security Information Event Management

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Policy Enforcement Point (PEP)
💡 PEP evaluates each request and enforces access decisions in Zero Trust architecture.

</details>

---

### 13. Which factor is **not required** in FIDO authentication?

* [ ] Server-stored password
* [ ] Biometric factor
* [ ] Cryptographic key pair
* [ ] Hardware token

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Server-stored password
💡 FIDO replaces passwords with key-based authentication and biometrics.

</details>

---

### 14. Zero Trust assumes:

* [ ] Network perimeter security is sufficient
* [ ] All threats are internal
* [ ] Breaches are inevitable
* [ ] VPN guarantees trust

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Breaches are inevitable
💡 Zero Trust designs security assuming attackers may already be inside the network.

</details>

---

### 15. FIDO authentication prevents which type of attack most effectively?

* [ ] Phishing
* [ ] DoS
* [ ] SQL Injection
* [ ] Brute-force password attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Phishing
💡 Private keys never leave the device, preventing stolen credentials from being used elsewhere.

</details>

---

### 16. In FIDO2, WebAuthn is responsible for:

* [ ] Browser-based authentication
* [ ] Hardware key generation
* [ ] Server certificate issuance
* [ ] OTP delivery

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Browser-based authentication
💡 WebAuthn API enables browsers to communicate with authenticators for secure login.

</details>

---

### 17. Which is a **Zero Trust security strategy**?

* [ ] Least privilege access
* [ ] Open trust zones
* [ ] Password-only access
* [ ] Default network-wide trust

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Least privilege access
💡 Users are granted minimal permissions necessary, reducing exposure.

</details>

---

### 18. CTAP in FIDO2 stands for:

* [ ] Client to Authenticator Protocol
* [ ] Cryptographic Token Authentication Protocol
* [ ] Certificate Transport Authentication Protocol
* [ ] Cloud Token Access Protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Client to Authenticator Protocol
💡 CTAP allows external authenticators, such as USB keys or smartphones, to communicate with browsers.

</details>

---

### 19. Which of the following is an example of a **Zero Trust tool**?

* [ ] Identity-aware proxy
* [ ] Traditional firewall only
* [ ] SSL certificate
* [ ] Password manager

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Identity-aware proxy
💡 Identity-aware proxies enforce access controls based on user identity and device compliance.

</details>

---

### 20. Zero Trust reduces risk by:

* [ ] Continuously validating trust
* [ ] Ignoring device compliance
* [ ] Allowing all internal traffic
* [ ] Reusing passwords

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Continuously validating trust
💡 Trust is never implicit; access requests are constantly evaluated.

</details>

---

### 21. FIDO U2F tokens are usually connected via:

* [ ] USB, NFC, or Bluetooth
* [ ] Only USB
* [ ] Wi-Fi
* [ ] Ethernet cable

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** USB, NFC, or Bluetooth
💡 FIDO U2F authenticators support multiple connection interfaces for flexibility.

</details>

---

### 22. Which of the following is **not part of FIDO2**?

* [ ] SAML
* [ ] WebAuthn
* [ ] CTAP
* [ ] Hardware authenticator

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SAML
💡 SAML is unrelated; FIDO2 relies on WebAuthn and CTAP.

</details>

---

### 23. Zero Trust recommends **network micro-segmentation** to:

* [ ] Limit lateral movement of attackers
* [ ] Reduce encryption
* [ ] Increase internal trust
* [ ] Simplify password management

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Limit lateral movement of attackers
💡 Micro-segmentation prevents attackers from moving freely within the network.

</details>

---

### 24. FIDO authentication **does not require**:

* [ ] Password storage on server
* [ ] Public key registration
* [ ] Device registration
* [ ] Biometric verification

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Password storage on server
💡 FIDO eliminates server-side passwords; authentication relies on key pairs.

</details>

---

### 25. Zero Trust **policy enforcement** occurs at:

* [ ] Network perimeter and application levels
* [ ] Only firewall
* [ ] VPN only
* [ ] Internal LAN only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Network perimeter and application levels
💡 Policies are enforced continuously across endpoints, apps, and networks.

</details>

---

### 26. FIDO authentication is **resistant to replay attacks** because:

* [ ] Private keys never leave the device
* [ ] It uses passwords only
* [ ] It relies on OTP only
* [ ] It requires user email verification

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Private keys never leave the device
💡 Without access to the private key, replaying a message is ineffective.

</details>

---

### 27. In Zero Trust, **device health checks** help:

* [ ] Ensure endpoint compliance before granting access
* [ ] Replace MFA
* [ ] Eliminate encryption
* [ ] Grant implicit trust

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ensure endpoint compliance before granting access
💡 Access decisions consider device posture, OS version, and security updates.

</details>

---

### 28. FIDO2 can be used for:

* [ ] Passwordless authentication
* [ ] VPN only
* [ ] SAML only
* [ ] OTP-only login

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Passwordless authentication
💡 FIDO2 allows users to authenticate without traditional passwords using secure keys.

</details>

---

### 29. Which of the following is a **Zero Trust network principle**?

* [ ] Assume breach and verify everything
* [ ] Trust internal traffic by default
* [ ] Use passwords as sole control
* [ ] Ignore device posture

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Assume breach and verify everything
💡 Zero Trust assumes attackers may already be inside and continuously evaluates all requests.

</details>

---

### 30. FIDO authentication improves security by:

* [ ] Eliminating passwords
* [ ] Using the same password everywhere
* [ ] Disabling MFA
* [ ] Using weak keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Eliminating passwords
💡 Passwordless authentication removes the most common attack vector.

</details>

---

### 31. In FIDO2, **CTAP allows**:

* [ ] External devices to communicate with the browser
* [ ] Server to generate passwords
* [ ] VPN access only
* [ ] OTP verification

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** External devices to communicate with the browser
💡 CTAP enables hardware keys and smartphones to act as authenticators.

</details>

---

### 32. Which of the following is **not a Zero Trust principle**?

* [ ] Implicit trust for internal network
* [ ] Least privilege
* [ ] Continuous verification
* [ ] Micro-segmentation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Implicit trust for internal network
💡 Zero Trust eliminates implicit trust; all access must be verified.

</details>

---

### 33. Which is a **benefit of Zero Trust**?

* [ ] Reduced risk of lateral movement
* [ ] Less monitoring needed
* [ ] Trusting internal users by default
* [ ] Eliminates need for MFA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reduced risk of lateral movement
💡 Micro-segmentation and continuous validation contain threats.

</details>

---

### 34. FIDO authentication **binds credentials to**:

* [ ] The device
* [ ] Any server
* [ ] Cloud only
* [ ] Password database

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The device
💡 FIDO private keys are stored securely on the user’s device.

</details>

---

### 35. Which of the following is an example of **FIDO2 authenticator**?

* [ ] USB security key
* [ ] Password database
* [ ] VPN client only
* [ ] Encrypted email

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** USB security key
💡 Hardware tokens like USB keys provide secure authentication in FIDO2.

</details>

---

### 36. Zero Trust recommends authentication based on:

* [ ] Contextual factors such as device, location, and user role
* [ ] Password only
* [ ] Network perimeter only
* [ ] Default internal trust

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Contextual factors such as device, location, and user role
💡 Access is granted only after evaluating multiple contextual signals.

</details>

---

### 37. Which is a **FIDO2 advantage** over password authentication?

* [ ] Resistant to phishing and credential theft
* [ ] Requires multiple passwords
* [ ] Cannot integrate with MFA
* [ ] Depends on server-side password storage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Resistant to phishing and credential theft
💡 Keys are bound to the device, making credential theft ineffective.

</details>

---

### 38. Zero Trust enforces access **based on**:

* [ ] Identity, device posture, and context
* [ ] Password alone
* [ ] Internal network only
* [ ] Location only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Identity, device posture, and context
💡 Policies are dynamic and evaluate multiple factors.

</details>

---

### 39. FIDO authentication supports:

* [ ] Passwordless, multi-factor, and phishing-resistant login
* [ ] Password-only login
* [ ] Single-factor only
* [ ] OTP-only login

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Passwordless, multi-factor, and phishing-resistant login
💡 FIDO provides flexible and secure authentication methods.

</details>

---

### 40. A **core Zero Trust approach** is:

* [ ] Never trust, always verify
* [ ] Trust all internal users
* [ ] Password-only authentication
* [ ] Network perimeter defense only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Never trust, always verify
💡 Zero Trust operates under the principle that trust must be continuously verified, regardless of location.

</details>

---
