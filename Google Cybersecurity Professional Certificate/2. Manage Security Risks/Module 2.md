# Security frameworks and controls
## The relationship between frameworks and controls

### Frameworks and controls

- **Security frameworks**:
  - Guidelines for building plans to mitigate risk and threats to data and privacy.
  - Support organizations’ ability to adhere to compliance laws and regulations.
  
- **Security controls**:
  - Safeguards designed to reduce specific security risks.
  - Measures used to lower risk and threats to data and privacy.

### Specific frameworks and controls

#### Cyber Threat Framework (CTF)

- Developed by the U.S. government to provide a common language for describing and communicating information about cyber threat activity.
- Helps cybersecurity professionals analyze and share information more efficiently.

#### International Organization for Standardization/International Electrotechnical Commission (ISO/IEC) 27001

- Internationally recognized framework for managing the security of assets across sectors and sizes.
- Outlines requirements for an information security management system, best practices, and controls.

#### Controls

- Used alongside frameworks to reduce the possibility and impact of security threats.
- Can be physical, technical, and administrative.
- Examples:
  - Physical controls: Gates, fences, locks, security guards, CCTV, access cards.
  - Technical controls: Firewalls, MFA, antivirus software.
  - Administrative controls: Separation of duties, authorization, asset classification.

### Key takeaways

- Frameworks and controls establish an organization’s security posture and support meeting security goals and compliance requirements.
- While voluntary, implementing these frameworks and controls is strongly encouraged to ensure the safety of critical assets.

---
## Use the CIA triad to protect organizations

### The CIA triad for analysts

- **CIA triad**:
    - Model informing risk considerations.
    - Comprises confidentiality, integrity, and availability.
    - Aids in establishing security posture.

#### **Confidentiality**

- **Confidentiality**:
    - Authorized user access to assets/data.
    - Enhanced via principles like least privilege.
    - Limits access to required information only.

#### **Integrity**

- **Integrity**:
    - Data correctness, authenticity, reliability.
    - Verification protocols essential.
    - Cryptography ensures data transformation to prevent tampering.

#### **Availability**

- **Availability**:
    - Authorized data accessibility.
    - Systems allowing data use when needed.
    - Remote employee access with limited data based on job role.

### Key takeaways

- **CIA triad** essential for security posture.
- Understanding aids in comprehending security team efforts in safeguarding organizations and stakeholders.

---
## NIST Cybersecurity Framework (CSF) and its 5 Functions

### NIST Cybersecurity Framework (CSF)

- Developed by the National Institute of Standards and Technology (NIST).
- Provides guidance on improving cybersecurity risk management.
- Comprises a set of best practices, standards, and guidelines.

### 5 Functions of NIST CSF

#### Identify

- Understand assets, data, and systems requiring protection.
- Develop risk management strategy.
- Prioritize resources based on risk assessment.

#### Protect

- Implement safeguards to ensure delivery of critical services.
- Include access controls, awareness training, and data security measures.
- Establish protective measures to mitigate risks.

#### Detect

- Develop capabilities to identify cybersecurity events promptly.
- Implement monitoring systems, anomaly detection tools, and incident response plans.
- Enable timely discovery of cybersecurity breaches.

#### Respond

- Develop and implement incident response plans.
- Take immediate action to contain and mitigate cybersecurity incidents.
- Communicate effectively with stakeholders during incident response.

#### Recover

- Develop resilience and recovery strategies.
- Restore systems and services affected by cybersecurity incidents.
- Learn from incidents to improve future response and recovery efforts.

---
## More about OWASP security principles

### Security principles

- Embedded in daily tasks: Used while analyzing logs, monitoring SIEM dashboards, or using a vulnerability scanner.

#### Previously Introduced OWASP Security Principles

1. **Minimize attack surface area**: Reduce potential vulnerabilities.
2. **Principle of least privilege**: Users have minimal access necessary for tasks.
3. **Defense in depth**: Implement various security controls.
4. **Separation of duties**: Critical actions require multiple individuals with least privilege.
5. **Keep security simple**: Avoid complex solutions.
6. **Fix security issues correctly**: Identify root causes, contain impacts, remediate vulnerabilities.

#### Additional OWASP Security Principles

1. **Establish secure defaults**: Optimal security state is default; extra work needed to make it insecure.
2. **Fail securely**: When control fails, defaults to most secure option.
3. **Don’t trust services**: Verify security of third-party partners.
4. **Avoid security by obscurity**: Security shouldn't depend on keeping details hidden.

### Key Takeaways

- **Applied by cybersecurity professionals**: Safeguard organizations and users.
- **Promote safe development practices**: Reduce risks for companies and users.

---
## **Plan a security audit**

- **Purpose of internal security audits:**
	- Identify organizational risk
	- Assess controls
	- Correct compliance issue

- **Common elements of internal audits:**
	- Establishing the scope and goals
	- Conducting a risk assessment
	- Completing a controls assessment
	- Assessing compliance
	- Communicating results

- **Audit questions:**
	- What is the audit meant to achieve?
	- Which assets are most at risk?
	- Are current controls sufficient to protect those assets?
	- What controls and compliance regulations need to be implemented?

