# Protocols' cheat sheet

| Abbr.     | Name                                                | Layer           | Dependecy   | Description  |
|:---:      |:---:                                                |:---:            |:---:        |:---:|
|**HTTP**   | **H**yper **T**ext **T**ransfer **P**rotocol        |Application Layer|`TCP`          |Pull Protocol, Web's application-layer protocol is a the heart of the Web. It is implemented in two programs: a client program and a server program.|
|**SMTP**   | **S**imple **M**ail **T**ransfer **P**rotocol       |Application Layer|`TCP`          |Push Protocol, Mail: major components: user agents, mail servers, and the Simple Mail Transfer Protocol (SMTP).|
|**FTP**    | **F**ile **T**ransfer **P**rotocol                  |Application Layer|`TCP`          |-|
|**Telnet** | **F**ile **T**ransfer **P**rotocol                  |Application Layer|`TCP`          |-|
|**SIP**    | **S**ession **I**nitiation **P**rotocol             |Application Layer|`UDP / TCP`    |-|
|**RTP**    | **R**eal-time **T**ransport **P**rotocol            |Application Layer|`UDP / TCP`    |-|
|**POP3**   | **P**ost **O**ffice **P**rotocol—Version 3          |Application Layer|`TCP`          |Pull Protocol, used in mails (Persistent only)|
|**IMAP**   | **I**nternet **M**ail **A**ccess **P**rotocol       |Application Layer|`TCP`          |Pull Protocol,  The IMAP protocol provides commands to allow users to create folders and move messages from one folder to another.({No/Persistent})|
|**DNS**    | **D**omain **N**ame **S**ystem                      |Application Layer|`UDP`          |translates domains into IP addresses.|
|**TCP**    | **T**ransmission **C**ontrol **P**rotocol           |Transport Layer  |-            |reliable, connection-oriented service four-tuple: (source IP address, source port number, destination IP address, destination port number) *20* bytes|
|**UDP**    | **U**ser **D**atagram **P**rotocol                  |Transport Layer  |-            |unreliable, connectionless service two-tuple: (destination IP address , destination port number) *8* bytes|
|**IP**     | **I**nternet **P**rotocol                           |Network Layer    |`TCP`          |large IP datagram divided (“fragmented”) within net, one datagram becomes several datagrams, “reassembled” only at final destination.|
|**ICMP**   | **I**nternet **C**ontrol **M**essage **P**rotocol   |Network Layer    |-            |Error reporting|
|**DHCP**   | **D**ynamic **H**ost **C**onfiguration **P**rotocol |Application Layer|`UDP`          |host broadcasts “DHCP discover” msg [optional], DHCP server responds with “DHCP offer” msg [optional], host requests IP address: “DHCP request” msg, DHCP server sends address: “DHCP ack” msg |
|**OSPF**   | **O**pen **S**hortest **P**ath **F**irst            |Link Layer       |`UDP / TCP`    |uses link-state algorithm, link state packet dissemination, topology map at each node, route computation using Dijkstra’s algorithm |
|**BGP**    | **B**order **G**ateway **P**rotocol                 |Application Layer|-            |-            | 
|**SNMP**   | **S**imple **N**etwork **M**anagement **P**rotocol  |Application Layer|-            |request/response mode, trap mode.|
|**MAC**    | **M**edium **A**ccess **C**ontrol                   |Link Layer       |-            |medium access control (MAC) sublayer is the layer that controls the hardware responsible for interaction with the wired, optical or wireless transmission medium.|
|**Slotted ALOHA**     |**Slotted ALOHA**                         |Link Layer       |-            |when node obtains fresh frame, transmits in next slot, if no collision: node can send new frame in next slot, if collision: node retransmits frame in each subsequent slot with prob. p until success|
|**Pure (unslotted) ALOHA**     |**Pure (unslotted) ALOHA**       |Link Layer       |-            |simpler, no synchronization, when frame first arrives -> transmit immediately, collision probability increases: frame sent at t0 collides with other frames sent in [t0-1,t0+1].|
|**CSMA**   | **C**arrier **S**ense **M**ultiple **A**ccess       |Link Layer       |-            |CSMA: listen before transmit:if channel sensed idle: transmit entire frame, if channel sensed busy, defer transmission|
|**Taking turns**   | **Taking turns**                            |Link Layer       |-            |channel partitioning MAC protocols: share channel efficiently and fairly at high load, inefficient at low load: delay in channel access, 1/N bandwidth allocated even if only 1 active node!|
|**ARP**   | **A**ddress **R**esolution **P**rotocol              |Link Layer       |-            |ARP table: each IP node (host, router) on LAN has table: IP/MAC address mappings for some LAN nodes: < IP address; MAC address; TTL>, TTL (Time To Live): |

# Abbreviation's cheat sheet

| Abbr.     |     Name                                                |Description|
| :---:     |     :---:                                               |:---:|
| **RFC**   | Request for comments                                    |-|
| **IETF**  | Internet Engineering Task Force                         |-|
| **DSL**   | Digital Subscriber Line                                 |use existing telephone line to central office DSLAM, < 2.5 Mbps upstream, < 24 Mbps|
| **SSL**   | Secure Sockets Layer                                    |provides critical process-to-process security services including encryption, data integrity and end-point authentication.|
| **API**   | Application programming interface                       |Interface (API) between the application and the network.|
| **ISP**   | Internet Service Provider                               |End systems connect to Internet via access ISPs (Internet Service Providers)|
| **TLD**   | Top - Level Domain                                      |responsible for com, org, net, edu, aero, jobs, museums, and all top-level country domains, e.g.: uk, fr, ca, jp|
| **DASH**  | Dynamic, Adaptive Streaming over HTTP                   |divides video file into multiple chunks,each chunk stored, encoded at different rates|
| **CDN**   | Content Distribution Networks                           |store/serve multiple copies of videos at multiple geographically distributed sites (CDN)|
| **GBN**   | Go Back-N                                               |sender can have up to N unacked packets in pipeline,receiver only sends cumulative ack|
| **FSM**   | Finite State Machine                                    |-|
| **CAs**   | Control Agents                                          |-|
| **SDN**   | Software Defined Network                                |implemented in (remote) servers|
| **HOL**   | Head of the Line blocking                               |Overloading in buffers in output buffers|
| **RTT**   | Round Trip Time                                         |is the length of time it takes for a signal to be sent plus the length of time it takes for an acknowledgement of that signal to be received. |
| **CIDR**  | Classless InterDomain Routing                           | is a method for allocating IP addresses and IP routing. |
| **ICANN** | Internet Corporation for Assigned Names and Numbers     |allocates addresses,manages DNS,assigns domain names, resolves disputes|
| **NAT**   | Network Address Translation                             |range of addresses not needed from ISP:  just one IP address for all devices can change addresses of devices in local network without notifying outside world|
| **FDM**   | Frequency Divison Multiplexing                          |different channels transmitted in different frequency bands|
| **TDM**   | Time Divison Multiplexing                               |different channels transmitted in different time slots|
| **MIB**   | Management Information Base                             |between server and agent.|
| **CRC**   | Cyclic redundancy check                                 |more powerful error-detection coding|
| **DOCSIS**   | data over cable service interface spec       |FDM over upstream, downstream frequency channels,TDM upstream: some slots assigned, some have contention|
