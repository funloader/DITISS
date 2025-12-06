### 🔐 What is Cryptography? (One-liner)
*Cryptography is the science of securing information using mathematical techniques to ensure confidentiality, integrity, authentication, and non-repudiation.*

**Keywords:** Encryption, Cipher, Key, Algorithm, Confidentiality, Integrity.
It protects data by converting readable information into an unreadable form using algorithms and keys. It includes encryption, decryption, cryptanalysis, and cryptology

### Basic Keywords
- **Plaintext**: Original readable data before encryption.

🎯 “Plaintext is human-readable data that needs protection before transmission or storage.”
- **Access Control**: Restricting access to resources based on authentication & authorization.

🎯 “Access control ensures only authorized users can access specific data. Common methods: DAC, MAC, RBAC.”
- **Encryption**: Converting plaintext → ciphertext using an algorithm + key.
- **Decryption**: Converting ciphertext → plaintext using the correct key.

🎯  “Encryption secures data; decryption restores it. Used to prevent unauthorized access during transmission or storage.”
- **Cryptanalysis**: Breaking or bypassing cryptographic systems.

🎯  “Cryptanalysis focuses on finding weaknesses in ciphers—like brute force, frequency analysis, or side-channel attacks.”
- **Cryptology**: Study of cryptography + cryptanalysis

🎯  “Cryptology is the overall field combining encryption techniques and methods to break them.”
- *Encryption Algorithm*: Mathematical function that transforms plaintext to ciphertext.

🎯 “Algorithms define how the encryption happens, while keys decide the strength.”
- **Cipher**: A cipher is the algorithm or process used to encrypt and decrypt information.

🎯 “Cipher defines how data is scrambled.”
### 🔹Encryption Method
 *The approach/technique used to encrypt plaintext.*
- **Why Encryption Method is Needed?**
  - To prevent unauthorized data access
  - To secure data integrity
  - To protect data during transit (CIA Triad)
  - To comply with security standards (GDPR, HIPAA)
### 🔸**Types of Classical Ciphers**
  - *Substitution Cipher* : Replaces each letter/symbol with another.
  - Two Types
    1. **Monoalphabetic Cipher** (one alphabet mapping)
    2. **Polyalphabetic Cipher** (multiple alphabet mappings)
### 1. Mono-alphabetic Substitution
 🔸 Each letter → one fixed substitute.    
  Examples 
  - Atbash Cipher : Reverses the alphabet (A↔Z, B↔Y).
  - Caesar Cipher : Shifts letters by N positions (e.g., shift 3).

🎯 “Mono-alpha ciphers are easy to break using frequency analysis.”

### 2. Polyalphabetic Substitution
 🔸 Uses multiple alphabets to increase complexity.
 Examples
 - Vigenère Cipher : Uses a repeating key to shift letters.
 - Homophonic Substitution : One plaintext letter may map to multiple ciphertext symbols to hide frequency patterns.

🎯 “Harder to break than mono-alpha because frequency distribution is masked.”

### 🔹 Transposition Cipher
- Rearranges the characters of plaintext without altering them.
Example: Scytale Cipher *(here nothing is added newly only jumbled)*

🎯 “Transposition ciphers change the order of characters instead of substituting them.”
