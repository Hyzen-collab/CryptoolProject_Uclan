# Computer Systems & Security — Cryptography & System Analysis

A practical report exploring core cryptographic algorithms and system analysis using PowerShell, with hands-on experiments carried out in **CrypTool 2**.

> **Module:** Computer Systems & Security  
> **Student:** K.A. Idusha Piumika — G21328023

---

## About

This project investigates three fundamental cryptographic algorithms — DES, RSA, and MD5 — through live encryption, decryption, and hashing experiments in CrypTool 2. It also includes PowerShell-based system analysis commands for monitoring memory and process usage on a Windows machine.

---

## Tasks Covered

### Task 01 — DES Encryption & Decryption
- Plaintext `"ThisIsSampleDES123"` was encrypted using the DES symmetric cipher in CrypTool 2
- Resulting ciphertext: `E6 E3 53 81 FB 81 29 FD 12 0B 86 7C 45 90 29 4A 5A D5`
- The ciphertext was successfully decrypted back to the original plaintext using the same key
- **Key observation:** DES uses a 56-bit key and 16-round Feistel structure — considered weak by modern standards and vulnerable to brute-force attacks; AES is the recommended alternative

### Task 02 — RSA Encryption & Decryption
- A 1024-bit RSA key pair (public + private) was generated in CrypTool 2 using randomly selected prime numbers
- Plaintext was encrypted using the public key `(N, e)` and decrypted using the private key `(N, d)`
- **Key observation:** RSA is asymmetric — only the private key can decrypt what the public key encrypted; 2048-bit or higher keys are recommended for modern security

### Task 03 — MD5 Hashing
- The string `"crypto123"` was hashed using the MD5 algorithm in CrypTool 2
- **Key observation:** MD5 produces a fixed-length hash; it is efficient but vulnerable to collision attacks and not recommended for cryptographic security — SHA-256 is preferred

### Task 04 — PowerShell System Analysis

| Command | Purpose |
|---|---|
| `Get-Process \| Select-Object Name, MemoryUsage \| Sort-Object -Descending` | Lists all running processes sorted by RAM usage (MB) |
| `Get-CimInstance Win32_OperatingSystem \| Select-Object TotalVisibleMemorySize, FreePhysicalMemory` | Retrieves total and free physical memory |
| `Get-Counter` | Monitors available system memory in real time |

---

## Tools Used

- **CrypTool 2** — for DES, RSA, and MD5 experiments
- **PowerShell** — for Windows system memory and process analysis

---

## Repository Contents

```
├── Report.docx          # Full written report with results and observations
└── CrypTool file        # CrypTool 2 workspace with DES, RSA, and MD5 configurations
```

---

## Author

**K.A. Idusha Piumika** 
Computer Systems & Security Module
