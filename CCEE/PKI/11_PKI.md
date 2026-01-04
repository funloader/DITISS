> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
# Session 11 – Strong Authentication & Identity Protocols 40 MCQs

---

### 1. Which of the following is considered **strong authentication**?

* [ ] Username only
* [ ] Password only
* [ ] Multi-factor authentication
* [ ] Security question only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Multi-factor authentication
💡 Strong authentication requires more than one type of credential, combining something you know, have, or are.

</details>

---

### 2. Single-factor authentication relies on:

* [ ] One type of credential
* [ ] Two types of credentials
* [ ] Three types of credentials
* [ ] Biometric and token combination

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** One type of credential
💡 Single-factor authentication typically uses only a password, PIN, or fingerprint, not a combination.

</details>

---

### 3. Which of the following is an example of **multi-factor authentication**?

* [ ] Password only
* [ ] OTP sent to mobile + password
* [ ] Security question only
* [ ] Username only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OTP sent to mobile + password
💡 Multi-factor authentication uses multiple independent factors: knowledge, possession, or inherence.

</details>

---

### 4. Single sign-on (SSO) enables:

* [ ] Multiple logins for different services
* [ ] One login for multiple applications
* [ ] Password-free access only
* [ ] Manual authentication for each service

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** One login for multiple applications
💡 SSO allows users to access several systems with a single authentication.

</details>

---

### 5. Which of the following is a **benefit of SSO**?

* [ ] Reduces password fatigue
* [ ] Requires multiple passwords
* [ ] Increases login complexity
* [ ] Only supports local accounts

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Reduces password fatigue
💡 SSO reduces the number of credentials users need to remember, improving usability.

</details>

---

### 6. OpenID is primarily used for:

* [ ] Authentication
* [ ] Encryption
* [ ] Time-stamping
* [ ] Data storage

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authentication
💡 OpenID allows users to authenticate to multiple websites using a single identity.

</details>

---

### 7. OAuth is mainly used for:

* [ ] Authorization
* [ ] Authentication only
* [ ] Data encryption
* [ ] Key management

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authorization
💡 OAuth enables a third-party app to access user data with user consent, without sharing passwords.

</details>

---

### 8. Which factor is classified as **“something you have”** in MFA?

* [ ] Password
* [ ] Security token
* [ ] Fingerprint
* [ ] PIN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Security token
💡 “Something you have” refers to physical devices like smart cards or OTP tokens.

</details>

---

### 9. Which factor is classified as **“something you know”** in MFA?

* [ ] Password
* [ ] Fingerprint
* [ ] Smart card
* [ ] OTP token

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Password
💡 “Something you know” includes passwords, PINs, or security questions.

</details>

---

### 10. Which factor is classified as **“something you are”** in MFA?

* [ ] Password
* [ ] Fingerprint
* [ ] Token
* [ ] OTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Fingerprint
💡 “Something you are” refers to biometrics like fingerprints, retina scans, or facial recognition.

</details>

---

### 11. Graphical passwords are based on:

* [ ] Clicking or drawing patterns
* [ ] Alphanumeric passwords
* [ ] Hardware tokens
* [ ] OTPs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Clicking or drawing patterns
💡 Graphical passwords involve images, patterns, or gestures as authentication methods.

</details>

---

### 12. Which of the following is a **disadvantage of graphical passwords**?

* [ ] Susceptible to shoulder surfing
* [ ] Complex to remember
* [ ] Incompatible with MFA
* [ ] Reduces usability

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Susceptible to shoulder surfing
💡 Graphical passwords can be observed by attackers, making them vulnerable to shoulder surfing.

</details>

---

### 13. In SSO, the **Identity Provider (IdP)** is responsible for:

* [ ] Authenticating the user
* [ ] Storing encrypted messages
* [ ] Issuing SSL certificates
* [ ] Generating passwords

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticating the user
💡 IdP manages authentication and provides a token for access to multiple services.

