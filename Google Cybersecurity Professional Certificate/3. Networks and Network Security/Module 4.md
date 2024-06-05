# Security hardening
## Security hardening

- **Security hardening:**
	- The process of strengthening a system to reduce its vulnerabilities and attack surface.

- **Penetration testing (pen test):**
	- A simulated attack that helps identify vulnerabilities in systems, networks, websites, applications, and processes.

---
## OS hardening practices

- **Operating system (OS):**
	- The interface between computer hardware and the user.

- **Patch update:**
	- A software and operating system update that addresses security vulnerabilities within a program or product.

- **Baseline configuration (baseline image):**
	- A documented set of specifications within a system that is used as a basis for future builds, releases, and updates.

- **Multi-factor authentication (MFA):**
	- A security measure which requires a user to verify their identity in two or more ways to access a system or network.

- **Categories of multi-factor identification:**
	- Something you know.
	- Something you have.
	- Something unique about you

---
## Brute Force Attacks and OS Hardening

### Brute Force Attacks

- **Definition**: Trial-and-error method to discover private information.
- **Types**:
  - Simple brute force attacks: Trying various username/password combinations.
  - Dictionary attacks: Using pre-existing lists of common passwords or those from previous breaches.

### Assessing Vulnerabilities

- **Virtual Machines (VMs)**:
  - Software versions of physical computers.
  - Provide isolated environments for testing suspicious files or malware.
  - Can be reset to a clean state after testing.

- **Sandbox Environments**:
  - Isolated testing environments for software or programs.
  - Useful for evaluating patches, identifying bugs, and simulating attacks.
  - Some malware can detect sandbox environments.

### Prevention Measures

- **Salting and Hashing**:
  - Hashing converts information into unique values.
  - Salting adds random characters to hashed passwords, enhancing security.

- **Multi-factor Authentication (MFA) and Two-factor Authentication (2FA)**:
  - Require users to verify identity using multiple factors.
  - Factors include passwords, fingerprints, or one-time passwords.

- **CAPTCHA and reCAPTCHA**:
  - Differentiate between humans and automated bots.
  - Prevent brute force attacks by requiring users to complete tests.

- **Password Policies**:
  - Enforce good password practices.
  - Include complexity requirements, regular updates, and login attempt limits.

### Key Takeaways

- Brute force attacks involve guessing passwords through trial and error.
- Sandboxes and virtual machines are valuable tools for testing and simulating attacks.
- Preventive measures like hashing, MFA, CAPTCHA, and password policies help enhance security.

---
## Network hardening practices

- **Network security hardening:**
	- Port filtering
	- Network access privilege
	- Encryption

- **Task performed:**
	- Firewall rules maintenance
	- Network log analysis
	- Patch updates
	- Server backups

- **Network log analysis:**
	- The process of examining network logs to identify events of interest.

- **Security information and event management (SIEM):**
	- An application that collects and analyzes log data to monitor critical activities for an organization.

- **Port filtering:**
	- A firewall function that blocks or allows certain port numbers to limit unwanted communication.

---
## Network Security Applications

### Introduction

- Focus on network hardening and monitoring.
- Defense in depth: Adding layers of security to protect the network.

### Devices and Tools
#### Firewall

- Stateless, stateful, and next-generation firewalls (NGFWs).
- Inspect packet headers and payloads.
- Each system should have its own firewall.

#### Intrusion Detection System (IDS)

- Monitors system activity and alerts on possible intrusions.
- Detects known attacks based on signatures.
- Can identify anomalies, but may miss sophisticated attacks.
- Alerts administrators for further investigation.

#### Intrusion Prevention System (IPS)

- Monitors and actively stops intrusive activity.
- Offers more protection than IDS by blocking suspicious traffic.
- Inline appliance, potential for connection failure and false positives.

#### Full Packet Capture Devices

- Record and analyze all data transmitted over the network.
- Aid in investigating alerts from IDS.

#### Security Information and Event Management (SIEM)

- Collects and analyzes log data from multiple network devices.
- Provides a centralized dashboard for monitoring security events.
- Does not take actions to prevent suspicious events.

### Key Takeaways

| Devices/Tools               | Advantages                                                                                                      | Disadvantages                                                                                                        |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Firewall                    | - Allows or blocks traffic based on rules.                                                                      | - Limited to filtering packets based on header information.                                                          |
| Intrusion Detection System | - Alerts on possible intrusions and attacks.                                                                    | - May miss sophisticated attacks and doesn't stop incoming traffic.                                                   |
| Intrusion Prevention System| - Actively stops intrusive activity.                                                                            | - Inline appliance with potential connection failure and false positives.                                             |
| SIEM                        | - Collects and analyzes log data for centralized monitoring.                                                    | - Doesn't prevent suspicious events, only reports them.                                                               |

