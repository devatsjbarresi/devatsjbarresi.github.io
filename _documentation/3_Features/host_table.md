---
layout: default
title: Host Table
parent: Features
nav_order: 2
---

<h1 align="center">Host Table</h1>

---

ShowShark automatically discovers and tracks all hosts on the network as packets are captured. The host tables provide a comprehensive view of discovered devices and their characteristics.

### Accessing Host Tables

Host tables can be accessed via **Tools > ShowShark > Host Table**. The tables update automatically as new packets are processed and additional information is discovered.

### Table Types

ShowShark provides three different table views:

#### Host Properties Table

The **Host Properties Table** displays detailed information about each discovered host:

- **ID** - Unique identifier for the host
- **Hostname** - Device hostname (from mDNS or other discovery protocols)
- **IP Address** - Current IP address
- **MAC Address** - Hardware address (shown at Advanced level)
- **Manufacturer** - Device manufacturer (derived from protocols, MAC OUI, or other sources)
- **MAC Manufacturer** - Manufacturer from MAC OUI lookup (shown at Advanced level)
- **Derived Manufacturer** - Manufacturer derived from entertainment protocols (shown at Advanced level)
- **Assumed Manufacturer** - Manufacturer assumed from device characteristics (shown at Advanced level)
- **Device Type** - Type of device (e.g., lighting console, fixture)
- **First Seen** - Timestamp when host was first observed (shown at Advanced level)
- **Last Seen** - Timestamp when host was most recently observed (shown at Advanced level)

#### Host Protocols Table

The **Host Protocols Table** shows which protocols each host is using:

- **ID** - Unique identifier for the host
- **Hostname** - Device hostname
- **IP Address** - Current IP address
- **Protocols** - List of protocols the host has been observed using

This table is useful for quickly identifying which devices are using specific protocols like sACN, Art-Net, RDM, OSC, or other entertainment control protocols.

#### Mega Table

The **Mega Table** combines both host properties and protocols into a single comprehensive view, showing all available information about each host in one place.

### Display Levels

The columns visible in the host tables depend on your current display level:

- **Essential** - Shows basic host information (hostname, IP, manufacturer, device type)
- **Advanced** - Includes additional details (MAC address, manufacturer sources, first/last seen timestamps)
- **Debug** - Shows all available fields including internal diagnostic information

You can change the display level via **Tools > ShowShark > Display Level**.

### Host Discovery

ShowShark discovers hosts through multiple sources:

- **MAC addresses** from Ethernet frames
- **IP addresses** from network packets
- **Hostnames** from mDNS, DNS, or entertainment protocols
- **Manufacturers** from MAC OUI lookups, SNMP, entertainment protocol data
- **Device types** from protocol analysis and manufacturer databases
- **Protocol usage** by monitoring which protocols each host sends or receives

As packets are captured, ShowShark continuously updates host information, building a comprehensive picture of the network topology and device characteristics.