</details>

---

### 14. SSO tokens are typically based on:

* [ ] Security assertions
* [ ] Passwords only
* [ ] Biometric hashes
* [ ] Encrypted files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Security assertions
💡 Security Assertion Markup Language (SAML) tokens carry authentication information in SSO.

</details>

---

### 15. Which of the following is a **challenge in SSO implementation**?

* [ ] Single point of failure
* [ ] Reduced usability
* [ ] Need for multiple passwords
* [ ] Cannot integrate with OAuth

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Single point of failure
💡 If the SSO server fails, users cannot access multiple applications, making it a critical point.

</details>

---

### 16. OpenID Connect adds **what to OAuth**?

* [ ] Authentication
* [ ] Encryption
* [ ] Time-stamping
* [ ] Certificate management

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authentication
💡 OpenID Connect extends OAuth 2.0 by providing identity verification.

</details>

---

### 17. Which of the following is a **common form of MFA attack**?

* [ ] SIM swapping
* [ ] SQL injection
* [ ] CSRF
* [ ] Cross-site scripting

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SIM swapping
💡 SIM swapping can bypass OTP-based multi-factor authentication.

</details>

---

### 18. OTP stands for:

* [ ] One-Time Password
* [ ] Open Token Protocol
* [ ] Offline Token Password
* [ ] Only Time-based Password

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** One-Time Password
💡 OTP is a password valid for a single login or transaction.

</details>

---

### 19. HOTP and TOTP are examples of:

* [ ] OTP generation algorithms
* [ ] Graphical passwords
* [ ] SSO protocols
* [ ] Certificate formats

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OTP generation algorithms
💡 HOTP is event-based, and TOTP is time-based OTP generation.

</details>

---

### 20. Which of the following best describes **single-factor authentication**?

* [ ] Only one credential needed
* [ ] Uses two or more independent factors
* [ ] Relies on biometrics only
* [ ] Requires token plus password

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Only one credential needed
💡 Single-factor authentication uses a single method such as password or PIN.

</details>

---

### 21. Which of the following is **true about OpenID**?

* [ ] Users can log into multiple sites using one identity
* [ ] It provides encrypted email
* [ ] It is only for mobile authentication
* [ ] It replaces OTPs

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Users can log into multiple sites using one identity
💡 OpenID is an authentication protocol allowing single digital identity across multiple sites.

</details>

---

### 22. OAuth 2.0 **access tokens** are used for:

* [ ] Resource access authorization
* [ ] User authentication only
* [ ] Graphical passwords
* [ ] SSO login

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Resource access authorization
💡 OAuth tokens grant applications access to user resources without sharing passwords.

</details>

---

### 23. Which of the following is **not a factor in MFA**?

* [ ] Something you know
* [ ] Something you have
* [ ] Something you are
* [ ] Something you read

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Something you read
💡 MFA factors include knowledge, possession, and inherence; “something you read” is not a factor.

</details>

---

### 24. Which type of SSO uses **SAML assertions**?

* [ ] Web-based SSO
* [ ] Local SSO
* [ ] Token-less authentication
* [ ] Graphical passwords

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Web-based SSO
💡 SAML assertions are XML-based tokens used in web SSO for authentication.

</details>

---

### 25. In MFA, **biometric factor** is classified as:

* [ ] Inherence
* [ ] Knowledge
* [ ] Possession
* [ ] Access

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Inherence
💡 Biometric factors depend on the user’s physical or behavioral traits.

</details>

---

### 26. Which of the following is an example of **“something you have”**?

* [ ] OTP token
* [ ] PIN
* [ ] Retinal scan
* [ ] Security question

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OTP token
💡 Tokens or smart cards represent possession-based authentication.

</details>

---

### 27. A **graphical password** can be based on:

* [ ] Selecting points on an image
* [ ] Typing an alphanumeric string
* [ ] Entering a PIN
* [ ] OTP generation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Selecting points on an image
💡 Users authenticate by clicking or drawing patterns on images.

