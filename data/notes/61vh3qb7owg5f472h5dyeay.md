## notes in plain text

Sep 23, 2022 networking_notes
An IP address is a 32 bit number that identifies a host on a network. But this  binary string is often converted to 4 decimal numbers separated by dots. A router only knows what the address of the next router is, not the exact destination of the packets. The first 24 bits specify where the host is, the last 8 specify the host itself. A subnet mask is a 32 bit string that splits the ip address host address from the network address.
IP addresses are divided into classes, class A addresses have the first octet from 1 to 127 and has a subnet mask of 255.0.0.0, class B addresses from 128 to 191 and a subnet mask of 255.255.0.0, and class C addresses from 192 to 223
A routing table is a table that holds the best routes for packets to go through.
Nov 1, 2022
Memory Vocabulary:
RAM - Random Access Memory
DRAM - Dynamic RAM: in the ram stick
SRAM - Static RAM: no need refresh, used for cache
SDRAM - Synchronous DRAM: has greater concurrency of read and writes, faster
The memory bus is the bus which connects the main memory to the memory controller in computer systems. 
DDR SDRAM - Double data rate SDRAM: SDRAM works on the clock signal, Double data rate means it can read and write on the falling and rising edge of the clock cycle. So it's twice as fast
DDR2 SDRAM - faster and needs less voltage
DDR3 SDRAM - doubles the bandwidth, my doubling clock rate, generates less heat, up to 800 MHz
DDR4 SDRAM - Quadruples the storage capacity, less power, has 288 pins, and doubles speed, first to support EEC
GDDR - Graphics DDR, used in GPU
Non Parity memory - doesn't have parity bit, redundant bit for error checking
Parity memory - has parity bit
ECC memory: Error Correction Code memory: fully tolerate to single bit errors
ROM - read only memory
Nonvolatile memory - memory that persists after power off
PROM - programmable rom
EPROM - erasable prom: erased through ultraviolet light
EEPROM - electrically eprom
DIP - Dual in-line package: old ICs
SIMM - single in-line memory module: new components that stick into connectors
DIMM - dual in-line memory module: 1990s upgrade
SODIMM - small outline dual in-line memory module
Cache memory - memory directly accessible to the the cpu
L1 cache - cache in cpu
L2 cache - cache out of the cpu
L3 cache - cache that improves performance
Nov 5, 2022
In computer architecture, a bus (shortened form of the Latin omnibus, and historically also called data highway or databus) is a communication system that transfers data between components inside a computer, or between computers.
In a computer system, a chipset is a set of electronic components in one or more integrated circuits known as a "Data Flow Management System" that manages the data flow between the processor, memory and peripherals.
PCIe xn - Peripheral component interconnect express (n data lanes) - a connector that connects to input and output devices
X is how many lanes the PCIe slot has
The Motherboard is the place chips connect to so they can communicate to other components of the computer. The CPU is the chip on a that connects to the motherboard that does the actual general data processing for the computer. The North bridge is a chip on a motherboard that connects the CPU to the rest of the computer (DRAM, PCIe, etc) through the FSB (front side bus), the south bridge is a different chip that connects many kinds of input and output to the north bridge. 
A protocol for computers to talk to each other
Port 80 is for HTTP.
RADIUS (Remote Authentication Dial-In User Service)
What uses radius
Authenticating supplicants trying to access a lan
It comes back with the permissions that the client has
 SATA
Basic Input Output System
Domain Name System, change domain names to ip address
Internet Service Provider
Universal serial bus, south bridge
Point-to-Point Protocol (PPP) is a data link layer (layer 2) communication protocol between two routers directly without any host or any other networking in between. It can provide connection authentication, transmission encryption,[1] and data compression.
Open Systems Interconnection model (OSI model)
 A network node can be defined as the connection point among network devices such as routers, printers, or switches that can receive and send data from one endpoint to the other.
Device connected to a network, that users use
https://www.rfc-editor.org/rfc/rfc2460#section-2:   node        - a device that implements IPv6. router      - a node that forwards IPv6 packets not explicitly addressed to itself.  [See Note below]   host        - any node that is not a router.  [See Note below].
OSI
Wireless fidelity
Media access control
The logical link control (LLC) data communication protocol layer is the upper sublayer of the data link layer (layer 2) of the seven-layer OSI model. The LLC sublayer acts as an interface between the media access control (MAC) sublayer and the network layer.
UDP - send data without having to wait for any more packets afterwards

