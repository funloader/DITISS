> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
# Session 4: Symmetric & Asymmetric Key Encryption – 40 MCQs

---

### 1. Which of the following is a **block cipher**?

* [ ] DES
* [ ] RC4
* [ ] One-time pad
* [ ] Stream cipher

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DES
💡 DES encrypts data in fixed-size blocks of 64 bits, making it a block cipher.

</details>

---

### 2. AES is designed to replace which older encryption standard?

* [ ] RSA
* [ ] DES
* [ ] RC5
* [ ] ECC

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DES
💡 AES (Advanced Encryption Standard) was introduced to replace DES due to its small key size and vulnerability to attacks.

</details>

---

### 3. Which of the following **key sizes is standard for AES**?

* [ ] 56 bits
* [ ] 128, 192, 256 bits
* [ ] 1024 bits
* [ ] 512 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 128, 192, 256 bits
💡 AES supports three key sizes: 128-bit, 192-bit, and 256-bit.

</details>

---

### 4. RC5 is characterized by which **flexible feature**?

* [ ] Fixed key size only
* [ ] Variable block size, key size, and number of rounds
* [ ] Only asymmetric encryption
* [ ] Hash function

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Variable block size, key size, and number of rounds
💡 RC5 is highly configurable, making it flexible for different security requirements.

</details>

---

### 5. Which of the following **modes of operation** is used with DES or AES?

* [ ] ECB
* [ ] CBC
* [ ] CFB
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 DES and AES can operate in multiple modes: ECB, CBC, CFB, OFB, and CTR.

</details>

---

### 6. Which property makes **AES more secure than DES**?

* [ ] Larger block size
* [ ] Larger key size options
* [ ] More rounds of encryption
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 AES improves upon DES with a larger block size (128-bit), larger keys, and more encryption rounds.

</details>

---

### 7. Which of the following **is true about DES**?

* [ ] Uses 64-bit key
* [ ] Uses 56-bit effective key
* [ ] Is a stream cipher
* [ ] Cannot be brute-forced

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Uses 56-bit effective key
💡 DES uses a 64-bit key input, but only 56 bits are effective; 8 bits are used for parity.

</details>

---

### 8. What is the **main security weakness of DES**?

* [ ] Small block size
* [ ] Small key size vulnerable to brute-force attacks
* [ ] Use of substitution
* [ ] Lack of hash functions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Small key size vulnerable to brute-force attacks
💡 DES’s 56-bit key is insufficient against modern computational power.

</details>

---

### 9. Which of the following **symmetric algorithms is used in Wi-Fi encryption (WPA2)**?

* [ ] DES
* [ ] AES
* [ ] RC4
* [ ] RSA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** AES
💡 AES is used in WPA2 for secure Wi-Fi encryption.

</details>

---

### 10. Which of the following is a **key feature of RC5**?

* [ ] Uses Feistel structure
* [ ] Uses large prime numbers
* [ ] Public-private key pair
* [ ] Elliptic curves

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Uses Feistel structure
💡 RC5 uses a Feistel network structure and is flexible in key size and rounds.

</details>

---

### 11. Which asymmetric algorithm relies on the **difficulty of factoring large numbers**?

* [ ] AES
* [ ] RSA
* [ ] ECC
* [ ] DES

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RSA
💡 RSA’s security is based on the mathematical challenge of factoring large integers.

</details>

---

### 12. ECC is preferred over RSA because it:

* [ ] Requires larger keys
* [ ] Provides equivalent security with smaller keys
* [ ] Is faster for large file encryption
* [ ] Cannot be used for key exchange

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provides equivalent security with smaller keys
💡 ECC achieves strong security with smaller key sizes, saving computational resources.

</details>

---

### 13. Which symmetric cipher is vulnerable to **differential and linear cryptanalysis**?

* [ ] AES
* [ ] DES
* [ ] RC5
* [ ] RSA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DES
💡 DES has been shown to be vulnerable to both differential and linear cryptanalysis due to its small key size.

