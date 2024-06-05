# Secure against network intrusions
## The case for securing networks

- **Common network intrusion attacks:**
	- Malware
	- Spoofing
	- Packet sniffing
	- Packet flooding

- **Attack can harm an organization by:**
	- Leaking valuable or confidential information.
	- Damaging an organization's reputation.
	- Impact customer retention.
	- Costing money and time.

---
## Intrusions and Their Impact on Organizations

### Network Interception Attacks

- Intercept network traffic, steal information, or disrupt transmission.
- Packet sniffing: Capturing and inspecting data in transit.
- Malicious alteration of messages or insertion of code.

### Backdoor Attacks

- Exploit weaknesses intentionally left in systems.
- Gain persistent access to networks.
- Install malware, perform denial of service attacks, steal sensitive information.

### Impacts on Organizations

- **Financial Impact**:
  - Revenue loss due to disrupted operations.
  - Costs for repairing infrastructure and paying ransoms.
  - Legal fees from potential litigation.
- **Reputation Damage**:
  - Eroded trust in security practices.
  - Potential loss of customers to competitors.
- **Public Safety Concerns**:
  - Risks to critical infrastructure.
  - Physical harm to citizens in severe cases.

### Key Takeaways

- **Constant Threat**: Malicious actors seek vulnerabilities continuously.
- **Understanding Attack Methods**: Knowledge of backdoor and network interception attacks is essential.
- **Impacts**: Financial losses, reputational damage, and public safety risks.
- **Security Importance**: Continuous education and proactive measures are crucial.

---
## Denial of Service (DoS) attacks

- **Denial of service (DoS) attack:**
	- An attack that targets a network or server and floods it with network traffic.

- **Distributed denial of service (DDoS) attack:**
	- A type of denial of service attack that uses multiple devices or servers located in different locations to flood the target network with unwanted traffic.

- **Synchronize (SYN) flood attack:**
	- A type of DoS attack that simulates a TCP/IP connection and floods a server with SYN packets.

- **Internet Control Message Protocol (ICMP):**
	- An internet protocol used by devices to tell each other about data transmission errors across the network.

- **Internet Control Message Protocol (ICMP) flood:**
	- A type of DoS attack performed by an attacker repeatedly sending ICMP request packets to a network server.

- **Ping of death:**
	- A type of DoS attack caused when a hacker pings a system by sending it an oversized ICMP packet that is bigger than 64KB.

---
## Reading tcpdump Logs

### Network Protocol Analyzers

- Tools for capturing and analyzing data traffic within a network.
- Aid in monitoring and identifying suspicious activity.

#### tcpdump Overview

- Command-line network protocol analyzer.
- Lightweight with low resource usage.
- Utilizes libpcap library.
- Text-based, executed in the terminal.
- Compatible with Linux/Unix and macOS®, preinstalled on many distributions.

#### Interpreting Output

- Output: Sniffed packets displayed in the command line or optionally to a log file.
- Packet capture contains crucial information:
  - **Timestamp**: Hours, minutes, seconds, and fractions.
  - **Source IP**: Originating IP address.
  - **Source port**: Originating port number.
  - **Destination IP**: Destination IP address.
  - **Destination port**: Destination port number.
- Default behavior: Resolves host addresses to hostnames, replaces port numbers with associated services.

#### Common Uses

- **Capturing and Viewing**: Monitor network communications and collect statistics.
- **Troubleshooting**: Identify and resolve network performance issues.
- **Malicious Traffic Detection**: Identify and investigate suspicious activity.
- **Alert Creation**: Customize alerts for network issues or security threats.
- **Unauthorized Activity Detection**: Identify unauthorized instant messaging or wireless access points.

#### Security Considerations

- **Potential Misuse**: Attackers may exploit tcpdump to capture sensitive information like usernames and passwords.
- **Importance for Analysts**: Understanding tcpdump's uses and potential risks is essential for effective network monitoring and defense.

#### Key Takeaways

- **Common Tool**: tcpdump is widely used for network monitoring and investigation.
- **Output Format**: Displays essential packet routing information.
- **Potential Risks**: Attackers may abuse tcpdump for malicious purposes.
- **Importance for Analysts**: Understanding tcpdump aids in detecting and mitigating security threats.

---
## Real-life DDoS Attack

### Introduction

- **Denial of Service (DoS)** attacks overwhelm networks.
- **Volumetric Distributed DoS (DDoS)** floods networks with unwanted data packets.

### Case Study: 2016 DDoS Attack on DNS Servers

- **Target**: DNS service provider hosting systems for large companies.
- **Function of DNS Servers**: Translate website domain names into IP addresses.
- **Date**: October 21, 2016.

### Leading up to the Attack

