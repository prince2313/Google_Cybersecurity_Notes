# Incident investigation and response
## The detection and analysis phase of the lifecycle

- **Detection:**
	- The prompt discovery of security events.

- **Analysis:**
	- The investigation and validation of alerts.

- **Challenges in the detection and analysis phase:**
	- Impossible to detect everything
	- High volume of alerts

---
## Cybersecurity Incident Detection Methods

### Introduction

- Security analysts use detection tools to help discover threats, but there are additional methods of detection that can be used as well.
- This reading introduces different detection methods that organizations can employ to discover threats.

#### Methods of Detection

- During the **Detection and Analysis Phase** of the incident response lifecycle:
  - Security teams are notified of a possible incident.
  - Teams investigate and verify the incident by collecting and analyzing data.
- **Detection** refers to the prompt discovery of security events.
- **Analysis** involves the investigation and validation of alerts.

##### Tools for Detection

- Intrusion Detection System (IDS):
  - Detects possible intrusions and sends alerts to security analysts.
- Security Information and Event Management (SIEM) tools:
  - Detect, collect, and analyze security data.

##### Challenges with Detection

- Detection tools can fail for various reasons, such as:
  - Improper configuration leading to missed suspicious activity.
- It's important to use additional detection methods for better coverage and accuracy.

##### Threat Hunting

- **Threat hunting** is the proactive search for threats on a network.
- Combines human analysis with technology to discover hidden threats.
- Used to uncover malicious activity not identified by detection tools and to perform further analysis on detections.
- Examples:
  - Identifying fileless malware, which uses sophisticated evasion techniques.
- Threat hunting specialists are known as **threat hunters**:
  - Perform research on emerging threats and attacks.
  - Determine the probability of an organization being vulnerable to specific attacks.
  - Use a combination of threat intelligence, indicators of compromise, indicators of attack, and machine learning.

##### Threat Intelligence

- **Threat intelligence** is evidence-based information providing context about existing or emerging threats.
- Sources of threat intelligence:
  - **Industry reports**: Details on attacker's tactics, techniques, and procedures (TTP).
  - **Government advisories**: Similar to industry reports, providing details on attackers' TTP.
  - **Threat data feeds**: Streams of threat-related data, useful against advanced persistent threats (APTs).
- Managing threat intelligence:
  - Use a **threat intelligence platform (TIP)** to collect, centralize, and analyze threat intelligence from different sources.
  - TIPs help identify and prioritize relevant threats and improve security posture.
- Note: Threat intelligence data feeds should be used to add context to detections and assessed before application.

##### Cyber Deception

- Cyber deception involves techniques to deliberately deceive malicious actors to increase detection and improve defensive strategies.
- Example: **Honeypots**
  - Systems or resources created as decoys vulnerable to attacks.
  - Attract potential intruders and capture their activity.
  - Example: A fake file labeled _Client Credit Card Information - 2022_ alerts security teams when accessed by malicious actors.

### Key Takeaways

- Implement various detection methods to identify and locate security events in an environment.
- Use a variety of detection methods, tools, and technologies to adapt to the evolving threat landscape and better protect assets.

### Resources for More Information