</details>

---

### 14. The **key expansion step** is performed in which algorithm?

* [ ] AES
* [ ] DES
* [ ] RC5
* [ ] All symmetric block ciphers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All symmetric block ciphers
💡 Key expansion generates multiple round keys from the main secret key.

</details>

---

### 15. RSA encryption uses:

* [ ] Single key
* [ ] Private key to encrypt, public key to decrypt
* [ ] Public key to encrypt, private key to decrypt
* [ ] Stream cipher

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Public key to encrypt, private key to decrypt
💡 Public key encrypts messages; private key is used to decrypt.

</details>

---

### 16. Which of the following **is true about DES rounds**?

* [ ] 8 rounds
* [ ] 16 rounds
* [ ] 32 rounds
* [ ] 10 rounds

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 16 rounds
💡 DES applies 16 rounds of Feistel operations for encryption.

</details>

---

### 17. Which of the following AES modes **adds error propagation resistance**?

* [ ] ECB
* [ ] CBC
* [ ] CTR
* [ ] OFB

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CBC
💡 CBC mode XORs each plaintext block with the previous ciphertext, providing error propagation.

</details>

---

### 18. In RSA, what does **key length** primarily affect?

* [ ] Encryption speed
* [ ] Security against brute-force
* [ ] Message size
* [ ] Hashing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Security against brute-force
💡 Longer keys increase difficulty of factoring and thus improve security.

</details>

---

### 19. Which of the following **is used for digital signatures**?

* [ ] AES
* [ ] DES
* [ ] RSA
* [ ] RC5

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RSA
💡 RSA can encrypt the hash of a message with the private key to create a digital signature.

</details>

---

### 20. RC5’s flexibility allows which of the following **parameters to be changed**?

* [ ] Block size
* [ ] Key size
* [ ] Number of rounds
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 RC5 can adjust block size, key size, and number of rounds to suit security requirements.

</details>

---

### 21. Which of the following is a **limitation of RSA**?

* [ ] Cannot encrypt small messages
* [ ] Slower for large messages
* [ ] Weak to brute-force
* [ ] Cannot be used for key exchange

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Slower for large messages
💡 RSA is computationally intensive and slower than symmetric algorithms for encrypting large data.

</details>

---

### 22. ECC is **based on** which mathematical structure?

* [ ] Prime factorization
* [ ] Elliptic curves over finite fields
* [ ] Modular exponentiation
* [ ] Polynomials

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Elliptic curves over finite fields
💡 ECC uses points on elliptic curves defined over finite fields for cryptography.

</details>

---

### 23. DES uses **how many S-boxes** in its Feistel structure?

* [ ] 4
* [ ] 8
* [ ] 16
* [ ] 32

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 8
💡 DES uses 8 substitution boxes (S-boxes) in each round for non-linear transformation.

</details>

---

### 24. AES performs which main operations per round?

* [ ] SubBytes, ShiftRows, MixColumns, AddRoundKey
* [ ] XOR, AND, OR
* [ ] SubBytes only
* [ ] Key expansion only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SubBytes, ShiftRows, MixColumns, AddRoundKey
💡 Each AES round applies these four transformations to ensure security.

</details>

---

### 25. In asymmetric encryption, which operation is **faster**?

* [ ] Encryption with public key
* [ ] Decryption with private key
* [ ] Symmetric key encryption
* [ ] Hashing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Symmetric key encryption
💡 Symmetric encryption is much faster than asymmetric encryption for large data.

</details>

---

### 26. Which of the following **is vulnerable to brute-force attack** due to small key size?

* [ ] AES-256
* [ ] DES
* [ ] RC5 with 256-bit key
* [ ] RSA-2048

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DES
💡 DES’s 56-bit key is easily breakable with modern computational power.

</details>

---

### 27. Which of the following **asymmetric schemes can be used for key exchange**?

