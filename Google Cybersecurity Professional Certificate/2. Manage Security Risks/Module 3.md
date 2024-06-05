# Introduction to cybersecurity tools
## Logs

- **Introduction:**
	- A record of events that occur within an organization's systems and networks.
- **Common Log Sources:**
	- Firewall logs:
		- A firewall log is a record of attempted or established connections for incoming traffic from the internet. It also includes outbound requests to the internet from within the network.
	- Network logs:
		- A network log is a record of all computers and devices that enter and leave the network. It also records connections between devices and services on the network.
	- Server logs:
		- A server log is a record of events related to services such as websites, emails, or file shares. It includes actions such as login, password, and username requests.

---
## Explore common SIEM tools

- **Different types of SIEM tools:**
	- Self-hosted
	- Cloud-hosted
	- Hybrid

---
## Future of SIEM Tools

### Current SIEM Solutions

- Collect and analyze log data for security monitoring.
- Offer real-time monitoring and tracking of security event logs.
- Require human interaction for analysis of security events.
- Provide various dashboard options for managing and monitoring organizational data.

### Future Trends

- **Cloud Functionality**:
  - Cloud-hosted and cloud-native SIEM solutions are becoming prevalent.
  - Offer benefits such as scalability, flexibility, and easier access.
- **Adaptation to New Threats**:
  - SIEM tools evolving to handle new threat actor tactics and techniques.
  - Need to accommodate the growing complexity of cyber attacks, especially with IoT devices.
- **Integration of AI and ML**:
  - AI and ML technologies enhancing SIEM capabilities.
  - Better threat detection, visualization, and data storage functionality.
- **Automation with SOAR**:
  - Security orchestration, automation, and response (SOAR) becoming integral to SIEM.
  - Enables faster response times to security incidents by automating common tasks.
- **Interconnected Systems**:
  - Improved communication and interaction between security platforms and devices.
  - SIEM tools expected to seamlessly integrate with other security solutions.
- **Continuous Learning**:
  - Security professionals should stay updated on advancements in cloud computing, SIEM integration, automation, and AI/ML.

### Key Takeaways

- SIEM tools play a crucial role in monitoring organizational data.
- Cloud computing, SIEM-application integration, and automation are key trends in the future of SIEM.
- Security professionals need to continuously learn and adapt to new developments in SIEM technology.

---
## Cybersecurity Tools

### Open-Source Tools

- Free to use and often user-friendly.
- Built collaboratively by the public, resulting in potentially more secure software.
- Allows for customization and creation of new services.
- Source code and training materials are readily available for users to modify and improve.
- Examples: Linux and Suricata.

### Proprietary Tools

- Developed and owned by a person or company; users typically pay for usage and training.
- Source code access and modification restricted to owners.
- Users may need to wait for updates and pay fees for them.
- Limited customization options compared to open-source tools.
- Examples: Splunk® and Chronicle SIEM tools.

### Common Misconceptions

- Misconception: Open-source tools are less effective and less safe.
- Reality: Open-source materials have become industry standards; wide exposure and access to source code by users make it harder for malicious manipulation.
- Examples refute the misconception.

### Examples of Open-Source Tools
#### Linux

- Open-source operating system widely used with a customizable command-line interface.
- Facilitates tailoring the OS to individual needs.
- Multiple versions exist for specific tasks.

#### Suricata

- Open-source network analysis and threat detection software.
- Inspects network traffic to identify suspicious behavior and generate network data logs.
- Developed by the Open Information Security Foundation (OISF).
- Widely used in public and private sectors, integrates with various SIEM tools.

### Key Takeaways

- Open-source tools are prevalent in cybersecurity.
- Both open-source and proprietary tools will be explored in-depth throughout the certificate program.

---

## Using SIEM Tools to Protect Organizations

### Splunk

- Offers Splunk® Enterprise and Splunk® Cloud for reviewing an organization's data.
- Enables collection, searching, monitoring, and analysis of log data from multiple sources.
- Dashboards help manage internal infrastructure and monitor security-related events.

#### Splunk Dashboards:

1. **Security Posture Dashboard**:
   - For Security Operations Centers (SOCs) to monitor notable security events and trends in the last 24 hours.
   - Helps determine if security infrastructure and policies are performing as designed.

2. **Executive Summary Dashboard**:
   - Analyzes and monitors the overall health of the organization over time.
   - Provides high-level insights to stakeholders about security incidents and trends.

3. **Incident Review Dashboard**:
   - Identifies suspicious patterns during incidents.
   - Provides a visual timeline of events leading up to an incident.

4. **Risk Analysis Dashboard**:
   - Helps analysts identify risk for each risk object (e.g., user, computer, IP address).
   - Analyzes potential impact of vulnerabilities in critical assets.

### Chronicle

- Cloud-native SIEM tool from Google that retains, analyzes, and searches log data.
- Allows collection and analysis of log data based on specific parameters such as asset, domain name, user, or IP address.

#### Chronicle Dashboards:

1. **Enterprise Insights Dashboard**:
   - Highlights recent alerts and identifies suspicious domain names in logs.
   - Provides confidence score and severity level for each threat.

2. **Data Ingestion and Health Dashboard**:
   - Shows the number of event logs, log sources, and success rates of data processed into Chronicle.
   - Ensures correct log source configuration and error-free log reception.

3. **IOC Matches Dashboard**:
   - Indicates top threats, risks, and vulnerabilities.
   - Identifies trends to direct focus on highest priority threats.

4. **Main Dashboard**:
   - Displays high-level summary of organization’s data ingestion, alerting, and event activity over time.
   - Helps identify threat trends across various parameters.

5. **Rule Detections Dashboard**:
   - Provides statistics related to incidents with highest occurrences, severities, and detections over time.
   - Helps manage recurring incidents and establish mitigation tactics.

6. **User Sign In Overview Dashboard**:
   - Provides information about user access behavior across the organization.
   - Helps identify unusual user activity and mitigate threats.

## Key Takeaways

- SIEM tools provide dashboards to organize and focus security efforts.
- Helps analysts reduce risk by identifying, analyzing, and remediating highest priority items.
- Practice using SIEM tool features and commands for search queries will be covered later in the program.

---
## **Cybersecurity Terms and Concepts****

| Term                                     | Definition                                                                                                   |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Chronicle                                | A cloud-native tool designed to retain, analyze, and search data                                             |
| Incident response                        | An organization’s quick attempt to identify an attack, contain the damage, and correct the effects of a security breach |
| Log                                      | A record of events that occur within an organization’s systems                                                |
| Metrics                                  | Key technical attributes such as response time, availability, and failure rate, which are used to assess the performance of a software application |
| Operating system (OS)                    | The interface between computer hardware and the user                                                          |
| Playbook                                 | A manual that provides details about any operational action                                                    |
| Security information and event management (SIEM) | An application that collects and analyzes log data to monitor critical activities in an organization     |
| Security orchestration, automation, and response (SOAR) | A collection of applications, tools, and workflows that use automation to respond to security events |
| SIEM tools                              | A software platform that collects, analyzes, and correlates security data from various sources across your IT infrastructure that helps identify and respond to security threats in real-time, investigate security incidents, and comply with security regulations |
| Splunk Cloud                            | A cloud-hosted tool used to collect, search, and monitor log data                                              |
| Splunk Enterprise                       | A self-hosted tool used to retain, analyze, and search an organization's log data to provide security information and alerts in real-time |

---