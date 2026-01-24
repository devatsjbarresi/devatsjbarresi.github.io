---
layout: default
title: Host Table
parent: Guide
nav_order: 2
permalink: /documentation/guide/host-table/
---

<h1 align="center">Host Table</h1>

---

## Host Discovery

ShowShark gathers information on devices as packets are captured, building a comprehensive picture of "Who is on the network and what they are doing?". ShowShark "learns" about hosts through multiple different methods, including:

- **IP addresses** from network packets.
- **Hostnames** from mDNS, DNS, or entertainment protocols.
- **Manufacturers** from MAC OUI lookups, SNMP, entertainment protocol data.
- **Device types** from protocol analysis and manufacturer databases.
- **Protocol usage** by monitoring which protocols each host sends or receives.

## Show Host Table Window



The **Tools > ShowShark > Show Host Table** menu option opens a dedicated window that combines both the Host Properties and Host Protocols tables into a single view. This window provides a comprehensive overview of all discovered devices and their characteristics.

{: .note }
> The table currently doesn't display well on small screens given all the parameters. The window can be stretched to view all columns. The next version will include filter buttons to show and hide columns for easier viewing.

## Packet Details Tables

In the packet details pane, depending on your [Options](/documentation/guide/menus/) settings, you'll see up to two additional tables:

- **Host Properties Table** - Shows detailed information about the source or destination host.
- **Host Protocols Table** - Lists all protocols the host has been observed using.

These tables appear for each packet, providing quick access to host information without opening the main Host Table window.

### Host Properties Table

The Host Properties Table displays detailed information about each discovered host:

| Field | Description |
|-------|-------------|
| **ID** | Unique identifier for the host. |
| **Hostname** | Device hostname (from mDNS or other discovery protocols). |
| **IP Address** | Current IP address. |
| **MAC Address** | Hardware address (shown at Advanced level). |
| **Manufacturer** | Device manufacturer (derived from protocols, MAC OUI, or other sources). |
| **MAC Manufacturer** | Manufacturer from MAC OUI lookup (shown at Advanced level). |
| **Derived Manufacturer** | Manufacturer derived from entertainment protocols (shown at Advanced level). |
| **Assumed Manufacturer** | Manufacturer assumed from device characteristics (shown at Advanced level). |
| **Device Type** | Type of device (e.g., lighting console, fixture). |
| **Additional Hostnames** | Other hostnames associated with the device. |

### Host Protocols Table

Shows which protocols each host is using with a cross (✕) in each protocol column. For example, a device sending sACN packets will have a cross in the sACN column.

---

<div style="display: flex; justify-content: space-between; align-items: center;">
  <a href="/documentation/guide/menus/">< Menus</a>
  <a href="/documentation/guide/columns/">Configure Columns ></a>
</div>