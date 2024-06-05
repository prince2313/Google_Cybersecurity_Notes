# The Linux operating system
## Introduction to Linux

- **Linux:**
	- An open source operating system.

---
## Linux architecture

- **Components of Linux:**
	- User
	- Application
	- Shell
	- Filesystem Hierarchy Standard
	- Kernel
	- Software

- **User:**
	- The person interacting with a computer.

- **Application:**
	- A program that performs a specific task.

- **Shell:**
	- The command-line interpreter.

- **Filesystem Hierarchy Standard (FHS):**
	- The component of the Linux OS that organizes data.

- **Kernel:**
	- The component of the Linux OS that manages processes and memory.

- **Hardware**:
	- The physical components of a computer.

---
## Linux Architecture Explained

- **User**
  - Initiates and manages computer tasks.
  - Linux is multi-user, allowing multiple users to access resources simultaneously.

- **Applications**
  - Programs performing specific tasks.
  - Managed via package managers; packages form applications.

- **Shell**
  - Command-line interpreter.
  - Facilitates communication between users and the kernel.

- **Filesystem Hierarchy Standard (FHS)**
  - Organizes data storage locations in the OS.
  - Specifies where data is stored.

- **Kernel**
  - Manages processes and memory.
  - Communicates with applications.
  - Controls hardware functions.

- **Hardware**
  - **Peripheral Devices**
    - Attached to and controlled by the computer.
    - Examples: monitors, printers, keyboard, mouse.
  - **Internal Hardware**
    - Essential components for computer operation.
    - Includes CPU, RAM, and hard drive(s).

### Key Takeaways

- Understanding Linux architecture is crucial for security analysts.
- Components include user, applications, shell, FHS, kernel, and hardware.
- Each component plays a vital role in Linux functionality.

---
## Linux distributions

- **Distributions:**
	- The different versions of Linux.

- **Parent distributions:**
	- Red Hat Enterprise Linux (CentOS)
	- Slackware (SUSE)
	- Debian (Ubuntu and KALI LINUX)

---
## KALI LINUX

- **Penetration test (pen test):**
	- A simulated attack that helps identify vulnerabilities in systems, networks, websites, applications, and processes.

- **Penetration testing tools in Kali Linux:**
	- Metasploit
	- Burp Suite
	- John the Ripper

- **Digital forensics:**
	- The practice of collecting and analyzing data to determine what has happened after an attack.

- **Digital forensics tools in Kali Linux::**
	- tcpdump
	- Wireshark
	- Autospy

---
## More Linux Distributions

### KALI LINUX

- Open-source distribution based on Debian.
- Widely used in the security industry.
- Pre-installed with tools for penetration testing and digital forensics.
- Key activities: penetration testing and digital forensics.

### Ubuntu

- Open-source, user-friendly distribution.
- Has both CLI and GUI.
- Debian-derived and includes common applications.
- Large community support.
- Widely used for cloud computing.

### Parrot

- Open-source distribution for security.
- Pre-installed with tools for penetration testing and digital forensics.
- Based on Debian.
- User-friendly with GUI and CLI.

### Red Hat Enterprise Linux

- Subscription-based distribution for enterprise use.
- Offers dedicated support team.
- Not free.

### CentOS

- Open-source distribution related to Red Hat.
- Uses Red Hat's source code.
- Community-supported.
- Does not offer enterprise support.

## Key Takeaways

- KALI LINUX ™, Ubuntu, Parrot, Red Hat, and CentOS are widely used Linux distributions.
- Important for security analysts to be familiar with these distributions.

---
## Package Managers for Installing Applications

### Introduction to Package Managers

- A package is a piece of software that can be combined with others to form an application.
- Packages contain necessary files, including dependencies, for installation.
- Package managers help install, manage, and remove packages.
- Using the most recent version of a package is important for security.

### Types of Package Managers

- Linux distributions often derive from parent distributions (e.g., Debian or Red Hat).
- Package managers are tailored to specific distributions.
- Red Hat Package Manager (RPM) for Red Hat-derived distributions.
- dpkg for Debian-derived distributions.
- Different file extensions: .rpm for RPM, .deb for dpkg.

### Package Management Tools

- Advanced Package Tool (APT)
  - Used with Debian-derived distributions.
  - Command-line tool for managing, searching, and installing packages.
