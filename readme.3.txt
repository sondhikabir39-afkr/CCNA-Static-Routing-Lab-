# CCNA Lab: IP Routing Using Static Routes

## 📌 Overview

This project demonstrates IP routing between two different networks using two Cisco routers in Cisco Packet Tracer. Static routing is configured to enable communication between devices located on separate LANs.

## 🎯 Objectives

* Understand IP routing concepts.
* Configure router interfaces with IP addresses.
* Configure static routes.
* Verify connectivity using the `ping` command.
* Understand packet forwarding between different networks.

## 🛠️ Topology

```
PC1 ---- Switch1 ---- Router1 ===== Router2 ---- Switch2 ---- PC2

192.168.1.0/24         10.0.0.0/30         192.168.2.0/24
```

## 🌐 IP Addressing

| Device  | Interface | IP Address    |
| ------- | --------- | ------------- |
| PC1     | NIC       | 192.168.1.3   |
| Router1 | G0/0      | 192.168.1.2   |
| Router1 | G0/1      | 10.0.0.1      |
| Router2 | G0/0      | 10.0.0.2      |
| Router2 | G0/1      | 192.168.2.1   |
| PC2     | NIC       | 192.168.2.3   |

Subnet Mask:

* 192.168.x.x networks → 255.255.255.0
* 10.0.0.x router link → 255.255.255.252

## ⚙️ Static Routes

Router1:

```
ip route 192.168.2.0 255.255.255.0 10.0.0.2
```

Router2:

```
ip route 192.168.1.0 255.255.255.0 10.0.0.1
```

## ✅ Verification

* Ping from PC1 to Router1
* Ping from PC1 to Router2
* Ping from PC1 to PC2
* Verify successful end-to-end communication across both networks

## 📚 Concepts Learned

* IP Addressing
* Router Interface Configuration
* Static Routing
* Default Gateway
* Packet Forwarding
* Network Troubleshooting
* ICMP (Ping)

## 🚀 Outcome

Successfully configured static routing between two routers and enabled communication between hosts located on different IP networks using Cisco Packet Tracer.

## 🛠️ Tools Used

* Cisco Packet Tracer
* Cisco IOS CLI

## 🏷️ Tags

CCNA • Cisco Packet Tracer • Networking • IP Routing • Static Routing • Network Fundamentals
