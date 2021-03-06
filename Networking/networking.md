 # COMPUTER NETWORKING

## Resources
1.[Complete Networking Course](https://www.youtube.com/watch?v=IPvYjXCsTg8)

2.[Networking](https://www.youtube.com/watch?v=Mad4kQ5835Y&list=PL7zRJGi6nMRzg0LdsR7F3olyLGoBcIvvg)

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

 ## Client Server Architecture

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

![Untitled-2022-02-21-1932](https://user-images.githubusercontent.com/75531528/155082223-03da8bc3-a91b-414a-8bd5-0b3228c31a74.png)


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

<b>HTTP</b>

- It is a client server protocol and it tells us how you request this data from the server and also tell us how the server sends back data to the client.
- When a client makes a request to the server it is known as HTTP request, when a server sendsback response to the client it is HTTP response.
- HTTP uses TCP
- It is a stateless protocol(server will not store any information about client by default.).
- Method is basically telling the server what to do.

<b>HTTP Methods</b>

- GET: You are requesting some data.
- POST: client gives some data to server e.g forms.
- PUT: puts data at a specific location 
- DELETE: To delete data from the server.

<b>Error/status codes:</b>

When you send a request to the the server, you need some sort of a way to know whether the request is successful or not. for this there exists status code.

    200 - request successful
    404 - not found
    400 - bad request
    500 - internal server error

    1xx --> Informational category
    2xx --> Success code
    3xx --> Redirecting purpose
    4xx --> Client error
    5xx --> Server error

<b>Cookies</b>

- It is a unique string stored on a client browser.
- When you visit the web page for the first time, the cookie is set and whenever you make a new request, the request header cookie will be sent.

## How email works

- Application layer protocol: SMTP(simple mail transfer protocol), POP3 PostOffice Protocol.
![image](https://miro.medium.com/max/1130/1*9ZW46uHlvlyvJb5moQs9aQ.jpeg)
- Command to view ip address of SMTP server `nslookup -type=mx gmail.com`. 
- IMAP - Internet message access protocol: Allows to view emails on multiple devices.

## DNS Domain Name System

- Domain names are mapped to ip address we use servicess to look up into this. The most popular service is DNS.(Imagine DNS server as a phonebook)
![image](https://academy.bit2me.com/wp-content/uploads/2019/05/49_DNS.png)
- When we type google.com http protocol take that domain name and use DNS to find the ip address and afterwards it connects to the server.

- <b>Root DNS server</b>: Root servers, or DNS root servers, are name servers that are responsible for the functionality of the DNS as well as the entire Internet. They're the first step in the name resolution of any domain name, meaning they translate domain names into IP addresses.
- <b>TLD Top Level Domain</b>:A top-level domain is one of the domains at the highest level in the hierarchical Domain Name System of the Internet after the root domain. eg .com,.org,.edu,.gov,.mil,.io ...
![image](https://info.varonis.com/hubfs/Imported_Blog_Media/how-dns-works@2x.png?hsLang=en)
- <b>Authoritative DNS</b>:It is the system that takes an address, like google.com, and provides an answer about the resources in that zone. The typical transaction looks something like this: User types an address into a web browser, or an application calls out to a given name of a resource on the Internet.
- Command to locate DNS server `dig example.com`

# Transport Layer:

- Data transfered between one computer to another is done by using network layer
- Transport layer is a layer that lies over device
- The role of the transport layer is to take the data from the network to the application.
![image](https://www.tutorialandexample.com/wp-content/uploads/2020/10/image-287.png)
- Provides abstraction, located on the devices.
- Data travels in packets.
- Transport layer will attach these socket port numbers to that packets.
![image](https://i.imgur.com/P4ZbIPb.png)
- It also takes care of congestion control.
- What is congestion?
A state occurs in the network layer when the message traffic is so heavy that it slows down network response time.
- Congestion control algorithms built in TCP.

## Checksum
A checksum is a value that represents the number of bits in a transmission message and is used by IT professionals to detect high-level errors within data transmissions. ... The common protocols used to determine checksum numbers are the transmission control protocol (TCP) and the user diagram protocol (UDP).

## Timers
- 
- 

# Transport Layer Protocol.

## UDP - User Datagram Protocol

- Data may or may not delivered,may change,not be in order.
- Connectionless Protocol
- UDP uses checksums if there any error it won't care.
![image](https://i2.wp.com/ipwithease.com/wp-content/uploads/2018/01/091-udp-user-datagram-protocol-01.png)
Header 8 bytes, data 2^16 -8;

**Uses of UDP**
- Very fast,Used in video conferencing apps, DNS uses udp, gaming.
    `sudo tcpdump -c 5`

## TCP - Transmission Control Protocol
- Application layer sends lot of raw data. TCP segments this data, divide into chunks, add headers...Simultaneously it collects data from network layer and the small chuncks are put in to one in the receiving end.
- Congestion control
- Takes care of: When data does not arrive, maintain the order of data.  

**Features**
- Connection oriented
- error control, congestion control, full duplex.

**__3- Way Handshake__**

![image](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/what-is-a-tcp-3-way-handshake-process-three-way-handshaking-establishing-connection-6a724e77ba96e241.jpg)

Sequence number(m) is a random number.

# Network Layer
Here we work with routers

![image](https://s3.ap-south-1.amazonaws.com/afteracademy-server-uploads/what-is-rip-routing-information-protocol-example-0b0fad96363f15fc.jpg)

- Every router has a network address
- Every router will check whether the packet is for that router, if not then it will forward that using <i>Forwarding table</i> in routing table.
- Command to trace route is:

      tracert example.com
<b> Control plane is used to build these routing tables.</b>

- Static routing and Dynamic routing.

## Network layer protocol
**ip- Internet Protocol**

IPv4 --> 32bit, 4 words

IPv6 --> 128bits

- Classes 

|CLASS|IP ADDRESS|DEFAULT SUBNET MASK|
|-----|----------|-------------------|
|A|0-126|255.0.0.0|
|B|128-191|255.255.0.0|
|C|192-223|255.255.255.0|
|D|224-239|N/A|
|E|240-255|N/A|

**Subnet Masking**

Subnet mask is going to mask the network part of the ip address and leaves us the host part.

eg: 15.0.0.0/30 this basically means the first 30 bits are my subnet/network part.

<b>Reserved address:</b>

127.0.0.0/8
eg: localhost: 127.0.0.1(loopback address) used for testing.
- <b>Packets</b>: Header is of 20bytes. It contains IPv,length,identification number,flags,protocols,checksum,TTL...
- TTL(Time to live): It is a number, after that number of hops the packet doesn't reach, then it eill leave.

**IPv6**
- IPv4: 2^32 ~ 4.3billion
- IPv6: 2^32*4=2^128
- Formate - a.a.a.a.a.a.a.a(hexadecimal)

**Middleboxes(Firewalls)**
- They are extra devices that also interacts with ip packets.
- Mostly it willl be in network layer but it can also be in transport layer.
- Firewall is of two types.1. Connected to global network.2. Your local network.
- It filters out ip packets based on various rules.
- Stateless and stateful firewalls.

## Network Address Translator(NAT):

It is a method of mapping anip address space into another by modifying network address information in the ip header of packets while they are in transit across a traffic routing device.
![image](https://i0.wp.com/edifyclue.in/wp-content/uploads/2021/02/network-address-translation-1.png?resize=500%2C300&ssl=1)

# Data Link Layer

The data packets that are receiving from the network layer .The data link layer is responsible to send these packets over a physical layer.
- In data link layer, the devices communicate with each other using <b>Data Link Layer Addresss(MAC address)</b>

![image](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRJ6qSgckwrOXctaHzQ62ZVfLrOrTQBU65_gw&usqp=CAU)

Let's say device 1 needs to send data to device 4, first it will lookup in it's <i>cache</i>, If it does not have then it will ask other devices. This is known as ARP Cache(Address Resolution Protocol)

      arp -a












