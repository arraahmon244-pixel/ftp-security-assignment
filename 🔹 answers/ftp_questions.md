# FTP Security Questions and Answers

## 1. What is FTP?

FTP is a protocol used to transfer files between systems over a network using a client-server model.

## 2. FTP vs SFTP vs FTPS

FTP is insecure (no encryption).
SFTP uses SSH encryption.
FTPS uses TLS encryption.

## 3. How FTP works

Uses control and data connections with authentication and file commands.

## 5. Active vs Passive mode

Active: server connects back → blocked by firewalls.
Passive: client connects → widely used.

## 6. Plain FTP risks

Credentials are sent in plain text → easy to intercept.

## 7. Weak credentials

Default/weak passwords allow brute-force attacks.

## 8. Anonymous FTP

Allows access without login → dangerous if misconfigured.

## 9. Banner grabbing

Reveals server type and version → helps attackers.

## 10. Outdated software

Contains known vulnerabilities → easier exploitation.

## 11. Directory listing

Reveals file structure and sensitive data.

## 12. Write permissions abuse

Allows uploading malicious files and backdoors.

## 13. Sensitive files usage

Attackers extract credentials and expand access.

## 14. Credentials vs vulnerabilities

Credentials = login abuse
Vulnerabilities = software flaws exploited

## 15. Misconfigured permissions

Can lead to privilege escalation and full compromise.

## 16. File processing attacks

Uploaded files executed by other services → RCE.

## 17. Logging importance

Helps detect attacks and investigate incidents.

## 18. Internal FTP risks

Not safe—insider threats and compromised systems exist.

## 19. Defensive measures

Encryption, strong auth, permissions, updates, monitoring.

## 20. Anonymous + sensitive files

Leads to data breaches and system compromise.
