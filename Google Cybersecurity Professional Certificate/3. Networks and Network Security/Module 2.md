# **Network operations**
## Network protocols

- **Network protocols:**
	- A set of rules used by two or more devices on a network to describe the order of delivery of data and the structure of data.

- **Transmission Control Protocol (TCP):**
	- An internet communication protocol that allows two devices to form a connection and stream data.

- **Address Resolution Protocol (ARP):**
	- A network protocol used to determine the MAC address of the next router or device on the path.

- **Hypertext Transfer Protocol Secure (HTTPS):**
	- A network protocol that provides a secure method of communication between clients and servers.

- **Domain Name System (DNS):**
	- A networking protocol that translates internet domain names into IP addresses.

- **Security Protocol:**
	- HTTPS
	- SSL/TLS

---
## Common network protocols

### Introduction

- Network protocols are sets of rules facilitating communication between devices on a network.
- They dictate data delivery order and structure, serving as instructions for receiving devices.

### Categories of Network Protocols

1. **Communication Protocols:**
   - Govern data exchange in network transmission.
   - Include TCP, UDP, HTTP, and DNS.

2. **Management Protocols:**
   - Used for monitoring and managing network activity.
   - Examples include SNMP and ICMP.

3. **Security Protocols:**
   - Ensure secure data transmission.
   - HTTPS and SFTP are common security protocols.

### Communication Protocols

1. **Transmission Control Protocol (TCP):**
   - Facilitates reliable data transmission.
   - Uses a three-way handshake for connection establishment.

2. **User Datagram Protocol (UDP):**
   - Connectionless protocol suitable for real-time applications.
   - Doesn't guarantee delivery or order.

3. **Hypertext Transfer Protocol (HTTP):**
   - Application layer protocol for client-server communication.
   - HTTP is insecure; HTTPS provides encryption.

4. **Domain Name System (DNS):**
   - Translates domain names to IP addresses.
   - Primarily uses UDP but switches to TCP for large responses.

### Management Protocols

1. **Simple Network Management Protocol (SNMP):**
   - Used for monitoring and managing devices.
   - Allows tasks like password resets and bandwidth checks.

2. **Internet Control Message Protocol (ICMP):**
   - Reports errors in data transmission.
   - Commonly used for network troubleshooting.

### Security Protocols

1. **Hypertext Transfer Protocol Secure (HTTPS):**
   - Secure version of HTTP, encrypts data transmission.
   - Ensures confidentiality and integrity.

2. **Secure File Transfer Protocol (SFTP):**
   - Secure protocol for file transfer.
   - Utilizes SSH for encryption.

### Key Takeaways

- Understanding network protocols is crucial for cybersecurity analysts.
- Protocols form the basis of network communication and security.
- Analysts can leverage protocol knowledge to mitigate vulnerabilities and prevent attacks.

---
## Additional Network Protocols

### Network Address Translation (NAT)

- **Description:** NAT is a process where devices on a local network with private IP addresses communicate with the public internet using a single public IP address assigned to the router. It involves replacing private IP addresses with a public IP address for outgoing messages.
- **Associated Ports:** NAT operates at Layer 2 (Internet Layer) and Layer 3 (Transport Layer) of the TCP/IP model.

### Dynamic Host Configuration Protocol (DHCP)

- **Description:** DHCP is used to configure devices on a network by assigning unique IP addresses, DNS server addresses, and default gateways. DHCP servers operate on UDP port 67, while DHCP clients operate on UDP port 68.

### Address Resolution Protocol (ARP)

- **Description:** ARP translates IP addresses in data packets into MAC addresses of hardware devices. Devices maintain an ARP cache to map IP addresses to MAC addresses.
- **Associated Ports:** ARP operates at the Network Access Layer of the TCP/IP model and does not have a specific port number.

### Telnet

- **Description:** Telnet is an application layer protocol used for remote system connection. It sends information in clear text and operates on TCP port 23.

### Secure Shell (SSH)

- **Description:** SSH provides a secure connection with remote systems, offering secure authentication and encrypted communication. It operates on TCP port 22 and is more secure than Telnet.

### Post Office Protocol (POP3)

- **Description:** POP3 is used to manage and retrieve email from a mail server. It operates on TCP/UDP port 110 for unencrypted communication and TCP/UDP port 995 using SSL/TLS encryption.

