# Learning and Exam Preparation Reference
## Official MTCNA Outline Modules
Follow the official MTCNA outline on this [URL](https://i.mt.lv/cdn/training_pdf/mtcna_outline_2019181161836.pdf).

**1. Introduction**
- About MikroTik
  - RouterOS and RouterBOARD definition
  - History and founders of MikroTik
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

**2. DHCP**
- DHCP server and client
  - DHCP client
  - DHCP server setup
  - leases management
  - DHCP server network configuration
- DHCP relay
- Address Resolution Protocol (ARP)
  - ARP modes
  - RouterOS ARP table
<br>

**3. Bridging**
- Bridging overview
  - Bridge concepts and settings
  - Creating bridges
  - Adding ports to bridges
- Bridge wireless networks
  - Station bridge
<br>

**4. Routing**
- Routing overview
  - Routing concepts
  - Route flags
- Static routing
  - Creating routes
  - Setting default route
  - Managing dynamic routes
  - Implementing static routing in a simple network
<br>

**5. Wireless**
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
<br>

**6. Firewall**
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
<br>

**7. QoS**
- Simple Queue
  - Target
  - Destinations
  - Max-limit and limit-at
  - Bursting
- One simple queue for the whole network
  - pcq-rate configuration
  - pcq-limit configuration
<br>

**8. Tunnels**
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
<br>

**9. Misc**
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
<br>
