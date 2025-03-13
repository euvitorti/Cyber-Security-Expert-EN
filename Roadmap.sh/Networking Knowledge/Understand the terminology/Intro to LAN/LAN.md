# What is a LAN?

**LAN** stands for **Local Area Network**. It refers to a network that connects devices in a limited geographical area, such as a home, office, or university campus.

## Key Characteristics

- **Limited Scope:**  
  Typically covers a small area, allowing multiple devices to be connected within close physical proximity.

- **High Speed:**  
  Due to short distances, transfer rates are high and latency is low.

- **Local Management:**  
  The network can be centrally managed, making it easier to control and maintain.

- **Resource Sharing:**  
  Allows devices to share printers, files, internet access, and other resources.

## Examples of Application

- **Home Networks:**  
  Connecting computers, smartphones, smart TVs, and other devices within a household.

- **Business Networks:**  
  Connecting workstations, servers, and devices within a corporate environment.

- **Educational Environments:**  
  Networks used in schools and universities to facilitate communication and data sharing.

## LAN vs WAN

- **LAN (Local Area Network):**  
  - Covers a limited geographical area.  
  - High speed and low latency.  
  - Usually managed locally.

- **WAN (Wide Area Network):**  
  - Covers large geographical areas, such as cities, countries, or continents.  
  - Speeds can be lower and latency higher.  
  - Typically consists of multiple interconnected LANs.

## Practical Example: Configuring and Testing a Virtual LAN

In this example, we use an environment with:

- **Host:** Windows 10  
- **Virtual Machine:** Kali Linux running on VirtualBox  
- **Network Settings:**  
  - Adapter 1 set as **Host-Only Network** (for direct communication between Windows and Kali)  
  - Adapter 2 set as **NAT** (for internet access)

### 1. Configuring VirtualBox

1. **Open VirtualBox** and select your virtual machine (in this example, Kali Linux).
2. Click on **Settings** and go to the **Network** tab.
3. In **Adapter 1**, enable the option and select **Host-Only Network** to create an isolated virtual LAN.
4. In **Adapter 2**, ensure **NAT** is selected to allow internet access.

### 2. Checking IP Settings

- **On Windows (Host):**  
  Open Command Prompt and run:
```
  ipconfig
```
Check that the interface associated with the "Host-Only" network has an IP (e.g., 192.168.56.1).

- **On Kali Linux (Virtual Machine):**  
  Open a terminal and run:
```
    ip addr
```
Check that the interface associated with the "Host-Only" network has an IP (e.g., 192.168.56.1).

- **On Kali Linux (Virtual Machine):**  
  Open a terminal and run:
```
    ping 192.168.56.101
```
You should see responses indicating that the packets were sent and received successfully.

2. **From Kali to Windows:**  
In Kali terminal, run:
```
    ping 192.168.56.1
```
Verify that Windows responds to the pings.

### 4. Starting an HTTP Server on Kali

1. On Kali Linux, open a terminal and run:
```
    python3 -m http.server 8080
```

This will start a simple HTTP server on port 8080.

2. Testing the Server:  
On Windows, open a browser and access:
```
    http://192.168.56.101:8080
```

The server on Kali should respond, displaying a directory listing.  
In Kali's terminal logs, you will see information like the client's IP address (Windows), access time, and the HTTP method (GET) used in the request.

### 5. Analyzing Logs and Exploring Further

1. Log Analysis:  
Observe the HTTP server logs in Kali's terminal to understand the details of each request (IP, date, method, etc.).

2. Exploring with Nmap:  
On Kali, you can scan the network to identify connected hosts:
```
    sudo nmap -sP 192.168.56.0/24
```
This will list all active devices in the virtual LAN.

## Conclusion
This practice demonstrates a simple and direct way to configure a virtual LAN using Kali Linux and Windows, enabling:

- Understanding of theoretical concepts of local networks.
- Configuration of an isolated and controlled test environment.
- Practical analysis of communication between devices through pings, running HTTP servers, and monitoring logs and traffic.
- By testing these concepts in practice, you build a solid foundation for further studies in networks and cybersecurity, integrating tools like Nmap, Wireshark, and others in your future projects.

This document was created to help with theoretical and practical understanding of LANs and serve as documentation for studies in networks and cybersecurity.