- Cost of devices/tools: Purchase, installation, and maintenance.
- Additional personnel may be required for monitoring.
- Decision-makers choose security levels based on cost and risk.

---
## Network security in the cloud

- **Cloud network:**
	- A collection of servers or computers that stores resources and data in a remote data center that can be accessed via the internet.

---
## Secure the Cloud

### Introduction

- **Cloud Computing**: Convenient, on-demand access to computing resources.

### Cloud Security Considerations
#### Identity Access Management (IAM)

- Manages digital identities and authorizes user access.
- Improper configuration of user roles poses security risks.

#### Configuration

- Each cloud service must be configured to meet security and compliance requirements.
- Misconfigured services are common sources of security issues.

#### Attack Surface

- Cloud service providers (CSPs) offer numerous applications, increasing attack surface.
- Proper network design can mitigate risks introduced by multiple services.

#### Zero-Day Attacks

- **Zero-Day Attacks**: Previously unknown exploits.
- CSPs often have mechanisms for detecting and mitigating zero-day attacks.

#### Visibility and Tracking

- CSPs offer tools like flow logs and packet mirroring for visibility.
- Organizations may have limited access compared to on-premise networks.

#### Rapid Changes

- CSPs regularly update their services, impacting security considerations.
- Organizations need to adapt IT processes to align with CSP updates.

### Shared Responsibility Model

- **Shared Responsibility Model**: CSPs responsible for cloud infrastructure, users for their assets and processes.
- Organizations must ensure proper configuration and adherence to security requirements.

### Key Takeaways

- Understand unique security considerations in the cloud.
- Familiarize with the shared responsibility model.
- Organizations responsible for configuring and maintaining security of their cloud services.

---
## Cloud Security and Cryptography

### Cloud Security Hardening

- **IAM (Identity Access Management)**:
  - Manages digital identities and access to cloud resources.
- **Hypervisors**:
  - Type one hypervisors commonly used by CSPs.
  - Misconfigurations can lead to security breaches.
- **Baselining**:
  - Establishes a reference point for monitoring cloud environment changes.
  - Examples: access controls, encryption, threat detection services.
- **Cryptography**:
  - Essential for securing data in the cloud.
  - Provides confidentiality and integrity.
- **Cryptographic Erasure**:
  - Destroys encryption keys to render data undecipherable.
  - Prevents unauthorized access to deleted data.
- **Key Management**:
  - Securely manages encryption keys.
  - Techniques: TPM, CloudHSM.

### Shared Responsibility Model

- **Cloud Service Provider (CSP)**:
  - Manages underlying infrastructure.
  - Provides regular patches and updates.
- **Customer Responsibility**:
  - Secures data and manages encryption keys.
  - Can request audits and security reports from CSP.
- **Benefits**:
  - Customers not solely responsible for cryptographic infrastructure maintenance.

### Key Takeaways

- Cloud security hardening is critical for assessing and improving security in public cloud environments.
- IAM, baselining, hypervisor security, cryptography, and cryptographic erasure are key methods for securing cloud infrastructure.

---
## **Cybersecurity Terms and Concepts**

| Term                                             | Definition                                                                                                                                  |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| Baseline Configuration                           | A documented set of specifications within a system that is used as a basis for future builds, releases, and updates.                        |
| Hardware                                         | The physical components of a computer system.                                                                                               |
| Multi-factor Authentication                      | A security measure that requires a user to verify their identity in two or more ways to access a system or network.                         |
| Network Log Analysis                             | The process of examining network logs to identify events of interest, such as security breaches or anomalies.                               |
| Operating System (OS)                            | The software that manages computer hardware resources and provides services to computer programs.                                           |
| Patch Update                                     | A software and operating system update that addresses security vulnerabilities within a program or product.                                 |
| Penetration Testing (Pen Test)                   | A simulated attack conducted to identify vulnerabilities in systems, networks, websites, applications, and processes.                       |
| Security Hardening                               | The process of strengthening a system to reduce its vulnerabilities and attack surface.                                                     |
| Security Information and Event Management (SIEM) | An application that collects and analyzes log data to monitor critical activities for an organization, such as security events and threats. |
| World-Writable File                              | A file that can be altered by anyone with write permissions, potentially posing a security risk if improperly configured.                   |

---