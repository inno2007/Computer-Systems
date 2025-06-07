# Internet and Web Basics

This file introduces how the internet works, basic network structures, devices, browser technologies, and the client-server model.

---

## Computer Networks

- A **computer network** is a group of connected devices that share data and resources.

### Network Types

- **LAN (Local Area Network)**:
  - Small scale (e.g., office, school lab)
  - Easy to manage, cost-effective

- **WAN (Wide Area Network)**:
  - Covers large geographic areas
  - Costly and complex
  - Internet is the world’s largest WAN

---

## Common Networking Devices

| Device                  | Function                                                               |
|-------------------------|------------------------------------------------------------------------|
| Modem                   | Converts between analog and digital signals                            |
| NIC (Network Interface Card) | Provides network connection to a computer                        |
| Hub                     | Broadcasts data to all connected ports (legacy)                        |
| Switch                  | Connects devices using MAC addresses (replaced hubs)                   |
| Router                  | Directs data using IP addresses; connects networks                     |
| Wireless Access Point   | Enables wireless network connectivity                                  |

---

## Internet Overview

- The **Internet** is a global collection of interconnected networks.
- No single owner; it's a “network of networks.”
- Provides access to information, services, and global communication.

---

## Internet Service Providers (ISPs)

- Offer internet access to users
- Major providers in Australia: Telstra, Optus
- Connection Types:
  - **Narrowband** (e.g., dial-up, 56Kbps)
  - **Broadband** (e.g., DSL, NBN)
  - **Wireless** (Wi-Fi, 4G, 5G)

---

## TCP/IP and Packet Switching

- The Internet uses **TCP/IP** protocols for communication.
- **Packet Switching**:
  - Data is broken into packets
  - Each packet may take a different path
  - Packets are reassembled at the destination

---

## Internet Architecture Models

### Two-Tier Client/Server

- **Client**: Web browser
- **Server**: Hosts website and processes requests
- Two types of clients:
  - **Fat client**: Processes data on the client
  - **Thin client**: Processing happens on the server (e.g., web apps)

### Three-Tier Web Architecture

1. **Presentation Tier**: Web page interface (HTML/CSS/JS)
2. **Processing Tier**: Server-side logic (e.g., PHP, Python)
3. **Database Tier**: Stores data (e.g., MySQL, PostgreSQL)

---

## Web Technologies

### URLs (Uniform Resource Locator)

- Format: `http://www.example.com/index.html`
  - **Protocol**: HTTP or HTTPS (secure)
  - **Domain name**: Server address
  - **Path**: Location of the resource

### HTTP vs HTTPS

- **HTTP**: Transfers data as plain text
- **HTTPS**: Secure; uses encryption and certificates (SSL/TLS)

---

## Browsers

Popular browsers: Chrome, Firefox, Safari, Edge  
Functions:
- **Download**: Get files from web to local device
- **Upload**: Send files from device to internet

---

## Web Servers and W3C

- **W3C**: World Wide Web Consortium – sets web standards
- Web servers host websites and respond to client requests
- Examples: Apache, Nginx, Microsoft IIS

---

## Peer-to-Peer (P2P) Networking

- Each device acts as both **client and server**
- Used in:
  - File sharing (e.g., BitTorrent)
  - Messaging (e.g., WhatsApp, Skype)
  - Distributed computing (e.g., SETI@home, cryptocurrency)

---

This file sets the foundation for web security and scripting which will follow next.
