# computer networking
> Computer networking is the practice of connecting multiple computers and devices together so they can communicate and share resources, such as data, files, internet connections, and printers.

| Network Type          | Description                                          | Typical Coverage Area      | Example                          |
|-----------------------|------------------------------------------------------|----------------------------|---------------------------------|
| Personal Area Network (PAN)  | Connects personal devices, usually wireless           | A few meters               | Bluetooth between phone and earbuds |
| Local Area Network (LAN)     | Connects devices within a small area like a home or office | Home, office, building     | Home Wi-Fi or office Ethernet   |
| Metropolitan Area Network (MAN) | Connects multiple LANs within a city or campus         | City or campus             | City-wide Wi-Fi, university network |
| Wide Area Network (WAN)      | Connects multiple LANs/MANs over large geographical areas | Countries, continents      | The Internet                   |
| Campus Area Network (CAN)    | Connects LANs within a limited area like a campus       | University or business campus | University network            |
| Storage Area Network (SAN)   | Specialized network for data storage access             | Data centers               | Networked storage devices       |

# how to connect computer networking:
**Behind the Scenes of Connecting Two Devices**

1. **Physical Layer Connection**  
   - Devices connect via cables (Ethernet) or wirelessly (Wi-Fi, Bluetooth).  
   - Data is transmitted as electrical signals or radio waves.

2. **Data Link Layer Setup**  
   - Devices use their unique **MAC addresses** to identify themselves locally.  
   - Protocols like Ethernet or Wi-Fi format data into frames and handle error detection.

3. **IP Address Assignment (Network Layer)**  
   - Devices receive an **IP address** to enable communication beyond physical connection.  
   - DHCP servers (e.g., routers) assign IPs automatically; otherwise, static IPs are set manually.  
   - IP addresses ensure data is routed correctly between devices.

4. **Establishing Connection (Transport Layer)**  
   - Protocols like **TCP** establish a reliable connection via a handshake process (SYN, SYN-ACK, ACK).  
   - TCP manages packet delivery, ordering, and error checking.

5. **Data Transfer (Application Layer)**  
   - Devices use application protocols (e.g., SMB for file sharing, HTTP for web) to exchange data.  
   - Network discovery allows devices to find each other and share resources.

6. **Acknowledgments and Error Handling**  
   - Devices send acknowledgments to confirm successful data receipt.  
   - Lost or corrupted packets are retransmitted to ensure data integrity.
# What is Topology in Computer Networking?
> Topology refers to the physical or logical layout of how devices (computers, printers, routers, etc.) are connected in a network. It shows the arrangement or structure of the network, including how data flows between device
# Types of Network Topology
 Physical Topology

 The actual physical layout of cables and devices.

For example, how devices are physically connected with cables or wirelessly positioned.
  Logical Topology

How data flows through the network, regardless of the physical connections.

For example, even if devices are physically connected in a star, data might flow in a ring pattern logically.

| Topology  | Description                                   | Example                          |
|-----------|-----------------------------------------------|---------------------------------|
| **Bus**   | All devices connected to a single central cable | Early Ethernet networks          |
| **Star**  | All devices connected to a central hub or switch | Most modern home or office networks |
| **Ring**  | Devices connected in a circular chain           | Token Ring networks              |
| **Mesh**  | Devices interconnected directly with many others | Wireless mesh networks           |
| **Tree**  | Hierarchical topology combining star and bus   | Large organizational networks   |


# What is MAC address:
>  MAC address (Media Access Control address) is a unique identifier assigned to a network interface card (NIC) for communications at the data link layer of a network.


Key Points:
* It’s used to identify devices on a local network (like your Wi-Fi).
* Usually consists of 12 hexadecimal digits (e.g., 00:1A:2B:3C:4D:5E).
* Often written in formats like 00-1A-2B-3C-4D-5E or 00:1A:2B:3C:4D:5E.
* Assigned by the manufacturer of the network device and is typically burned into the hardware.

# What is an IP Address?

An **IP address** (Internet Protocol address) is a unique string of numbers (and sometimes letters) that identifies a device on a network. It allows devices to communicate with each other over the internet or a local network.

---

## Types of IP Addresses

### 1. **IPv4 (Internet Protocol version 4)**
- Format: Four sets of numbers separated by dots (e.g., `192.168.1.1`)
- Each number ranges from 0 to 255
- Most common form today

