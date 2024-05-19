# 2.0 - Networking
---

## 2.1 - Compare and contrast Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) ports, protocols, and their purposes.

---

### Ports and protocols

[**TCP (Transmission Control Protocol)**](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)

- Connection-oriented protocol.
- Ensures reliable and ordered delivery of data.
- Uses three-way handshake (SYN, SYN-ACK, ACK) for connection establishment.
- Examples: HTTP, HTTPS, FTP, SMTP.

[**UDP (User Datagram Protocol)**](https://en.wikipedia.org/wiki/User_Datagram_Protocol)

- Connectionless protocol.
- Unreliable, unordered delivery of data.
- No handshake; data is sent without establishing a connection.
- Examples: DNS, DHCP, SNMP.


**20/21 – [File Transfer Protocol (FTP)**](https://en.wikipedia.org/wiki/File_Transfer_Protocol)

- Port 20: Data transfer.
- Port 21: Control (commands).
- Purpose: Transfer files between client and server.
- Uses TCP for reliable communication.

**22 – [Secure Shell (SSH)**](https://en.wikipedia.org/wiki/Secure_Shell)

- Purpose: Secure remote login and command execution.
- Uses TCP for encrypted communication.
- Replaces Telnet for secure connections.

**23 – [Telnet**](https://en.wikipedia.org/wiki/Telnet)

- Purpose: Unencrypted remote login and command execution.
- Uses TCP; insecure, replaced by SSH.

**25 – [Simple Mail Transfer Protocol (SMTP)**](https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol)

- Purpose: Sending email between servers.
- Uses TCP for reliable email transmission.

**53 – [Domain Name System (DNS)**](https://en.wikipedia.org/wiki/Domain_Name_System)

- Purpose: Translating domain names to IP addresses.
- Uses both TCP (for zone transfers) and UDP (for queries).

**67/68 – [Dynamic Host Configuration Protocol (DHCP)**](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)

- Port 67: Server.
- Port 68: Client.
- Purpose: Assigning IP addresses and network configuration to devices.
- Uses UDP for fast, connectionless communication.

**80 – [Hypertext Transfer Protocol (HTTP)**](https://en.wikipedia.org/wiki/HTTP)

- Purpose: Web page requests and data transfer.
- Uses TCP for reliable delivery.

**110 – [Post Office Protocol 3 (POP3)**](https://en.wikipedia.org/wiki/Post_Office_Protocol)

- Purpose: Receiving email; downloading messages from server to client.
- Uses TCP for reliable communication.

**137/139 – [Network Basic Input/Output System (NetBIOS)](https://en.wikipedia.org/wiki/NetBIOS)/[NetBIOS over TCP/IP (NetBT)**](https://en.wikipedia.org/wiki/NetBIOS_over_TCP/IP)

- Port 137: NetBIOS Name Service.
- Port 138: NetBIOS Datagram Service.
- Port 139: NetBIOS Session Service.
- Purpose: Network communication and file sharing in legacy Windows networks.
- Uses TCP and UDP for different services.

**143 – [Internet Message Access Protocol (IMAP)**](https://en.wikipedia.org/wiki/Internet_Message_Access_Protocol)

- Purpose: Email retrieval; allows accessing emails from multiple devices.
- Uses TCP for reliable communication.

**161/162 – [Simple Network Management Protocol (SNMP)**](https://en.wikipedia.org/wiki/Simple_Network_Management_Protocol)

- Port 161: SNMP agent (receives requests).
- Port 162: SNMP manager (receives traps/notifications).
- Purpose: Network management and monitoring.
- Uses UDP for fast, connectionless communication.

**389 – [Lightweight Directory Access Protocol (LDAP)**](https://en.wikipedia.org/wiki/Lightweight_Directory_Access_Protocol)

- Purpose: Directory services (e.g., user information, credentials).
- Uses TCP for reliable directory access.

**443 – [Hypertext Transfer Protocol Secure (HTTPS)**](https://en.wikipedia.org/wiki/HTTPS)

- Purpose: Secure web page requests and data transfer.
- Uses TCP with SSL/TLS for encrypted communication.

**445 – [Server Message Block (SMB)/Common Internet File System (CIFS)**](https://en.wikipedia.org/wiki/Server_Message_Block)

- Purpose: File sharing, printer sharing, network browsing in Windows networks.
- Uses TCP for reliable communication.

**3389 – [Remote Desktop Protocol (RDP)**](https://en.wikipedia.org/wiki/Remote_Desktop_Protocol)

- Purpose: Remote desktop access.
- Uses TCP for secure and reliable remote control.

### TCP vs. UDP

#### Connectionless Protocol (UDP)

**1. DHCP (Dynamic Host Configuration Protocol)**

- **Port**: 67 (server), 68 (client).
- **Purpose**: Automatically assigns IP addresses and other network configuration to devices on a network.
- **Characteristics**:
    - Uses UDP for fast, connectionless communication.
    - No handshake process; data packets are sent without establishing a connection.
    - Suitable for scenarios where speed is more critical than reliability.

**2. TFTP (Trivial File Transfer Protocol)**

- **Port**: 69.
- **Purpose**: Simple, lightweight file transfer protocol.
- **Characteristics**:
    - Uses UDP for connectionless communication.
    - Minimalistic, lacking many features of FTP (no authentication, no directory browsing).
    - Used for simple file transfers, such as transferring firmware to network devices.

#### Connection-oriented Protocol (TCP)

**1. HTTPS (Hypertext Transfer Protocol Secure)**

- **Port**: 443.
- **Purpose**: Secure web page requests and data transfer.
- **Characteristics**:
    - Uses TCP for reliable communication.
    - Encrypted using SSL/TLS, ensuring data integrity and privacy.
    - Requires a three-way handshake to establish a connection.

**2. SSH (Secure Shell)**

- **Port**: 22.
- **Purpose**: Secure remote login and command execution.
- **Characteristics**:
    - Uses TCP for reliable and secure communication.
    - Encrypts the session to protect data in transit.
    - Replaces insecure protocols like Telnet.
    - Requires a three-way handshake to establish a connection.

---
## 2.2 - Compare and contrast common networking hardware
---

[**Routers**](https://en.wikipedia.org/wiki/Router_(computing))

- Purpose: Directs data packets between different networks; connects multiple networks together.
- Key Features:
    - Determines best path for data to travel.
    - Assigns IP addresses using DHCP.
    - Provides NAT (Network Address Translation) to allow multiple devices to share a single public IP address.

[**Switches**](https://en.wikipedia.org/wiki/Network_switch)

- Purpose: Connects devices within a single network, allowing them to communicate.
- Types:
    - **Managed Switch**:
        - Offers advanced features like VLANs, QoS, and network monitoring.
        - Configurable through interfaces (CLI, web).
    - **Unmanaged Switch**:
        - Plug-and-play; no configuration needed.
        - Basic connectivity without advanced features.

[**Access Points (APs)**](https://en.wikipedia.org/wiki/Wireless_access_point)

- Purpose: Extends wireless coverage, allowing wireless devices to connect to a wired network.
- Key Features:
    - Can be standalone or part of a larger network (e.g., enterprise Wi-Fi solutions).
    - Supports multiple Wi-Fi standards (e.g., 802.11ac, 802.11ax).

[**Patch Panel**](https://en.wikipedia.org/wiki/Patch_panel)

- Purpose: Central point for managing and organizing network cables.
- Key Features:
    - Provides a static endpoint for network cables.
    - Facilitates easy changes and troubleshooting.

[**Firewall**](https://en.wikipedia.org/wiki/Firewall_(computing))

- Purpose: Monitors and controls incoming and outgoing network traffic based on security rules.
- Types:
    - Hardware Firewall: Dedicated device.
    - Software Firewall: Runs on a host system.

[**Power over Ethernet (PoE)**](https://en.wikipedia.org/wiki/Power_over_Ethernet)

- Purpose: Supplies power and data over the same Ethernet cable.
- Components:
    - **Injectors**:
        - Adds power to an Ethernet cable for PoE devices.
        - Used when network switches don’t support PoE.
    - **Switch**:
        - PoE Switch: Provides power directly from the switch to connected devices.
    - **PoE Standards**:
        - 802.3af: Up to 15.4W.
        - 802.3at (PoE+): Up to 30W.
        - 802.3bt (PoE++): Up to 60W or 100W.

[**Hub**](https://en.wikipedia.org/wiki/Ethernet_hub)

- Purpose: Connects multiple Ethernet devices, making them act as a single network segment.
- Key Features:
    - Broadcasts data to all ports.
    - Collision domain: All devices share the same bandwidth.

[**Cable Modem**](https://en.wikipedia.org/wiki/Cable_modem)

- Purpose: Connects a local network to the Internet via a cable service provider.
- Key Features:
    - Converts analog signals to digital for data transmission over coaxial cables.

[**Digital Subscriber Line (DSL)**](https://en.wikipedia.org/wiki/Digital_subscriber_line)

- Purpose: Provides Internet access over telephone lines.
- Key Features:
    - Uses existing phone lines.
    - DSL modem required.

[**Optical Network Terminal (ONT)**](https://en.wikipedia.org/wiki/Network_interface_device#Optical_network_terminals)

- Purpose: Converts fiber optic signals to electronic signals in fiber-to-the-home (FTTH) installations.
- Key Features:
    - Terminates fiber optic cable.
    - Provides Ethernet, phone, and TV connections.

[**Network Interface Card (NIC)**](https://en.wikipedia.org/wiki/Network_interface_controller)

- Purpose: Connects a computer to a network.
- Key Features:
    - Can be wired (Ethernet) or wireless (Wi-Fi).
    - Provides a physical interface for network access.

[**Software-defined Networking (SDN)**](https://en.wikipedia.org/wiki/Software-defined_networking)

- Purpose: Centralized management of network resources and configurations via software.
- Key Features:
    - Decouples control plane from data plane.
    - Provides flexibility, scalability, and automation in network management.
---

## 2.2 - Compare and Contrast Protocols for Wireless Networking
---


**Frequencies**

**2.4GHz**

- **Characteristics**:
    - Longer range, better penetration through walls and obstacles.
    - More prone to interference from other devices (e.g., microwaves, cordless phones).
    - Typically used by older and lower-bandwidth devices.
- **Channels**: 11 (North America), with significant overlap between channels.

**5GHz**

- **Characteristics**:
    - Shorter range, less penetration through obstacles.
    - Less interference, higher bandwidth, and faster speeds.
    - More channels available, with less overlap.
- **Channels**: 24 (North America), less crowded, non-overlapping.

**Channels**

**Regulations**
	[Allocation of frequencies Chapter II ITU](https://search.itu.int/history/HistoryDigitalCollectionDocLibrary/1.44.48.en.101.pdf)
	[Wikipedia chart of allocations](https://en.wikipedia.org/wiki/ISM_radio_band#Frequency_allocations)

- **2.4GHz**: Governed by international regulations (e.g., ITU), specific regional rules (FCC in the US).
- **5GHz**: More strictly regulated, channels divided into UNII (Unlicensed National Information Infrastructure) bands.

**2.4GHz vs. 5GHz**

- **2.4GHz**: Better for longer range, higher penetration, but more interference.
- **5GHz**: Better for high-speed applications, less interference, but shorter range.

**Bluetooth**

- **Purpose**: Short-range wireless communication between devices.
- **Frequencies**: Operates in the 2.4GHz band.
- **Uses**: Headsets, keyboards, mice, data transfer.

[**802.11 Standards**](https://en.wikipedia.org/wiki/IEEE_802.11)

**802.11a**

- **Frequency**: 5GHz.
- **Speed**: Up to 54 Mbps.
- **Range**: Shorter range due to higher frequency.
- **Adoption**: Less common.

**802.11b**

- **Frequency**: 2.4GHz.
- **Speed**: Up to 11 Mbps.
- **Range**: Better range and penetration.
- **Adoption**: Widely adopted initially, now outdated.

**802.11g**

- **Frequency**: 2.4GHz.
- **Speed**: Up to 54 Mbps.
- **Range**: Similar to 802.11b, backward compatible with 802.11b.

**802.11n**

- **Frequency**: 2.4GHz and 5GHz (dual-band).
- **Speed**: Up to 600 Mbps with MIMO (Multiple Input Multiple Output).
- **Range**: Improved range and speed.

**802.11ac (WiFi 5)**

- **Frequency**: 5GHz.
- **Speed**: Up to 1.3 Gbps (theoretical).
- **Range**: Higher speeds, reduced range compared to 2.4GHz.
- **Features**: Beamforming, wider channels.

**802.11ax (WiFi 6)**

- **Frequency**: 2.4GHz and 5GHz.
- **Speed**: Up to 9.6 Gbps (theoretical).
- **Range**: Improved efficiency and capacity.
- **Features**: OFDMA (Orthogonal Frequency Division Multiple Access), MU-MIMO (Multi-User MIMO), better performance in crowded environments.

[**Long-range Fixed Wireless**](https://en.wikipedia.org/wiki/Long-range_Wi-Fi)

**Licensed**

- **Characteristics**: Requires a government-issued license for operation.
- **Advantages**: Less interference, more reliable.
- **Use Cases**: Critical infrastructure, large-scale deployments.

**Unlicensed**

- **Characteristics**: No licensing required, open for public use.
- **Advantages**: Easier to deploy, cost-effective.
- **Disadvantages**: More interference, less reliable.

**Power**

- **Considerations**: Transmit power affects range and coverage.
- **Regulations**: Governed by regulatory bodies to prevent interference and ensure safety.

[**Regulatory Requirements for Wireless Power**](https://en.wikipedia.org/wiki/Title_47_CFR_Part_15)

- [**IEC 62368-1**](https://ewh.ieee.org/r6/ocs/pses/62368-1.pdf)
- [**ISO/IEC 18092**](https://cdn.standards.iteh.ai/samples/56692/616addcc04df4b31a2dff6d5b754c4ca/ISO-IEC-18092-2013.pdf)
- [**IEEE 1901**](https://en.wikipedia.org/wiki/IEEE_1901)
- **Agencies**: FCC (US), CE (Europe).
- **Rules**: Specific limits on transmit power, frequency use, and safety standards to minimize interference and health risks.

**NFC (Near Field Communication)**

- [ISO NFC Standards and Specs Overview](https://e2e.ti.com/cfs-file/__key/communityserver-discussions-components-files/667/2072.ISO_5F00_NFC-Standards-and-Specifications-Overview_5F00_2014.pdf)
- https://ecma-international.org/nfc-standards/#tab-id-3
- [**ISO/IEC 18092**](https://cdn.standards.iteh.ai/samples/56692/616addcc04df4b31a2dff6d5b754c4ca/ISO-IEC-18092-2013.pdf)
- **Purpose**: Short-range communication for contactless transactions, data exchange.
- **Range**: Typically up to 10 cm.
- **Uses**: Mobile payments, access control, data sharing.

**Radio-frequency Identification (RFID)**

- **Purpose**: Wireless identification and tracking of objects using electromagnetic fields.
- **Components**: Tags (active or passive) and readers.
- **Frequencies**: Low-frequency (LF), high-frequency (HF), ultra-high-frequency (UHF).
- **Uses**: Inventory management, asset tracking, security access.
- [Standards:](https://www.asiarfid.com/common-rfid-standards-and-protocols.html)
	

| Standard    | Explanation                                                                                                                                                                        |                                                                                                       |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| ISO 10536   | ISO RFID standard for close-coupled cards, mostly physical characteristics of the card                                                                                             |                                                                                                       |
| ISO 14223   | Radiofrequency identification of animals – Advanced transponder                                                                                                                    | https://en.wikipedia.org/wiki/ISO_14223                                                               |
| ISO 11784   | ISO RFID standard that defines the way in which data is structured on an RFID tag                                                                                                  |                                                                                                       |
| ISO 11785   | ISO RFID standard that defines the air interface protocol.                                                                                                                         | https://en.wikipedia.org/wiki/ISO_11784_and_ISO_11785                                                 |
| ISO 14443   | ISO RFID standard that provides the definitions for air interface protocol for RFID tags used in proximity systems – aimed for use with payment systems                            | https://en.wikipedia.org/wiki/ISO/IEC_14443                                                           |
| ISO 15459   | Unique identifiers for transport units (used in supply chain management)                                                                                                           |                                                                                                       |
| ISO 15693   | ISO RFID standard for use with what are termed vicinity cards                                                                                                                      | https://en.wikipedia.org/wiki/ISO/IEC_15693                                                           |
| ISO 15961   | ISO RFID standard for Item Management (includes application interface (part 1), registration of RFID data constructs (part 2), and RFID data constructs (part 3).                  |                                                                                                       |
| ISO 15962   | ISO RFID standard for item management – data encoding rules and logical memory functions.                                                                                          |                                                                                                       |
| ISO 15963   | ISO RFID standard for item management – unique identifier of RF tag.                                                                                                               | https://en.wikipedia.org/wiki/ISO/IEC_15693                                                           |
| ISO 18000   | ISO RFID standard for the air interface for RFID frequencies around the globe                                                                                                      | https://en.wikipedia.org/wiki/List_of_ISO_standards_18000%E2%80%9319999#ISO_18000_%E2%80%93_ISO_18999 |
| ISO 18001   | RFID for item management – application requirements profiles.                                                                                                                      |                                                                                                       |
| ISO 18046   | RFID tag and interrogator performance test methods.                                                                                                                                |                                                                                                       |
| ISO 18047   | The ISO RFID standard that defines the testing including conformance testing of RFID tags and readers. This is split into several parts that mirror the parts for ISO 18000.       |                                                                                                       |
| ISO 18185   | This is the industry standard for electronic seals or “e-seals” for tracking cargo containers using the 433 MHz and 2.4 GHz frequencies.                                           |                                                                                                       |
| ISO 18092   | Information technology—Telecommunications and information exchange between systems—Near Field Communication—Interface and Protocol (NFCIP-1)                                       |                                                                                                       |
| ISO 21481   | Information technology—Telecommunications and information exchange between systems—Near Field Communication Interface and Protocol −2 (NFCIP-2)                                    |                                                                                                       |
| ISO 24710   | Information technology, automatic identification, and data capture techniques – RFID for item management – Elementary tag license plate functionality for ISO 18000 air interface. |                                                                                                       |
| ISO 24729   | RFID implementation guidelines – part : RFID enabled labels; part 2: recyclability of RF tags; part 3: RFID interrogator / antenna installation.                                   |                                                                                                       |
| ISO 24730   | RFID real-time locating system: Part 1: Application Programming Interface (API); Part 2: 2.4 GHz; Part 3: 433 MHz; Part 4: Global Locating Systems                                 |                                                                                                       |
| ISO 24752   | System management protocol for automatic identification and data capture using RFID                                                                                                |                                                                                                       |
| ISO 24753   | Air interface commands for battery assist and sensor functionality                                                                                                                 |                                                                                                       |
| ISO 24769   | Real Time Locating System (RTLS) device conformance test methods                                                                                                                   |                                                                                                       |
| ISO 24770   | Real Time Locating System (RTLS) device performance test methods                                                                                                                   | https://en.wikipedia.org/wiki/Real-time_locating_system                                               |
| ISO 28560-2 | Specifies encoding standards and data model to be used within libraries                                                                                                            |                                                                                                       |
| ASTM D7434  | Standard Test Method for Determining the Performance of Passive Radio Frequency Identification (RFID) Transponders on Palletized or Unitized Loads                                 | https://en.wikipedia.org/wiki/ASTM_International                                                      |
| ASTM D7435  | Standard Test Method for Determining the Performance of Passive Radio Frequency Identification (RFID) Transponders on Loaded Containers                                            |                                                                                                       |
| ASTM D7580  | Standard Test Method for Rotary Stretch Wrapper Method for Determining the Readability of Passive RFID Transponders on Homogenous Palletized or Unitized Loads                     |                                                                                                       |

---

## 2.4 - Summarize Services Provided by Networked Hosts
---


#### **Server Roles**

[**DNS (Domain Name System)**](https://en.wikipedia.org/wiki/Domain_Name_System)

- **Purpose**: Translates domain names into IP addresses.
- **Function**: Enables users to access websites using human-readable names instead of numerical IP addresses.

[**DHCP (Dynamic Host Configuration Protocol)**](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)

- **Purpose**: Automatically assigns IP addresses and network configurations to devices on a network.
- **Function**: Reduces the need for manual IP address configuration and ensures unique addresses are assigned.

[**Fileshare**](https://en.wikipedia.org/wiki/File_sharing)

- **Purpose**: Provides centralized storage and access to files.
- **Function**: Allows multiple users to share, access, and collaborate on files over a network.

[**Print Servers**](https://en.wikipedia.org/wiki/Print_server)

- **Purpose**: Manages print jobs and printers on a network.
- **Function**: Facilitates sharing of printers among multiple users, handling print requests, and managing print queues.

[**Mail Servers**](https://en.wikipedia.org/wiki/Message_transfer_agent)

- **Purpose**: Handles sending, receiving, and storing emails.
- **Function**: Manages email accounts, processes incoming and outgoing emails, and ensures delivery.

[**Syslog**](https://en.wikipedia.org/wiki/Syslog)

- **Purpose**: Collects and stores log data from network devices and systems.
- **Function**: Provides centralized logging for monitoring, troubleshooting, and security analysis.

[**Web Servers**](https://en.wikipedia.org/wiki/Web_server)

- **Purpose**: Hosts websites and web applications.
- **Function**: Serves web content to users via HTTP/HTTPS protocols.

[**Authentication, Authorization, and Accounting (AAA)**](https://en.wikipedia.org/wiki/AAA_(computer_security))

- **Purpose**: Manages user authentication, authorization, and accounting.
- **Function**: Controls access to resources, verifies user identities, enforces permissions, and tracks user activities.

#### **Internet Appliances**

[**Spam Gateways**](https://en.wikipedia.org/wiki/Anti-spam_techniques)

- **Purpose**: Filters and blocks spam emails.
- **Function**: Analyzes incoming emails and filters out unwanted or malicious messages before they reach the mail server.

[**Unified Threat Management (UTM)**](https://en.wikipedia.org/wiki/Unified_threat_management)

- **Purpose**: Provides comprehensive security by integrating multiple security functions.
- **Function**: Combines firewall, intrusion detection/prevention, antivirus, and other security features into a single appliance.

[**Load Balancers**](https://en.wikipedia.org/wiki/Load_balancing_(computing))

- **Purpose**: Distributes network or application traffic across multiple servers.
- **Function**: Ensures no single server is overwhelmed, improving performance and reliability.

[**Proxy Servers**](https://en.wikipedia.org/wiki/Proxy_server)

- **Purpose**: Acts as an intermediary between clients and servers.
- **Function**: Improves security, performance, and anonymity by caching content and filtering requests.

#### **Legacy/Embedded Systems**

[**Supervisory Control and Data Acquisition (SCADA)**](https://en.wikipedia.org/wiki/SCADA)

- **Purpose**: Manages and monitors industrial control systems.
- **Function**: Collects data from sensors and equipment, provides real-time monitoring, and controls industrial processes.

[**Internet of Things (IoT) Devices**](https://en.wikipedia.org/wiki/Internet_of_things#Applications)

- **Purpose**: Connects everyday objects to the internet for monitoring and control.
- **Function**: Includes smart home devices, wearable tech, industrial sensors, and other devices that collect and exchange data.
---

## 2.5 - Given a Scenario, Install and Configure Basic Wired/Wireless Small Office/Home Office (SOHO) Networks
---


#### **Internet Protocol (IP) Addressing**

[**IPv4**](https://en.wikipedia.org/wiki/IPv4)

[IPv4 Addressing Configuration Guide, Cisco](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/ipaddr_ipv4/configuration/xe-3s/ipv4-xe-3s-book/configuring_ipv4_addresses.html)
- **Private Addresses**:
    - Used within private networks; not routable on the internet.
    - Ranges:
        - 10.0.0.0 to 10.255.255.255
        - 172.16.0.0 to 172.31.255.255
        - 192.168.0.0 to 192.168.255.255
    - Example: 192.168.1.1
- **Public Addresses**:
    - Assigned by Internet Service Providers (ISPs); routable on the internet.
    - Unique across the entire internet.
    - Example: 203.0.113.1

[**IPv6**](https://en.wikipedia.org/wiki/IPv6)

[IPv6 Addressing and Basic Configuration Guide, Cisco](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/ipv6_basic/configuration/xe-3s/ip6b-xe-3s-book/ip6-add-basic-conn-xe.html)
- **Purpose**: Provides a larger address space than IPv4; supports 128-bit addresses.
- **Format**: Eight groups of four hexadecimal digits.
    - Example: 2001:0db8:85a3:0000:0000:8a2e:0370:7334
- **Features**: Built-in support for automatic address configuration, improved security, and better routing efficiency.

[**Automatic Private IP Addressing (APIPA)**](https://en.wikipedia.org/wiki/Link-local_address)

- [explanation, how-to](https://ipwithease.com/apipa-automatic-private-ip-addressing/)
- **Purpose**: Assigns an IP address automatically when DHCP server is not available.
- **Range**: 169.254.0.0 to 169.254.255.255
- **Use Case**: Enables local network communication even without a DHCP server.

[**Static IP Addressing**](https://en.wikipedia.org/wiki/IP_address#IP_address_assignment)

- [explanation, how-to](https://whatismyipaddress.com/how-to-get-static-ip-address)
- **Purpose**: Manually assigned IP addresses; do not change over time.
- **Use Case**: Suitable for devices requiring a consistent IP address (e.g., servers, printers).
- **Configuration**: Entered manually in the device’s network settings.

**Dynamic IP Addressing**

- **Purpose**: IP addresses are assigned automatically by a DHCP server.
- **Use Case**: Suitable for devices that do not need a permanent IP address (e.g., client computers, mobile devices).
- **Configuration**: Obtained automatically; minimal manual setup required.
- Usually the default for most devices

[**Gateway**](https://en.wikipedia.org/wiki/Gateway_(telecommunications))

- [Cisco configure gateway](https://www.cisco.com/c/en/us/td/docs/switches/lan/catalyst4000/8-2glx/configuration/guide/supcfg.html)
- **Purpose**: Acts as an access point for devices in a network to communicate with devices in another network, usually the internet.
- **Function**: Routes traffic from the local network to external networks.
- **Configuration**: Typically the IP address of the router within a SOHO network.
---

## 2.6 - Compare and Contrast Common Network Configuration Concepts
---


#### [**DNS (Domain Name System)**](https://en.wikipedia.org/wiki/Domain_Name_System)

**Address Records**

- [**A Record**:](https://en.wikipedia.org/wiki/List_of_DNS_record_types#A)
    - **Purpose**: Maps a domain name to an IPv4 address.
    - **Example**: `example.com -> 192.0.2.1`
- [**AAAA Record**:](https://en.wikipedia.org/wiki/List_of_DNS_record_types#AAAA)
    - **Purpose**: Maps a domain name to an IPv6 address.
    - **Example**: `example.com -> 2001:0db8:85a3:0000:0000:8a2e:0370:7334`

**Mail Exchanger (MX)**

- **Purpose**: Specifies the mail server responsible for receiving email on behalf of a domain.
- **Example**: `example.com -> mail.example.com`

**Text (TXT)**

- **Purpose**: Provides text information to outside sources; often used for email verification and security purposes.
- **Spam Management**:
    - **DomainKeys Identified Mail (DKIM)**:
        - **Purpose**: Allows email receivers to verify that an email was indeed sent and authorized by the owner of that domain.
        - **Function**: Uses cryptographic authentication.
    - **Sender Policy Framework (SPF)**:
        - **Purpose**: Prevents email spoofing by specifying which mail servers are permitted to send email on behalf of a domain.
        - **Function**: Defines authorized IP addresses for sending mail.
    - **Domain-based Message Authentication, Reporting, and Conformance (DMARC)**:
        - **Purpose**: Combines SPF and DKIM to protect against email spoofing.
        - **Function**: Provides a mechanism for email receivers to report back to domain owners about email that fails SPF or DKIM checks.

#### [**DHCP (Dynamic Host Configuration Protocol)**](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)

- [**Leases**:](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol#Operation)
    - **Purpose**: Temporarily assigns an IP address to a device for a specific period.
    - **Function**: Ensures dynamic allocation of IP addresses and reuse of IP addresses over time.
- **Reservations**:
    - **Purpose**: Permanently assigns a specific IP address to a specific device based on its MAC address.
    - **Use Case**: Ensures a device always receives the same IP address.
- **Scope**:
    - **Purpose**: Defines the range of IP addresses that a DHCP server can assign to devices.
    - **Configuration**: Includes settings such as default gateway, DNS servers, and lease duration.

[**Virtual LAN (VLAN)**](https://en.wikipedia.org/wiki/VLAN)

- **Purpose**: Segments a physical network into multiple logical networks.
- **Function**: Improves security and traffic management by isolating network segments.
- **Use Case**: Separating network traffic between different departments or groups within an organization.

[**Virtual Private Network (VPN)**](https://en.wikipedia.org/wiki/Virtual_private_network)

- **Purpose**: Creates a secure, encrypted connection over a less secure network, such as the internet.
- **Function**: Provides remote users with secure access to their organization’s network.
- [**Types**:](https://en.wikipedia.org/wiki/Virtual_private_network#Types)
    - **Site-to-Site VPN**: Connects entire networks to each other.
    - **Remote Access VPN**: Connects individual users to a network.
---

## 2.7 - Compare and Contrast Internet Connection Types, Network Types, and Their Features
---


#### **Internet Connection Types**

[**Satellite**](https://en.wikipedia.org/wiki/Satellite_Internet_access)

- **Description**: Internet service delivered via satellites.
- **Features**:
    - Wide coverage, especially in remote areas.
    - High latency due to the distance signals must travel.
    - Affected by weather conditions.

[**Fiber**](https://en.wikipedia.org/wiki/Fiber_to_the_x#Fiber_to_the_premises)

- **Description**: Internet service using fiber-optic cables.
- **Features**:
    - Extremely high speeds (up to 1 Gbps or more).
    - Low latency.
    - High reliability and bandwidth capacity.

[**Cable**](https://en.wikipedia.org/wiki/Cable_Internet_access)

- **Description**: Internet service via coaxial cables.
- **Features**:
    - High speeds (up to several hundred Mbps).
    - Shared bandwidth with neighbors, which can lead to slower speeds during peak times.
    - Widely available in urban and suburban areas.

[**DSL (Digital Subscriber Line)**](https://en.wikipedia.org/wiki/Digital_subscriber_line)

- **Description**: Internet service over telephone lines.
- **Features**:
    - Moderate speeds (up to 100 Mbps).
    - Dedicated line for each subscriber, so speed doesn’t vary with network congestion.
    - Limited distance from the service provider’s location affects speed.

[**Cellular**](https://en.wikipedia.org/wiki/Cellular_network)

- **Description**: Internet service through cellular networks (e.g., 4G, 5G).
- **Features**:
    - Mobile and can be accessed anywhere with cellular coverage.
    - Variable speeds based on network technology and signal strength.
    - Often subject to data caps and throttling.

[**Wireless Internet Service Provider (WISP)**](https://en.wikipedia.org/wiki/Wireless_Internet_service_provider)

- **Description**: Internet service provided wirelessly, typically in rural areas.
- **Features**:
    - Uses radio signals to connect subscribers to the internet.
    - Coverage can be limited by terrain and distance.
    - Speeds and reliability vary depending on the provider and technology used.

#### **Network Types**

[**Local Area Network (LAN)**](https://en.wikipedia.org/wiki/Local_area_network)

- **Description**: A network confined to a small geographic area, like a single building.
- **Features**:
    - High-speed connections.
    - Low latency.
    - Typically used for connecting computers, printers, and other devices within a single location.

[**Wide Area Network (WAN)**](https://en.wikipedia.org/wiki/Wide_area_network)

- **Description**: A network that spans large geographic areas, connecting multiple LANs.
- **Features**:
    - Can cover cities, countries, or even global distances.
    - Uses various transmission methods (e.g., leased lines, satellite).
    - Slower speeds and higher latency compared to LANs.

[**Personal Area Network (PAN)**](https://en.wikipedia.org/wiki/Personal_area_network)

- **Description**: A network for personal devices, typically within a range of a few meters.
- **Features**:
    - Connects devices like smartphones, tablets, and laptops.
    - Uses technologies like Bluetooth and USB.
    - Short-range and low-power.

[**Metropolitan Area Network (MAN)**](https://en.wikipedia.org/wiki/Metropolitan_area_network)

- **Description**: A network that covers a city or a large campus.
- **Features**:
    - Larger than a LAN but smaller than a WAN.
    - Often uses high-speed fiber connections.
    - Can connect multiple LANs within a city.

[**Storage Area Network (SAN)**](https://en.wikipedia.org/wiki/Storage_area_network)

- **Description**: A dedicated network for data storage.
- **Features**:
    - Provides block-level storage access.
    - High-speed connections for data transfer.
    - Used in data centers and enterprise environments.

[**Wireless Local Area Network (WLAN)**](https://en.wikipedia.org/wiki/Wireless_LAN)

- **Description**: A LAN that uses wireless technology (Wi-Fi).
- **Features**:
    - Allows devices to connect to the network without physical cables.
    - Flexibility and mobility for connected devices.
    - Speeds and range can be affected by physical obstructions and interference.
---

## 2.8 - Given a Scenario, Use Networking Tools
---


[**Crimper**](https://en.wikipedia.org/wiki/Crimp_(joining))

- **Purpose**: Used to attach connectors (e.g., RJ45) to cables (e.g., Ethernet).
- **Function**:
    - Crimps the connector onto the cable, ensuring a secure and stable connection.
    - Essential for creating custom-length network cables.
- **Usage**:
    - Insert the cable into the connector, place the connector into the crimper, and squeeze the handle.

[**Cable Stripper**](https://en.wikipedia.org/wiki/Pliers#Types)

- **Purpose**: Removes the outer insulation from cables without damaging the inner conductors.
- **Function**:
    - Prepares cables for crimping or other termination processes.
- **Usage**:
    - Adjust the stripper for the cable diameter, rotate it around the cable to cut the insulation, and pull off the cut section.

[**WiFi Analyzer**](https://en.wikipedia.org/wiki/Packet_analyzer)

- **Purpose**: Analyzes wireless networks, detecting signal strength, channel usage, and interference.
- **Function**:
    - Helps identify optimal placement for access points.
    - Detects unauthorized access points and network issues.
- **Usage**:
    - Run the analyzer software on a laptop or mobile device to scan for WiFi networks and analyze their properties.

[**Toner Probe**](https://www.flukenetworks.com/datacom-cabling/copper-testing/IntelliTone-Pro-Toner-and-Probe)

- **Purpose**: Locates cables in a bundle by sending a tone through one end and using a probe to detect the tone at the other end.
- **Function**:
    - Identifies and traces cables, useful for cable management and troubleshooting.
- **Usage**:
    - Connect the toner to one end of the cable, and use the probe to follow the tone along the cable run.

[**Punchdown Tool**](https://en.wikipedia.org/wiki/Punch_down_tool)

- **Purpose**: Used to terminate wires into punchdown blocks, patch panels, or keystone jacks.
- **Function**:
    - Ensures a secure connection by pushing wires into IDC (Insulation Displacement Connector) contacts.
- **Usage**:
    - Place the wire in the slot, position the tool over the wire, and push down to secure the wire and cut off the excess.

[**Cable Tester**](https://en.wikipedia.org/wiki/Cable_tester)

- **Purpose**: Tests the continuity, wiring, and signal strength of network cables.
- **Function**:
    - Verifies that cables are correctly wired and can transmit data without issues.
- **Usage**:
    - Connect the cable tester to both ends of the cable, run the test, and interpret the results to ensure proper connectivity.

[**Loopback Plug**](https://en.wikipedia.org/wiki/RS-232#Loopback_testing)

- [see also](https://ascentoptics.com/blog/loopback-plug-what-you-need-to-know/)
- **Purpose**: Tests network interfaces by looping the signal back to the device.
- **Function**:
    - Helps diagnose network interface and port issues by verifying if the device can send and receive signals.
- **Usage**:
    - Plug the loopback into the network port, run a diagnostic tool, and check for successful signal return.

[**Network Tap**](https://en.wikipedia.org/wiki/Network_tap)

- **Purpose**: Inserts into a network link to monitor traffic without disrupting the connection.
- **Function**:
    - Allows for passive monitoring and analysis of network traffic.
- **Usage**:
    - Connect the tap between the network devices, and connect the monitoring device to the tap to capture and analyze traffic.
