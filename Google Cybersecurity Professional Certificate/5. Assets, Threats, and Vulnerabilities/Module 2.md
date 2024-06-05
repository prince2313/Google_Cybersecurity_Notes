# Protect organizational assets
## Security controls

- **Security controls:**
	- Safeguards designed to reduce specific security risks.

- **Types of security controls:**
	- Technical.
	- Operational.
	- Managerial.

- **Information privacy:**
	- The protection of unauthorized access and distribution of data.

- **Data owner:**
	- The person that decides who can access, edit, use, or destroy their information.

- **Data custodian:**
	- Anyone or anything that’s responsible for the safe handling, transport, and storage of information.

---
## Principle of Least Privilege (PoLP)

### Overview

- Security concept to minimize risk by granting users the minimum level of access needed.
- Supports the confidentiality, integrity, and availability (CIA) triad of information security.

### Limiting Access Reduces Risk

- Reduces data breaches, accidental modifications, and tampering.
- Key benefits:
    - Limits access to sensitive information.
    - Reduces chances of accidental data modification, tampering, or loss.
    - Supports system monitoring and administration.
- Connects specific resources to specific users with defined limits.
- First step: Clearly define who or what the users are.

### Determining Access and Authorization

- Key questions:
    1. Who is the user?
    2. How much access do they need to a specific resource?
- User types:
    - **Guest accounts:** External users (customers, clients, contractors, business partners).
    - **User accounts:** Staff based on job duties.
    - **Service accounts:** Applications or software interacting with the network.
    - **Privileged accounts:** Elevated permissions or administrative access.
- Best practices:
    - Establish a baseline access level for each account type.
    - Access levels should be dynamic and change as needed.
    - Consistent and routine monitoring is essential.

**Pro tip:** Strong passwords are crucial for maintaining security even with PoLP.
### Auditing Account Privileges

- Regular audits are key to maintaining security.
- Types of audits:
    - **Usage Audits:**
        - Review resources accessed by each account and activities performed.
        - Ensure compliance with security policies.
        - Identify unnecessary privileges for revocation.
    - **Privilege Audits:**
        - Address "privilege creep" where users accumulate excessive access over time.
        - Ensure alignment of user roles with their access rights.
    - **Account Change Audits:**
        - Review logs and records of changes to user accounts.
        - Detect unauthorized changes and ensure legitimacy of modifications.
        - Directory services can alert administrators of suspicious activities.

### Key Takeaways

- PoLP reduces the risk of unauthorized access to sensitive information.
- Implementation involves setting up user accounts with appropriate access levels.
- Regular audits are crucial for maintaining security.
- Helps maintain confidentiality, integrity, and availability of information.

---
## Data Lifecycle and Governance

### Data Lifecycle

- **Collect**
- **Store**
- **Use**
- **Archive**
- **Destroy**
- Each stage requires specific security measures.

### Data Governance

- **Definition**: Set of processes for managing information.
- **Includes**:
  - Policies for privacy, accuracy, availability, and security.
- **Roles**:
  - Data Owner: Decides access, editing, usage, and destruction.
  - Data Custodian: Handles safe handling, transport, and storage.
  - Data Steward: Implements governance policies.

### Protecting Data

- **Data Governance Policy**: Defines procedures for data safety.
- **Responsibility**: Data custodians ensure data integrity and security.

### Legally Protected Information

- **PII (Personally Identifiable Information)**: Used to infer identity.
- **PHI (Protected Health Information)**: Regulated by HIPAA (US) and GDPR (EU).
- **SPII (Sensitive Personally Identifiable Information)**: Requires stricter handling.
- **Regulatory Guidelines**: Governments specify data protection rules.

### Key Takeaways

- Data privacy and security are paramount.
- Data custodians play a crucial role.
- Legal regulations dictate protection standards.

---
## Information Privacy: Regulations and Compliance

### Information Security vs. Information Privacy

- **Information Privacy**:
  - Protects unauthorized access and distribution of data.
- **Information Security** (InfoSec):
  - Keeps data away from unauthorized users.
- **Difference**: Privacy provides control over personal data, while security protects data from threats.

### Why Privacy Matters in Security

- **Increased Attention**: Data privacy gained prominence in the late 1990s.
- **Concerns**: Data misuse, abuse, and security vulnerabilities.
- **Response**: Transparency, data protection measures.

### Notable Privacy Regulations

