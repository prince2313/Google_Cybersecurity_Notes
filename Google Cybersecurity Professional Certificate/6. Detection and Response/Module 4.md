# Network traffic and logs using IDS and SIEM tools
## Best Practices for Log Collection and Management
### Logs

- **Definition**: Records of events within an organization's systems.
- **Original Purpose**: Troubleshooting technology issues (e.g., error logs).
- **Modern Use**: Provides insights beyond troubleshooting; essential for security incident investigations.

#### Log Sources

- **Logging Receivers**: Tools like SIEM (Security Information and Event Management) systems consolidate logs for centralized access.
- **Log Analysis**: Process of examining logs to identify events of interest.

#### Types of Logs

- **Network Logs**: Generated by network devices (firewalls, routers, switches).
- **System Logs**: Generated by operating systems (Chrome OS™, Windows, Linux, macOS®).
- **Application Logs**: Generated by software applications (e.g., smartphone apps).
- **Security Logs**: Generated by devices/systems (e.g., antivirus software, intrusion detection systems).
- **Authentication Logs**: Generated during authentication events (e.g., successful login attempts).

#### Log Details

- **Common Elements**: Date, time, location, action, author.
- **Example**:
  - Standard Log: `Login Event [05:45:15] User1 Authenticated successfully`
  - Verbose Log: `Login Event [2022/11/16 05:45:15.892673] auth_performer.cc:470 User1 Authenticated successfully from device1 (192.168.1.2)`

### Log Management

- **Definition**: Process of collecting, storing, analyzing, and disposing of log data.

#### What to Log

- **Critical Aspect**: Choose log sources that contain useful information.
- **Considerations**: Avoid overlogging to reduce storage/maintenance costs and performance issues.
- **PII**: Handle personally identifiable information (PII) with care, considering legal restrictions.

#### The Issue with Overlogging

- **Disadvantages**:
  - Increased storage/maintenance costs.
  - System performance issues.
  - Difficulty in identifying important events.

#### Log Retention

- **Regulatory Requirements**: Some industries have specific log retention requirements.
- **Examples**:
  - Public Sector: Federal Information Security Modernization Act (FISMA)
  - Healthcare: Health Insurance Portability and Accountability Act of 1996 (HIPAA)
  - Financial Services: Payment Card Industry Data Security Standard (PCI DSS), Gramm-Leach-Bliley Act (GLBA), Sarbanes-Oxley Act of 2002 (SOX)

#### Log Protection

- **Importance**: Maintain log integrity to prevent tampering by malicious actors.
- **Centralized Log Server**:
  - Logs are sent to a dedicated server rather than stored locally.
  - Provides a barrier between attackers and log data.

### Key Takeaways

- Proper collection, storage, and protection of logs are crucial for incident investigations.
- A detailed log management plan improves log usefulness and resource efficiency.

---
## Log File Formats Overview

### JSON (JavaScript Object Notation)

#### Lightweight Data Interchange Format

- Designed for easy data exchange.
- Commonly used in web technologies and cloud environments.

#### Key Characteristics

- **Key-Value Pairs**: Basic unit of JSON data.
    - Consists of a key and its corresponding value.
- **Syntax Elements**: Comma, double quotes, curly brackets, square brackets.
- **Example**:

```json
{
  "Alert": "Malware",
  "Alert code": 1090,
  "severity": 10
}
```

### Syslog

#### Versatile Logging System

- Serves as a protocol, service, and log format.
- Widely used in Unix® systems.

#### Components

- **Header**:
	- Timestamp: YYYY-MM-DDTHH:MM.sssZ (Ex - 2022-03-21T01:11:11.003Z)
    - Hostname: Name of the logging machine.
    - Application: Name of the logging application.
    - Message ID: Identifier for the message.
- **Structured-Data**:
    - Additional context provided in key-value pairs.
- **Message**:
    - Detailed description of the event.
- **Priority (PRI)**:
    - Indicates the urgency of the event.

#### Example:

