# Introduction to detection and incident response
## Introduction to the incident response lifecycle

- **Incident:**
	- An occurrence that actually or imminently jeopardizes, without lawful authority, the confidentiality, integrity, or availability of information or an information system; or constitutes a violation or imminent threat of violation of law, security policies, security procedures, or acceptable use policies.

- **Event:**
	- An observable occurrence on a network, system, or device.

- **The 5 W's of an incident:**
	- Who triggered the incident
	- What happened
	- When the incident took place
	- Where the incident took place
	- Why the incident occurred

- **Incident handler’s journal:**
	- A form of documentation used in incident response.
---
## Incident response teams

- **Computer security incident response teams (CSIRT):**
	- A specialized group of security professionals that are trained in incident management and response.

- **Roles in CSIRT:**
	- Security analyst
	- Technical lead
	- Incident coordinator

---
## Roles in Incident Response Teams

- **Definition**:
	- Specialized group of security professionals trained in incident management and response.
	- Responsible for coordinating and executing incident response activities within an organization.

### Command, Control, and Communication

- **Command**:
  - Having the appropriate leadership and direction to oversee the response.

- **Control**:
  - Ability to manage technical aspects during incident response, like coordinating resources and assigning tasks.

- **Communication**:
  - Ability to keep stakeholders informed.

### Roles in CSIRTs

- **Security Analyst**
  - Continuous monitoring for threats and triage of alerts.
  - Root-cause investigations and escalation of critical threats.

- **Technical Lead**
  - Manages technical aspects, determines root cause, and implements response strategies.
  - Collaborates with other teams to align response with business priorities.

- **Incident Coordinator**
  - Coordinates with relevant departments, ensures clear communication.
  - May exist in other teams like SOC.

#### Additional Roles

- Various specialized roles like communications lead, legal lead, etc.
- Organizational structures vary based on company needs.

### Security Operations Center (SOC)

- Monitors networks, systems, and devices for security threats.
- Integral part of the blue team responsible for defense against attacks.

#### SOC Organization

- **Tier 1 SOC Analyst**
  - Monitors alerts and performs initial triage, escalates incidents.

- **Tier 2 SOC Analyst**
  - Conducts deeper investigations, refines security tools.

- **Tier 3 SOC Lead**
  - Manages team operations, performs advanced threat detection.

- **SOC Manager**
  - Overall team management, hiring, training, and evaluation.
  - Develops incident reports, communicates findings to management.

#### Specialized Roles

- Forensic investigators: Collect, preserve, and analyze digital evidence.
- Threat hunters: Detect, analyze, and defend against new threats.

### Key Takeaways

- Understanding team structures aids in effective incident response.
- Collaboration among roles is crucial for successful resolution.
- Recognizing individual responsibilities enhances problem-solving abilities.

### Resources

