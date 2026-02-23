# CCNA Lab – NAT + DHCP + Internet Simulation

## Overview

This lab demonstrates Network Address Translation (NAT), DHCP configuration, and Internet connectivity simulation. Internal devices receive IP addresses automatically via DHCP and access an external network using NAT overload (PAT).

Built and tested using Cisco Packet Tracer.

---

## Network Design

Components:

* Internal LAN: 192.168.1.0/24
* DHCP Server: Router
* NAT Device: Edge Router
* External Network (Internet Simulation): 209.165.200.0/24

Inside interface: G0/0
Outside interface: G0/1

---

## Key Configuration

DHCP configuration:

```id="l27ah5"
ip dhcp pool LAN
network 192.168.1.0 255.255.255.0
default-router 192.168.1.1
dns-server 8.8.8.8
```

NAT Overload configuration:

```id="v9t3op"
access-list 1 permit 192.168.1.0 0.0.0.255

ip nat inside source list 1 interface g0/1 overload
```

Interface configuration:

```id="7udn5x"
interface g0/0
ip nat inside

interface g0/1
ip nat outside
```

---

## Verification

Commands used:

* show ip nat translations
* show ip nat statistics
* show ip dhcp binding
* show ip interface brief

Ping to external network confirms Internet connectivity.

---

## Skills Demonstrated

* DHCP configuration
* NAT overload (PAT)
* Inside and Outside NAT configuration
* Internet access simulation
* IP address management
* Network verification and troubleshooting

---

## Lab File

CCNA LAB 8 – NAT + DHCP + Internet Simulation (.pkt)

---

## Author

Amir Samandi
CCNA Certified
