# CCNA Lab – OSPF Multi-Router Network

## Overview

This lab demonstrates dynamic routing using OSPF (Open Shortest Path First). Multiple routers exchange routing information automatically to provide full network connectivity.

Built and tested using Cisco Packet Tracer.

---

## Network Design

Routers connected in multi-network topology.

Example networks:

* 192.168.1.0/24
* 192.168.2.0/24
* 192.168.3.0/24

Routing protocol: OSPF Area 0

---

## Key Configuration

Enable OSPF:

```id="ospf1"
router ospf 1
network 192.168.1.0 0.0.0.255 area 0
network 192.168.2.0 0.0.0.255 area 0
network 192.168.3.0 0.0.0.255 area 0
```

Router ID example:

```id="ospf2"
router ospf 1
router-id 1.1.1.1
```

---

## Verification

Commands used:

* show ip ospf neighbor
* show ip route
* show ip protocols

All routers successfully learned routes dynamically.

---

## Skills Demonstrated

* OSPF configuration
* Dynamic routing
* Router neighbor adjacency
* Route advertisement
* Network troubleshooting
* Enterprise routing concepts

---

## Lab File

CCNA OSPF Lab (.pkt)

---

## Author

Amir Samandi
CCNA Certified
Network+ Certified
