---
name: networks-mtcna-learning-generator
description: Generate computer networks challenges: quizzes and labs specifically focused in MikroTik Certified Network (MTCNA).
---



# Summary
This skill is designed to create numerous questions based on quiz and practice about computer networking focusing on MikroTik Certified Network Associate (MTCNA). This focus is chosen with consideration to build comprehensive and structured learning flow.

# When to Use
- User mentions exactly: "mtcna learning creation"
- User implies: "computer networks learning flow" OR "computer network learning creation"

# Instruction
When generating content, follow these strict behavioral rules:
1. **Scope strictly to MTCNA:** Keep questions at the associate level. Focus on RouterOS CLI/Winbox navigation, basic bridging, static routing, basic dynamic routing protocols, wireless fundamentals, simple queues, basic firewall filters/NAT, and basic tunneling.
2. **Use RouterOS v7 syntax:** Unless v6 is specifically requested, use current RouterOS v7 terminology (e.g., Interface Templates for OSPF, no separate "Networks" tab).
3. **Separate the Answer Key:** Always provide the answer key and explanations at the very bottom of the response, separated by a markdown divider (`---`). Do not put the answers immediately under the questions.

## Formatting Rule
### 1. Quizzes
Provide the questions and choices first. At the bottom of the output, provide the answers using these exact formats:
- **Multiple-Choice Single-Answer:** `Correct answer: [Letter]` <br> `Explanation: [Reasoning]`
- **Multiple Answer:** `Correct answer(s): [Letters, comma-separated]` <br> `Explanation: [Reasoning]`
- **True/False:** `Correct answer: [True/False]` <br> `Explanation: [Reasoning]`
- **Essay:** `Expected Answer Criteria: [Key points that must be mentioned]`

### 2. Practice: Troubleshooting / Use-case
- **Provide in text:** Describe the network layout and the exact symptom the "client" is experiencing.
- **At the bottom provide:**
  - **Procedural fix:** Step-by-step CLI or Winbox fix.
  - **Error evidence:** What command shows the failure (e.g., `/ping`, `/routing ospf neighbor print`).
  - **Expected result:** How to verify it works.

 ### 3. Practice: Experiment
 The life-cycle is: ideation (objective or hypotheses), validation, and refinements

### 4. Practice: Proof-of-concept / Experiment
  - **Mandatory components:** Problem statement, Challenge definition, Challenge goals, and Required resources (e.g., number of CHR nodes, subnets).
  - **Supporting components:** Methodology, framework, or mindset required to solve it.

## Output format for experiment
## Output format for proof-of-concept
- Provide mandatory components: problem statement, challenge definition, challenge goals, and required resources
- Provide supporting components: methodology, framework, or mindset

# Constraint
A section for strict negative boundaries. For example, "Never invent proprietary protocol commands" or "Always provide the answer key separately at the bottom."
## Dos
## Don'ts
- Do not elaborate about routing protocols too deeper

# Learning Mechanisms
- Quizzes
  - Multiple-choice single-answer
  - Multiple-choice multiple-answers
  - True-or-false
  - Essay
- Practice
  - Troubleshooting
  - Experiment
  - Proof-of-concept

# Learning and Exam Preparation References
## 1. Official MTCNA Outline
Follow the official MTCNA outline on this [URL](https://i.mt.lv/cdn/training_pdf/mtcna_outline_2019181161836.pdf).

**Module 1: Introduction**
- About MikroTik
  - What is RouterOS
  - What is RouterBOARD
  - History and founder of MikroTik
- First time accessing the router
  - WinBox and MAC-WinBox
  - WebFig and Quick Set
  - Default configuration
- RouterOS command line interface (CLI)
  - Null Modem cable
  - SSH and Telnet
  - New terminal in WinBox/WebFig
- RouterOS CLI principles
  - <tab>, double <tab>, "?", navigation
  - Command history and its benefits
- Initial configuration (internet access)
  - WAN DHCP-client
  - LAN IP address and default gateway
  - Basic Firewall - NAT masquerade
- Upgrading RouterOS
  - Package types
  - Ways of upgrading
  - RouterBOOT firmware upgrade
- Router identity
- Manage RouterOS logins
- Manage RouterOS services
- Managing configuration backups
  - Saving and restoring the backup
  - Difference between a backup and an export (.rsc) file
  - Editing an export file
- Resetting a RouterOS device
- Reinstalling a RouterOS device (Netinstall)
- RouterOS license levels
- Sources of additional information
  - https://help.mikrotik.com/docs/
  - https://forum.mikrotik.com/
  - https://mum.mikrotik.com/
<br>

**Module 2: DHCP**
- DHCP server and client
  - DHCP client
  - DHCP server setup
  - leases management
  - DHCP server network configuration
- DHCP relay
- Address Resolution Protocol (ARP)
  - ARP modes
  - RouterOS ARP table
- Module 2 laboratories and experiments
<br>

**Module 3: Bridging**
- Bridging overview
  - Bridge concepts and settings
  - Creating bridges
  - Adding ports to bridges
- Bridge wireless networks
  - Station bridge
- Module 3 laboratories and experiments
<br>

**Module 4: Routing**
- Routing overview
  - Routing concepts
  - Route flags
- Static routing
  - Creating routes
  - Setting default route
  - Managing dynamic routes
  - Implementing static routing in a simple network
- Module 4 laboratories and experiments
<br>

**Module 5: Wireless**
- 802.11a/b/g/n/ac/ax concepts
  - Frequencies (bands, channels) data-rates / chains (tx power, rx sensitivity, country regulations)
- Setup a simple wireless link
  - Access Point configuration
  - Station configuration
- Wireless security and encryption
  - Access list
  - Connect list
  - Default authenticate
  - Default forward
  - WPA-PSK, WPA2-PSK
  - WPS accept, WPS client
- Monitoring tools
  - Snooper
  - Registration table
- Module 5 laboratories and experiments
<br>

**Module 6: Firewall**
- Firewall principles
  - Connection tracking and states
  - Structure, chains and actions
- Firewall Filter in action
  - Filter actions
  - Protecting your router (input)
  - Protecting your customers (forward)
- Basic address-list
- Source NAT
  - Masquerade and src-nat action
- Destination NAT
  - dst-nat and redirect actions
- FastTrack
- Module 6 laboratories and experiments
<br>

**Module 7: QoS**
- Simple Queue
  - Target
  - Destinations
  - Max-limit and limit-at
  - Bursting
- One simple queue for the whole network
  - pcq-rate configuration
  - pcq-limit configuration
- Module 7 laboratories and experiments
<br>

**Module 8: Tunnels**
- PPP settings
  - PPP profile
  - PPP secret
  - PPP status
- IP pool
  - Creating pool
  - Managing ranges
  - Assigning to a service
- Secure local network
  - PPPoE service-name
  - PPPoE client
  - PPPoE server
- Point-to-point addresses
- Secure remote networks communication
  - PPTP client and PPTP server (quick set)
  - SSTP client
- Module 8 laboratories and experiments
<br>

**Module 9: Misc**
- RouterOS tools
  - E-mail
  - Netwatch
  - Ping
  - Traceroute
  - Profiler (CPU load)
- Monitoring
  - Interface traffic monitor
  - Torch
  - Graphs
  - SNMP
  - The Dude
- Contacting support@mikrotik.com
  - supout.rif, autosupout.rf, and viewer
  - System logs, enabling debug logs
  - Readable configuration (item comments and names)
  - Network diagrams
- Module 9 laboratories and experiments
<br>

**2. Other References on the Internet**
- YouTube videos and/or playlists
- Files with open-access and available on the internet
- Free and open-access learning platforms
