# Introduction to operating systems
## Introduction to operating systems

- **Operating system (OS)**:
	- The interface between computer hardware and the user.

- **Hardware:**
	- The physical components of a computer.

---
## Operating System Comparison and Vulnerabilities

### Common Operating Systems

#### Windows and macOS

- **Windows:**
  - Introduced in 1985.
  - Closed-source.
  - [Microsoft Security Response Center (MSRC)](https://msrc.microsoft.com/update-guide/vulnerability) provides updates.
- **macOS:**
  - Introduced in 1984.
  - Partially open source.
  - Updates from [Apple Security Updates](https://support.apple.com/en-us/HT201222).

#### Linux

- Introduced in 1991.
- Completely open-source.
- Vulnerabilities listed in [CVE Report for Ubuntu](https://ubuntu.com/security/cves).

#### ChromeOS

- Launched in 2011.
- Partially open source, derived from Chromium OS.

#### Android and iOS

- **Android:**
  - Introduced in 2008.
  - Open source.
- **iOS:**
  - Introduced in 2007.
  - Partially open source.

### Vulnerabilities

#### Legacy Operating Systems

- Outdated systems still in use.
- Vulnerable due to lack of support.
  
#### General Vulnerability Management

- Regular updates crucial.
- Resources like [Microsoft Security Response Center (MSRC)](https://msrc.microsoft.com/update-guide/vulnerability), [Apple Security Updates](https://support.apple.com/en-us/HT201222), [CVE Report for Ubuntu](https://ubuntu.com/security/cves), and [Google Cloud Security Bulletin](https://cloud.google.com/support/bulletins) help manage vulnerabilities.

### Key Takeaways

- **Operating System Awareness:**
  - Understand common OSs and their vulnerabilities.
- **Legacy System Awareness:**
  - Recognize risks posed by legacy systems.
- **Vulnerability Management:**
  - Keep systems updated for security.

---
## Operating System Functionality

### Booting Process

- **BIOS vs. UEFI**:
  - BIOS: Basic Input/Output System, prevalent in older systems.
  - UEFI: Unified Extensible Firmware Interface, replaces BIOS in modern systems.
  - UEFI offers enhanced security features compared to BIOS.

- **Bootloader Activation**:
  - BIOS or UEFI activates the bootloader, a software program that boots the operating system.

### Task Completion Process

- **User**:
  - Initiates the task, such as accessing a reading or performing an action on the computer.

- **Application**:
	- Software program used by the user to complete a specific task, like a calculator or word processor.
	- Acts as an interface between the user and the operating system, facilitating user interactions and requests.

- **Operating System**:
  - Receives user's request from the application and directs its flow.
  - Interprets the request and communicates with hardware components to fulfill the task.

- **Hardware**:
  - Performs processing tasks to fulfill user-initiated requests.
  - Examples include CPU for calculations and hard drive for file storage.

### Analogy: Operating System as a Car

- Similarities between operating a computer and driving a car.
- Processes in the computer, like booting, are analogous to starting a car's engine.
- Users don't directly observe inner workings but rely on smooth operation.

### Analogy: Operating System as a Restaurant

- Ordering at a restaurant compared to using applications on a computer.
- Users make specific requests, like placing an order or printing a document.
- Operating system functions like the kitchen, interpreting requests and ensuring tasks are completed.

### Example: Downloading a File

- User initiates file download in the internet browser application.
- Browser communicates with the operating system to start the download process.
- Operating system directs the request to the appropriate hardware for processing.
- Hardware downloads the file, and the browser informs the user upon completion.

### Key Takeaways

- The operating system is essential for connecting applications and hardware to facilitate user tasks.
- It operates in the background, orchestrating communication and processing to ensure task completion.

---
## Virtualization Technology Notes

### Virtual Machines (VMs)

- Virtual machine (VM) is a virtual version of a physical computer.
- Example of virtualization: using software to create virtual representations of physical machines.
- **Virtualization:** Using software to simulate physical hardware, creating virtual systems.
- Virtual systems operate like physical machines but exist as code.
- Utilize virtual CPU, storage, and other hardware components.
- Multiple VMs can run on a single physical computer, sharing its resources.

### Benefits of VMs
#### Security

- VMs provide isolated environments, or sandboxes, enhancing security.
- Each VM is isolated from the host machine and other VMs.
- Isolation prevents malware from spreading across systems.
- Enables secure examination of infected systems or running malware for analysis.

#### Efficiency

- VMs streamline security tasks by allowing easy switching between them.
- Enables simultaneous operation of multiple VMs, enhancing efficiency.
- Comparable to city buses transporting many people simultaneously, reducing resource consumption.

### Managing VMs

- **Hypervisor:** Software for managing multiple VMs and connecting virtual and physical hardware.
- Hypervisors allocate shared resources of the physical host machine to VMs.
- Example: Kernel-based Virtual Machine (KVM), an open-source hypervisor supported by major Linux distributions.
- Built into the Linux kernel, simplifying VM creation on Linux machines.

### Other Forms of Virtualization

- Besides VMs, other virtualization technologies exist.
- Examples: Creating multiple virtual servers from a single physical server, establishing virtual networks for efficient hardware utilization.

### Key Takeaways

- Virtualization, including VMs, is crucial in the security industry.
- Benefits include isolation of malware and increased efficiency in security tasks.
- Despite benefits, vigilance is necessary as there's a risk of malicious software escaping virtualized environments.

---
## GUI versus CLI

- **User interface:**
	- A program that allows the user to control the functions of the operating system.

- **Graphical user interface (GUI):**
	- A user interface that uses icons on the screen to manage different tasks on the computer.

- **Basic GUI components:**
	- Start menu
	- Task bar
	- Desktop with icons and shortcuts

- **Command-line interface (CLI):**
	- A text-based user interface that uses commands to interact with the computer.

---
## The Command Line in Use

### CLI vs. GUI

- **Graphical User Interface (GUI):** Uses icons on the screen to manage tasks.
- **Command-Line Interface (CLI):** Text-based interface using commands to interact.

#### Display

- GUI: Graphics and icons.
- CLI: Text-based, resembling lines of code.

#### Function

- GUI: Allows one request at a time.
- CLI: Enables multiple requests simultaneously.

### Advantages of CLI in Cybersecurity

- **Efficiency:** CLI allows quicker navigation for experienced users, efficient for multiple tasks.
- **History File:** Linux CLI records command history, aiding incident response and tracking attacker actions.

### Key Takeaways

- Security analysts should be proficient in both GUI and CLI.
- CLI preferred in cybersecurity for multitasking and history tracking.

---
## **Cybersecurity Terms and Concepts**

| Term                              | Definition                                                                                      |
|-----------------------------------|------------------------------------------------------------------------------------------------|
| Application                       | A program that performs a specific task                                                        |
| Basic Input/Output System (BIOS) | A microchip that contains loading instructions for the computer and is prevalent in older systems |
| Bootloader                       | A software program that boots the operating system                                             |
| Command-line interface (CLI)     | A text-based user interface that uses commands to interact with the computer                    |
| Graphical user interface (GUI)   | A user interface that uses icons on the screen to manage different tasks on the computer        |
| Hardware                          | The physical components of a computer                                                          |
| Legacy operating system          | An operating system that is outdated but still being used                                       |
| Operating system (OS)            | The interface between computer hardware and the user                                            |
| Random Access Memory (RAM)       | A hardware component used for short-term memory                                                 |
| Unified Extensible Firmware Interface (UEFI) | A microchip that contains loading instructions for the computer and replaces BIOS on more modern systems |
| User interface                   | A program that allows the user to control the functions of the operating system                 |
| Virtual machine (VM)             | A virtual version of a physical computer                                                        |

---