* [ ] DES
* [ ] AES
* [ ] RSA or ECC
* [ ] RC5

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RSA or ECC
💡 Both RSA and ECC allow secure key exchange between parties.

</details>

---

### 28. AES-256 has **how many rounds** in standard encryption?

* [ ] 10
* [ ] 12
* [ ] 14
* [ ] 16

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 14
💡 AES-256 applies 14 rounds of transformation for encryption.

</details>

---

### 29. Which of the following **describes a Feistel network**?

* [ ] Same operation for encryption and decryption
* [ ] Uses hash functions only
* [ ] Cannot be decrypted
* [ ] Requires asymmetric keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Same operation for encryption and decryption
💡 Feistel networks allow identical operations for encryption and decryption, just reversing keys.

</details>

---

### 30. Which of the following **attacks targets weak symmetric keys**?

* [ ] Brute-force attack
* [ ] Chosen-plaintext attack
* [ ] Ciphertext-only attack
* [ ] Replay attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Brute-force attack
💡 Weak symmetric keys are susceptible to exhaustive search attacks.

</details>

---

### 31. In DES, the **initial permutation** is applied to:

* [ ] The key only
* [ ] The plaintext block
* [ ] The ciphertext only
* [ ] Hash values

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The plaintext block
💡 DES begins encryption with an initial permutation of the 64-bit plaintext.

</details>

---

### 32. AES uses which **algebraic structure** for MixColumns?

* [ ] Modular addition
* [ ] Finite field GF(2^8)
* [ ] Prime numbers
* [ ] XOR only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Finite field GF(2^8)
💡 MixColumns operation in AES is performed over GF(2^8) for diffusion.

</details>

---

### 33. Which of the following **reduces ECC key size** compared to RSA for equivalent security?

* [ ] Factorization problem
* [ ] Discrete logarithm problem
* [ ] Brute-force search
* [ ] XOR operations

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Discrete logarithm problem
💡 ECC relies on the elliptic curve discrete logarithm problem for security, allowing smaller keys.

</details>

---

### 34. DES encryption **uses how many subkeys** per 64-bit block?

* [ ] 8
* [ ] 16
* [ ] 32
* [ ] 64

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 16
💡 DES generates 16 round keys (subkeys) for encryption.

</details>

---

### 35. Which of the following **encryption methods is deterministic**?

* [ ] ECB mode
* [ ] CBC mode
* [ ] CTR mode
* [ ] OFB mode

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ECB mode
💡 ECB encrypts identical plaintext blocks into identical ciphertext blocks.

</details>

---

### 36. Which of the following **algorithms supports variable number of rounds**?

* [ ] AES
* [ ] DES
* [ ] RC5
* [ ] RSA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RC5
💡 RC5 allows user-defined rounds, block size, and key size.

</details>

---

### 37. Which of the following **asymmetric encryption algorithms can be used for encryption, decryption, and digital signatures**?

* [ ] DES
* [ ] AES
* [ ] RSA
* [ ] RC5

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RSA
💡 RSA can encrypt, decrypt, and generate digital signatures.

</details>

---

### 38. AES’s **SubBytes step** provides:

* [ ] Diffusion
* [ ] Confusion
* [ ] Integrity
* [ ] Authentication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Confusion
💡 SubBytes replaces each byte using S-boxes to introduce non-linearity (confusion).

</details>

---

### 39. In DES, the **expansion permutation** increases 32-bit half-block to:

* [ ] 32 bits
* [ ] 48 bits
* [ ] 64 bits
* [ ] 56 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 48 bits
💡 DES expands 32-bit R block to 48 bits before XOR with subkey in each round.

</details>

---

### 40. Which of the following **asymmetric key algorithms is suitable for IoT devices**?

* [ ] RSA-4096
* [ ] ECC-256
* [ ] DES
* [ ] AES-128

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ECC-256
💡 ECC provides strong security with smaller keys, ideal for resource-constrained IoT devices.

</details>

---
