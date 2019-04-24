# OWASP (Open Web Application Security Project)

## OWASP Top 10 - 2017

### 1. Injection
Injection flaws, such as SQL injection, LDAP injection, and CRLF injection, occur when an attacker sends untrusted data to an interpreter that is executed as a command without proper authorization.

Application security testing can easily detect injection flaws. Developers should use parameterized queries when coding to prevent injection flaws.

### 2. Broken Authentication and Session Management
Incorrectly configured user and session authentication could allow attackers to compromise passwords, keys, or session tokens, or take control of users’ accounts to assume their identities.

Multi-factor authentication, such as FIDO or dedicated apps, reduces the risk of compromised accounts.

### 3. Sensitive Data Exposure
Applications and APIs that don’t properly protect sensitive data such as financial data, usernames and passwords, or health information, could enable attackers to access such information to commit fraud or steal identities.

Encryption of data at rest and in transit can help you comply with data protection regulations.

### 4. XML External Entity
Poorly configured XML processors evaluate external entity references within XML documents. Attackers can use external entities for attacks including remote code execution, and to disclose internal files and SMB file shares.

Static application security testing (SAST) can discover this issue by inspecting dependencies and configuration.

### 5. Broken Access Control
Improperly configured or missing restrictions on authenticated users allow them to access unauthorized functionality or data, such as accessing other users’ accounts, viewing sensitive documents, and modifying data and access rights.

Penetration testing is essential for detecting non-functional access controls; other testing methods only detect where access controls are missing.

### 6. Security Misconfiguration
This risk refers to improper implementation of controls intended to keep application data safe, such as misconfiguration of security headers, error messages containing sensitive information (information leakage), and not patching or upgrading systems, frameworks, and components.

Dynamic application security testing (DAST) can detect misconfigurations, such as leaky APIs.

### 7. Cross-Site Scripting
Cross-site scripting (XSS) flaws give attackers the capability to inject client-side scripts into the application, for example, to redirect users to malicious websites.

Developer training complements security testing to help programmers prevent cross-site scripting with best coding best practices, such as encoding data and input validation.

### 8. Insecure deserialization
Insecure deserialization flaws can enable an attacker to execute code in the application remotely, tamper or delete serialized (written to disk) objects, conduct injection attacks, and elevate privileges.

Application security tools can detect deserialization flaws but penetration testing is frequently needed to validate the problem.

### 9. Using Components With Known Vulnerabilities
Developers frequently don’t know which open source and third-party components are in their applications, making it difficult to update components when new vulnerabilities are discovered. Attackers can exploit an insecure component to take over the server or steal sensitive data.

Software composition analysis conducted at the same time as static analysis can identify insecure versions of components

### 10. Insufficient Logging and Monitoring
The time to detect a breach is frequently measured in weeks or months. Insufficient logging and ineffective integration with security incident response systems allow attackers to pivot to other systems and maintain persistent threats.

Think like an attacker and use pen testing to find out if you have sufficient monitoring; examine your logs after pen testing.