```cs
<236>1 2022-03-21T01:11:11.003Z virtual.machine.com evntslog - ID01 [user@32473 iut="1" eventSource="Application" eventID="9999"] This is a log entry!
```

### XML (eXtensible Markup Language)

#### Flexible Data Format

- Widely used for data storage and transmission.
- Native to Windows systems.

#### Core Elements

- **Tags**:
    - Enclosed in angle brackets.
    - Must have a start and end tag.
- **Elements**:
    - Combination of data and tags.
    - Root element contains child elements.
- **Attributes**:
    - Provide additional information about elements.
    - Enclosed within the start tag.

#### Example:

```xml
<EventData>
  <Data Name='SubjectUserSid'>S-2-3-11-160321</Data>
  <Data Name='SubjectUserName'>JSMITH</Data>
  <Data Name='SubjectDomainName'>ADCOMP</Data>
  <Data Name='SubjectLogonId'>0x1cf1c12</Data>
  <Data Name='NewProcessId'>0x1404</Data>
</EventData>
```

### CSV (Comma Separated Value)

#### Tabular Data Format

- Uses commas to separate data values.
- Commonly used in spreadsheet applications.

#### Characteristics

- Fields correspond to the position of data values.
- Field names might not be included in logs.

#### Example:

```cs
2009-11-24T21:27:09.534255,ALERT,192.168.2.7, 1041,x.x.250.50,80,TCP,ALLOWED,1:2001999:9,"ET MALWARE BTGrab.com Spyware Downloading Ads",1
```

### CEF (Common Event Format)

- **Common Event Format (CEF):** A log format that uses key-value pairs to structure data and identify fields and their corresponding values

- **Fields:** The CEF syntax is defined as containing the following fields: 
	- **Syslog Timestamp**: Sep 29 08:26:10
	- **Syslog Hostname**: host
	- **Version**: CEF:1
	- **Device Vendor**: Security
	- **Device Product**: threatmanager
	- **Device Version**: 1.0
	- **Signature ID**: 100
	- **Name**: worm successfully stopped
	- **Severity**: 10
	- **Extension**: This field contains data written as key-value pairs. There are two IP addresses, src=10.0.0.2 and dst=2.1.2.2, and a source port number spt=1232. Extensions are not required and are optional to add.

#### Example:

```cs
Sep 29 08:26:10 host CEF:1|Security|threatmanager|1.0|100|worm successfully stopped|10|src=10.0.0.2 dst=2.1.2.2 spt=1232
```

### Additional Notes

#### Log Contents

- Logs typically include a header, structured data, and a message.
- Headers contain timestamps, hostnames, application names, and message IDs.

#### Key Takeaways

- Understanding various log formats is crucial for effective security analysis.
- Logs from different sources may require different interpretation techniques.

## Resources for more information