- [The security operations ecosystem](https://chronicle.security/blog/posts/soc-ecosystem-infographic/)
- [Cyber career pathways tool](https://niccs.cisa.gov/workforce-development/cyber-career-pathways-tool)
- [Detection and Response at Google](https://www.youtube.com/watch?v=QZ0cpBocl3c): Episode 2 of the Hacking Google series


---
## Incident response plans

- **Elements of a security plan:**
	- Policies
	- Standards
	- Procedures

 - **Incident response plan:** 
	 - A document that outlines the procedures to take in each step of incident response.

- **Elements of a incident plan:**
	- Incident response procedures
	- System information
	- Other documents

---
## Incident response tools

- **Tool types:**
	- Detection and management tools
	- Documentation tools
	- Investigative tools

---
## The value of documentation

- **Documentation:**
	- Any form of recorded content that is used for a specific purpose.

- **Types of documentation:**
	- Playbooks
	- Incident handler's journal
	- Policies
	- Plans
	- Final reports

- **Playbook:**
	- A manual that provides details about any operational action.

- **Word processor tools:**
	- Google Docs
	- OneNote
	- Evernote
	- Notepad++

- **Ticketing system:**
	- Jira

- **Other tools:**
	- Google Sheets
	- Audio recorders
	- Cameras
	- Handwritten notes

---
## Intrusion detection systems

- **Intrusion detection system (IDS):**
	- An application that monitors system activity and alerts on possible intrusions.

- **Intrusion prevention system (IPS):**
	- An application that monitors system activity for intrusive activity and takes action to stop the activity.

- **IDS and IPS tools:**
	- Snort
	- Zeek
	- Kismet
	- Sagan
	- Suricata

---
## Overview of Detection Tools
### Why You Need Detection Tools

- Detection tools serve as the cybersecurity equivalent of home security systems, monitoring and protecting networks and systems against unauthorized access and security threats.
- They continuously monitor networks and systems for any suspicious activity and trigger alerts when potential intrusions are detected.

### Detection Tools Comparison

| Capability            | IDS   | IPS   | EDR   |
|-----------------------|-------|-------|-------|
| Detects malicious activity | ✓ | ✓ | ✓ |
| Prevents intrusions         | N/A | ✓ | ✓ |
| Logs activity               | ✓ | ✓ | ✓ |
| Generates alerts            | ✓ | ✓ | ✓ |
| Performs behavioral analysis | N/A | N/A | ✓ |

### Overview of IDS Tools

- Intrusion Detection Systems (IDS) monitor system activity and alert on possible intrusions.
- They aim to detect potential malicious activity but do not prevent it; instead, they generate alerts for further investigation.
- IDS tools include Zeek, Suricata, Snort®, and Sagan.

#### Detection Categories

1. **True Positive**: Alerts accurately identify actual threats, aiding effective responses.
2. **True Negative**: Indicates no malicious activity, confirming system integrity.
3. **False Positive**: Incorrectly raises alarms for harmless activities, potentially wasting resources.
4. **False Negative**: Fails to detect actual threats, leaving systems vulnerable to exploitation.

### Overview of IPS Tools

- Intrusion Prevention Systems (IPS) monitor system activity and take action to prevent intrusive activity.
- They detect and alert on intrusions while also actively preventing and minimizing their effects.
- Many IDS tools can operate as IPS as well, offering both detection and prevention capabilities.

### Overview of EDR Tools

- Endpoint Detection and Response (EDR) tools monitor endpoints for malicious activity.
- Installed on devices connected to the network (endpoints), they collect, record, and analyze system activity to identify, alert, and respond to suspicious behavior.
- EDR tools utilize behavioral analysis and automation to detect and respond to threats without manual intervention.
- Examples include Open EDR®, Bitdefender™ Endpoint Detection and Response, and FortiEDR™.

### Key Takeaways

- Detection tools are essential for organizations to gain awareness of activity in their environments and respond effectively to security threats.
- IDS, IPS, and EDR serve different but complementary roles in detecting, logging, alerting, and preventing potential malicious activity.

---
## Alert and event management with SIEM and SOAR tools

### SIEM (Security Information and Event Management)

- **Definition:** SIEM is an application that collects and analyzes log data to monitor critical activities in an organization.
- **Function:** SIEM tools help security analysts perform log analysis to identify events of interest.
- **Advantages:** Provides access to real-time event data, monitors, detects, and alerts on suspicious activity, and acts as a system for log storage.

### SOAR (Security Orchestration, Automation, and Response)

- **Definition:** SOAR is a technology stack that enables organizations to collect, aggregate, and analyze security data from multiple sources. It then uses automation to respond to security incidents.
- **Function:** SOAR platforms automate repetitive tasks, orchestrate workflows, and facilitate incident response activities to improve efficiency and effectiveness.
- **Advantages:** Streamlines incident response processes, reduces manual intervention, and enhances overall security posture.

---

## Overview of SIEM Technology

### SIEM Advantages

- **Access to Event Data:** SIEM tools provide access to real-time event and activity data across networks.
- **Monitoring, Detecting, and Alerting:** SIEM tools continuously monitor systems, analyze data, and generate alerts for suspicious activity.
- **Log Storage:** SIEM tools act as a system for data retention, providing access to historical data.

### The SIEM Process

1. **Collect and Aggregate Data**
   - SIEM collects event data from various sources like firewalls, servers, routers, etc.
   - Aggregates log data into a centralized location.
   - Parsing occurs to map data fields and values for easier interpretation.
2. **Normalize Data**
   - Transforms data from different sources into a standardized format.
   - Normalization converts data into structured formats for easy processing.
3. **Analyze Data**
   - SIEM tools analyze normalized data using detection logic to identify potential threats.
   - Correlation techniques are applied to compare multiple log events for common threat patterns.

### SIEM Tools

- AlienVault OSSIM
- Chronicle
- Elastic
- Exabeam
- IBM QRadar Security Intelligence Platform
- LogRhythm
- Splunk

---
## **Cybersecurity Terms and Concepts**

| Term                                                | Definition                                                                                                   |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Computer security incident response teams (CSIRT)   | A specialized group of security professionals that are trained in incident management and response          |
| Documentation                                       | Any form of recorded content that is used for a specific purpose                                            |
| Endpoint detection and response (EDR)               | An application that monitors an endpoint for malicious activity                                             |
| Event                                               | An observable occurrence on a network, system, or device                                                    |
| False negative                                      | A state where the presence of a threat is not detected                                                      |
| False positive                                      | An alert that incorrectly detects the presence of a threat                                                   |
| Incident                                            | An occurrence that actually or imminently jeopardizes, without lawful authority, the confidentiality, integrity, or availability of information or an information system; or constitutes a violation or imminent threat of violation of law, security policies, security procedures, or acceptable use policies |
| Incident handler’s journal                          | A form of documentation used in incident response                                                            |
| Incident response plan                             | A document that outlines the procedures to take in each step of incident response                            |
| Intrusion detection system (IDS)                   | An application that monitors system activity and alerts on possible intrusions                               |
| Intrusion prevention system (IPS)                  | An application that monitors system activity for intrusive activity and takes action to stop the activity     |
| National Institute of Standards and Technology (NIST) Incident Response Lifecycle | A framework for incident response consisting of four phases: Preparation; Detection and Analysis; Containment, Eradication, and Recovery; and Post-incident activity |
| Playbook                                           | A manual that provides details about any operational action                                                  |
| Security information and event management (SIEM)   | An application that collects and analyzes log data to monitor critical activities in an organization         |
| Security operations center (SOC)                   | An organizational unit dedicated to monitoring networks, systems, and devices for security threats or attacks |
| Security orchestration, automation, and response (SOAR) | A collection of applications, tools, and workflows that uses automation to respond to security events    |
| True negative                                      | A state where there is no detection of malicious activity                                                    |
| True positive                                      | An alert that correctly detects the presence of an attack                                                    |

---