Jan 20, 2023
1. DRAM - Dynamic Random Access Memory - the memory which stores the data that the processor is actively using 2. PCIe xn - Peripheral component interconnect express (n data lanes) - a connector that connects to input and output devices, usually known for connecting a graphics card, the x with the number represents how many units of data can be transferred at a time 3. Power connector - powers motherboard 4. VGA - Video Graphics Array - connection for the sending of data from monitors and other video devices to the computer 5. Parallel port - Connection for input and output devices that sends multiple bits at a time, predecessor to USB 6. USB - Universal Serial Bus - industry standard for connecting devices together, for input and output, for sending and receiving data from other computers, for even powering devices. 7. Serial port - connection where information travels one bit at a time 8. Fan connector - connection that allows communication between a computer fan and the computer it is cooling 9. SATA - Serial Advanced Technology Attachment - connects mass storage devices to the motherboard 10. PATA/IDE/ATA - Parallel Advanced Technology Attachment - connection used for storage devices, predecessor to SATA 11. North Bridge - connects the processor to the rest of the computer (DRAM, PCIe, etc) through the front-side bus 12. South Bridge - connects many kinds of input and output to the north bridge

Open Systems Interconnection model (OSI model)

1. Physical layer - Transmission and reception of raw bit streams over a physical medium -
The physical technology that is used to actually send the data like hardware and cables

2. Data link layer - Transmission of data frames between two nodes connected by a
physical layer - The data that wraps around the packets/units of data to tell when a
packet starts and ends and similar things

3. Network layer - Structuring and managing a multi-node network, including addressing,
routing and traffic control - The actual headers (beginnings) of packets which have the
information the directs where the data goes in a network and similar information

4. Transport layer - Reliable transmission of data segments between points on a network,
including segmentation, acknowledgement and multiplexing - The data that manages
network traffic and the organization of units of data

A. TCP - Transmission Control Protocol - A protocol in the transport layer of the OSI
model, which gives reliable, organized communication between computers in a
network, it is used by the world wide web, email, file transfer, among other
internet applications because of this

B. UDP - User Datagram Protocol - A protocol that allows for the sending of data
without having to communicate beforehand or make some kind of connection or
communication channel, this makes it very simple but not reliable or organized

5. Session layer - Managing communication sessions, i.e., continuous exchange of
information in the form of multiple back-and-forth transmissions between two nodes -
The data and mechanisms that maintains responses and requests between computers

6. Presentation layer - Translation of data between a networking service and an
application; including character encoding, data compression and encryption/decryption -
The conversion of data from a form that can be transported, which may be compressed,
encoded, or encrypted into data that can be actively used by programs

7. Application layer - High-level protocols such as for resource sharing or remote file
access, e.g. HTTP (hypertext transfer protocol) - The procedures that actually end up
managing the content that the human sees

IEEE 802.1x is the standard (defined by the Institute of Electrical and Electronics Engineers Standards Association) that specifies how you authenticate devices that wish to join a LAN (local area network). It determines how you use EAP (extensible authentication protocol), which is a flexible way of authenticating connections. In the standard there is an authenticator which prevents access to the network, and an authentication server, which uses RADIUS (Remote Authentication Dial-In User Service), a protocol which manages what is authorized on a network (or diameter which is RADIUS’s successor). The authentication server can respond with access rejection (it denies all access to the network), access challenge (the server asks for more credentials), and access accept (Where the device requesting access is allowed into the LAN with certain permissions).
IEEE 802.1x is implemented in all major operating systems, and is a central part of network security. Despite this there are vulnerabilities in this standard. It was shown in 2005 that a man in the middle attack (where someone goes between a communication and frauds both sides) was possible, because after authentication, someone unauthorized could physically insert themselves. There are some alternatives to IEEE 802.1x, such as PANA (Protocol for Carrying Authentication for Network Access), but they are not used as widely.

The six steps to troubleshooting:
Identify the problem.
Question user and identify user changes to the computer.
Perform backups before making changes.
Inquire regarding environmental or infrastructure changes.
Review system and application logs.
Establish a theory of probable cause (question the obvious and if necessary
conduct internal or external research based on symptoms).
Test the theory to determine cause:
Once theory is confirmed, determine next steps to resolve the problem.
If theory is not confirmed, re-establish new theory or escalate.
Establish a plan of action to resolve the problem and implement the solution.
Verify full system functionality, and if applicable, implement preventative
measures.
Document findings, actions, and outcomes.

The use of 802.1x on Linux depends on what distribution of Linux you are using. But, in general there are 2 main projects for 802.1x supplicants, Xsupplicant and wpa_supplicant, which are developed by Open1x and Jouni Malinen respectively. They both work on windows too and wpa_supplicant also supports BSD and OS X. On the Linux distribution Ubuntu, wpa_suplicant is already loaded.[1] 
On Linux 802.1x is mainly configured using networkManager, which is a program for configuring network interfaces. Mac OS has supported 802.1x out of the box since version 10.3. The settings for 802.1x on Mac OS are in settings then network. While iOS has had support since version 2.0.