- To learn more about the syslog protocol including priority levels, check out [The Syslog Protocol](https://www.rfc-editor.org/rfc/rfc5424).
- If you would like to explore generating log formats, check out this open-source [test data generator tool](https://generatedata.com/).
- To learn more about timestamp formats, check out [Date and Time on the Internet: Timestamps](https://www.rfc-editor.org/rfc/rfc3339).

---
## Detection Tools and Techniques

### Overview

- **Intrusion Detection Systems (IDS)**:
  - Vital for cybersecurity.
  - Detect and respond to security threats.
  - Utilize various detection techniques.

#### Host-based Intrusion Detection System (HIDS)

- **Definition**:
  - A **Host-based Intrusion Detection System (HIDS)** is an application that monitors the activity of individual hosts (endpoints) on a network.
  
- **Functionality**:
  - Monitors individual hosts.
  - Detects anomalies and unauthorized behavior.
  - Focuses on file system changes, resource utilization, etc.

#### Network-based Intrusion Detection System (NIDS)

- **Definition**:
  - A **Network-based Intrusion Detection System (NIDS)** is an application that monitors network traffic and data flows.
  
- **Functionality**:
  - Monitors network traffic and data flows.
  - Identifies potential security threats.
  - Analyzes network packets for malicious activities.

### Detection Techniques

#### Signature-based Analysis

- **Definition**:
  - **Signature-based Analysis** is a detection method that compares events with predefined signatures of known threats.

- **Approach**:
  - Compares events with predefined signatures.
  - Effective against known threats.

- **Advantages**:
  - Low false positive rate.

- **Disadvantages**:
  - Vulnerable to evasion.
  - Requires frequent signature updates.
  - Limited to known threats.

#### Anomaly-based Analysis

- **Definition**:
  - **Anomaly-based Analysis** is a detection method that identifies deviations from normal behavior.

- **Approach**:
  - Identifies deviations from normal behavior.
  - Detects new or unknown threats.

- **Advantages**:
  - Ability to detect new threats.

- **Disadvantages**:
  - Higher false positive rate.
  - Susceptible to pre-existing compromises.

### Additional Definitions
#### Telemetry

- **Definition**:
	- **Telemetry** refers to the process of collecting and transmitting data from remote or inaccessible sources to a monitoring or control system for analysis.
#### Endpoint

- **Definition**:
	- An **Endpoint** is any device connected to a network, such as a computer, laptop, smartphone, or server. Endpoints are often the target of cyberattacks and are protected by security measures like HIDS and antivirus software.

### Conclusion

- **Importance of IDS**:
  - Crucial for proactive threat detection.
  - Enhances cybersecurity posture.
  - Enables effective incident response.

---
## Overview of Suricata

- **Introduction to Suricata**
    - [Suricata](https://suricata.io/) is an open-source intrusion detection system, intrusion prevention system, and network analysis tool.
    - **Features**: 
        - **IDS**: Network-based IDS to monitor network traffic and alert on suspicious activities and intrusions. Can also be host-based IDS.
        - **IPS**: Can function as an intrusion prevention system to detect and block malicious activity and traffic.
        - **NSM**: Network security monitoring to produce and save relevant network logs, useful for forensics and incident response.
        
- **Rules**
    - Used to identify specific patterns, behavior, and conditions of network traffic indicating malicious activity.
    - **Signature Analysis**:
        - **Action**: Describes the action to take if network or system activity matches the signature.
        - **Header**: Includes network traffic information like source/destination IP addresses, ports, protocol, and traffic direction.
        - **Rule Options**: Provide customization options for signatures.
    - **Custom Rules**: Modify or customize existing rules to meet specific security requirements.

- **Configuration File**
    - Used to configure Suricata settings.
    - Configuration file is `suricata.yaml`, utilizing YAML format.

- **Log Files**
    - **eve.json**: Standard Suricata log file containing detailed event and alert information in JSON format.
    - **fast.log**: Records minimal alert information including basic IP address and port details.
    - **Suricata Log Types**:
	    - Alert logs
	    - Network Telemetry Logs.
	- **Suricata Log Format Types**:
		- **EVE JSON:** Extensible Event Format JavaScript Object Notation
## Key Takeaways

- Understanding how to configure detection technologies and write effective rules provides insight into network activity, enhancing detection capability.
- Customizing rules is essential to tailor detection and monitoring, minimizing false positive alerts.
- Configuration and log files are crucial components for proper functioning and analysis of Suricata.

## Resources for more information

- [Suricata user guide](https://suricata.readthedocs.io/en/latest/index.html#) 
- [Suricata features](https://suricata.io/features/) 
- [Rule management](https://suricata.readthedocs.io/en/latest/rule-management/suricata-update.html)
- [Rule performance analysis](https://suricata.readthedocs.io/en/latest/configuration/suricata-yaml.html#engine-analysis-and-profiling)
- [Suricata threat hunting webinar](https://youtu.be/kaDGolhTu94)
- [Introduction to writing Suricata rules](https://youtu.be/tvoqFBVSShA)
- [Eve.json jq examples](https://suricata.readthedocs.io/en/latest/output/eve/eve-json-examplesjq.html)

---
## Log Sources and Log Ingestion

### SIEM Process Overview

- **Collect and Aggregate Data**:
    - SIEM tools collect event data from various data sources.
- **Normalize Data**:
    - Event data becomes normalized to convert it into a standard format for easier reading and searching.
- **Analyze Data**:
    - SIEM tools analyze and correlate the normalized data to identify unusual activity.

### Log Ingestion

- **Importance**:
    - Log ingestion is crucial for SIEM tools to effectively monitor critical activities.
- **Process**:
    - SIEM tools create copies of event data from log sources and retain them within their storage for analysis.
    - Event data includes authentication attempts, network activity, etc.

#### Log Forwarders

- **Definition**:
    - Log forwarders are software used to automate the process of collecting and sending log data to SIEM tools.
- **Usage**:
    - Organizations commonly use log forwarders to collect log data efficiently.
    - They automate the process of collecting and sending log data to SIEM tools.

**Note**: SIEM tools may utilize proprietary or open-source log forwarders depending on specific requirements and compatibility.

### Key Takeaways

- Understanding log ingestion helps security analysts identify and prioritize security incidents effectively.
- Proper log ingestion enables security analysts to access and analyze logs during incident investigations.

### Resources

- [Guide on getting data into Splunk](https://docs.splunk.com/Documentation/SplunkCloud/9.0.2303/Data/Howdoyouwanttoadddata)
- [Guide on data ingestion into Chronicle](https://cloud.google.com/chronicle/docs/data-ingestion-flow)

---
## Search Methods with SIEM Tools

### Splunk Searches

- **Search Processing Language (SPL)**:
  - SPL is used in Splunk to search and retrieve events from indexes.
  - SPL searches can contain various commands and arguments to manipulate search results.
- **Basic Search**:
  - Syntax: `index=main fail`
  - Explanation:
    - `index=main`: Retrieve events from the "main" index.
    - `fail`: Filter events containing the term "fail".

#### Pipes

- **Definition**:
  - Pipes (`|`) chain commands together, passing output from one command as input to the next.
- **Example**:
  - Syntax: `index=main fail| chart count by host`
  - Explanation:
    - `chart count by host`: Transform search results into a chart based on event count by host.

#### Wildcard

- **Definition**:
  - Wildcards (e.g., `*`) substitute for any character in a search term.
- **Example**:
  - Syntax: `index=main fail*`
  - Explanation:
    - `fail*`: Match any events with terms starting with "fail".

### Chronicle Searches

#### Unified Data Model (UDM) Search

- **Overview**:
  - Default search type in Chronicle, faster than Raw Log Search.
  - Uses normalized data with structured UDM fields.
- **Example**:
  - Syntax: `metadata.event_type = “USER_LOGIN”`
  - Explanation:
    - `metadata.event_type`: Field indicating the type of event.
    - `"USER_LOGIN"`: Filter events related to user logins.

#### Raw Log Search

- **Overview**:
  - Searches through raw, unparsed logs.
  - Slower than UDM Search but useful for specific searches.
- **Example**:
  - Syntax: `username="admin" action="failed"`
  - Explanation:
    - `username="admin" action="failed"`: Search for events with the username "admin" and action "failed".

#### Types of Searches

- **UDM Search**:
  - Default and faster search type in Chronicle.
  - Utilizes normalized data with structured UDM fields.
- **Raw Log Search**:
  - Searches through raw, unparsed logs in Chronicle.
  - Slower than UDM Search but useful for specific queries.

#### YARA L in Chronicle

- **YARA L**:
  - Chronicle supports YARA L, a subset of the YARA rule language, for advanced searching.
  - Allows for complex pattern matching and detection in logs.

### Key Takeaways

- Understanding search methods in SIEM tools enables efficient event data retrieval.
- Leveraging specific commands and fields allows for precise searches and analysis.

### Resources

- [Splunk’s Search Manual](https://docs.splunk.com/Documentation/Splunk/9.0.1/Search/GetstartedwithSearch)
- [Chronicle's Quickstart Guide](https://cloud.google.com/chronicle/docs/review-security-alert)

---
## Follow-along Guide for Splunk Sign-up

### Instructions

#### Part 1 - Create a Splunk Cloud Account

- Go to the [Splunk Cloud Platform Trial](https://www.splunk.com/en_us/download/splunk-cloud.html) page.
- Fill in the fields in the **Start Your Cloud Platform Trial** sign-up form.
- Click **Create Your Account**.

#### Part 2 - Verify Your Email

- Check the inbox for the email address that you used to sign up for the Splunk account. Find the verification email from Splunk with the subject line **Confirm your email address**.
- Open the email and click the **Verify Your Email** button.

#### Part 3 - Activate a Splunk Cloud Trial

- Click the **Start Trial** button.
- Check your inbox for an email from Team Splunk with the subject line **Welcome to Splunk Cloud Platform!**
- Open the email to access your Splunk Cloud login information.
- Enter the username and password credentials that were included in the email.
- You will be prompted to change the password of the Splunk Cloud Platform account. Enter a new password and click **Save Password**.
- Check the box next to **I accept these terms** and click **Ok**.

#### Part 4 - Download and Upload Splunk Data

- Go to the Splunk Home dashboard.
- On the Splunk bar, click **Settings** and then click **Add Data**.
- Click **Upload**.
- Click **Select File** to upload the **tutorialdata.zip** file. Alternatively, you can also drag and drop your file in the **Drop your data file here** box.
- Once the file is uploaded, click **Next** to continue to **Input Settings**.
- By the **Host** section, select **Segment in path** and enter **1** as the segment number.
- Click **Review** and check the details of the upload before you submit.
- After you've verified that the details are correct, click **Submit**.
- Once Splunk has ingested the data, you will receive a confirmation message stating that the file has been uploaded successfully.
- Click the **Splunk Cloud** logo to return to the home page.

---
## **Cybersecurity Terms and Concepts**

| Term                                         | Definition                                                                                                         |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Anomaly-based analysis                      | A detection method that identifies abnormal behavior                                                               |
| Array                                        | A data type that stores data in a comma-separated ordered list                                                     |
| Common Event Format (CEF)                    | A log format that uses key-value pairs to structure data and identify fields and their corresponding values         |
| Configuration file                          | A file used to configure the settings of an application                                                            |
| Endpoint                                    | Any device connected on a network                                                                                  |
| Endpoint detection and response (EDR)        | An application that monitors an endpoint for malicious activity                                                   |
| False positive                              | An alert that incorrectly detects the presence of a threat                                                        |
| Host-based intrusion detection system (HIDS) | An application that monitors the activity of the host on which it’s installed                                      |
| Intrusion detection systems (IDS)           | An application that monitors system activity and alerts on possible intrusions                                     |
| Key-value pair                             | A set of data that represents two linked items: a key, and its corresponding value                                 |
| Log                                         | A record of events that occur within an organization’s systems                                                     |
| Log analysis                                | The process of examining logs to identify events of interest                                                       |
| Log management                              | The process of collecting, storing, analyzing, and disposing of log data                                           |
| Logging                                     | The recording of events occurring on computer systems and networks                                                 |
| Network-based intrusion detection system (NIDS) | An application that collects and monitors network traffic and network data                                      |
| Object                                     | A data type that stores data in a comma-separated list of key-value pairs                                           |
| Search Processing Language (SPL)            | Splunk’s query language                                                                                            |
| Security information and event management (SIEM) | An application that collects and analyzes log data to monitor critical activities in an organization          |
| Signature                                  | A pattern that is associated with malicious activity                                                               |
| Signature analysis                         | A detection method used to find events of interest                                                                 |
| Suricata                                   | An open-source intrusion detection system, intrusion prevention system, and network analysis tool                |
| Telemetry                                  | The collection and transmission of data for analysis                                                              |
| Wildcard                                   | A special character that can be substituted with any other character                                               |
| YARA-L                                     | A computer language used to create rules for searching through ingested log data                                    |
| Zero-day                                   | An exploit that was previously unknown                                                                             |

---