- **GDPR (General Data Protection Regulation)**:
  - EU regulation giving data owners control over personal information.
- **PCI DSS (Payment Card Industry Data Security Standard)**:
  - Security standards for credit and debit card transactions.
- **HIPAA (Health Insurance Portability and Accountability Act)**:
  - U.S. law protecting patient health information.

#### GDPR

- Applies to any business handling EU citizen data.
- Personal information includes name, address, financial, and medical data.

#### PCI DSS

- Focuses on securing financial transactions against data theft and fraud.

#### HIPAA

- Requires protection of sensitive patient health information.

### Security Assessments and Audits

- **Security Audit**:
  - Reviews security controls against expectations.
- **Security Assessment**:
  - Checks security resilience against threats.
- **Importance**: Validates compliance and demonstrates commitment to privacy.

### Key Takeaways

- Organizations prioritize data protection for maintaining customer trust.
- Security assessments and audits evaluate security gaps.
- Overlooking assessment results can lead to fines or data breaches.

---
## Fundamentals of cryptography

- **Personally identifiable information (PII):**
	- Any information used to infer an individual's identity.

- **Cryptography:**
	- The process of transforming information into a form that unintended readers can’t understand.

- **Cipher:**
	- An algorithm that encrypts information.

- **Algorithm:**
	- A set of rules used to solve a problem.

- **Cryptographic key:**
	- A mechanism that decrypts ciphertext.

- **Brute force attack:**
	- The trial and error process of discovering private information.

---
## Public key infrastructure

- **Public key infrastructure (PKI):**
	- An encryption framework that secures the exchange of online information.

- **Public key infrastructure process:**
	- Exchange of encrypted information.
	- Establish trust using a system of digital certificate.

- **Asymmetric encryption:**
	- The use of a public and private key pair for encryption and decryption of data.

- **Symmetric encryption:**
	- The use of a single secret key to exchange information.

- **Digital certificate:**
	- A file that verifies the identity of a public key holder.

---
## Symmetric and Asymmetric Encryption

### Types of Encryption

#### Symmetric Encryption

- Uses a single secret key for encryption and decryption.
- Sender and receiver must know the secret key.
- Examples: Triple DES, AES.

#### Asymmetric Encryption

- Uses a public and private key pair.
- Public key encrypts data, private key decrypts it.
- Examples: RSA, DSA.

#### The Importance of Key Length

- Longer key lengths provide more security against brute force attacks.
- Longer keys mean more possibilities for attackers to try.
- Drawback: Slower processing times.

### Approved Algorithms

#### Symmetric Algorithms

- **Triple DES (3DES)**:
  - Generates 192-bit keys.
  - Derived from Data Encryption Standard (DES).
- **Advanced Encryption Standard (AES)**:
  - Generates 128, 192, or 256-bit keys.
  - Highly secure, resistant to brute force attacks.

#### Asymmetric Algorithms

- **RSA (Rivest Shamir Adleman)**:
  - Generates key sizes of 1,024, 2,048, or 4,096 bits.
  - Creates public and private key pair.
- **DSA (Digital Signature Algorithm)**:
  - Generates 2,048-bit keys.
  - Widely used in public key infrastructure.

#### Generating Keys

- Implemented using tools like OpenSSL.
- OpenSSL is open-source and commonly used for generating keys.

### Obscurity is Not Security

- Cipher details should be knowable without sacrificing security.
- Custom encryption algorithms can be risky if not properly vetted.
- Encryption systems should not rely on secrecy of algorithm.

### Encryption is Everywhere

- Companies use both symmetric and asymmetric encryption.
- Asymmetric encryption secures important data, symmetric for speed.
- Compliance regulations like FIPS 140-3 and GDPR mandate encryption.

### Key Takeaways

- Symmetric encryption uses a single key, asymmetric uses a key pair.
- Key length affects security against brute force attacks.
- Compliance regulations drive encryption adoption.

---
## Non-repudiation and hashing

- **Hash function:**
	- An algorithm that produces a code that can’t be decrypted.

- **Non-repudiation:**
	- The concept that the authenticity of information can’t be denied.

---
## The Evolution of Hash Functions

### Origins of Hashing

#### Hash functions initially developed for data searching and representation.

- Hash tables used for efficient data storage and retrieval.
- Early hash function: MD5 (Message Digest 5), developed by Ronald Rivest.