The IP address is the 32 bit (binary digit) number that is related to networking, and it is
simply what identifies hosts on an internet network. A host on a network is any computer or
device that connects to a network, while a network is a group of computers that are connected
together to communicate data. An octet is a group of eight bits. Because an IP address is 32
bits long, it is also four octets long. Because humans struggle to read binary, the IP address is
converted to four decimal numbers separated by dots for humans to read.
The parts of the IP address which designate the host address and the network address
aren't fixed, so the information for which part of the IP address is what, is in the subnet mask.
This number may be something like 255.255.255.0. The number 255 is special in that it is the
eight bit unsigned integer limit, which means that it is represented in binary as 11111111. This
means that in binary 255.255.255.0 is 11111111111111111111111100000000. How the information
is read is that the ones represent parts of the IP address that are for the network address, and
The zeros are the parts that are the host address. So for the subnet mask 255.255.255.0, the
The first three octets are for the network address and the last one is for the host address. IP
addresses are split into classes. A class A subnet mask looks like 255.0.0.0, and the first octet
of a class A address is in a range from 1 to 127. A class B subnet mask looks like 255.255.0.0,
and the first octet is in a range from 128 to 191. A class C subnet mask looks like 
255.255.255.0 and the first octet is in a range from 192 to 223.


A system administrator is someone with access to a system of computers and operates and manages a network. . A subnet mask is a 32 bit number that separates the network and host addresses. The 1 bits on a subnet mask mean that the section of bits is in the network address. The 0 bits on a subnet mask means that the section of bits is in the host address. The subnet mask 255.255.255.0 in binary looks like 11111111111111111111111100000000. When you change a subnet mask from 255.255.255.255.0 to .192 it causes 4 new networks to be available, because 11111111111111111111111111000000 has 2 more bits as part of the network address, so 4x as many possible network addresses. A default gateway is what lets a device on one subnet access devices on other networks. If you have an incorrect subnet mask, then devices on the subnet can communicate with hosts outside the subnet, but not with each other. If you have an incorrect IP address, hosts on the same network won’t be able to communicate because they will think they are on different networks. If you have an incorrect default gateway, then a host will be able to communicate with hosts on its subnet, but not with hosts outside of it. The 2 references are "TCP/IP Illustrated, Volume 1: The Protocols," Richard Stevens, Addison Wesley, 1994, and "Internetworking with TCP/IP, Volume 1: Principles, Protocols, and Architecture," Douglas E. Comer, Prentice Hall, 1995.


Domain
Different users different access rights
Work groups should be at most 20, domains make sense to move to after
Storage database/active directory in server
Centralized server for
Google does it for school
Don't have to be on the same local network
Have hierarchy, root, top level, second level, sub domain

Workgroups are computers that are peers for small networks on a local network.
No central admin, each device has its own storage and is managed by the user, 
A user must have an account on the device to log in
Workgroups let sharing of files and resources, 

