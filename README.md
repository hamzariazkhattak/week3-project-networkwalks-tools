# week3-project-networkwalks-tools

&#x20;\<div align="center">

\<!-- ═══════════ HEADER ═══════════ -->

# ☠️ CYBERSECURITY OPERATIONS

### `PASSWORD CRACKING & HASH ANALYSIS`

```text
 ██████╗ ███████╗██████╗     ████████╗███████╗ █████╗ ███╗   ███╗
██╔════╝ ██╔════╝██╔══██╗    ╚══██╔══╝██╔════╝██╔══██╗████╗ ████║
██║  ███╗█████╗  ██████╔╝       ██║   █████╗  ███████║██╔████╔██║
██║   ██║██╔══╝  ██╔══██╗       ██║   ██╔══╝  ██╔══██║██║╚██╔╝██║
╚██████╔╝███████╗██║  ██║       ██║   ███████╗██║  ██║██║ ╚═╝ ██║
 ╚═════╝ ╚══════╝╚═╝  ╚═╝       ╚═╝   ╚══════╝╚═╝  ╚═╝╚═╝     ╚═╝
```

**`[ WEEK 03 ]` | `[ PROJECT MODULE 01 ]`**



\


```text
[ SYSTEM STATUS ]     ONLINE
[ OPERATION ]         PDF PASSWORD AUDITING
[ ENVIRONMENT ]       AUTHORIZED LAB
[ TRAINING ]          NETWORKWALKS
[ MISSION STATUS ]    FLAG CAPTURED ✓
```

### 👨‍💻 OPERATOR INFORMATION

**HAMZA RIAZ (Intern)**

`Cybersecurity Student | Ethical Hacking Enthusiast`

**Training Organization:** NETWORKWALKS
**Batch:** [HAMZA RIAZ/ B084]
**Instructor:** WAQAS KARIM, CCIE
**Project:** Week 03 – Module 01

\</div>

---

## 💀 `0x01 // MISSION OVERVIEW`

This repository documents a practical cybersecurity lab focused on **PDF password hash extraction and offline dictionary-based password cracking** using John the Ripper.

The objective was to extract the cryptographic password hash from an encrypted PDF, analyze it using a password-cracking utility, recover the plaintext password, and successfully unlock the protected document.

```text
┌───────────────────────────────────────────────────────────────┐
│                                                               │
│  [ TARGET ]     My Locked PDF1.pdf                            │
│  [ TOOL ]       John the Ripper                               │
│  [ EXTRACTOR ]  pdf2john                                      │
│  [ WORDLIST ]   rockyou.txt                                   │
│  [ ATTACK ]     Offline Dictionary Attack                    │
│  [ RESULT ]     PASSWORD RECOVERED                            │
│  [ OBJECTIVE ]  FIRST FLAG CAPTURED ✓                         │
│                                                               │
└───────────────────────────────────────────────────────────────┘
```

## 🛠️ `0x02 // ARSENAL & TOOLS USED`

| Component        | Tool / Resource      | Purpose                      |
| :--------------- | :------------------- | :--------------------------- |
| Operating System | Kali Linux           | Security testing environment |
| Hash Extraction  | `pdf2john`           | Extract PDF password hash    |
| Cracking Engine  | John the Ripper      | Password recovery            |
| Wordlist         | `rockyou.txt`        | Dictionary attack candidates |
| Target           | `My Locked PDF1.pdf` | Encrypted PDF sample         |
| Technique        | Dictionary Attack    | Offline password auditing    |

## ⚡ `0x03 // EXPLOITATION WORKFLOW`

### `STEP 01` — Target Acquisition

Obtained the encrypted PDF file provided for the authorized Networkwalks training lab.

**Target:** `My Locked PDF1.pdf`

### `STEP 02` — Hash Extraction

Used `pdf2john` to extract the PDF encryption hash.

```bash
pdf2john "My Locked PDF1.pdf" > hash1.txt
```

**Output:** Extracted hash saved in `hash1.txt`.

### `STEP 03` — Wordlist Preparation

Prepared the RockYou wordlist available in Kali Linux.

```bash
sudo gzip -d /usr/share/wordlists/rockyou.txt.gz
```

### `STEP 04` — Dictionary Attack

Executed John the Ripper against the extracted hash.

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt hash1.txt
```

### `STEP 05` — Password Recovery

Retrieved the recovered password using:

```bash
john --show hash1.txt
```

### `STEP 06` — PDF Decryption & Flag Capture

Used the recovered password to unlock the encrypted PDF and verified the successful flag confirmation.

```text
╔══════════════════════════════════════════════════════╗
║                                                      ║
║               [ ACCESS GRANTED ]                     ║
║                                                      ║
║       ✓ HASH EXTRACTION SUCCESSFUL                   ║
║       ✓ PASSWORD RECOVERED                           ║
║       ✓ PDF UNLOCKED                                  ║
║       ✓ FIRST FLAG CAPTURED                           ║
║                                                      ║
║              MISSION COMPLETED                       ║
║                                                      ║
╚══════════════════════════════════════════════════════╝
```

## 📸 `0x04 // DIGITAL EVIDENCE`

Screenshots documenting the actual practical execution.

|   Hash Cracking   |  Flag Confirmation |
| :---------------: | :----------------: |
|                   |                    |
| `jtr-cracked.png` | `unlocked-pdf.png` |

## 🛡️ `0x05 // DEFENSIVE COUNTERMEASURES`

- **Strong Passwords:** Avoid common passwords and predictable combinations.
- **High Entropy:** Use long, unique passphrases.
- **Modern Encryption:** Use strong PDF encryption configurations such as AES-256 where supported.
- **Password Management:** Store credentials securely using trusted password managers.
- **Security Awareness:** Understand how offline dictionary attacks can expose weak passwords.

## 🧠 `0x06 // KEY LEARNINGS`

Through this practical lab, I gained hands-on experience with:

- Understanding PDF password protection.
- Extracting cryptographic hashes using `pdf2john`.
- Preparing and using the RockYou wordlist.
- Performing offline dictionary attacks with John the Ripper.
- Retrieving recovered passwords.
- Understanding the security risks of weak passwords.
- Learning defensive password security practices.

## ⚠️ `0x07 // LEGAL DISCLAIMER`

```diff
- UNAUTHORIZED ACCESS IS STRICTLY PROHIBITED.
+ This project was performed for educational and defensive
+ cybersecurity training purposes within an authorized
+ Networkwalks laboratory environment.
+
+ All techniques must only be used on files and systems
+ for which explicit permission has been granted.
```

---

\<div align="center">

## 👨‍💻 OPERATOR // HAMZA RIAZ KHATTAK

**CYBERSECURITY | ETHICAL HACKING | PENETRATION TESTING**

`NETWORKWALKS` • `WEEK 03` • `PROJECT MODULE 01`

```text
[ LEARN ]  →  [ PRACTICE ]  →  [ ANALYZE ]  →  [ SECURE ]
```

**"Think Like an Attacker. Defend Like a Professional."**

\


⭐ **If you find this project useful, consider starring the repository!**

\</div>
