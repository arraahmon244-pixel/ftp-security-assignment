# FTP Security Assignment

##  Overview

This repository contains answers and explanations for 20 questions on FTP (File Transfer Protocol), including its functionality, risks, and security best practices.

The assignment covers:

* FTP fundamentals
* Security weaknesses
* Common attack techniques
* Defensive strategies

---

##  Repository Structure

* `answers/ftp_questions.md` → Full detailed answers
* `assets/` → (Optional) screenshots or supporting files

---

##  Learning Objectives

By completing this assignment, you will understand:

* How FTP works
* Why FTP is insecure by default
* How attackers exploit FTP services
* How to secure file transfer systems

##  Practical Demonstration (Command Examples)

This section shows real-world commands used to discover and interact with FTP services.

---

###  1. Scanning for FTP with Nmap

```bash
nmap -p 21 -sV 192.168.1.1
```

**Explanation:**

* `-p 21` → scans FTP port
* `-sV` → detects service version

**Sample Output:**

```
21/tcp open  ftp  vsftpd 3.0.3
```

---

###  2. Banner Grabbing

```bash
nc 192.168.1.1 21
```

**Output:**

```
220 (vsFTPd 3.0.3)
```

---

###  3. Connecting to FTP Server

```bash
ftp 192.168.1.1
```

---

###  4. Anonymous Login Attempt

```bash
Name: anonymous
Password: anonymous
```

---

###  5. Listing Files

```bash
ls
```

---

###  6. Downloading a File

```bash
get backup.zip
```

---

###  7. Uploading a File

```bash
put shell.php
```

---

###  8. Exiting FTP

```bash
bye
```

---

###  9. Brute Force Example (Hydra)

```bash
hydra -l admin -P passwords.txt ftp://192.168.1.1
```

**Explanation:**

* `-l` → username
* `-P` → password list

---

##  Ethical Note

All commands are for educational purposes only and should be used in authorized lab environments.


---

##  Key Takeaways

* FTP sends data in plain text → insecure
* Weak credentials and misconfigurations are major risks
* Anonymous access can lead to serious data breaches
* Secure alternatives like SFTP/FTPS should always be used

---

##  Security Best Practices

* Use SFTP or FTPS instead of FTP
* Enforce strong passwords and disable anonymous access
* Apply least privilege permissions
* Keep systems updated
* Monitor logs for suspicious activity

---

##  Author

Your Name: ABDURRAHMON IDRIS

---

##  Submission

This repository was created as part of a cybersecurity assignment on FTP security.