</details>

---

### 28. Which of the following **reduces password fatigue**?

* [ ] SSO
* [ ] Single-factor authentication
* [ ] OTP only
* [ ] Graphical password

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SSO
💡 SSO allows one login to access multiple applications, reducing repeated password entry.

</details>

---

### 29. TOTP tokens are **valid for**:

* [ ] A short time interval, usually 30-60 seconds
* [ ] Until manually revoked
* [ ] 24 hours
* [ ] Permanent

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A short time interval, usually 30-60 seconds
💡 TOTP tokens are time-limited to prevent replay attacks.

</details>

---

### 30. Which of the following is **true about MFA**?

* [ ] Even if one factor is compromised, other factors provide protection
* [ ] Compromising one factor gives full access
* [ ] Only biometric factors are used
* [ ] MFA replaces SSO

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Even if one factor is compromised, other factors provide protection
💡 MFA adds security by requiring multiple independent factors.

</details>

---

### 31. SSO reduces:

* [ ] Number of passwords users need to remember
* [ ] System uptime
* [ ] Multi-factor authentication
* [ ] Biometric authentication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Number of passwords users need to remember
💡 SSO centralizes authentication, reducing password management overhead.

</details>

---

### 32. OpenID allows users to:

* [ ] Log in with a single identity across multiple websites
* [ ] Encrypt emails
* [ ] Generate OTPs
* [ ] Store certificates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Log in with a single identity across multiple websites
💡 OpenID provides federated authentication for multiple applications.

</details>

---

### 33. Which of the following is a **risk of SSO**?

* [ ] If compromised, access to multiple apps is lost
* [ ] Requires multiple passwords
* [ ] Reduces usability
* [ ] Cannot integrate with web apps

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** If compromised, access to multiple apps is lost
💡 SSO centralizes access, so a compromise affects all connected applications.

</details>

---

### 34. Which of the following is a **knowledge-based authentication** factor?

* [ ] Password
* [ ] OTP token
* [ ] Fingerprint
* [ ] Smart card

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Password
💡 Knowledge-based factors are something the user knows.

</details>

---

### 35. In OAuth, **access tokens** are issued by:

* [ ] Authorization server
* [ ] Identity provider
* [ ] Resource server
* [ ] Client app only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authorization server
💡 OAuth authorization server issues access tokens after user consent.

</details>

---

### 36. Which of the following is **not a biometric factor**?

* [ ] Retina scan
* [ ] Password
* [ ] Fingerprint
* [ ] Facial recognition

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Password
💡 Biometric factors are inherent traits; passwords are knowledge-based.

</details>

---

### 37. Graphical passwords improve usability but are vulnerable to:

* [ ] Shoulder surfing
* [ ] Hash collisions
* [ ] Replay attacks only
* [ ] Token theft

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Shoulder surfing
💡 Observers can see graphical input patterns, making them susceptible to attacks.

</details>

---

### 38. OpenID Connect is an extension of:

* [ ] OAuth 2.0
* [ ] SAML
* [ ] PKCS#7
* [ ] FIDO

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OAuth 2.0
💡 OpenID Connect adds authentication capabilities to OAuth 2.0 for identity verification.

</details>

---

### 39. Which of the following is **true about HOTP**?

* [ ] Event-based OTP algorithm
* [ ] Time-based OTP algorithm
* [ ] Graphical password system
* [ ] SSO protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Event-based OTP algorithm
💡 HOTP generates OTPs based on an incrementing counter rather than time.

</details>

---

### 40. Which of the following authentication methods **can be combined in MFA**?

* [ ] Password + OTP + Fingerprint
* [ ] Password only
* [ ] OTP only
* [ ] Biometric only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Password + OTP + Fingerprint
💡 MFA combines knowledge, possession, and inherence factors to strengthen security.

</details>

---
