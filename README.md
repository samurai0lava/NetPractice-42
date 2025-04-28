# NetPractice - 42  
*The Basics of Networking*

---

## OSI Model (Open Systems Interconnection)

Created by **ISO** (International Organization for Standardization).

**7 Layers:**

1. **Physical Layer (Layer 1)**  
   - Converts bits into electrical signals, radio waves (for wireless), or light pulses (for fiber optics).  
   - Deals with the physical transmission of data.

2. **Data Link Layer (Layer 2)**  
   - Ensures reliable transmission between two devices on the same network (e.g., PC to Switch, Router to Router).  
   - Detects and corrects physical transmission errors.  
   - Devices: **Switches**.

3. **Network Layer (Layer 3)**  
   - Provides logical addressing (IP addresses).  
   - Handles packet forwarding, including routing through routers.  
   - Devices: **Routers**.

4. **Transport Layer (Layer 4)**  
   - Segments and reassembles data for communication (host-to-host communication).  
   - Ensures complete data transfer.

5. **Session Layer (Layer 5)**  
   - Manages sessions (dialogues) between applications.

6. **Presentation Layer (Layer 6)**  
   - Translates data (e.g., encryption, decryption, compression).  
   - Ensures that the data is in a usable format.

7. **Application Layer (Layer 7)**  
   - Closest to the end-user, interacts directly with software applications.  
   - Example protocols: **HTTP**, **HTTPS**.  
   - Identifies and secures communication.

---

## TCP/IP Model

Created by **DARPA** (U.S. Department of Defense).

**4 Layers:**

1. **Link Layer**  
   (Corresponds to OSI Layers 1 & 2)

2. **Internet Layer**  
   (Corresponds to OSI Layer 3)

3. **Transport Layer**  
   (Corresponds to OSI Layer 4)

4. **Application Layer**  
   (Corresponds to OSI Layers 5, 6, 7)

The TCP/IP model simplifies the OSI model by combining similar functions into fewer layers.

---

## DHCP (Dynamic Host Configuration Protocol)

- Automatically assigns **IP addresses**, **subnet masks**, **default gateways**, and **DNS servers** to devices.
- Devices like routers and servers usually have **static IP addresses**.
- **Small Networks:** Router often acts as the DHCP server.
- **Large Networks:** A dedicated DHCP server (often Linux-based) is used.
- **Lease Time:** IP addresses are leased for a period determined by the DHCP server.

### DHCP Process (DORA):

- **D**iscover: Client broadcasts a request for an IP address.  
- **O**ffer: DHCP server offers an available IP address (Broadcast or Unicast).  
- **R**equest: Client requests to use the offered IP address (Broadcast).  
- **A**ck: DHCP server acknowledges the lease (Broadcast or Unicast).

---

## DNS (Domain Name System)

- **Purpose:** Translates domain names (like `youtube.com`) into IP addresses (like `142.250.190.78`).
- **DNS Cache:** Stores previous DNS lookups to reduce network traffic and speed up access.

---

## Routing

- **Routing** is the process routers use to determine the path packets take across networks.

### Types of Routing:
- **Static Routing:** Manually configured routes.
- **Dynamic Routing:** Routers share routing information automatically.

### Key Concepts:
- **Route:** Tells the router to forward packets destined for "X" to the next-hop "Y" (next router).
- **Default Gateway:** A device (usually a router) where a host sends traffic that is destined for outside its local network.

---

## TCP & UDP (Transport Layer Protocols)

### TCP (Transmission Control Protocol)

- **Connection-oriented:** Establishes a connection before data is transferred.
- **Reliable communication:** Ensures that data arrives intact and in order.
- **Sequencing:** Maintains the correct order of packets.
- **Flow control:** Manages the rate of data transmission between sender and receiver.

### TCP 3-Way Handshake:

```plaintext
Client (PC1)        Server (Serv1)
    SYN  ---------------->
                  SYN+ACK  ---------------->
    ACK  ---------------->