- **Botnet Creation**: University students create botnet to attack gaming servers.
- **Botnet**: Collection of malware-infected computers.
- **Code Sharing**: Botnet code shared online, accessible to malicious actors.

### Attack Execution

- **Botnet Assault**: Tens of millions of DNS requests overwhelm service provider.
- **Impact**: DNS service shut down, rendering websites inaccessible.
- **Scope**: Outages across North America and Europe.

### Response and Mitigation

- **Duration**: Service restored after two hours of downtime.
- **Subsequent Attacks**: Mitigation measures in place.

### Key Takeaways

- **Seriousness of DDoS Attacks**: Damaging to organizations' operations and reputation.
- **Preparedness**: Importance of proactive measures and mitigation strategies.
- **Continued Learning**: Security analysts must stay informed about mitigation techniques.

---
## Malicious packet sniffing

- **Passive packet sniffing:**
	- A type of attack where a malicious actor connects to a network hub and looks at all traffic on the network.

- **Active packet sniffing:**
	- A type of attack where data packets are manipulated in transit.

---
## IP Spoofing

- **IP spoofing:**
	- A network attack performed when an attacker changes the source IP of a data packet to impersonate an authorized system and gain access to a network.

- **Common IP spoofing attacks:**
	- On-path attack
	- Replay attack
	- Smurf attack

- **On-path attack:**
	- An attack where a malicious actor places themselves in the middle of an authorized connection and intercepts or alters the data in transit.

- **Replay attack:**
	- A network attack performed when a malicious actor intercepts a data packet in transit and delays it or repeats it at another time.

- **Smurf attack:**
	- A network attack performed when an attacker sniffs an authorized user’s IP address and floods it with ICMP packets.

---
## Overview of Interception Tactics

### Packet Sniffing

- Capturing and inspecting data packets across a network.
- NIC set to promiscuous mode allows capturing all traffic.
- Tools like Wireshark facilitate packet sniffing.
- Malicious actors gather personal information for later use or IP spoofing.

### IP Spoofing

- Impersonating authorized devices' IP and MAC addresses.
- Firewalls crucial for preventing IP spoofing attacks.
  
#### On-Path Attack

- Intercepting communication between trusted devices.
- Gathering valuable information like usernames, passwords, or DNS look-ups.
- Encryption (e.g., TLS) essential for protection.

#### Smurf Attack

- Flooding authorized user's IP with packets, often combined with ICMP ping requests.
- Flood of traffic overwhelms servers, causing denial of service.
- Advanced firewalls (NGFWs) detect and prevent attacks by monitoring network traffic.

#### DoS Attack

- Preventing legitimate activity on a compromised system without expecting a response.
- Layered defense strategies crucial, including encryption and network monitoring.

### Key Takeaways

- Implement mitigation strategies to counter interception attacks effectively.
- Strategies include encryption, advanced firewalls, and a defense-in-depth approach.

---
## **Cybersecurity Terms and Concepts**

| Term                                   | Definition                                                                                                      |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Active packet sniffing                | A type of attack where data packets are manipulated in transit.                                                |
| Botnet                                 | A collection of computers infected by malware that are under the control of a single threat actor, known as the “bot-herder”. |
| Denial of service (DoS) attack        | An attack that targets a network or server and floods it with network traffic.                                   |
| Distributed denial of service (DDoS) attack | A type of denial of service attack that uses multiple devices or servers located in different locations to flood the target network with unwanted traffic. |
| Internet Control Message Protocol (ICMP) | An internet protocol used by devices to tell each other about data transmission errors across the network. |
| Internet Control Message Protocol (ICMP) flood | A type of DoS attack performed by an attacker repeatedly sending ICMP request packets to a network server. |
| IP spoofing                            | A network attack performed when an attacker changes the source IP of a data packet to impersonate an authorized system and gain access to a network. |
| On-path attack                        | An attack where a malicious actor places themselves in the middle of an authorized connection and intercepts or alters the data in transit. |
| Packet sniffing                       | The practice of capturing and inspecting data packets across a network.                                          |
| Passive packet sniffing               | A type of attack where a malicious actor connects to a network hub and looks at all traffic on the network.      |
| Ping of death                         | A type of DoS attack caused when a hacker pings a system by sending it an oversized ICMP packet that is bigger than 64KB. |
| Replay attack                         | A network attack performed when a malicious actor intercepts a data packet in transit and delays it or repeats it at another time. |
| Smurf attack                          | A network attack performed when an attacker sniffs an authorized user’s IP address and floods it with ICMP packets. |
| Synchronize (SYN) flood attack        | A type of DoS attack that simulates a TCP/IP connection and floods a server with SYN packets.                     |

---