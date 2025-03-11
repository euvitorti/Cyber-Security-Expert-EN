# What is Network?

**Network**, in general terms, refers to a set of elements or systems connected to each other to exchange information and resources. The concept can be applied in various areas, such as social networks, business networks, or computer networks.

## Generic Example of Network

In a broader context, imagine a social network where people can interact, share photos, texts, and messages. Each user is a "node" of the network and can communicate with others through connections called "edges." The goal is to facilitate the exchange of information between network participants.

---

# What is Network in Computing?

In the context of **computing**, a **computer network (network)** is a set of interconnected devices to enable communication and data exchange. These networks can vary in size, from local networks (LAN) to global networks like the **Internet**.

## Main Components of a Computer Network

- **Network Devices**: These are physical or virtual elements connected to the network, such as computers, servers, routers, switches, and mobile devices.
  
- **Communication Protocols**: These are rules and conventions that define how data will be transmitted between devices on the network. Examples include TCP/IP, HTTP, FTP, etc.

- **Transmission Media**: These are the channels through which data travels, which can be wired (such as Ethernet cables) or wireless (like Wi-Fi).

- **IP Addressing**: Each device on the network has a **unique (IP)** address to be identified and communicate with other devices. There are two main types of addresses:
  - **Public IP Address**: Used to identify the device on the Internet.
  - **Private IP Address**: Used to identify devices within a local network, such as a home or corporate network.
  
- **MAC Address**: Each device also has a **MAC (Media Access Control)** address, which is unique to the hardware of the network interface and used for identification within the local network.

## Example of Network in Computing

Imagine a company with several computers in an office. These computers are connected to each other through cables and switches, forming a local area network (LAN). Using protocols like TCP/IP, these devices can share files, access the Internet, or communicate via email.

Each computer has a unique IP address, allowing correct identification and communication between devices. Additionally, each device has a unique MAC address, which is used within the local network to identify the network interface uniquely. Communication on the local network is done through these addresses, ensuring that data packets reach the correct device.

---

# What is the Internet?

The **Internet** is a global network of interconnected networks that allows communication between devices worldwide. It provides access to information, services, instant communication, and much more. The Internet is fundamental to many daily activities, such as web browsing, sending emails, social networking, and instant messaging.

## Public and Private Internet

- **Public Internet**: Refers to the part of the Internet that is accessible to anyone with a network connection. This includes websites, email services, social media platforms, etc. Anyone can access these resources from anywhere, as long as they have the necessary infrastructure, like an Internet connection.

- **Private Internet**: This is a network restricted to a specific group of people or organizations. It is typically used in companies or institutions to connect devices internally without exposure to the public network. Examples include Intranets, which are private networks within an organization for securely sharing resources and information.

---

# How Did the Internet Start?

The **Internet** began as a military project in the United States called **ARPANET**, developed in the 1960s by the Advanced Research Projects Agency (ARPA). The goal was to create a communication network that would be resistant to failures during wartime situations. ARPANET used basic communication protocols that evolved over time.

In the 1980s, the **TCP/IP** concept was introduced, providing a standard for communication between different networks. This helped the Internet grow and expand, allowing the interconnection of different systems worldwide. In 1991, scientist Tim Berners-Lee developed the **World Wide Web (WWW)**, popularizing the use of the Internet and making it accessible to a broader audience.

---

# What is Ping?

**Ping** is one of the most fundamental and widely used network tools to test connectivity and performance between devices on a network. The **ping** command uses ICMP (Internet Control Message Protocol) packets to determine if a device is reachable on a network and to check the latency of the connection.

## How Does Ping Work?

The **ping** sends an **ICMP echo packet** to the destination device and waits for a response, called the **echo reply**. The time between sending and receiving the packets is measured and shown as the latency time (in milliseconds). This latency helps determine the quality of the connection between the devices.

### Example of Ping Command:

```
    ping www.google.com
```

This command sends ICMP echo packets to Google's server and measures the response time. The response might look like this:

```
    Pinging www.google.com [142.250.72.196] with 32 bytes of data:
    Reply from 142.250.72.196: bytes=32 time=15ms TTL=52
    Reply from 142.250.72.196: bytes=32 time=14ms TTL=52
    Reply from 142.250.72.196: bytes=32 time=13ms TTL=52
```


In this case, the response times were 15ms, 14ms, and 13ms, indicating a fast connection.

---

## What is ICMP?

ICMP (Internet Control Message Protocol) is a protocol used to send network control messages, such as error notifications and diagnostic information. It is essential for maintaining a healthy network and is used by tools like ping to check connectivity between devices.

ICMP is not responsible for transferring data between devices, but for communicating the status of the network. It can send error messages, such as when one device cannot reach another, or informational messages, like the response time of packets.

### Common ICMP Functions:

1. **Echo Request and Echo Reply**: Used in the ping command to test connectivity between devices.
2. **Destination Unreachable**: Indicates that a destination cannot be reached.
3. **Time Exceeded**: Used when a packet's time-to-live (TTL) expires, usually during routing.

---

## Conclusion

In summary, a network in computing refers to the structure that enables communication and data sharing between devices, facilitating access to resources and the exchange of information. The Internet, as a global network, connects millions of devices and allows the exchange of information on an unprecedented scale. There are public and private versions of the Internet, with the public being accessible to everyone and the private restricted to specific groups.

Furthermore, the IP address and MAC address are essential for identifying and communicating between devices within a network. The IP can be public or private, depending on where the device is located, while the MAC is unique to the network interface hardware and is primarily used in local networks. With the increase in the number of connected devices, the evolution of IP addresses, such as IPv6, has been crucial to ensure the continuous expansion of the Internet and connectivity for all devices.

Ping, using ICMP packets, is an essential tool for testing connectivity and network latency, helping to diagnose problems and check if a device is reachable. ICMP itself is a crucial protocol for network diagnostics and control, providing information on the status of communication between devices.

---

### Learn more
- [What is the Internet Control Message Protocol (ICMP)?](https://www.cloudflare.com/learning/ddos/glossary/internet-control-message-protocol-icmp/)