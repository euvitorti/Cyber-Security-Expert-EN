# Connectivity Analysis and Packet Monitoring (Unencrypted Communication)

In this project, I set up a network between my host system (Windows, Mac, or another) and a virtual machine (Kali Linux) to analyze unencrypted network traffic. The goal is to understand how data flows between the machines, view the "bare" packets with Wireshark, and prepare the environment to implement encryption in communication in the next step.

## Network Setup

I used VirtualBox to create a network between the host system and Kali Linux. To do this, I configured the VM with the Host-Only Adapter option, creating an isolated local network that allows communication between the machines without passing through the physical router or the internet.

## How to Get My IP Address

Before setting up the network, it's important to know the IP address of my system. Here's how to find the IP address on different operating systems:

### On Windows

1. Open the **Command Prompt** and type the command:
```
   ipconfig
```

Look for the active network interface (for example, "VirtualBox Host-Only Network Adapter" or "Ethernet"). The displayed IPv4 address (e.g., 192.168.56.1) is the IP of my system.

### On Kali Linux

1. Open the **terminal** and type one of the commands:
```
    ip a
```
```
    ifconfig
```

Identify the correct network interface (usually eth0, enp0s3, or similar) and note the assigned IP address.

### On Mac OS

1. Open the **terminal** and type the command:
```
    ifconfig
```

Look for the network interface (usually en0 for Ethernet or en1 for Wi-Fi) and locate the IPv4 address.

---

## Connectivity Test

After setting up the network and checking the IP address of each machine, I performed tests to confirm that the machines are communicating correctly:

1. Ping:

- **On Windows (or Mac), run:**

```
    ping [IP do Kali]
```

- **On Kali Linux, run:**

```
    ping [IP do Hospedeiro]
```

If the packets respond, it means the connection is working.

2. Traceroute:

- **On Windows:**

```
    tracert [IP do Kali]
```

- **On Kali Linux:**

```
    traceroute [IP do Hospedeiro]
```

This command shows the path taken by the packets, confirming that the machines are on the same network or the correct path.

---

## Monitoring with Wireshark

To analyze unencrypted network traffic, I used Wireshark on Kali Linux.

### Steps for Capture and Analysis:

1. Open Wireshark: I started Wireshark on Kali Linux.
2. Select the Network Interface: I chose the interface (e.g., eth0 or enp0s3) that is connected to the network set up in VirtualBox.
3. Start Capture: I clicked "Start" to begin capturing packets.
4. Generate Traffic: On Windows (or Mac), I ran commands like ping or traceroute to generate network traffic between the host and Kali.
5. Apply Filters: I used filters to make the analysis easier, for example:
    - **To view ICMP packets:**
    ```
        icmp
    ```
    - **To filter traffic between specific IPs:**
    ```
        ip.addr == [Host IP] || ip.addr == [Kali IP]
    ```
    - **To see HTTP traffic (if any):**
    ```
        tcp.port == 80
    ```
6. Analyze the Packets: I examined the packet details (source/destination IP addresses, protocol type, response time, etc.) to confirm that the data is being transmitted without encryption.

## Conclusion

In this phase, the focus was on analyzing unencrypted network communication and demonstrating how traffic can be captured and visualized with Wireshark. This analysis reveals the transparency of the transmitted data, highlighting security risks in the absence of protection.