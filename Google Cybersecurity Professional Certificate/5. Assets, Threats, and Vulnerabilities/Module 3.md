# Vulnerabilities in system
## Vulnerability management

- **Vulnerability:**
	- A weakness that can be exploited by a threat.

- **Exploit:**
	- A way of taking advantage of a vulnerability.

- **Vulnerability management:**
	- The process of finding and patching vulnerabilities.

- **Vulnerability management:**
	- Identify vulnerabilities
	- Consider potential exploits
		- Prepare defenses threats
		- Evaluate those defenses

- **Zero-day:**
	- An exploit that was previously unknown.

---
## Defense in depth strategy

- **Defense in depth:**
	- A layered approach to vulnerability management that reduces risk.

- **Defense in depth strategy:**
	- Perimeter layer
	- Network layer
	- Endpoint layer
	- Application layer
	- Data layer

---
## Common vulnerabilities and exposures

- **Exposure:**
	- A mistake that can be exploited by a threat.

- **Common Vulnerabilities and Exposures (CVE®) list:**
	- An openly accessible dictionary of known vulnerabilities and exposures.

- **MITRE:**
	- A collection of non-profit research and development centers.

- **CVE Numbering Authority (CNA):**
	- An organization that volunteers to analyze and distribute information on eligible CVEs.

- **Common Vulnerability Scoring System (CVSS):**
	- A measurement system that scores the severity of a vulnerability.

---
## The OWASP Top 10
### What is OWASP?

- Nonprofit foundation focused on improving software security.
- Open platform for sharing information, tools, and events related to web security.

### The OWASP Top 10

- Published since 2003 to spread awareness of the web’s most targeted vulnerabilities.
- Mainly applies to new or custom-made software.
- Referenced by many large organizations during application development to address common security mistakes.
- Updated every few years based on evolving technologies and the prevalence and risk level of vulnerabilities.

#### Notes

