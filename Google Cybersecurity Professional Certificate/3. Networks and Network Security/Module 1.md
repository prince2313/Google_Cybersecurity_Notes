# Network architecture
## What are networks?

- **Network:**
	- A group of connected devices.

- **Local Area Network (LAN):**
	- A network that spans small areas like an office building, a school, or a home.

- **Wide Area Network (WAN):**
	- A network that spans a large geographic area like a city, state, or country.

---
## Network tools

- **Hub:**
	- A network device that broadcasts information to every device on the network.

- **Switch:**
	- A device that makes connections between specific devices on a network by sending and receiving data between them

- **Router:**
	- A network device that connects multiple networks together.

- **Modem:**
	- A device that connects your router to the internet and brings internet access to the LAN.

- **Virtualization tools:**
	- Pieces of software that perform network operations.

---
## Network Components, Devices, and Diagrams

### Network Devices

- Devices maintain network information and services.
- Connect via wired and wireless connections.
- Send data packets with source and destination information.

### Router

- Connects to the internet through a modem.
- Directs traffic to devices on the network.
- May include firewall features for security.

### Firewall

- Monitors traffic to/from the network.
- Acts as the first line of defense.
- Configured by the organization for security rules.

### Server

- Provides information and services to clients.
- Examples: DNS servers, file servers, mail servers.

### Hubs and Switches

- Hubs: Broadcast data to all connected devices.
- Switches: Forward data only to intended recipients.

### Routers

- Connect different networks and direct traffic.
- Include firewall features for security.

### Modems and Wireless Access Points

- Modems: Connect to ISPs and translate signals.
- Wireless access points: Create Wi-Fi networks.

### Network Diagrams

- Visualize network architecture.
- Show connections between devices.
- Aid in understanding and securing the network.

---
## Cloud networks

- **Cloud computing:**
	- The practice of using remote servers, application, and network services that are hosted on the internet instead of on local physical devices.

- **Cloud network:**
	- A collection of servers or computers that stores resources and data in remote data centers that can be accessed via the internet.

- **Cloud service providers offer:**
	- On-demand storage
	- Processing power
	- Analytics

---
## Cloud Computing and Software-Defined Networks

### Computing Processes in the Cloud

- **Traditional Networks**: On-premise networks with physical devices.
- **Cloud Computing**: Utilizes remote servers, applications, and network services hosted on the internet.
- **Cloud Service Provider (CSP)**: Offers cloud computing services with large data centers.
    - **Categories of Services**:
        - **Software as a Service (SaaS)**: Operated by CSP, remotely accessible.
        - **Infrastructure as a Service (IaaS)**: Virtual computer components offered by CSP.
        - **Platform as a Service (PaaS)**: Tools for designing custom applications.

### Hybrid Cloud Environments

- Organizations use CSP services alongside on-premise resources.
- Multi-cloud: Organizations use multiple CSPs.
- **Benefits**: Cost reduction, resource control.

### Software-Defined Networks

- Virtual network devices and services provided by CSPs.
- **Modern Network Hardware**: Supports network virtualization and software-defined networking.
- **Cloud Networking**: SDN tools hosted on CSP servers.

### Benefits of Cloud Computing and SDNs

- **Reliability**: Consistent access with minimal interruption.
- **Cost**: Reduced upfront costs compared to on-premise infrastructure.
- **Scalability**: Elastic utility model for resource consumption.

### Key Takeaways

- CSPs offer modern technology services through the internet.
- SDNs enable dynamic network configurations, akin to cloud computing.
- Organizations benefit from improved reliability, cost savings, and scalability with CSPs.

### Additional Resources