- Yellowdog Updater Modified (YUM)
  - Used with Red Hat-derived distributions.
  - Command-line tool for managing, searching, and installing packages.
  - Works with .rpm files.

## Key Takeaways

- Packages are software pieces forming applications.
- Managed by package managers tailored to specific Linux distributions.
- Package management tools like APT and YUM aid in package handling through the shell.
- Debian-derived distributions use dpkg and APT.
- Red Hat-derived distributions use RPM and YUM.

---
## Introduction to the shell

- **Shell:**
	- The command-line interpreter.

- **Command:**
	- An instruction telling the computer to do something.

---
## Different Types of Shells

### Communicate through a Shell

- The shell is a command-line interpreter.
- Acts as a translator between users and the computer system.
- Executes commands, sends them to the kernel, and returns results.

### Types of Shells

- **Bourne-Again Shell (bash)**
- **C Shell (csh)**
- **Korn Shell (ksh)**
- **Enhanced C Shell (tcsh)**
- **Z Shell (zsh)**
- Each shell may have different features and syntax.

### Bash

- Default shell in most Linux distributions.
- User-friendly and suitable for basic commands and larger projects.
- Widely used in the cybersecurity profession.

## Key Takeaways

- Shells are fundamental in Linux, acting as translators between users and the system.
- Various shell types exist, each with its own features and syntax.
- Bash is the most commonly used shell in cybersecurity, known for its user-friendliness and versatility.

---
## Input and output in the shell

- **Standard input:**
	- Information received by the OS via the command line.

- **echo:**
	- A Linux command that outputs a specified string of text..

- **String data:**
	- Data consisting of an ordered sequence of characters.

- **Standard output:**
	- Information returned by the OS through the shell.

- **Standard error:**
	- An error message returned by the OS through the shell.

---
## **Cybersecurity Terms and Concepts**

| Term                                | Description                                                                                         |
| ----------------------------------- | --------------------------------------------------------------------------------------------------- |
| Application                         | A program that performs a specific task                                                             |
| Bash                                | The default shell in most Linux distributions                                                       |
| CentOS                              | An open-source distribution closely related to Red Hat                                              |
| Central Processing Unit (CPU)       | A computer’s main processor, used to perform general computing tasks                                |
| Command                             | An instruction telling the computer to do something                                                 |
| Digital forensics                   | The practice of collecting and analyzing data to determine what has happened after an attack        |
| Directory                           | A file that organizes where other files are stored                                                  |
| Distributions                       | Different versions of Linux                                                                         |
| File path                           | The location of a file or directory                                                                 |
| Filesystem Hierarchy Standard (FHS) | The component of the Linux OS that organizes data                                                   |
| Graphical user interface (GUI)      | A user interface that uses icons on the screen to manage different tasks on the computer            |
| Hard drive                          | A hardware component used for long-term memory                                                      |
| Hardware                            | The physical components of a computer                                                               |
| Internal hardware                   | Components required to run the computer                                                             |
| Kali Linux ™                        | An open-source distribution of Linux widely used in the security industry                           |
| Kernel                              | The component of the Linux OS that manages processes and memory                                     |
| Linux                               | An open-source operating system                                                                     |
| Package                             | A piece of software that can be combined with other packages to form an application                 |
| Package manager                     | A tool that helps users install, manage, and remove packages or applications                        |
| Parrot                              | An open-source distribution commonly used for security                                              |
| Penetration test (pen test)         | A simulated attack that helps identify vulnerabilities in systems, networks, websites, applications |
| Peripheral devices                  | Hardware components that are attached and controlled by the computer system                         |
| Random Access Memory (RAM)          | A hardware component used for short-term memory                                                     |
| Red Hat® Enterprise Linux®          | A subscription-based distribution of Linux built for enterprise use                                 |
| Shell                               | The command-line interpreter                                                                        |
| Standard error                      | An error message returned by the OS through the shell                                               |
| Standard input                      | Information received by the OS via the command line                                                 |
| Standard output                     | Information returned by the OS through the shell                                                    |
| String data                         | Data consisting of an ordered sequence of characters                                                |
| Ubuntu                              | An open-source, user-friendly distribution widely used in security and other industries             |
| User                                | The person interacting with a computer                                                              |

---