# Session 11 – Strong Authentication & Identity Protocols
---

## 1. Authentication – Basics

### 1.1 Definition

**Authentication** is the process of **verifying the identity of a user or system**.

**MCQ Line:**

> Authentication answers **“Who are you?”**

---

### 1.2 Authentication Factors

| Factor Type        | Example               |
| ------------------ | --------------------- |
| Something you know | Password, PIN         |
| Something you have | Smart card, OTP token |
| Something you are  | Fingerprint, Iris     |

---

## 2. Strong Authentication

### 2.1 Definition

**Strong authentication** uses **more than one authentication factor** to verify identity.

**MCQ Line:**

> Strong authentication = **Multi-factor authentication**

---

### 2.2 Characteristics

* Higher security
* Reduced risk of credential theft
* Resistant to phishing

---

## 3. Single-Factor Authentication (SFA)

### 3.1 Definition

Authentication using **only one factor**.

### 3.2 Examples

* Username + password
* PIN

**MCQ Line:**

> SFA is **least secure**

---

## 4. Multi-Factor Authentication (MFA)

### 4.1 Definition

Authentication using **two or more independent factors**.

---

### 4.2 MFA Examples

* Password + OTP
* Smart card + PIN
* Biometric + OTP

---

### 4.3 MFA Advantages

* Prevents brute-force attacks
* Reduces credential reuse risk
* Improves compliance

---

### 4.4 SFA vs MFA (High MCQ Weight)

| Feature             | SFA  | MFA         |
| ------------------- | ---- | ----------- |
| Factors             | One  | Two or more |
| Security            | Low  | High        |
| Phishing resistance | Poor | Good        |

---

## 5. Single Sign-On (SSO)

### 5.1 Definition

**Single Sign-On (SSO)** allows users to **log in once and access multiple systems**.

**MCQ Line:**

> SSO improves **usability**

---

### 5.2 SSO Characteristics

* Centralized authentication
* Reduced password fatigue
* One login, multiple services

---

### 5.3 SSO Technologies

* Kerberos
* SAML
* OAuth
* OpenID Connect

---

### 5.4 SSO Advantages & Risks

**Advantages**

* User convenience
* Reduced admin overhead

**Risks**

* Single point of failure
* Compromised account → multiple services

---

## 6. OpenID

### 6.1 Definition

**OpenID** is an **authentication protocol** that allows users to authenticate using a **third-party identity provider**.

**MCQ Line:**

> OpenID provides **authentication**, not authorization

---

### 6.2 OpenID Connect (OIDC)

* Built on **OAuth 2.0**
* Uses JSON Web Tokens (JWT)
* Modern SSO standard

---

## 7. OAuth

### 7.1 Definition

**OAuth** is an **authorization framework** that allows applications to **access user resources without sharing passwords**.

**MCQ Line:**

> OAuth provides **authorization**, not authentication

---

### 7.2 OAuth Roles

* Resource Owner
* Client
* Authorization Server
* Resource Server

---

### 7.3 OAuth Tokens

* Access token
* Refresh token

---

### 7.4 OAuth Use Case

* “Login with Google”
* API access delegation

---

## 8. OpenID vs OAuth (Very High MCQ Weight)

| Feature          | OpenID         | OAuth         |
| ---------------- | -------------- | ------------- |
| Purpose          | Authentication | Authorization |
| Identity proof   | Yes            | No            |
| Password sharing | No             | No            |
| Common use       | Login          | API access    |

---

## 9. Graphical Passwords

### 9.1 Definition

**Graphical passwords** authenticate users using **images, patterns, or visual elements** instead of text.

---

### 9.2 Types of Graphical Passwords

| Type              | Example                 |
| ----------------- | ----------------------- |
| Recognition-based | Select known images     |
| Recall-based      | Draw a pattern          |
| Cued-recall       | Click sequence on image |

---

### 9.3 Advantages

* Better memorability
* Resistant to dictionary attacks

---

### 9.4 Disadvantages

* Shoulder surfing risk
* Slower login
* Limited deployment

---

## 10. Important MCQ Facts

* Strong authentication = MFA
* SSO improves usability
* OAuth ≠ Authentication
* OpenID Connect = modern SSO
* Graphical passwords use images

---

## 11. Common Exam Traps

* ❌ OAuth authenticates users
* ❌ SSO increases security always
* ❌ MFA uses same factor twice
* ✔ MFA uses different factors
* ✔ OpenID authenticates identity

---

## 12. Lab Mapping (Session 11)

| Lab Task     | Tool            |
| ------------ | --------------- |
| MFA setup    | OTP apps        |
| OAuth demo   | Google APIs     |
| OpenID login | OIDC provider   |
| SSO setup    | SAML / Kerberos |

---

## 13. Corrections / Best Practices

* Enforce MFA for privileged users
* Use OpenID Connect for SSO
* Avoid password-only systems
* Combine MFA with SSO carefully

---