### 2. **IPv6 (Internet Protocol version 6)**
- Format: Eight groups of four hexadecimal digits (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`)
- Designed to replace IPv4 due to limited address space

---

## Categories of IP Addresses

| Type           | Description                                             |
|----------------|---------------------------------------------------------|
| **Public IP**  | Used on the internet, assigned by ISPs                  |
| **Private IP** | Used within private networks (like your home Wi-Fi)     |
| **Static IP**  | Does not change; manually configured                    |
| **Dynamic IP** | Changes periodically; assigned by DHCP servers          |

---

## Example

If you're browsing the web from home:
- Your **router** has a **public IP address** on the internet.
- It assigns **private IP addresses** to your devices (like `192.168.0.101`).

---
# 📡 IP Address and MAC Address Bit Lengths

---

## 🔢 IP Address Bit Lengths

| IP Version | Bits     | Description                                                   |
|------------|----------|---------------------------------------------------------------|
| **IPv4**   | 32 bits  | Written as 4 decimal numbers (e.g., `192.168.1.1`)            |
| **IPv6**   | 128 bits | Written in 8 groups of 4 hexadecimal digits (e.g., `2001:0db8:85a3:...`) |

- **IPv4** supports about **4.3 billion** unique addresses (`2^32`).
- **IPv6** supports an extremely large number — **340 undecillion** addresses (`2^128`).

---

## 🎯 MAC Address Bit Length

| Type    | Bits     | Description                                                             |
|---------|----------|-------------------------------------------------------------------------|
| **MAC** | 48 bits  | Uniquely identifies network hardware (e.g., `00:1A:2B:3C:4D:5E`)         |

- MAC addresses are usually shown as **six pairs** of hexadecimal digits.
- Assigned to a device's **network interface card (NIC)** by the manufacturer.

---

## 📝 Summary

| Address Type | Bit Length |
|--------------|------------|
| **IPv4**     | 32 bits    |
| **IPv6**     | 128 bits   |
| **MAC**      | 48 bits    |


Here's how to check your **IP address** on both **Linux** and **Windows** systems.

---

## ✅ **How to Check IP Address on Windows**

### 🖥️ Using Command Prompt:

1. Press `Windows + R`, type `cmd`, and hit **Enter**
2. In the Command Prompt, type:

   ```bash
   ipconfig
   ```
3. Look for the line that says:

   * **IPv4 Address**: This is your private IP (e.g., `192.168.1.100`)
   * **Default Gateway**: This is usually your router’s IP

---

## 🐧 **How to Check IP Address on Linux**

### 🧾 Using Terminal:

#### For modern systems (uses `ip` command):

```bash
ip addr show
```

* Look for `inet` under your active network interface (like `eth0`, `wlan0`, or `enp0s3`)
* Example output:

  ```
  inet 192.168.1.42/24
  ```

#### For older systems:

```bash
ifconfig
```

* Note: You may need to install it first:

  ```bash
  sudo apt install net-tools
  ```

---

## 🌐 To Check Public IP Address (Both Linux & Windows)

### Use terminal with `curl` (if installed):

```bash
curl ifconfig.me
```

or

```bash
curl ipinfo.io/ip
```

---
## image of ip address

# Classes in IP Address

IP addresses (IPv4) are divided into **five classes** — A, B, C, D, and E — based on the first few bits of the address. This classification helps organize networks of different sizes.

---

## IP Address Classes Overview

| Class | First Octet Range (Decimal) | First Bits Pattern | Default Subnet Mask    | Usage                              |
|-------|-----------------------------|--------------------|-----------------------|----------------------------------|
| **A** | 1 – 126                     | 0xxxxxxx           | 255.0.0.0             | Large networks (millions of hosts) |
| **B** | 128 – 191                   | 10xxxxxx           | 255.255.0.0           | Medium-sized networks (thousands of hosts) |
| **C** | 192 – 223                   | 110xxxxx           | 255.255.255.0         | Small networks (up to 254 hosts)  |
| **D** | 224 – 239                   | 1110xxxx           | N/A                   | Multicast groups                   |
| **E** | 240 – 255                   | 1111xxxx           | N/A                   | Experimental/Research             |

---

## Details

### Class A
- Starts with a **0** bit.
- Supports **large networks** with up to about 16 million hosts.
- Example: `10.0.0.1`

### Class B
- Starts with bits **10**.
- Supports medium networks with up to ~65,000 hosts.
- Example: `172.16.0.1`

### Class C
- Starts with bits **110**.
- Supports small networks with up to 254 hosts.
- Example: `192.168.1.1`

### Class D
- Starts with bits **1110**.
- Used for **multicasting** (sending data to multiple destinations).

### Class E
- Starts with bits **1111**.
- Reserved for future or experimental use.

---

### Note:
- The addresses `127.x.x.x` are reserved for **loopback** (testing on your own machine).
- Classful networking is mostly replaced by **CIDR** now, but understanding classes is still useful.


# What Is Subnetting?
> Subnetting (short for sub-networking) is the process of dividing a large IP network into smaller, more manageable subnetworks, called subnets.
>

**📌 Why Use Subnetting?**

**Subnetting helps with:**
* Improved network management: Smaller subnets are easier to monitor and control.
* Efficient IP address allocation: Reduces waste of IP addresses.
* Improved security: Traffic can be isolated between departments or regions.
* Reduced congestion: Local traffic stays within the subnet, reducing overall load.
