# OSI Model Layer 2: Data Link

## What is the Data Link Layer?

The Data Link Layer is the **second layer** of the OSI model. It is responsible for ensuring **reliable communication** between devices connected to the same physical network. Here, data is organized into **frames** and sent to the physical layer (Layer 1).

---

## Key Functions

- **Physical Addressing (MAC):** Each device has a unique MAC (Media Access Control) address, used for identification on the local network.
- **Error Detection and Correction:** Checks if the data was transmitted correctly using techniques like CRC (Cyclic Redundancy Check).
- **Media Access Control:** Decides which device can use the network at a given time, avoiding collisions (CSMA/CD, CSMA/CA).
- **Data Encapsulation:** Organizes Network Layer (Layer 3) packets into frames for transmission.

---

## Associated Protocols

- **Ethernet:** The most common protocol for LANs.
- **Wi-Fi (802.11):** Wireless protocol for local networks.
- **PPP (Point-to-Point Protocol):** Used for direct connections between two points.

---

## Importance of the Data Link Layer

This layer is essential because it creates a reliable channel for data transmission. Without it, there would be more errors in data delivery, and devices wouldn’t be able to identify each other properly.

---

## How to Practice

Here’s a basic example of how to view Layer 2 information using network commands:

---

### View MAC Address on Windows:

In the terminal, run:

```
    ipconfig /all
```

---

## Learn More

- [Data Link Layer in OSI Model](https://www.geeksforgeeks.org/data-link-layer/)