### Internet Message Access Protocol (IMAP)

- **Description:** IMAP is used for incoming email, downloading headers, and message content. It operates on TCP port 143 for unencrypted communication and TCP port 993 with SSL/TLS encryption.

### Simple Mail Transfer Protocol (SMTP)

- **Description:** SMTP transmits and routes email from the sender to the recipient's address. It operates on TCP/UDP port 25 for unencrypted communication and TCP/UDP port 587 with TLS encryption.

### SMTPS

- **Description:** SMTPS is an extension of SMTP that uses TLS encryption on TCP/UDP port 587 to secure email transmission.

***"As a cybersecurity analyst, it's crucial to comprehend these protocols and their associated port numbers. This understanding is essential for effective network monitoring and security management."***

---
## Wireless protocols

- **IEEE 802.11 (Wi-Fi):** 
	- A set of standards that define communication for wireless LANs.

- **Wi-Fi Protected Access (WPA):** 
	- A wireless security protocol for devices to connect to the internet.

---
## The Evolution of Wireless Security Protocols

### Introduction to Wireless Communication Protocols

- Wi-Fi refers to a set of standards defining communication for wireless LANs.
- Wi-Fi standards are based on the 802.11 family of internet communication standards by IEEE.

### Wired Equivalent Privacy (WEP)

- **Description:** Developed in 1999, WEP aimed to provide privacy on wireless networks similar to wired networks.
- **Issues:** Vulnerable to attacks due to weak encryption.
- **Usage:** Largely obsolete but may still be encountered.

### Wi-Fi Protected Access (WPA)

- **Description:** Developed in 2003 as an improvement over WEP.
- **Features:** Used Temporal Key Integrity Protocol (TKIP) and message integrity check for better security.
- **Vulnerabilities:** Vulnerable to KRACK attacks due to flaws in authentication handshake.
- **Transitional:** Intended as a transitional measure with backwards compatibility.

### WPA2

- **Description:** Released in 2004, improved upon WPA by using Advanced Encryption Standard (AES).
- **Features:** Used Counter Mode Cipher Block Chain Message Authentication Code Protocol (CCMP) for encapsulation and message authentication.
- **Modes:** Personal mode for home networks, enterprise mode for business applications.
- **Vulnerabilities:** Vulnerable to KRACK attacks.

### WPA3

- **Description:** Released in 2018 as a secure Wi-Fi protocol.
- **Improvements:** Addresses KRACK attacks vulnerability, uses Simultaneous Authentication of Equals (SAE), and offers increased encryption.
- **Key Differences:** Enhanced security with 128-bit encryption, optional 192-bit encryption in WPA3-Enterprise mode.

### Key Takeaways

- Understanding the history and vulnerabilities of Wi-Fi security protocols is crucial for protecting wireless networks.
- Importance of ensuring devices use up-to-date security technologies to mitigate risks.

---
## Firewalls and network security measures

- **Firewall:**
	- A network security device that monitors traffic to or from your network.

- **Port filtering:**
	- A firewall function that blocks or allows certain port numbers to limit unwanted communication.

- **Cloud-based firewalls:**
	- Software firewalls that are hosted by the cloud service provider.

- **Stateful:**
	- A class of firewall that keeps track of information passing through it and proactively filters out threats.

- **Stateless:**
	- A class of firewall that operates based on predefined rules and does not keep track of information from data packets.

- **Benefits of next generation firewalls (NGFWs):**
	- Deep packet inspection.
	- Intrusion protection.
	- Threat intelligence.

---
## Virtual private networks (VPNs)

- **Virtual private network (VPN):**
	- A network security service that changes your public IP address and masks your virtual location so that you can keep your data private when you are using a public network like the internet.

- **Encapsulation:**
	- A process performed by a VPN service that protects your data by wrapping sensitive data in other data packets.

---
## Security zones

- **Security zone:**
	- A segment of a company’s network that protects the internal network from the internet.

- **Network segmentation:**
	- A security technique that divides the network into segments.

- **Uncontrolled zone:**
	- The portion of the network outside the organization.

- **Controlled zone:**
	- A subnet that protects the internal network from the uncontrolled zone.

- **Area of the controlled zone:**
	- Demilitarized zone (DMZ)
	- Internal network
	- Restricted zone

---
## Subnetting and CIDR