- OWASP’s Top 10 is also used by auditors for regulatory compliance checks.
- [OWASP Top 10](https://owasp.org/www-project-top-ten/) is a useful resource.

### Common Vulnerabilities

Businesses make critical security decisions based on the OWASP Top 10, influencing the design of new software on their network.

#### Broken Access Control

- Limits what users can do in a web application.
- Failures can lead to unauthorized information disclosure, modification, or destruction.
- Example: Unauthorized access to other business applications.

#### Cryptographic Failures

- Protecting information is crucial, as mandated by laws like GDPR.
- Vulnerabilities occur when sensitive data isn’t properly encrypted.
- Example: Using weak hashing algorithms like MD5 increases data breach risk.

#### Injection

- Malicious code inserted into a vulnerable application.
- Can provide attackers with backdoor access to information systems.
- Common target: Website login forms.

#### Insecure Design

- Applications need to be resilient to attacks.
- Insecure design includes missing or poorly implemented security controls.
- Vulnerabilities like injection attacks or malware infections are more likely.

#### Security Misconfiguration

- Security settings not properly set or maintained.
- Common in interconnected systems that aren’t properly set up or audited.
- Example: Deploying network servers with default settings.

#### Vulnerable and Outdated Components

- Relates to the use of open-source libraries in application development.
- Applications using unmaintained, vulnerable components are at greater risk.
- Maintained by volunteer programmer communities.

#### Identification and Authentication Failures

- Applications fail to properly recognize users and their authorization levels.
- Example: Home Wi-Fi router login failures leading to unauthorized network access.

#### Software and Data Integrity Failures

- Inadequately reviewed updates or patches can be exploited.
- Can lead to supply chain attacks, affecting multiple third parties.
- Example: SolarWinds cyber attack (2020).

#### Security Logging and Monitoring Failures

- Logging and tracing events is crucial for identifying and fixing problems.
- Sufficient monitoring and incident response are essential.

#### Server-Side Request Forgery (SSRF)

- Attackers manipulate server operations to access unauthorized resources.
- Possible when an application on the server is vulnerable.
- Example: Malicious code in a vulnerable app fetching unauthorized data from the server.

### Key Takeaways

- Staying informed about cybersecurity trends is crucial for defending against attacks and preparing for future risks.
- OWASP’s Top 10 is a valuable resource for understanding common vulnerabilities.

### Resources

- [OWASP Top 10](https://owasp.org/www-project-top-ten/)

---
## Open Source Intelligence
### Information vs Intelligence

- **Information**: Collection of raw data or facts about a specific subject.
- **Intelligence**: Analysis of information to produce knowledge or insights to support decision-making.

#### Example

- New information about an OS update.
- Intelligence derived from researching cybersecurity news linking new threats to the OS update.

### Intelligence Improves Decision-Making

- Businesses use information to gain insights into customer behavior.
- In security, open-source information provides insights into threats and vulnerabilities.

#### Uses of OSINT in InfoSec

- Provide insights into cyber attacks.
- Detect potential data exposures.
- Evaluate existing defenses.
- Identify unknown vulnerabilities.

#### Example

- InfoSec team monitors forums for emerging vulnerabilities.
- Use findings to prioritize patching and implement safeguards.

### OSINT Tools

- **VirusTotal**: Analyzes suspicious files, domains, URLs, and IP addresses for malicious content.
    - [VirusTotal](https://www.virustotal.com/gui/home/upload)

- **MITRE ATT&CK**: Knowledge base of adversary tactics and techniques based on real-world observations.
    - [MITRE ATT&CK](https://attack.mitre.org/)

- **OSINT Framework**: Web-based interface for finding OSINT tools for various sources or platforms.
    - [OSINT Framework](https://osintframework.com/)

- **Have I Been Pwned**: Searches for breached email accounts.
    - [Have I Been Pwned](https://haveibeenpwned.com/)

### Key Takeaways

- Gathering information and intelligence are critical aspects of cybersecurity.
- OSINT is used to make evidence-based decisions to prevent attacks.
- Security professionals need to be skilled at searching for information.
- Familiarity with popular OSINT tools and resources will ease the process of gathering information and collecting intelligence.

---
## Vulnerability assessments

- **Vulnerability assessment:**
	- The internal review process of a company’s security systems.

- **Vulnerability assessment process:**
	- Identification
	- Vulnerability analysis
	- Risk assessment
	- Remediation

---
## Approaches to Vulnerability Scanning
### What is a Vulnerability Scanner?

- **Vulnerability Scanner**: Software that automatically compares known vulnerabilities and exposures against the technologies on the network. These tools scan systems to find misconfigurations or programming flaws.
  
#### Attack Surfaces

1. **Perimeter layer**: Authentication systems that validate user access
2. **Network layer**: Technologies like network firewalls and others
3. **Endpoint layer**: Devices on a network, like laptops, desktops, or servers
4. **Application layer**: Software that users interact with
5. **Data layer**: Any information that’s stored, in transit, or in use

- The scanning tool compares findings against databases of security threats.
- Vulnerability databases are routinely updated by the company that designed the scanning software.

### Performing Scans

- Vulnerability scanners are meant to be non-intrusive, simply scanning a surface and alerting to any potentially unlocked doors in systems.
- Note: Vulnerability scanners can inadvertently cause issues, like crashing a system.

#### External vs. Internal Scans

- **External scans**: Test the perimeter layer outside of the internal network. Uncover vulnerable network ports or servers.
- **Internal scans**: Examine internal systems, analyzing application software for weaknesses in handling user input.

#### Authenticated vs. Unauthenticated Scans

- **Authenticated scans**: Test a system by logging in with a real user account or admin account to check for vulnerabilities like broken access controls.
- **Unauthenticated scans**: Simulate external threat actors without access to business resources, checking if unauthorized access is possible.

#### Limited vs. Comprehensive Scans

- **Limited scans**: Analyze particular devices on a network, such as firewalls.
- **Comprehensive scans**: Analyze all devices connected to a network, including operating systems and user databases.

- **Pro tip**: Discovery scanning should be done prior to limited or comprehensive scans to get an idea of the computers, devices, and open ports on a network.

### Key Takeaways

- Finding vulnerabilities requires thinking of all possibilities.
- Vulnerability scans vary depending on the surfaces that an organization is evaluating.
- Seasoned security professionals often lead the effort of configuring and performing scans to create a security profile.
- Analysts play an important role in interpreting scan results, leading to renewed compliance efforts, procedural changes, and system patching.

**Tip**: To explore vulnerability scanner software commonly used in the cybersecurity industry, search for terms like “popular vulnerability scanner software” and “open source vulnerability scanner software used in cybersecurity”.

---
## The Importance of Updates

- **Patching Gaps in Security:**
  - An outdated computer is like a house with unlocked doors, inviting unauthorized access. Updates act as locks to keep intruders out.
  - **Patch Update:** Addresses security vulnerabilities within a program or product, often containing bug fixes for common security issues.

### Common Update Strategies

- **Manual Updates:**
  - Advantages: Allows control over updates.
  - Disadvantages: Risk of forgetting critical updates.

- **Automatic Updates:**
  - Pro tip: Recommended by CISA.
  - Advantages: Simplifies deployment, keeps systems current.
  - Disadvantages: Potential instability if patches are not thoroughly tested.

### End-of-Life Software

- Some software reaches end-of-life (EOL) when developers cease support for older versions.
- [CISA recommends discontinuing the use of EOL software](https://www.cisa.gov/news-events/news/understanding-patches-and-software-updates) due to unfixable risks.
- Risks of EOL software increase with the proliferation of connected devices, such as IoT devices.
- **Note:** Patches and updates differ from upgrades, which refer to entirely new versions of software or hardware.

#### Key Takeaways

- Regular updates and patching are essential for cybersecurity.
- WannaCry attack of 2017 illustrates the importance of updates, as it could have been prevented with timely patching.

---
## Penetration Testing

- **Penetration Testing Overview:**
    - Simulated attacks to identify vulnerabilities in systems, networks, websites, and applications.
    - Mimics real-life attacks using tools and techniques of malicious actors.
    - Considered ethical hacking as it's authorized.

### Learning Approaches

- **Red Team Tests:**
    - Simulate attacks to identify vulnerabilities.
- **Blue Team Tests:**
    - Focus on defense and incident response.
- **Purple Team Tests:**
    - Collaborative approach combining elements of red and blue team exercises.

### Penetration Testing Strategies

- **Open-Box Testing:**
    - Tester has privileged access and knowledge of internal systems.
- **Closed-Box Testing:**
    - Tester has minimal to no access to internal systems, simulating external attackers.
- **Partial Knowledge Testing:**
    - Tester has limited access and knowledge, similar to a customer service representative.

### Skills for Penetration Testers

- Network and application security knowledge.
- Experience with operating systems, especially Linux.
- Proficiency in vulnerability analysis, threat modeling, and detection/response tools.
- Programming skills, particularly in Python and BASH.
- Strong communication skills for reporting findings.

#### Bug Bounty Programs

- Organizations offer financial rewards for reporting vulnerabilities.
- Opportunities for amateur security professionals to participate and enhance skills.
- [HackerOne](https://hackerone.com/bug-bounty-programs) is a platform with active bug bounties.

### Key Takeaways

- Penetration testing is crucial for identifying and addressing vulnerabilities in systems.
- Growing demand for specialized security professionals in penetration testing.
- Opportunities for skill development and career advancement in ethical hacking.

---
## Protect all entry points

- **Attack surface:**
	- All the potential vulnerabilities that a threat actor could exploit.

- **Security hardening:**
	- The process of strengthening a system to reduce its vulnerability and attack surface.

---
## Approach Cybersecurity with an Attacker Mindset

- **Introduction:**
    - Cybersecurity is dynamic, requiring anticipation of change.
    - Importance of vulnerability assessments in understanding security weaknesses.
    - Utilizing findings of vulnerability assessments with an attacker mindset.

### Adopting an Attacker Mindset

- **Experimentation Approach:**
    - Applying controlled experiments to cause and evaluate problems.
    - Provides alternative perspective for security challenges.
    - Insights gained aid in establishing or modifying security plans.

### Simulating Threats

- **Proactive Simulations:**
    - Assume attacker role, exploiting vulnerabilities and breaching defenses (red team exercises).
- **Reactive Simulations:**
    - Assume defender role, responding to attacks (blue team exercises).
- Both aim to enhance system security through team efforts.

### Scanning for Trouble

- **Vulnerability Scanning:**
    - Identifies common vulnerabilities and exposures on the network.
    - Essential tool for uncovering weaknesses in defenses.
- **Reactive Simulations Example:**
    - External vulnerability scan identifies outdated OS on a server.
    - Vulnerability analysis, risk assessment, and remediation process follows.

### Staying Informed

- **Innovative Solutions:**
    - Criminals constantly seek ways to bypass existing defenses.
    - Security controls often developed reactively to emerging risks.
- **Resource Recommendation:**
    - [NISTs National Vulnerability Database (NVD)](https://nvd.nist.gov/) for staying current on common vulnerabilities.

### Key Takeaways

- Vulnerability assessments aid in security risk planning.
- Participation in proactive and reactive simulations enhances preparedness.
- Continuous learning about emerging technologies and security trends is essential for innovative problem-solving.

---
## Types of Threat Actors

- **Introduction:**
    - Understanding threat actors and their motivations.
    - Exploring the categories and types of threat actors.

### Categories of Threat Actors

- **Competitors:**
    - Rival companies seeking to benefit from leaked information.
- **State Actors:**
    - Government intelligence agencies engaged in cyber operations.
- **Criminal Syndicates:**
    - Organized groups profiting from criminal activities.
- **Insider Threats:**
    - Individuals with authorized access compromising assets.
- **Shadow IT:**
    - Individuals using unauthorized technologies lacking IT governance.

### Types of Hackers

- **Unauthorized Hackers:**
    - Commit crimes using programming skills.
    - Range from skilled to less experienced (script kiddies).
- **Authorized (Ethical) Hackers:**
    - Improve organization's security by testing and evaluating systems.
    - Include internal security teams and external vendors.
- **Semi-Authorized Hackers:**
    - Violate ethical standards but not necessarily malicious.
    - Examples include hacktivists aiming to achieve political goals.

### Advanced Persistent Threats (APTs)

- **Definition:**
    - Threat actors maintain unauthorized access to systems for extended periods.
    - Often associated with nation-states and state-sponsored actors.
- **Targets and Objectives:**
    - Surveillance to gather information for manipulation.
    - Targets government, defense, financial, and telecom sectors.
    - Private businesses targeted as stepping stones toward larger entities.

### Access Points

- **Attack Vectors:**
    - **Direct Access:** Physical access to systems.
    - **Removable Media:** Portable hardware like USB flash drives.
    - **Social Media Platforms:** Communication and content sharing.
    - **Email:** Personal and business accounts.
    - **Wireless Networks:** On-premises.
    - **Cloud Services:** Third-party providers.
    - **Supply Chains:** Third-party vendors presenting backdoors.

### Key Takeaways

- Understanding threat actors' motivations aids in anticipating attacks.
- Recognizing attack vectors and intentions helps in effective defense strategies.
- Developing an attacker mindset involves thinking proactively about potential risks and vulnerabilities.

---
## Pathways through defenses

- **Attack vector:**
	- The pathways attackers use to penetrate security defenses.

- **Practicing an attacker mindset:**
	- Identify a target.
	- Determine how the target can be accessed.
	- Evaluate attack vectors that can be exploited.
	- Find the tools and methods of attack.

- **Defending attack vectors:**
	- Educating users.
	- Applying the principles of least privilege.
	- Using the right security controls and tools.
	- Building a diverse security team

---
## Fortifying Against Brute Force Cyber Attacks
### Understanding Brute Force Attacks

- **Simple Brute Force Attacks:**
    - Attackers guess login credentials systematically until they find the correct combination.
- **Dictionary Attacks:**
    - Attackers use a list of commonly used credentials to access a system.
- **Reverse Brute Force Attacks:**
    - Starting with a single credential, attackers try it on various systems until a match is found.
- **Credential Stuffing:**
    - Attackers use stolen credentials from previous breaches to access user accounts in another organization.

#### Tools of the Trade

- Attackers employ various software tools to automate and expedite brute force attacks:
    - Aircrack-ng
    - Hashcat
    - John the Ripper
    - Ophcrack
    - THC Hydra

### Prevention Measures

- **Hashing and Salting:**
    - Hashing converts information into a unique value, while salting adds random characters to strengthen hash functions.
- **Multi-factor Authentication (MFA):**
    - Requires users to verify their identity through multiple methods, reducing the risk of successful brute force attacks.
- **CAPTCHA:**
    - A challenge-response authentication system that distinguishes humans from automated software by presenting tests that only humans can pass.

![Text-based and image-based CAPTCHA examples.](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/tPsircWORfqlMVM3Pj3fEw_4ef34f0193e5481e8cac9e2379a02cf1_S36G003.png?expiry=1716508800000&hmac=y5bLLQslYkYzw5eWLIQD_MAAmp96d9ukD7ejpY0lM4U)

- **Password Policy:**
    - Organizations enforce stringent password policies to standardize good password practices, such as minimum length and complexity requirements.

#### Key Takeaways

- Brute force attacks remain a significant threat to systems, emphasizing the need for robust prevention measures.
- Strong passwords, coupled with hashing, salting, MFA, CAPTCHA, and password policies, fortify systems against brute force attacks.
- Understanding attacker tactics and employing preventive strategies is essential for effective cybersecurity defense.

---
## **Cybersecurity Terms and Concepts**

| Term                                         | Definition                                                                                         |
|----------------------------------------------|----------------------------------------------------------------------------------------------------|
| Advanced persistent threat (APT)            | An instance when a threat actor maintains unauthorized access to a system for an extended period of time |
| Attack surface                               | All the potential vulnerabilities that a threat actor could exploit                                  |
| Attack tree                                  | A diagram that maps threats to assets                                                              |
| Attack vector                                | The pathways attackers use to penetrate security defenses                                           |
| Bug bounty                                   | Programs that encourage freelance hackers to find and report vulnerabilities                       |
| Common Vulnerabilities and Exposures (CVE®) list | An openly accessible dictionary of known vulnerabilities and exposures                         |
| Common Vulnerability Scoring System (CVSS)  | A measurement system that scores the severity of a vulnerability                                   |
| CVE Numbering Authority (CNA)               | An organization that volunteers to analyze and distribute information on eligible CVEs             |
| Defense in depth                            | A layered approach to vulnerability management that reduces risk                                    |
| Exploit                                      | A way of taking advantage of a vulnerability                                                       |
| Exposure                                     | A mistake that can be exploited by a threat                                                         |
| Hacker                                       | Any person who uses computers to gain access to computer systems, networks, or data                |
| MITRE                                        | A collection of non-profit research and development centers                                        |
| Security hardening                          | The process of strengthening a system to reduce its vulnerability and attack surface               |
| Threat actor                                 | Any person or group who presents a security risk                                                    |
| Vulnerability                                | A weakness that can be exploited by a threat                                                        |
| Vulnerability assessment                    | The internal review process of a company’s security systems                                         |
| Vulnerability management                    | The process of finding and patching vulnerabilities                                                |
| Vulnerability scanner                       | Software that automatically compares existing common vulnerabilities and exposures against the technologies on the network |
| Zero-day                                    | An exploit that was previously unknown                                                              |

---