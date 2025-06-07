# Web and Internet Security Fundamentals

This document summarizes the fundamental concepts of web security, including authentication, encryption, types of attacks, and defenses. It draws from the practical and theoretical aspects of your coursework.

---

## Why Web Security Matters

- The Internet is global and publicly accessible, increasing exposure to cyber threats.
- Web-based attacks are growing in number and sophistication.
- Every organization with online services must prioritize **security from the design stage**.

---

## Key Security Goals

| Goal              | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| **Confidentiality**  | Ensure information is accessible only to authorized users (via encryption) |
| **Integrity**        | Ensure accuracy and completeness of data (using hashes, audit trails)      |
| **Authentication**   | Confirm identity of users, apps, or systems                                 |
| **Non-repudiation**  | Prove the origin of communication (prevent sender denial)                  |
| **Availability**     | Ensure systems are accessible when needed (prevent DoS)                    |

---

## Authentication: Verifying Identity

Used for **access control** and **non-repudiation**.

### Methods:
- **Something you know**: Password, PIN
- **Something you have**: Token, smart card, certificate
- **Something you are**: Biometrics – fingerprint, face, retina, voice

---

## Types of Attacks

### 1. Interruption
- Makes systems or data **unavailable**
- Targets: availability, sometimes integrity
- Example: **DoS (Denial of Service)** – overloads server with requests

### 2. Interception
- Unauthorized access to data
- Targets: **confidentiality**
- Example: **Spyware**, **Man-in-the-middle attacks**

### 3. Modification
- Unauthorized changes to data or software
- Targets: **data integrity**
- Example: Malware, Viruses

### 4. Fabrication
- Faking identities or data
- Targets: authenticity, sometimes confidentiality/integrity
- Example: **Hacking**, fake emails

---

## Encryption

Encryption protects data **in transit and at rest**.

- **Encryption**: Converts plaintext → ciphertext
- **Decryption**: Reverses ciphertext → plaintext

### Example (rot13):
- "The butler did it!" → "Gur ohgyre qvq vg!"

---

## Cryptography Techniques

### Symmetric Key Cryptography
- Same key for encryption and decryption
- Example: **DES (56-bit)**, AES (128-2048 bits)
- Risk: key exchange is a weak point

### Public Key Cryptography (Asymmetric)
- Two keys: public (shared) and private (secret)
- Public encrypts, private decrypts
- More secure but slower
- Used for:
  - **Authentication**
  - **Confidentiality**
  - **Integrity**
  - **Non-repudiation**

---

## Applications of Encryption

| Tool  | Description                                           |
|-------|-------------------------------------------------------|
| SSH   | Secure Shell – like encrypted telnet                  |
| SCP   | Secure Copy – file transfer over SSH                  |
| SFTP  | Secure FTP – encrypted file transfer                  |

---

## File Integrity Checking

- Use checksums/hashes: **SHA-256**, **MD5**
- Example in Unix:
```bash
md5sum file.txt
```
- If the output changes, the file was modified.

---

## Defense-in-Depth Strategy

- Implement layered security:
  - Secure protocols (HTTPS, SSH)
  - Authentication at endpoints
  - Use **firewalls**, **IDS/IPS**
  - Regular patching and updates
  - Education and training

---

