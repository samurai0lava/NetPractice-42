# NetPractice-42
The basics of networking

## OSI Model (Open Systems interconnection) created by the ISO.

**7 layers :**



*the 7th layer :*Application layer* 
                ->the closet to the end USER, intercat with the web dev.
                ->http and https are layer 7.
                ->identify and secure the connection.

*the 6th layer :*
*the 5th layer :*
*the 4th layer :*
*the 3th layer :*
*the 2th layer :*
*the 1st layer :*

## TCP/IP Suite 
created by USA defense (DARPA).

->Conceptual Model used in the internet and other Network
->like OSI model but with fewer layers

**4 layers :**

*the 4th layer :* Application (7th , 6th , 5th layer of OSI model)
*the 3th layer :* Transport (4th layer of OSI model)
*the 2nd layer :* Internet (3th layer of OSI model)
*the 1st layer :* Link (2nd , 1st layer of OSI model)


## DHCP (Dynamic Host Configuration Protocol)

->DHCP allows hosts to automatically learn various aspects of their network config. IP address , Subnet Mask, default gateway, DNS Server
->Routers and Servers... are manually configured because they need a fixed IP
->Small Networks router act like as the DHCP server for host in the LAN
->Large Network a DHCP server is Linux Server
->*Lease time* determinated by DHCP sever , the client must give the address of the en of the lease/

**DHCP requests:**

*DORA*
->DHCP **D**iscover (is there any DHCP server in this NETWORK i need a an IP address). request type : BROADCAST.
->DHCP **O**ffer (hmmm what about this IP add u can use it).request type : BROADCAST or UNICAST.
->DHCP **R**equest (i thick im using this ip address u did gave me). request type : BROADCAST.
->DHCP **A**ck (okay u can use it, and thank u for letting me know :p). request type : BROADCAST or UNICAST.

## DNS
**The purpose of DNS** 

is used to convert names (www.smtg.com) to a ip adresses, youtube.com ->> #.#.#.# 
DNS CACHE : device will save the DNS dervers responds to save on network traffic.

## ROUTING 

A process that router use to determine the path that ip packet take over a network to rach their destination 
**Dynamic Routing :** Share each other automatically ...
**Static Routing :** manually configures 

**Route :** tell the router to send a packet to **destination X**, should send to the packet to **next-hop Y** "next router"

**WAN**: Wide Area Network.
**LAN**: Local Area Network.

**Default Gateway** : send all "non-local" traffic to.

## TC & UDP (protocols from the 4th Layer) :

**TCP** is connection-oriented.
**TCP** provides reliable communication.
        |-> the destination host must acknowledge that.
**TCP** provides squencing.
**TCP** flow control.



**TCP three way handshake**
 ________
|        |      SYN FLAG
|________|---------->
  *PC1*

 ________
|        |      SYN FLAG, ACK FLAG.
|________|---------->
  *serv1*

 ________
|        |     ACK FLAG
|________|---------->
  *PC1*