- [Google Cloud (GC)](https://cloud.google.com/)

---
## Introduction to network communication

- **Data packet:**
	- A basic unit of information that travels from one device to another within a network.

- **Bandwidth:**
	- The maximum data transmission capacity over a network, measured by bits per second.

- **Speed:**
	- The rate at which a device sends and receives data, measured by bits per second.

- **Packet sniffing:**
	- The practice of capturing and inspecting data packets across a network.

---
## The TCP/IP Model

- **Transmission Control Protocol (TCP):**
	- An internet communication protocol that allows two devices to form a connection and stream data.

- **Internet Protocol (IP):**
	- A set of standards used for routing and addressing data packets as they travel between devices on a network.

- **Port:**
	- A software-based location that organizes the sending and receiving of data between devices on a network.

- **Common Port Number:**
	- Port 25 - Email.
	- Port 443 - Secure internet communication.
	- Port 20 - Large file transfers.

---
## The four layers of the TCP/IP model

- **TCP/IP model:**
	- A framework used to visualize how data is organized and transmitted across a network.

- Layers of the TCP/IP model:
	- Network access layer.
	- Internet layer.
	- Transport layer.
	- Application layer.

---
## Learn More about the TCP/IP Model

### Overview

- TCP/IP model: Framework for organizing and transmitting data across networks.
- Helps conceptualize network processes and communication.

### Differences between TCP/IP and OSI Model

- OSI Model: Organizes network protocols into seven layers.
- TCP/IP Model: Simplified version, four layers.

### TCP/IP Model Layers
#### Network Access Layer

- Deals with data packet creation and transmission.
- Includes physical hardware like hubs, modems, cables.
- Uses Address Resolution Protocol (ARP) to map IP to MAC addresses.

#### Internet Layer

- Ensures delivery to destination host on different networks.
- Attaches IP addresses to data packets.
- Common protocols: IP, ICMP.

#### Transport Layer

- Controls traffic flow between systems.
- Protocols: TCP (reliable transmission), UDP (connectionless).

##### Transmission Control Protocol (TCP)

- Establishes connection and streams data.
- Ensures reliable transmission.

##### User Datagram Protocol (UDP)

- Connectionless protocol.
- Used for real-time, performance-sensitive applications.

#### Application Layer

- Similar to application, presentation, session layers in OSI.
- Responsible for network requests and responses.
- Common protocols: HTTP, SMTP, SSH, FTP, DNS.

### TCP/IP Model versus OSI Model

- OSI: Seven layers, visually organizes network protocols.
- TCP/IP: Four layers, simplified version of OSI.
- Both define standards for networking and divide communication process into layers.

### Key Takeaways

- TCP/IP and OSI models help visualize network processes and protocols.
- TCP/IP: Four layers, OSI: Seven layers.
- Both aid in understanding data transmission between systems.

---
## OSI Model

### TCP/IP Model vs. OSI Model

- **TCP/IP Model:**
  - Framework for organizing and transmitting data across a network.
  - Four layers: Network Access, Internet, Transport, Application.
  - Helps in understanding network processes and identifying disruptions or threats.

- **OSI Model:**
  - Standardized concept with seven layers for network communication.
  - Used for communication among network and security professionals.
  - Provides a detailed understanding of network processes.

### Layer 7: Application Layer

- Involves processes directly interacting with the user.
- Includes networking protocols for user connection to the internet via applications.
- Examples: HTTP, HTTPS, SMTP, DNS.

### Layer 6: Presentation Layer

- Involves data translation and encryption.
- Adds and replaces data formats for compatibility.
- Functions: encryption, compression, character code set interpretation.
- Example: SSL for encrypting data between web servers and browsers.

### Layer 5: Session Layer

- Establishes and maintains connections between devices.
- Manages sessions for data transfer.
- Responsible for authentication, reconnection, and setting checkpoints.
- Coordinates with layers 4 and 6 for service requests and data transfer.

### Layer 4: Transport Layer

- Delivers data between devices.
- Handles data transfer speed, flow, and segmentation.
- Protocols: TCP, UDP.
- Segmentation: dividing large data transmissions into smaller segments.

### Layer 3: Network Layer

- Receives frames from the data link layer and delivers them to the destination.
- Uses IP addresses for routing data packets between networks.

### Layer 2: Data Link Layer

- Organizes data packet transmission within a single network.
- Home to switches and network interface cards.
- Protocols: NCP, HDLC, SDLC.

### Layer 1: Physical Layer

- Involves physical hardware for network transmission.
- Includes hubs, modems, cables, and wiring.
- Converts data packets into 0s and 1s for transmission across cables.

---
## IP addresses and network communication

- **Internet Protocol (IP):**
	- A set of standards used for routing and addressing data packets as they travel between devices on a network.

- Types of IP addresses:
	- IP version 4 (IPv4)
	- IP version 6 (IPv6)

- **Media Access Control (MAC) address:**
	- A unique alphanumeric identifier that is assigned to each physical device on a network.

---
## Components of Network Layer Communication

### Operations at the Network Layer

- Functions:
  - Addressing and delivery of data packets across the network.
  - Routing packets from one router to another until reaching the destination IP address.
  - Storage of destination IP address in routing tables along the packet's path.

- Data Packets:
  - Contain an IP address, used for routing by routers.
  - Referred to as IP packets (TCP) or datagrams (UDP).

### Format of an IPv4 Packet

- **Header:** Variable length (20 to 60 bytes).
  - Contains:
    - Source and destination IP addresses.
    - Header length and total packet length.
    - Identification, flags, and fragmentation offset.
    - Time to Live (TTL), protocol, and checksum.
    - Options field for security options.

- **Data:** Variable size, maximum of 65,535 bytes.
  - Carries message for transmission, like website information or email text.

### Difference between IPv4 and IPv6

- IPv4:
  - Addresses: Four decimal numbers separated by periods.
  - Example: 198.51.100.0.
  - Limited to 4.3 billion addresses.

- IPv6:
  - Addresses: Eight hexadecimal numbers separated by colons.
  - Example: 2002:0db8::ff21:0023:1234.
  - Allows up to 340 undecillion addresses.

- Packet Header:
  - IPv6 header format is simpler than IPv4.
  - IPv6 introduces the Flow Label field for special handling.

- Security:
  - IPv6 offers more efficient routing and eliminates address collisions.

### Key Takeaways

- Analyzing IP packet fields reveals security information.
- Examples: Packet origin and destination, used protocol.
- Understanding packet data aids in security decision-making.

---
## **Cybersecurity Terms and Concepts**

| Term                                     | Definition                                                                                                              |
| ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Bandwidth                                | The maximum data transmission capacity over a network, measured by bits per second.                                     |
| Cloud computing                          | The practice of using remote servers, applications, and network services that are hosted on the internet.               |
| Cloud network                            | A collection of servers or computers that stores resources and data in remote data centers accessible via the internet. |
| Data packet                              | A basic unit of information that travels from one device to another within a network.                                   |
| Hub                                      | A network device that broadcasts information to every device on the network.                                            |
| Internet Protocol (IP)                   | A set of standards used for routing and addressing data packets as they travel between devices on a network.            |
| Internet Protocol (IP) address           | A unique string of characters that identifies the location of a device on the internet.                                 |
| Local Area Network (LAN)                 | A network that spans small areas like an office building, a school, or a home.                                          |
| Media Access Control (MAC) address       | A unique alphanumeric identifier assigned to each physical device on a network.                                         |
| Modem                                    | A device that connects your router to the internet and brings internet access to the LAN.                               |
| Network                                  | A group of connected devices.                                                                                           |
| Open Systems Interconnection (OSI) model | A standardized concept that describes the seven layers computers use to communicate and send data over the network.     |
| Packet sniffing                          | The practice of capturing and inspecting data packets across a network.                                                 |
| Port                                     | A software-based location that organizes the sending and receiving of data between devices on a network.                |
| Router                                   | A network device that connects multiple networks together.                                                              |
| Speed                                    | The rate at which a device sends and receives data, measured by bits per second.                                        |
| Switch                                   | A device that makes connections between specific devices on a network by sending and receiving data between them.       |
| TCP/IP model:                            | A framework used to visualize how data is organized and transmitted across a network                                    |
| Transmission Control Protocol (TCP)      | An internet communication protocol that allows two devices to form a connection and stream data.                        |
| User Datagram Protocol (UDP)             | A connectionless protocol that does not establish a connection between devices before transmissions.                    |
| Wide Area Network (WAN)                  | A network that spans a large geographic area like a city, state, or country.                                            |

---