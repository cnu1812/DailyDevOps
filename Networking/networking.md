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
->It ensures that the data will reach its destination and not get corrupted on the way i.e 100% of the datawill be received.
- `UDP - User Datagram Protocols`
-> It is a lightweight data transport protocol.
-> It provides a mechanism to detect corrupt data in packets, but it does not attempt to solve other problems that arise with packets, such as lost or out of order packets.
- `HTTP - Hyper Text Transfer Protocol`
-> It is an application-layer protocol for transmitting hypermedia documents, such as HTML.
-> Is used by web browsers, this is the data which be being transferred between clients and servers.

  
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

**SONET:** Synchronous Optical Networking
**Frame relay:** A wave for connecting local area network to the wide area like internet

## MODEM, ROUTER

**Modem** is a combined device for modulation and demodulation. It is used to convert digital to analog and vice-versa.

**Router** is a device that forwards data packets between computer network.

**ISP:** Internet Service Provider are companies that provide us access to the internet
