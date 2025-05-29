# Task 3: Perform a Basic Vulnerability Scan on Your PC

## Objective:
To identify common vulnerabilities present on the local machine using Nessus Essentials, a free vulnerability scanner. This helps in understanding local system exposures and how to mitigate them.

## Tools Used:
- Nessus Essentials (by Tenable)
- Operating System: Windows 10
- Scan Target: Localhost (127.0.0.1)

## Steps Followed:

1. Downloaded and installed Nessus Essentials.
   - Registered for a free activation code.
   - Accessed Nessus via https://localhost:8834 in the browser.

2. Created a Basic Network Scan.
   - Target set to: 127.0.0.1 (Localhost)
   - Scan Type: Basic Network Scan

3. Launched a Full Vulnerability Scan.
   - Scan completed in approximately 10 minutes.

4. Scan Results Overview:

| Severity      | Count |
|---------------|-------|
| Critical      | 0     |
| High          | 0     |
| Medium        | 2     |
| Low           | 0     |
| Info / Others | 20    |
| **Total**     | **22**|

## Key Vulnerabilities Identified:

### 1. SMB Signing Not Required

- **Port:** 445/tcp (CIFS)
- **Host:** 127.0.0.1
- **Severity:** Medium
- **Description:**  
  The SMB server does not enforce message signing. This allows man-in-the-middle attacks by intercepting or modifying SMB traffic.

- **Solution:**  
  - Go to `Local Security Policy` > `Local Policies` > `Security Options`
  - Enable the setting: `Microsoft network server: Digitally sign communications (always)`

### 2. SSL Certificate Cannot Be Trusted

- **Port:** 8834/tcp (Nessus Web UI)
- **Host:** 127.0.0.1
- **Severity:** Medium
- **Description:**  
  The Nessus web server uses a self-signed certificate not issued by a public certificate authority, making it untrusted by browsers.

- **Solution:**  
  - For production: Use a certificate from a trusted CA (e.g., Let’s Encrypt)
  - **For localhost/testing (which was our case):** Optionally add the certificate to your system's trusted root store or use a locally trusted certificate generator like `mkcert`


## Conclusion

The system has no critical or high-risk vulnerabilities. Two medium-level issues were identified:
- One related to insecure SMB configuration
- One related to self-signed SSL certificate on localhost

These issues can be fixed by enabling SMB signing and configuring a proper SSL certificate. Regular vulnerability scans are recommended to maintain system security.