#### MD5

- Converts data into a 128-bit value (32 characters).
- Vulnerable to hash collisions: different inputs produce the same hash value.

### Next-generation Hashing

#### Secure Hashing Algorithms (SHAs)

- Developed to address MD5 vulnerabilities.
- SHA family includes SHA-1, SHA-224, SHA-256, SHA-384, and SHA-512.
- Hash values range from 160 to 512 bits.
- Collision-resistant, approved by NIST.

### Secure Password Storage

#### Hashing Passwords

- Passwords stored as hashed values in databases.
- Prevents plaintext exposure in case of database breaches.

#### Rainbow Tables

- Pre-generated tables of hash values and corresponding plaintext.
- Used by attackers to crack hashed passwords.

### Adding Some "Salt"

#### Salting

- Random string added to data before hashing.
- Increases uniqueness of hash values.
- Prevents rainbow table attacks.

### Key Takeaways

- Hash functions crucial for authentication and data integrity.
- MD5 vulnerable to collisions and rainbow table attacks.
- Next-gen hashing algorithms like SHA provide greater security.
- Salting enhances hash function resilience against attacks.

---
## Access controls and authentication systems

- **Access controls:**
	- Security controls that manage access, authorization, and accountability of information.

- **AAA framework:**
	- Authentication
	- Authorization
	- Accounting

- **Factors of authentication:**
	- **Knowledge:**
		- something the user knows.
	- **Ownership:**
		- something the user possesses.
	- **Characteristic:**
		- something the user is.

- **Single Sign-On (SSO):**
	- A technology that combines several different logins into one.

- **Multi-factor authentication (MFA):**
	- A security measure that requires a user to verify their identity in two or more ways to access a system or network.

---
## The Rise of SSO and MFA

### A Better Approach to Authentication

#### Single Sign-On (SSO)

- Combines multiple logins into one.
- Improves user experience, reduces costs, and enhances security.
- Addresses "password fatigue" by simplifying authentication.

##### How SSO Works

- Automates trust establishment between user and service provider.
- Relies on trusted third-parties and encrypted access tokens.
- Common protocols: LDAP and SAML.

### Limitations of SSO

#### Risk Associated with Single Authentication

- Vulnerable to password-related risks.
- Loss or theft of password can expose multiple services.

### MFA to the Rescue

#### Multi-Factor Authentication (MFA)

- Requires two or more forms of identification to access a system or network.
- Enhances security by requiring additional proof of identity.

##### Strengthening Authentication

- Users must provide multiple factors:
  - Something they know (e.g., password).
  - Something they have (e.g., one-time passcode).
  - Something they are (e.g., biometric data).

### Key Takeaways

- SSO simplifies authentication but may not provide sufficient security alone.
- MFA adds an extra layer of security by requiring multiple forms of identification.
- Combining SSO and MFA improves security without compromising user experience.

---
## The mechanisms of authorization

- **Separation of duties:**
	- The principle that users should not be given levels of authorization that would allow them to misuse a system.

- **Basic auth:**
	- The technology used to establish a user’s request to access a server.

- **OAuth:**
	- An open-standard authorization protocol that shares designated access between applications.

- **Application programming interface (API) token:**
	- A small block of encrypted code that contains information about a user.

---
## Why we audit user activity

- **Session:**
	- A sequence of network HTTP basic auth requests and responses associated with the same user.

- **Session cookie:**
	- A token that websites use to validate a session and determine how long that session should last.

- **Session hijacking:**
	- An event when attackers obtain a legitimate user’s session ID.

- **Session ID:**
	- A unique token that identifies a user and their device while accessing a system.

---
## Identity and Access Management

### Understanding Security Principles

#### Principle of Least Privilege

- Grants users only the minimum level of access required.
- Helps limit potential damage from security breaches.

#### Separation of Duties

- Ensures users are not given authorization levels to misuse systems.
- Works in conjunction with least privilege to enhance security.

### IAM Framework

#### Basics of Identity and Access Management (IAM)

- Collection of processes and technologies for managing digital identities.
- Aims to authenticate users, determine access privileges, and track activities.

#### Authentication

- Involves proving a user's identity through factors like knowledge, ownership, and characteristic.
- Implemented using single sign-on (SSO) and multi-factor authentication (MFA).

#### User Provisioning

- Process of creating and maintaining a user's digital identity.
- Includes provisioning and deprovisioning users as per organization's policies.

