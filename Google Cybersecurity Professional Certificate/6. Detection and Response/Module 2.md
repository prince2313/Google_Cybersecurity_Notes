# Network monitoring and analysis
## Maintain Awareness with Network Monitoring
### Network Communication

- **Network traffic**: The amount of data that moves across a network, including the type of data transferred (e.g., HTTP).
- **Network data**: The data transmitted between devices on a network.

### Importance of Network Monitoring

- Essential for maintaining situational awareness of network activity.
- Helps in detecting suspicious network activity.

### Know Your Network

- Networks connect devices, which communicate and exchange data using network protocols.
- Network communications provide information about:
  - Source and destination IP addresses
  - Amount of data transferred
  - Date and time

#### Baseline

- A reference point used for comparison.
- Helps establish a standard of expected or normal behavior for systems, devices, and networks.
- Identifies deviations from normal network behavior.

### Monitor Your Network

- Monitoring involves examining network components to detect unusual activities.
- Examples of network components to monitor:

#### Flow Analysis

- Refers to the movement of network communications, including information related to packets, protocols, and ports.
- Ports are often associated with network protocols (e.g., HTTPS commonly uses port 443).
- Malicious actors may use non-standard ports and protocols (e.g., HTTPS over port 8088) for command and control (C2) communications.

#### Packet Payload Information

- Network packets contain source and destination IP addresses and payload information.
- Payload information may be encrypted and requires decryption to be readable.
- Monitoring packet payloads can uncover unusual activities, such as data exfiltration.

#### Temporal Patterns

- Network packets contain time-related information.
- Time patterns help understand normal network activity (e.g., bulk traffic during business hours).
- Large traffic volumes outside normal hours indicate off-baseline activity.

### Protect Your Network

- **Security Operations Centers (SOC)** monitor systems against security threats and attacks.
- **Network Operations Centers (NOC)** focus on maintaining network performance, availability, and uptime.

#### Network Monitoring Tools

- **Intrusion Detection Systems (IDS)**
  - Monitor system activity and alert on possible intrusions.
  - Detect and alert on configured deviations.
  - Commonly monitor packet payload content for threat patterns.
  
- **Network Protocol Analyzers (Packet Sniffers)**
  - Capture and analyze network data traffic.
  - Tools like tcpdump and Wireshark record and investigate network communications.

#### Indicators of Compromise (IoC)

- Observable evidence that suggests signs of a potential security incident.

### Key Takeaways

- Monitoring and protecting networks from intrusions and attacks are key responsibilities of security professionals.
- Understanding network components and communications is essential for protection.
- Baselines help identify deviations from expected traffic patterns.
- Tools like IDS and packet sniffers support network monitoring efforts.

### Resources