### Overview of Subnetting

- Subnetting is the subdivision of a network into logical groups called subnets.
- It divides up a network address range into smaller subnets based on IP addresses and network masks.
- Subnetting creates a network of devices to function as their own network, improving efficiency and enabling the creation of security zones.

### Classless Inter-Domain Routing (CIDR) Notation for Subnetting

- CIDR is a method of assigning subnet masks to IP addresses to create subnets.
- It replaced classful addressing, expanding the number of available IPv4 addresses.
- CIDR IP addresses are formatted like IPv4 addresses but include a slash ("/") followed by a number indicating the IP network prefix.
- CIDR addressing reduces routing table entries and provides more available IP addresses within networks.
- You can try converting CIDR to IPv4 addresses and vice versa through an online conversion tool, like [IPAddressGuide](https://www.ipaddressguide.com/cidr), for practice and better understanding.

### Security Benefits of Subnetting

- Subnetting allows organizations to create smaller networks within their private network without requesting additional IP addresses from ISPs.
- It uses network bandwidth more efficiently and improves network performance.
- Subnetting is a component of creating isolated subnetworks through physical isolation, routing configuration, and firewalls.

### Key Takeaways

- Subnetting is a common security strategy used by organizations to improve network efficiency and create security zones within their networks.

---
## Proxy servers

- **Proxy server:**
	- A server that fulfills the requests of its clients by forwarding them to other servers.

- **Forward proxy server:**
	- A server that regulates and restricts a person’s access to the internet.

- **Reverse proxy server:**
	- A server that regulates and restricts the internet's access to an internal server.

---
## Virtual networks and privacy

### Overview

- Understanding network operations fundamentals is crucial for network security.
- Securing private networks involves maintaining data confidentiality and restricting access to authorized users.
- Explores network security topics: virtual private networks (VPNs), proxy servers, firewalls, and security zones.

### Common network protocols

- **Communication Protocols:**
    - TCP, UDP, SMTP
    - Establish connections between servers.
- **Management Protocols:**
    - ICMP
    - Troubleshoot network issues.
- **Security Protocols:**
    - IPSec, SSL/TLS
    - Provide encryption for data in transit.

### Additional Protocols

- **HTTP (HyperText Transfer Protocol):**
    - Application layer protocol for browser-server communication.
- **DNS (Domain Name System):**
    - Application layer protocol for host name to IP address translation.
- **ARP (Address Resolution Protocol):**
    - Network layer protocol for IP address to physical machine/MAC address mapping.

### Wi-Fi Security Protocols

- Introduces wireless security protocols: WEP, WPA, WPA2, WPA3.
- WPA3 encrypts traffic using AES cipher.
- WPA2 and WPA3 offer personal and enterprise modes.

### Network security tools and practices
#### Firewalls

- Network virtual appliances or hardware devices.
- Inspect and filter network traffic before entering the private network.
- Categories: Stateless and Stateful.
- Next-generation firewalls (NGFWs) offer advanced features like deep packet inspection and intrusion prevention.

#### Proxy servers

- Utilize NAT to serve as a barrier between internal clients and external threats.
- Forward proxies handle internal client queries, while reverse proxies handle external system requests to internal services.
- Some proxy servers can be configured with filtering rules.

#### Virtual Private Networks (VPN)

- Encrypt data in transit and hide IP addresses.
- Use encapsulation to wrap unencrypted data in encrypted packets.
- Used by enterprises and individuals for privacy and security.
- Integration with SD-WAN for secure connectivity across multiple locations.

### Key takeaways

- Three main categories of network protocols: communication, management, and security.
- Fundamentals of firewalls, proxy servers, and VPNs.
- Increasing adoption of cloud-based network security with VPN and SD-WAN capabilities.

---
## VPN protocols: Wireguard and IPSec

### Introduction to VPNs

- VPN (Virtual Private Network): A network security service that changes your public IP address and hides your virtual location to keep your data private, especially when using public networks like the internet.
- VPNs provide a server that acts as a gateway between a computer and the internet, creating a secure tunnel to encrypt data in transit.

### Remote access and site-to-site VPNs

- **Remote access VPNs:**
    - Used by individual users to establish a connection between a personal device and a VPN server.
    - Encrypt data sent or received through a personal device.
- **Site-to-site VPNs:**
    - Used by enterprises to extend their network to other networks and locations, particularly useful for organizations with multiple offices worldwide.
    - IPSec commonly used to create encrypted tunnels between primary and remote networks.
    - Complex to configure and manage compared to remote VPNs.

### WireGuard VPN vs. IPSec VPN

- **WireGuard VPN:**
    - High-speed VPN protocol with advanced encryption.
    - Simple to set up and maintain.
    - Can be used for both site-to-site and client-server connections.
    - Relatively newer and known for enhanced download speeds due to fewer lines of code.
    - Open-source, making it easier for deployment and debugging.
    - Suitable for processes requiring faster download speeds like streaming video or downloading large files.
- **IPSec VPN:**
    - Older and more complex VPN protocol.
    - Widely used by VPN providers to encrypt and authenticate data packets.
    - Supported by many operating systems due to its longer history and widespread adoption.
    - Known for extensive security testing and widespread adoption.
    - Some clients prefer IPSec due to its history and security features.

### Key Takeaways

- VPN protocols determine how data moves between endpoints, similar to network protocols.
- Two main types of VPNs: remote access and site-to-site.
- Remote access VPNs establish connections between personal devices and VPN servers, encrypting data exchanged.
- Site-to-site VPNs extend networks to different locations, often using IPSec for encrypted connections.
- WireGuard and IPSec are VPN protocols with different characteristics, suitable for various use cases based on speed, simplicity, and compatibility.

---
## **Cybersecurity Terms and Concepts**

| Term                                       | Description                                                                                                                                                               |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Address Resolution Protocol (ARP)          | A network protocol used to determine the MAC address of the next router or device on the path                                                                            |
| Cloud-based firewalls                     | Software firewalls that are hosted by the cloud service provider                                                                                                         |
| Controlled zone                           | A subnet that protects the internal network from the uncontrolled zone                                                                                                    |
| Domain Name System (DNS)                   | A networking protocol that translates internet domain names into IP addresses                                                                                              |
| Encapsulation                             | A process performed by a VPN service that protects your data by wrapping sensitive data in other data packets                                                             |
| Firewall                                  | A network security device that monitors traffic to or from your network                                                                                                    |
| Forward proxy server                      | A server that regulates and restricts a person’s access to the internet                                                                                                    |
| Hypertext Transfer Protocol (HTTP)        | An application layer protocol that provides a method of communication between clients and website servers                                                                  |
| Hypertext Transfer Protocol Secure (HTTPS) | A network protocol that provides a secure method of communication between clients and servers                                                                              |
| IEEE 802.11 (Wi-Fi)                       | A set of standards that define communication for wireless LANs                                                                                                             |
| Network protocols                         | A set of rules used by two or more devices on a network to describe the order of delivery of data and the structure of data                                                |
| Network segmentation                      | A security technique that divides the network into segments                                                                                                                 |
| Port filtering                            | A firewall function that blocks or allows certain port numbers to limit unwanted communication                                                                             |
| Proxy server                              | A server that fulfills the requests of its clients by forwarding them to other servers                                                                                      |
| Reverse proxy server                      | A server that regulates and restricts the internet's access to an internal server                                                                                          |
| Secure File Transfer Protocol (SFTP)      | A secure protocol used to transfer files from one device to another over a network                                                                                         |
| Secure shell (SSH)                        | A security protocol used to create a shell with a remote system                                                                                                             |
| Security zone                             | A segment of a company’s network that protects the internal network from the internet                                                                                      |
| Simple Network Management Protocol (SNMP) | A network protocol used for monitoring and managing devices on a network                                                                                                    |
| Stateful                                  | A class of firewall that keeps track of information passing through it and proactively filters out threats                                                                 |
| Stateless                                 | A class of firewall that operates based on predefined rules and does not keep track of information from data packets                                                        |
| Subnetting                                | The subdivision of a network into logical groups called subnets                                                                                                             |
| Transmission Control Protocol (TCP)       | An internet communication protocol that allows two devices to form a connection and stream data                                                                            |
| Uncontrolled zone                         | The portion of the network outside the organization                                                                                                                        |
| Virtual private network (VPN)             | A network security service that changes your public IP address and masks your virtual location so that you can keep your data private when you are using a public network |
| Wi-Fi Protected Access (WPA)              | A wireless security protocol for devices to connect to the internet                                                                                                         |

---