#### Authorization

- Determines access privileges using frameworks like Mandatory Access Control (MAC), Discretionary Access Control (DAC), and Role-Based Access Control (RBAC).

### Access Control Technologies

#### Seamless User Experience

- Authentication and authorization often perceived as a single experience due to integrated access control technologies.

#### Third-Party Solutions

- Many organizations opt for third-party IAM solutions offering a suite of tools.
- Custom in-house solutions require significant time and resources.

### Key Takeaways

- IAM and AAA frameworks ensure the right user accesses the right resources at the right time.
- Security analysts play crucial roles in user provisioning and collaborating with IAM or AAA teams.
- Familiarity with IAM models aids in achieving security objectives and maintaining a secure environment.

### Resources for More Information

- [IDPro](https://idpro.org/):
	- Professional organization dedicated to sharing essential IAM industry knowledge.

---
## **Cybersecurity Terms and Concepts**

| Term                                   | Definition                                                                                   |
|----------------------------------------|----------------------------------------------------------------------------------------------|
| Access controls                        | Security controls that manage access, authorization, and accountability of information     |
| Algorithm                              | A set of rules used to solve a problem                                                      |
| Application programming interface (API) token | A small block of encrypted code that contains information about a user                |
| Asymmetric encryption                  | The use of a public and private key pair for encryption and decryption of data              |
| Basic auth                             | The technology used to establish a user’s request to access a server                        |
| Bit                                    | The smallest unit of data measurement on a computer                                         |
| Brute force attack                     | The trial and error process of discovering private information                              |
| Cipher                                 | An algorithm that encrypts information                                                      |
| Cryptographic key                      | A mechanism that decrypts ciphertext                                                        |
| Cryptography                           | The process of transforming information into a form that unintended readers can’t understand |
| Data custodian                         | Anyone or anything that’s responsible for the safe handling, transport, and storage of information |
| Data owner                             | The person that decides who can access, edit, use, or destroy their information              |
| Digital certificate                    | A file that verifies the identity of a public key holder                                    |
| Encryption                             | The process of converting data from a readable format to an encoded format                  |
| Hash collision                         | An instance when different inputs produce the same hash value                               |
| Hash function                          | An algorithm that produces a code that can’t be decrypted                                   |
| Hash table                             | A data structure that's used to store and reference hash values                             |
| Identity and access management (IAM)   | A collection of processes and technologies that helps organizations manage digital identities in their environment |
| Information privacy                    | The protection of unauthorized access and distribution of data                              |
| Multi-factor authentication (MFA)     | A security measure that requires a user to verify their identity in two or more ways to access a system or network |
| Non-repudiation                       | The concept that the authenticity of information can’t be denied                             |
| OAuth                                  | An open-standard authorization protocol that shares designated access between applications    |
| Payment Card Industry Data Security Standards (PCI DSS) | A set of security standards formed by major organizations in the financial industry  |
| Personally identifiable information (PII) | Any information used to infer an individual's identity                                  |
| Principle of least privilege           | The concept of granting only the minimal access and authorization required to complete a task or function |
| Protected health information (PHI)    | Information that relates to the past, present, or future physical or mental health or condition of an individual |
| Public key infrastructure (PKI)       | An encryption framework that secures the exchange of online information                     |
| Rainbow table                          | A file of pre-generated hash values and their associated plaintext                          |
| Salting                                | An additional safeguard that’s used to strengthen hash functions                            |
| Security assessment                    | A check to determine how resilient current security implementations are against threats      |
| Security audit                         | A review of an organization's security controls, policies, and procedures against a set of expectations |
| Security controls                      | Safeguards designed to reduce specific security risks                                         |
| Separation of duties                   | The principle that users should not be given levels of authorization that would allow them to misuse a system |
| Session                                | A sequence of network HTTP basic auth requests and responses associated with the same user    |
| Session cookie                         | A token that websites use to validate a session and determine how long that session should last |
| Session hijacking                      | An event when attackers obtain a legitimate user’s session ID                                |
| Session ID                             | A unique token that identifies a user and their device while accessing a system              |
| Single Sign-On (SSO)                   | A technology that combines several different logins into one                                 |
| Symmetric encryption                  | The use of a single secret key to exchange information                                       |
| User provisioning                      | The process of creating and maintaining a user's digital identity                            |

---