- [Informational repository about threat hunting from The ThreatHunting Project](https://www.threathunting.net/)
- [Research on state-sponsored hackers from Threat Analysis Group (TAG)](https://blog.google/threat-analysis-group/)

---
### Indicators of Compromise
#### Indicators of Compromise

- **Indicators of Compromise (IoCs)**: Observable evidence suggesting signs of a potential security incident.
  - Example: A file name associated with a type of malware.
  - IoCs indicate the _who_ and _what_ of an attack after it's taken place.

- **Indicators of Attack (IoAs)**: Series of observed events indicating a real-time incident.
  - Focus on identifying behavioral evidence of an attacker, including methods and intentions.
  - Example: Observing a process that makes a network connection.

- Note: IoCs are not always confirmation of a security incident. They can result from human error, system malfunctions, etc.

#### Pyramid of Pain

- Created by security researcher David J. Bianco.
- Captures the relationship between IoCs and the difficulty level for attackers when IoCs are blocked by security teams.
- Levels of difficulty represent the “pain” levels for attackers when IoCs are blocked.

  1. **Hash Values**: Hashes that correspond to known malicious files.
      - Example: Unique references to specific malware samples.
  2. **IP Addresses**: Internet protocol addresses.
      - Example: 192.168.1.1
  3. **Domain Names**: Web addresses.
      - Example: www.google.com
  4. **Network Artifacts**: Observable evidence created by malicious actors on a network.
      - Example: Information found in network protocols such as User-Agent strings.
  5. **Host Artifacts**: Observable evidence created by malicious actors on a host (any device connected to a network).
      - Example: Name of a file created by malware.
  6. **Tools**: Software used by a malicious actor to achieve their goal.
      - Example: Password cracking tools like John the Ripper.
  7. **Tactics, Techniques, and Procedures (TTPs)**: Behavior of a malicious actor.
      - Tactics: High-level overview of the behavior.
      - Techniques: Detailed descriptions of the behavior relating to the tactic.
      - Procedures: Highly detailed descriptions of the technique.
      - TTPs are the hardest to detect.

### Key Takeaways

- IoCs and IoAs are valuable for detecting incidents.
- The Pyramid of Pain helps understand different types of IoCs and their value in detecting and stopping malicious activity.

---
## Indicators of Compromise (IoC) Analysis

### Contextualizing IoCs

- Identifying and blocking individual IoCs may not provide comprehensive insights into an attack.
- Broaden perspective through **threat intelligence** to construct a narrative around security incidents.
- Helps in making more informed response actions.

### Crowdsourcing Threat Intelligence

- **Crowdsourcing**: Gathering information from global cybersecurity community.
- Platforms like **ISACs** and **OSINT** provide collective knowledge.
- Enhances detection and response capabilities.

### [VirusTotal](https://www.virustotal.com/gui/home)

- Service for analyzing suspicious files, domains, URLs, and IP addresses.
- Provides detailed reports:
  - Detection verdicts from third-party vendors.
  - Static analysis details.
  - Related IoCs.
  - Behavioral insights.
  - Community feedback.
- Plays a significant role in sharing threat intelligence.

### Other Investigative Tools

- **[Jotti's Malware Scan](https://virusscan.jotti.org/)**: Scans suspicious files with multiple antivirus programs.
- **[Urlscan.io](https://urlscan.io/)**: Analyzes URLs and provides detailed reports.
- [MalwareBazaar](https://bazaar.abuse.ch/verify-ua/): Repository of malware samples for research.

### Key Takeaways

- Importance of adding context to IoC analyses.
- Leveraging investigative tools and threat intelligence improves detection capabilities.
- Enables informed decision-making and enhances overall cybersecurity posture.

---
## Best Practices for Effective Documentation
### Documentation Benefits
#### Transparency

- Critical for demonstrating compliance with regulations, internal processes, and legal proceedings.
- **Chain of custody**: Process of documenting evidence possession and control during an incident lifecycle.
- **Broken Chain of Custody**: Occurs when there's a gap or inconsistency in documenting evidence possession, which can undermine its credibility in legal proceedings.

#### Standardization

- Supports continuous improvement efforts, knowledge transfer, and onboarding of new team members.
- **Standards**: References informing how to set policies.
- Example: **Incident Response Plan**: Outlines procedures for incident response, ensuring standardized response processes.

#### Clarity

- Clear documentation helps users quickly access information and take necessary action.
- Security analysts document reasoning behind actions to ensure clarity to their team.

### Best Practices
#### Know Your Audience

- Consider the audience's needs and tailor documentation accordingly.
- Differentiate between technical and non-technical audiences.

#### Be Concise

- Establish the purpose of the document immediately.
- Use executive summaries for brief overviews, allowing easy identification of key findings.

#### Update Regularly

- New vulnerabilities constantly emerge, necessitating regular review and updates to documentation.
- After incident resolution, conduct a comprehensive review to identify necessary changes.

### Key Takeaways

- Effective documentation benefits everyone in an organization.
- Essential skill for security analysts.
- Practice audience-awareness, conciseness, and regular updates for effective documentation.

---
## The value of cybersecurity playbooks

- **Playbook:**
	- A manual that provides details about any operational action.

- **Types of Playbooks:**
	- Non-automated
	- Automated
	- Semi-automated

---
## The role of triage in incident response

- **Triage**:
	- The prioritizing of incidents according to their level of importance or urgency.

- **Triage process:**
	- Receive and assess 
	- Assign priority 
	- Collect and analyze

- **Question to ask:**
	- Is there anything out of the ordinary?
	- Are there multiple failed login attempts?
	- Did the login happen outside of normal working hours?
	- Did the login happen outside of the network?

---
## The Triage Process

### Triage Process

#### Receive and Assess
- Security analyst receives alert from intrusion detection system (IDS).
- Verify validity of alert and gather information:
  - Determine if alert is a false positive.
  - Review past history of alert.
  - Assess if alert is triggered by a known vulnerability.
  - Determine severity of alert.

#### Assign Priority
- Prioritize incidents based on:
  - Functional impact on IT systems.
  - Information impact on data confidentiality, integrity, and availability.
  - Recoverability of systems and data.

#### Collect and Analyze
- Perform comprehensive analysis of incident:
  - Gather evidence from different sources.
  - Conduct external research.
  - Document investigative process.
- Escalate to level two analyst or manager if necessary.

### Benefits of Triage

#### Resource Management
- Focus resources on threats requiring urgent attention.
- Avoid dedicating time to lower priority tasks.
- Potentially reduce response time.

#### Standardized Approach
- Triage provides standardized incident handling.
- Process documentation (e.g., playbooks) ensures proper assessment and validation of alerts.

### Key Takeaways

- Triage allows prioritization of incidents based on importance or urgency.
- Helps meet incident response goals.
- Essential skill for security professionals to effectively respond to and resolve security incidents.

---
## The containment, eradication, and recovery phase of the lifecycle

- **Containment:**
	- The act of limiting and preventing additional damage caused by an incident.

- **Eradication:**
	- The complete removal of the incident elements from all affected systems.

- **Recovery:**
	- The process of returning affected systems back to normal operations.

---
## Business Continuity Considerations

### Business Continuity Planning

- **Business Continuity Plan (BCP)**: Document outlining procedures to sustain business operations during and after significant disruptions.
- Ensures critical business functions can resume or be quickly restored post-incident.
- **Not** the same as disaster recovery plans.

#### Impacts of Ransomware to Business Continuity

- Ransomware attacks can cause significant disruption to business operations.
- Examples include healthcare sector disruptions due to encrypted medical records, hindering patient care.
- BCPs minimize interruptions to essential services.

#### Recovery Strategies

- BCPs include recovery strategies to return to normal operations.
- **Site Resilience**: Prepare for, respond to, and recover from disruptions.
- Three types of recovery sites:
  - **Hot sites**: Fully operational duplicate of primary environment, activated immediately.
  - **Warm sites**: Contains fully updated and configured version of hot site, not fully operational but quickly made so.
  - **Cold sites**: Backup facility with some necessary infrastructure, may require additional setup.

### Key Takeaways

- Security incidents can disrupt business operations significantly.
- Business continuity plans mitigate impacts and ensure organizations can continue functioning.
- Essential for organizations to have plans in place to resume normal operations post-incident.

---
## Post-Incident Review

### Lessons Learned

- Occurs after containment, eradication, and recovery phases.
- Aim: learn from incidents, improve handling processes.
- Conducted via lessons learned meetings.
  - Participants: all involved in incident response.
  - Questions addressed: what, when, who, how, why.
  - **Example Questions:**
    - What happened?
    - When did it happen?
    - Who discovered it?
    - How was it contained?
    - What actions were taken for recovery?
    - What could have been done differently?
- **Benefits:**
  - Opportunity for organizational learning and improvement.
  - Platform for team collaboration and information sharing.
- **Preparation:**
  - Meeting agenda development and distribution.
  - Assignment of meeting roles (moderator, scribe).
- **Recommendations:**
  - Identify errors, gaps, and ineffective controls.
  - Prioritize actionable recommendations for improvement.
  - Examples of changes: updating playbook instructions, implementing new security tools.

### Final Report

- Essential documentation after incident response.
- Varied format based on audience.
- **Common Elements:**
  - **Executive Summary:**
    - High-level summary including key findings and essential facts.
  - **Timeline:**
    - Detailed chronological sequence of events leading to the incident.
  - **Investigation Details:**
    - Actions taken during detection and analysis, e.g., network artifact analysis.
  - **Recommendations:**
    - List of suggested actions for future prevention.
- **Considerations:**
  - Audience awareness for effective communication.
- **Pro Tip:**
  - Audience-oriented report writing for better comprehension.

### Key Takeaways

- Concludes incident response lifecycle.
- Opportunity for reflection, improvement, and documentation.
- Final report serves as a comprehensive review and communication tool.

---
## **Cybersecurity Terms and Concepts**

| Term                                      | Definition                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Analysis                                  | The investigation and validation of alerts                                                                   |
| Broken chain of custody                   | Inconsistencies in the collection and logging of evidence in the chain of custody                           |
| Business continuity plan (BCP)           | A document that outlines the procedures to sustain business operations during and after a significant disruption |
| Chain of custody                         | The process of documenting evidence possession and control during an incident lifecycle                      |
| Containment                               | The act of limiting and preventing additional damage caused by an incident                                    |
| Crowdsourcing                             | The practice of gathering information using public input and collaboration                                    |
| Detection                                 | The prompt discovery of security events                                                                       |
| Documentation                             | Any form of recorded content that is used for a specific purpose                                             |
| Eradication                               | The complete removal of the incident elements from all affected systems                                       |
| Final report                             | Documentation that provides a comprehensive review of an incident                                             |
| Honeypot                                 | A system or resource created as a decoy vulnerable to attacks with the purpose of attracting potential intruders |
| Incident response plan                   | A document that outlines the procedures to take in each step of incident response                            |
| Indicators of attack (IoA)               | The series of observed events that indicate a real-time incident                                              |
| Indicators of compromise (IoC)          | Observable evidence that suggests signs of a potential security incident                                      |
| Intrusion detection system (IDS)         | An application that monitors system activity and alerts on possible intrusions                                |
| Lessons learned meeting                  | A meeting that includes all involved parties after a major incident                                            |
| Open-source intelligence (OSINT)        | The collection and analysis of information from publicly available sources to generate usable intelligence    |
| Playbook                                 | A manual that provides details about any operational action                                                   |
| Post-incident activity                   | The process of reviewing an incident to identify areas for improvement during incident handling               |
| Recovery                                 | The process of returning affected systems back to normal operations                                           |
| Resilience                               | The ability to prepare for, respond to, and recover from disruptions                                           |
| Standards                                | References that inform how to set policies                                                                   |
| Threat hunting                           | The proactive search for threats on a network                                                               |
| Threat intelligence                     | Evidence-based threat information that provides context about existing or emerging threats                    |
| Triage                                  | The prioritizing of incidents according to their level of importance or urgency                               |
| VirusTotal                             | A service that allows anyone to analyze suspicious files, domains, URLs, and IP addresses for malicious content|

---