- **Stakeholder Communication:**
	- Summarizes the scope and goals.
	- Lists existing risks.
	- Notes how quickly those risks need to be addressed.
	- Identifies compliance regulations.
	- Provides recommendations.

---
## Security Audits

### Definition and Purpose

- Review of organization's security controls, policies, and procedures.
- Ensure meeting internal and external criteria.
- Identify threats, risks, and vulnerabilities.
- Maintain security posture and remediate issues.

### Factors Influencing Audits

- Industry type
- Organization size
- Regulatory compliance
- Geographical location

### Role of Frameworks and Controls

- NIST CSF, ISO 27000 aid in compliance.
- Frameworks guide implementation of controls.
- Controls: administrative, technical, physical.

### Audit Checklist

- Define scope
  - List assets
  - Audit goals
  - Frequency
- Risk assessment
- Conduct audit
- Mitigation plan
- Communicate results to stakeholders

### Key Takeaways

- Understand security audits, frameworks, controls, compliance.
- Foundation for effective auditing.

### Resources

- [NIST Assessment and Auditing Resources](https://www.nist.gov/cyberframework/assessment-auditing-resources)
- [IT Disaster Recovery Plan](https://www.ready.gov/it-disaster-recovery-plan)
- To review common compliance regulations, refer to [the reading about controls, frameworks, and compliance](https://www.coursera.org/learn/foundations-of-cybersecurity/supplement/xu4pr/controls-frameworks-and-compliance).
- Link to template: [Control categories](https://docs.google.com/document/d/1Ut_H5A9FHwuQEy6_qG6Lfy3zwF6GSJnj3DZTMaNRWEE/template/preview?resourcekey=0-i4dR5qZFqQyfzr8uk3OOmA)

---
## **Cybersecurity Terms and Concepts**

| Term                                                                                      | Definition                                                                                                                                                                                  |
| ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Asset                                                                                     | An item perceived as having value to an organization.                                                                                                                                       |
| Attack vectors                                                                            | The pathways attackers use to penetrate security defenses.                                                                                                                                  |
| Authentication                                                                            | The process of verifying who someone is.                                                                                                                                                    |
| Authorization                                                                             | The concept of granting access to specific resources in a system.                                                                                                                           |
| Availability                                                                              | The idea that data is accessible to those who are authorized to access it.                                                                                                                  |
| Biometrics                                                                                | The unique physical characteristics that can be used to verify a person’s identity.                                                                                                         |
| Confidentiality                                                                           | The idea that only authorized users can access specific assets or data.                                                                                                                     |
| Confidentiality, integrity, availability (CIA) triad                                      | A model that helps inform how organizations consider risk when setting up systems and security policies.                                                                                    |
| Detect                                                                                    | A NIST core function related to identifying potential security incidents and improving monitoring capabilities.                                                                             |
| Encryption                                                                                | The process of converting data from a readable format to an encoded format.                                                                                                                 |
| Goals                                                                                     | Goals are an outline of the organization's security objectives, or what they want to achieve in order to improve their security posture.                                                    |
| Identify                                                                                  | A NIST core function related to management of cybersecurity risk and its effect on an organization’s people and assets.                                                                     |
| Integrity                                                                                 | The idea that the data is correct, authentic, and reliable.                                                                                                                                 |
| National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF)       | A voluntary framework that consists of standards, guidelines, and best practices to manage cybersecurity risk.                                                                              |
| National Institute of Standards and Technology (NIST) Special Publication (S.P.) 800-53   | A unified framework for protecting the security of information systems within the U.S. federal government.                                                                                  |
| Open Web Application Security Project/Open Worldwide Application Security Project (OWASP) | A non-profit organization focused on improving software security.                                                                                                                           |
| Protect                                                                                   | A NIST core function used to protect an organization through the implementation of policies, procedures, training, and tools.                                                               |
| Recover                                                                                   | A NIST core function related to returning affected systems back to normal operation.                                                                                                        |
| Respond                                                                                   | A NIST core function related to making sure that the proper procedures are used to contain, neutralize, and analyze security incidents, and implement improvements to the security process. |
| Risk                                                                                      | Anything that can impact the confidentiality, integrity, or availability of an asset.                                                                                                       |
| Scope                                                                                     | Scope refers to the specific criteria of an internal security audit.                                                                                                                        |
| Security audit                                                                            | A review of an organization's security controls, policies, and procedures against a set of expectations.                                                                                    |
| Security controls                                                                         | Safeguards designed to reduce specific security risks.                                                                                                                                      |
| Security frameworks                                                                       | Guidelines used for building plans to help mitigate risk and threats to data and privacy.                                                                                                   |
| Security posture                                                                          | An organization’s ability to manage its defense of critical assets and data and react to change.                                                                                            |
| Threat                                                                                    | Any circumstance or event that can negatively impact assets.                                                                                                                                |
| Vishing                                                                                   | A type of social engineering attack where attackers use voice communication to deceive individuals into providing sensitive information or performing actions.                              |

---