- [Network traffic - MITRE ATT&CK®](https://attack.mitre.org/datasources/DS0029/)
- [Data exfiltration techniques - MITRE ATT&CK®](https://attack.mitre.org/tactics/TA0010/)

---
## Data exfiltration attacks

- **Data exfiltration:**
	- Unauthorized transmission of data from a system.

- **Defensive measures:**
	- Prevent attacker access.
	- Monitor network activity.
	- Protect assets.
	- Detect and stop the exfiltration.

---
## Learn More About Packet Captures

### Packets

- **Data packet**: A basic unit of information that travels from one device to another within a network.
- Packets form the basis of information exchange over a network.
- Each activity on the internet, like visiting a website, involves sending and receiving packets.
- In cybersecurity, packets provide valuable information for investigations.

#### Packet Components

1. **Header**
   - The most essential component; can have several headers (e.g., Ethernet, IP, TCP).
   - Provides routing information: source and destination IP addresses, packet length, protocol, packet identification numbers, etc.
   ![An IPv4 header with its thirteen fields](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Mi_kryGkRiyYUOJDIwnPCw_ac942d1eec284467a5ca533cb99c4bf1_S20G003.png?expiry=1716768000000&hmac=M9jxUVQIlFL4otgvsR6W2CG_Tuatu7ZuWsxQaseOjyA)

2. **Payload**
   - Follows the header and contains the actual data being delivered (e.g., the image being uploaded to a website).

3. **Footer**
   - Also known as the trailer, provides error-checking information.
   - Not used by most protocols, such as the Internet Protocol (IP).

### Network Protocol Analyzers (packet sniffer)

- Tools designed to capture and analyze data traffic within a network.
- Examples: tcpdump, Wireshark, TShark.
- Used for:
  - Monitoring networks and identifying suspicious activity.
  - Collecting network statistics (bandwidth, speed).
  - Troubleshooting network performance issues.

#### How Network Protocol Analyzers Work

1. **Packet Collection**
   - Packets are collected via the **Network Interface Card (NIC)**.
   - NICs must be in monitoring or promiscuous mode to capture all visible network data packets.
   - Positioning the network protocol analyzer in the appropriate network segment is crucial.

2. **Data Conversion**
   - The analyzer collects network traffic in raw binary format.
   - Converts binary data into a human-readable format for analysis.

### Capturing Packets

- **Packet sniffing**: The practice of capturing and inspecting data packets across a network.
- **Packet capture (p-cap)**: A file containing intercepted data packets.
- P-cap files can be analyzed using network protocol analyzers.
- P-cap libraries and formats:
  1. **Libpcap**: For Unix-like systems (e.g., Linux, MacOS).
  2. **WinPcap**: Older format for Windows systems.
  3. **Npcap**: Commonly used in Windows systems, designed by Nmap.
  4. **PCAPng**: Modern format that can capture packets and store data simultaneously.

**Note**: Intercepting private network communications without permission is illegal in many places.

### Key Takeaways

- Network protocol analyzers are essential investigative tools.
- Analysts use these tools to view and analyze packet capture files.
- Understanding network communications helps defend against intrusions.

### Resources for More Information

- [Packet Crafting - A Serious Crime](https://resources.infosecinstitute.com/topic/packet-crafting-a-serious-crime/)

---
## Investigate Packet Details

### Internet Protocol (IP)

#### IPv4

- **Version**: Indicates IP version (IPv4).
- **Internet Header Length (IHL)**: Specifies the length of the IPv4 header including any Options.
- **Type of Service (ToS)**: Provides information about packet priority for delivery.
- **Total Length**: Specifies the total length of the entire IP packet including the header and the data.
- **Identification**: Unique identifier for fragments of an original IP packet.
- **Flags**: Information about packet fragmentation.
- **Fragment Offset**: Identifies the correct sequence of fragments.
- **Time to Live (TTL)**: Limits how long a packet can be circulated in a network.
- **Protocol**: Specifies the protocol used for the data portion of the packet.
- **Header Checksum**: Checksum value used for error-checking the header.
- **Source Address**: Specifies the source address of the sender.
- **Destination Address**: Specifies the destination address of the receiver.
- **Options**: Optional field used to apply security options to a packet.

![IPv4 Header](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/jkb0TBrPQSq9YoCeruRfqA_e1ec815e1edd4447a9a51b7f8945ccf1_7Fe1r5PP-rO933_0njaasi_PLYxnCK70uwxT7ZVgtLukfU1L_3B4ppP4aiLOiZ1QNlZCuuLku28h-mpQ5lEnQKly8HIeoDkaEvqkdh4Xbb_U9ba52JscXUcrmQFcluGPBPqNqA1v_gYZwv_JqR4di7niNF2R5uy2JBR0r-QshhE6zOIghv4lUCWa96872A?expiry=1716768000000&hmac=nq_Pl06CKWRjHteIanwoPalKhD4fDdDL18uG1AU5024)

#### IPv6

- **Version**: Indicates IP version (IPv6).
- **Traffic Class**: Similar to the IPv4 Type of Service field.
- **Flow Label**: Identifies the packets of a flow.
- **Payload Length**: Specifies the length of the data portion of the packet.
- **Next Header**: Indicates the type of header that follows the IPv6 header such as TCP.
- **Hop Limit**: Similar to the IPv4 Time to Live field.
- **Source Address**: Specifies the source address of the sender.
- **Destination Address**: Specifies the destination address of the receiver.

![IPv6 Header](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/i8ZlXBWcQnKMc9AvaOlTrg_9ae604f634bc4ea3b0bced51911d32f1_XjvmdLkZuzfhKQ0zQ_4RnCZGNxP0FDCtB0i8iwWtu30GL05Ziixkcd3YNSK8ng5tiu3X3XVOypCPywtGP01diUAvVWEkjwGWk7E_4fpFZdntBgohToxkS5cNsyZtqKsRCmssQUmWlH8Xhn2oJKG55Kv0-CUjA8Kj3yhZXTWbjjV4pYcCH9EUwPWpyFnhCQ?expiry=1716768000000&hmac=sdBfuwZY8q3uzkwq0rOmW5OtKmjtz0X-P32BaQPZkrQ)
### Wireshark

#### Display Filters

##### Comparison Operators

|**Operator type**|**Symbol**|**Abbreviation**|
|---|---|---|
|Equal|==|eq|
|Not equal|!=|ne|
|Greater than|>|gt|
|Less than|<|lt|
|Greater than or equal to|>=|ge|
|Less than or equal to|<=|le|

**Pro tip:** Combine comparison operators with Boolean logical operators (and, or) and use parentheses for grouping and prioritizing search terms.

##### Contains Operator

- Filters packets that contain an exact match of a string of text.
- Example: `http contains "moved"`

![Contains Operator](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/U-VFvCZpR-C7DiBud3CJ6Q_3d58fbc8790a4163b1fbd8d6689cf0f1_CS_R-125_packet-capture.png?expiry=1716768000000&hmac=BH6kkWmg-YvOxG6fcfcEQ6Qso5tzNTQhAAUYr7I3ns8)

##### Matches Operator

- Filters packets based on regular expressions (regex).

#### Filter Toolbar

- Apply filters to a packet capture using Wireshark's filter toolbar.
- Example: `dns` to display packets containing the DNS protocol.

![Filter Toolbar](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/S2HoKdS_TnS0idDiU9XbJw_cb303cb11f2f45db944a6b22cbf3b4f1_ADA_R-125_DNS.png?expiry=1716768000000&hmac=Smjihwf1Y6DXUq2cZl6nG-nBTLEtn3ax_jaiL8AA9b0)

#### Filter for Protocols

- **dns**
- **http**
- **ftp**
- **ssh**
- **arp**
- **telnet**
- **icmp**

#### Filter for IP Address

- **Any IP address**: `ip.addr == 172.21.224.2`
- **Source IP address**: `ip.src == 10.10.10.10`
- **Destination IP address**: `ip.dst == 4.4.4.4`

#### Filter for MAC Address

- **Example**: `eth.addr == 00:70:f4:23:18:c4`

#### Filter for Ports

- **UDP port**: `udp.port == 53`
- **TCP port**: `tcp.port == 25`

### Follow Streams

- Wireshark feature that filters packets specific to a protocol and views streams.
- Useful for understanding the details of a conversation.
- Example: Examining HTTP conversation details to view the content of the exchanged request and response messages.

![Follow Stream](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qGiuzTybTNyYJXCUSuSStA_2353ba616b0c404d9b3d6df3af1fdef1_CS_R-125_dialog-box.png?expiry=1716768000000&hmac=6Wye9j-xv9tkUyx75snN59vtnt7yz2wcsUo1z4gktM0)

### Key Takeaways

- Packet analysis is an essential skill in cybersecurity.
- Display filters in Wireshark help isolate relevant packets.
- Practice investigating packet capture files using Wireshark.

### Resources

- [Wireshark official user guide](https://www.wireshark.org/docs/wsug_html/)

---
## Overview of tcpdump

### Introduction:

- A **network protocol analyzer (packet sniffer)** is a tool designed to capture and analyze data traffic within a network.

### What is tcpdump?

- **Tcpdump**: Command-line network protocol analyzer.
- **Packet Sniffing**: Capturing and inspecting data packets.

### Capturing Packets with tcpdump:

- **Syntax**: `sudo tcpdump [-i interface] [option(s)] [expression(s)]`
- **Root or Sudo Required**: Elevated permissions needed.
- **Network Interface**: Specify interface.
- **Options and Expressions**: Provide flexibility.

### Options:

- **-w**: Write captured packets to a file.
- **-r**: Read packets from a capture file.
- **-v**: Control verbosity.
- **-c**: Specify number of packets.
- **-n**: Disable name resolution.

### Expressions:

- **Filter Expressions**: Optional filters.
  - **Searching by Protocol**: Filter expressions can isolate network packets based on protocol (e.g., `ip6` for IPv6 traffic).
  - **Boolean Operators**: Use boolean operators like `and`, `or`, or `not` to further filter network traffic.
  - **Example**: `sudo tcpdump -r packetcapture.pcap -n 'ip and port 80'` combines two expressions (`ip` and `port 80`) using the `and` boolean operator.
  - **Pro Tip**: Use single or double quotes for multiple expressions. Parentheses can group and prioritize expressions, especially for complex commands (e.g., `ip and (port 80 or port 443)`).

### Interpreting Output:

- **Output Format**: Timestamp, source IP, source port, destination IP, destination port.
- **Additional Details**: TCP connection, flags, sequence numbers.

### Key Takeaways:

- Importance of capturing, filtering, and interpreting network packets.

### Resources:

- Tcpdump's official [tutorials and guides](https://www.tcpdump.org/).
- [Tcpdump tutorial by Daniel Miessler](https://danielmiessler.com/p/tcpdump/) for further learning.

---
## **Cybersecurity Terms and Concepts**

| Term                                                  | Definition                                                                                                       |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Command and control (C2)                              | The techniques used by malicious actors to maintain communications with compromised systems                      |
| Command-line interface (CLI)                          | A text-based user interface that uses commands to interact with the computer                                     |
| Data exfiltration                                     | Unauthorized transmission of data from a system                                                                  |
| Data packet                                           | A basic unit of information that travels from one device to another within a network                             |
| Indicators of compromise (IoC)                        | Observable evidence that suggests signs of a potential security incident                                          |
| Internet Protocol (IP)                                | A set of standards used for routing and addressing data packets as they travel between devices on a network       |
| Intrusion detection systems (IDS)                     | An application that monitors system activity and alerts on possible intrusions                                    |
| Media Access Control (MAC) Address                    | A unique alphanumeric identifier that is assigned to each physical device on a network                           |
| National Institute of Standards and Technology (NIST) | A framework for incident response consisting of four phases: Preparation; Detection and Analysis; Containment, Eradication and Recovery; and Post-incident activity |
| Network data                                          | The data that’s transmitted between devices on a network                                                        |
| Network protocol analyzer (packet sniffer)            | A tool designed to capture and analyze data traffic within a network                                             |
| Network traffic                                       | The amount of data that moves across a network                                                                 |
| Network Interface Card (NIC)                          | Hardware that connects computers to a network                                                                   |
| Packet capture (p-cap)                                | A file containing data packets intercepted from an interface or network                                          |
| Packet sniffing                                       | The practice of capturing and inspecting data packets across a network                                           |
| Playbook                                              | A manual that provides details about any operational action                                                     |
| Root user (or superuser)                              | A user with elevated privileges to modify the system                                                            |
| Sudo                                                  | A command that temporarily grants elevated permissions to specific users                                          |
| tcpdump                                               | A command-line network protocol analyzer                                                                         |
| Wireshark                                             | An open-source network protocol analyzer                                                                         |

---