` 
IDE is an interface (basically ATA)



Mar 1, 2023
Nslookup
name server lookup
Command-line tool for network administration; it queries DNS servers for the IP addresses and other information corresponding to domain names. 
This command is similar to the dig and host unix commands, and is available on many operating systems, such as unix-like OSes and windows.
Example: 
nslookup -type=ns google.com ##find name servers for domain
nslookup google.com ns1.google.com ##use a name server for a dns request
nslookup 1.1.1.1 ##reverse dns lookup for cloudflare
Netstat
network statistics
A command-line utility for displaying TCP connections, routing tables, network interfaces, and protocol statistics. Used for finding network problems and usage statistics/performance.
It is available on many systems, unix/unix-like and windows.
Example:
netstat -ab ##displays all tcp connections and tcp/udp ports listened on, while also displaying the executable involved in making the connection
netstat -an ##displays all tcp connections and tcp/udp ports listened on, but no attempt is made to determine names (shown numerically), so it's a faster command to run
netstat -ao 5 ##displays the process ID for all connections, every 5 seconds
Net user
maintains network users
Adds or modifies user accounts, or displays user account information; takes as parameters, username, password, domain, and options.
This command has many options, such as disabling users, or listing accounts if not provided with parameters. It is available on windows.
Example:
net user friend /add /passwordreq:no /homedir:c:\ ##add a user with no pass requirements, whos home directory is c
net user carlo student /add ##add a user with pass student
net user carlo NewPass /logonpasswordchg:yes ## change a users password and force them to change while logging in

Mar 3, 2023
LISTEN - represents waiting for a connection request from any remote
    TCP and port.
	The device is waiting for a computer to request a connection from a port.
SYN-SENT - represents waiting for a matching connection request
    after having sent a connection request.
	The device has sent a SYN (synchronize) message to the server and is waiting for a SYN-ACK (acknowledge) message.
SYN-RECEIVED - represents waiting for a confirming connection
    request acknowledgment after having both received and sent a
    connection request.
	The device has received a SYN-ACK, and has sent an ACK.
ESTABLISHED - represents an open connection, data received can be
In computer architecture, a bus (shortened form of the Latin omnibus, and historically also called data highway or databus) is a communication system that transfers data between components inside a computer, or between computers.
In a computer system, a chipset is a set of electronic components in one or more integrated circuits known as a "Data Flow Management System" that manages the data flow between the processor, memory and peripherals.
PCIe xn - Peripheral component interconnect express (n data lanes) - a connector that connects to input and output devices
X is how many lanes the PCIe slot has
The Motherboard is the place chips connect to so they can communicate to other components of the computer. The CPU is the chip on a that connects to the motherboard that does the actual general data processing for the computer. The North bridge is a chip on a motherboard that connects the CPU to the rest of the computer (DRAM, PCIe, etc) through the FSB (front side bus), the south bridge is a different chip that connects many kinds of input and output to the north bridge. 
A protocol for computers to talk to each other
Port 80 is for HTTP.
RADIUS (Remote Authentication Dial-In User Service)
What uses radius
Authenticating supplicants trying to access a lan
It comes back with the permissions that the client has
 SATA
Basic Input Output System
Domain Name System, change domain names to ip address
Internet Service Provider
Universal serial bus, south bridge
Point-to-Point Protocol (PPP) is a data link layer (layer 2) communication protocol between two routers directly without any host or any other networking in between. It can provide connection authentication, transmission encryption,[1] and data compression.
Open Systems Interconnection model (OSI model)
 A network node can be defined as the connection point among network devices such as routers, printers, or switches that can receive and send data from one endpoint to the other.
Device connected to a network, that users use
https://www.rfc-editor.org/rfc/rfc2460#section-2:   node        - a device that implements IPv6. router      - a node that forwards IPv6 packets not explicitly addressed to itself.  [See Note below]   host        - any node that is not a router.  [See Note below].
OSI
Wireless fidelity
Media access control
The logical link control (LLC) data communication protocol layer is the upper sublayer of the data link layer (layer 2) of the seven-layer OSI model. The LLC sublayer acts as an interface between the media access control (MAC) sublayer and the network layer.
UDP - send data without having to wait for any more packets afterwards
    delivered to the user.  The normal state for the data transfer phase
    of the connection.
	The computers know they can communicate with each other.
FIN-WAIT-1 - represents waiting for a connection termination request
    from the remote TCP, or an acknowledgment of the connection
    termination request previously sent.
	Server receives 
FIN-WAIT-2 - represents waiting for a connection termination request
    from the remote TCP.
	
CLOSE-WAIT - represents waiting for a connection termination request
    from the local user.
	Waiting for all the packets to make it, waiting for the request to end the connection from the user.
CLOSING - represents waiting for a connection termination request
    acknowledgement from the remote TCP.
	
LAST-ACK - represents waiting for an acknowledgment of the
    connection termination request previously sent to the remote TCP
    (which includes an acknowledgment of its connection termination
    request).
	
Waiting for the final acknowledgment from the server.
TIME-WAIT - represents waiting for enough time to pass to be sure
    the remote TCP received the acknowledgment of its connection
    termination request.
	
CLOSED - represents no connection state at all.
	The computer is not connected, or going to, it has finished a connection.
Apr 12, 2023


Quad Cyber Challenge the white house
Landy was immigrants went from working with steven spiel beer g to boeing a restriction cyber security all of them did to go protect the nation
Work for the government got to west point declare war on the terrorism then into I


Apr 18, 2023
Chrome OS is web based and on linux
Operating system
Kernel
Multiprocessing-
Multi threading-
Multi tasking-ability to run multiple applications simultaneously
Enterprise
BASH
STaaS storage as a service
IaaS
Mission control:
[[Dashboard multiple desktop all windows ]]secure notes spotlight boot camp system preferences 
Find document they no have: spotlight
Flash drives to storage media cheap
Sata 3 used for hard drives
4 ports 4 devices
Blu ray disk that can hold up to 100 gb of data: triple layer
Redundant array of independent disks
Parity and striping
RAID 5 striping + parity, minimum 3 drives
RAID 10 - 
Fat32

Install a new storage device on the system
Add free space on a new storage device to a storage pool
Allocate space from storage to existing storage space
Failure of hard drive arm

Keeps the data private : private cloud storage

Hypervisor - thin layer of software the virtual machine and the hardware
Host machine
Virtual machine
Virtual hard disk




Syn 
Ack
Syn-ack