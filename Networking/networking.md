 # COMPUTER NETWORKING


**What is network ?**

  -> In a simple terms Computers connected together.

  **INTERNET**
  -> A collection of these computer networks.

  **PROTOCOL**
  -> Rules/procedures set by people to send or receive data.
     e.g TCP, I.P, UDP
     _Internet Society_ are responsible for creating these protocols.

 **World Wide Web**
     -> The world wide web commonly known as the web, is an information system where documents and other web resources are identified by URL's, which may be interlinked by hyperlinks and are accessible over the internet.

 ## Client Srever Architecture

![client srever architecture](https://madooei.github.io/cs421_sp20_homepage/assets/client-server-1.png)

 **Some Basic Protocols:**
- `TCP - Transmission Control Protocols`
It ensures that the data will reach its destination and not get corrupted on the way i.e 100% of the datawill be received.
- `UDP - User Datagram Protocols`</br>
 It is a lightweight data transport protocol.</br>

  It provides a mechanism to detect corrupt data in packets, but it does not attempt to solve other problems that arise with packets, such as lost or out of order packets.
- `HTTP - Hyper Text Transfer Protocol`</br>
 It is an application-layer protocol for transmitting hypermedia documents, such as HTML.</br>

  It is used by web browsers, this is the data which be being transferred between clients and servers.

  
An **IP address** is a unique address that identifies a device on the internet or a local network.

Every single device on the internet that can communicate with each other, they have an IP address.

**Format of IP Address** <br/>
X.X.X.X <br/>
| <br/>
It can have values between 0-25

Command used to check the ip address of you own computer
 `curl ifconfig.me -s`


![internet connection](https://smartnetworkgeek.com/wp-content/uploads/2021/03/Modem-Router-Diagram-1024x728.jpeg)

- Modem assigns these IP addresses through DHCP
- DHCP - Dynamic Host Configuration Protocol
- Modem/Router will decide who requested it. It is done by using **NAT - Network Access Translator**
-> IP Address decides which device to send the data whereas Port numbers are used to identify which application made that request
- Ports are basically 16 bit numbers
-  HTTP  port 80
- MongoDB port - 27017
- `0 - 1023` --> Reserved Ports <br/>
  `1024 - 49152` --> Registered for applications <br/>
   Remaining is for our use


- `LAN` Local Area Network <br/>
   It interconnects computer within a limited area such as a residence, school, university etc 
- `MAN` Metropolitan Area Network <br/>
   It interconnects users with computer resources in a geographic region of the size of a metropolitan areas such as cities.
- `WAN` Wide Area Network
   It extends over large geographic area such as countries.

**SONET:** Synchronous Optical Networking</br>
**Frame relay:** A wave for connecting local area network to the wide area like internet

## MODEM, ROUTER

**Modem** is a combined device for modulation and demodulation. It is used to convert digital to analog and vice-versa.

**Router** is a device that forwards data packets between computer network.

**ISP:** Internet Service Provider are companies that provide us access to the internet


### Topologies
- Bus topology
- Ring topology
- star topology
- Tree topology
- Mesh topology

# OSI MODEL OPEN SYSTEM INTERCONNECTION MODEL

|Layer|Working|
|-----|-------|
|Application|Implemented in software.used by client eg.whatsapp|
|Presentation|It converts data into machine readblebinary format, encoding,encryption abstract compression, translation..|
|Session|Helps in setting up and managing the connections and enables sending and receiving of data followed by termination of connected session. Authentication and authorization takes place.|
|Transport|Data received from sessions layer is divided into small data units called segment every segment has source and destination's port as well as sequence number. flow,error control takes place.|
|Network|The transmission of the received data segments from one computer to other that is located in different network ip adderssing done here is called logical addressing, routing, load balancing are done here|
|Data link|Physical addressing is done here Mac addresses are physical addresses now these addresses of sender's and receivers are assigned to packets called frames.|
|Physical|Hardwares like cable wires|

- <b>MAC Address</b>: A media access control address (MAC address) is a unique identifier assigned to a network interface controller (NIC) for use as a network address in communications within a network segment. 
- Command to see mac,dhcp,dns address is `ipconfig /all`
- A packet consists of sender's,receiver's ip address along with subnet mask e.g (192.68.2.1,192.65.2.2,subnet mask)   

## TCP/IP MODEL
It consists of five layers:
- Application layer
- Transport layer
- Network layer
- Datalink layer
- Physical layer

# Application layer

This is the layer where user interacts with. It consists of applications like web browsers chat applications etc.

- A server is basically a system that that controls the website you are hosting.
- The application has two parts client and server part they communicate through each other.
- Clients are the one who are using  these resources like making a request to google.
- A collection of servers is known as data centers.
- Data centers is a collection of huge number of computers. It may have a static ip address. `ping google.com`
- Ping measures the round trip time for messages send from the originating host to the destination computer and are echoed back.

## Peer to Peer Architecture
![image](https://www.itrelease.com/wp-content/uploads/2019/05/Peer-to-peer-network-diagram.png)

- There is no one dedicated server,thet are just connected with each other.
- the key advantage is you can scale it rapidly.
- Here, every single computer can act as both server and client.

## Protocols:

- HTTP: Hyper Text Transfer Protocol
- DHCP: Dynamic Host Control Protocol
- FTP: File Transfer Protocol
- SMTP: Simple mail Transfer Protocol (used to send mails)
- pop3 & IMAC:(used to receive mails)
- SSH: Secure Shell
- VNC: Virtual Network Computing
- Telnet: Terminal immulation that enables theuser to connect to remote host/device using telnet client. It runs on port:23
- UDP: User Datagram Protocol

### Program

- Process (send a message, record a video) is ike one of the featureof the program or a running instance. one program can have multiple process running at once.
- Thread(set up a page, open camera) lighter version of process one process can have multiple running threads.

<b>Sockets</b>
Interface between process and internet.

<b>Ports</b>

i.p address tells us which device we are working with while ports tell us which application we are working with.

There may be possibility of many processes of single application is running like openung up many tabs in chrome when the response is coming back how it will know which tab to give data. this can be resolved using <i>Ephemeral ports.</i>



