# Password Cracking Analysis Using Kali Linux

## Overview

This project demonstrates password cracking techniques performed in a controlled cybersecurity lab environment using Kali Linux. The goal was to evaluate password security weaknesses by extracting password hashes and applying various cracking techniques.
The lab involved analyzing both Windows and Linux password storage mechanisms and testing the effectiveness of common password cracking tools and wordlists.

## Tools Used

- Kali Linux
- John the Ripper
- Hashcat
- CeWL
- Username Generator
- rockyou.txt wordlist

## Lab Environment

Virtual Lab Environment: SimSpace Cyber Range

Operating System:
Kali Linux Rolling (2025.1)

Resources Allocated:
- 4 CPU cores
- 8GB RAM

## Attack Scenario

The lab simulated a password cracking scenario where password hashes were obtained from two system files:

Windows:
SAM PWDumped file containing NTLM hashes

Linux:
Shadow file containing SHA-512 password hashes

The objective was to recover plaintext passwords using dictionary attacks and password cracking tools.

## Password Cracking Process

### Step 1: Identify Hash Type

The Windows SAM file contained NTLM hashes.

The Linux shadow file contained SHA-512 hashes identified by the prefix:

'$6$'

Identifying the hash type was critical in configuring the appropriate cracking tools.

### Step 2: Cracking NTLM Hashes with John the Ripper

Dictionary attacks were performed using the rockyou.txt wordlist.

Command used:

john --format=NT --wordlist=/usr/share/wordlists/rockyou.txt sam_file

John the Ripper successfully cracked six passwords from the Windows SAM file.

### Step 3: Cracking SHA-512 Hashes with Hashcat

Hashcat was used to crack Linux SHA-512 hashes.

Command used:

hashcat -m 1800 -a 0 shadow_file /usr/share/wordlists/rockyou.txt --force

Five passwords were successfully recovered from the Linux shadow file.

## Additional Reconnaissance Tools

Two additional tools were used to simulate real-world password attack preparation.

### CeWL

CeWL was used to scrape a university faculty webpage to generate a custom wordlist.

Command used:

cewl https://hcap.utsa.edu/kinesiology/faculty/ -e -w custom.txt

### Username Generator

The Username Generator script was used to generate possible usernames from extracted names.

git clone https://github.com/therodri2/username_generator.git

## Key Findings

Several important security observations were identified during this lab.
- Weak or predictable passwords can be cracked quickly using dictionary attacks.
- Password complexity significantly impacts cracking success.
- Targeted wordlists created with CeWL can increase password cracking efficiency.
- Hardware limitations such as lack of GPU acceleration can slow down cracking attempts.

## Security Recommendations

Organizations should implement several defensive measures:

- Enforce strong password policies
- Require longer passphrases
- Implement multi-factor authentication (MFA)
- Monitor authentication logs for suspicious activity
- Use modern cryptographic hashing algorithms

## Skills Demonstrated

- Password hash analysis
- Dictionary attack execution
- Cybersecurity reconnaissance
- Ethical hacking techniques
- Security vulnerability analysis
- Cybersecurity documentation

