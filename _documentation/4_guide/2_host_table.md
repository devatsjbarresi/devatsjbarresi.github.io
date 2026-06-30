---
layout: default
title: Host Table
parent: Features
nav_order: 30
permalink: /docs/host-table/
---

<h1 align="center">Host Table</h1>

---

Host Table gives you a running inventory of devices discovered in the capture, including identity, protocols, and derived metadata.

## Where You Can See Host Table Data

Host Table information appears in two places:

1. **Main Host Table Window** via _Tools > ShowShark Tools > Host Table_.
2. **Packet Details Tables** in the packet details pane for the selected packet.

Use the main window for network-wide overview and filtering. Use packet details tables for quick per-packet context while drilling into traffic.

## Quick Start

1. Open a capture and let traffic run for a short time.
2. Open _Tools > ShowShark Tools > Host Table_.
3. Review discovered hosts and protocols.
4. Use the bottom controls to filter visible columns and find values.
5. Export Host Table data to **CSV** when needed.

{: .tip }
> The longer you capture, the more complete Host Table becomes.

## Host Discovery

ShowShark gathers information on devices as packets are captured, building a comprehensive picture of "who is on the network and what they are doing?". ShowShark learns about hosts through multiple different methods, including:

- **Manufacturers** from MAC address OUIs and protocol metadata.
- **Hostnames** from entertainment protocol announcements.
- **Entertainment protocols** by monitoring the protocol traffic each host sends and receives.
- **Device types** inferred from protocol usage and metadata.

{: .new }
> The longer you leave a capture running, the more detail ShowShark can gather for the Host Table. Host Table data persists when you stop and restart captures, so you can capture in stages and the table remains intact.

## Main Host Table Window

The _Tools > ShowShark Tools > Host Table_ option opens a dedicated window that shows all discovered hosts and their characteristics.

{: .tip }
> If you don't have a capture to hand, open the example capture file from the ShowShark download zip in Wireshark to see the Host Table in action.

{: .note }
> User Level (Essential/Advanced) currently does not change Host Table window columns.

### Main Window Controls

The Host Table window includes a highlight field plus bottom-row controls for view management.

Available controls:

- **Refresh Table**
- **ID**
- **Hostname**
- **MAC Addresses**
- **Manufacturers**
- **IP Addresses**
- **Addl Hostnames**
- **Addl Properties**
- **Protocols**
- **Export CSV**
- **Clear Discovered Hosts**

The **Highlight** field can be used with these controls to focus the table on what you need to inspect.

Buttons such as **ID**, **Hostname**, **Manufacturers**, and **Protocols** are used to toggle which columns are visible.

{: .note }
> Export currently supports CSV.

![Host Table window placeholder](/assets/images/placeholders/host-table-placeholder.svg)

{: .warning }
> The table currently doesn't display well on small screens given all the parameters. The window can be stretched to view all columns. The next version will not use the display level settings, but will include filter buttons to show and hide columns for easier viewing.

## Packet Details Tables

In the [packet details pane](https://www.wireshark.org/docs/wsug_html_chunked/ChUsePacketListPaneSection.html) (bottom left of the packet windows), depending on your [Options](/docs/menus/#4-options) settings, you'll see up to two additional tables:

- **Host Properties Table** - Shows detailed information about the source or destination host.
- **Host Protocols Table** - Lists all protocols the host has been observed using.

These tables appear for each packet, providing quick access to host information without opening the main Host Table window.

<p align="center">
  <img src="/assets/images/host_table/hosttable_packet_details.png" alt="Host table packet details view"
       style="width: 75%; border: 1px solid #ddd;">
</p>

### When To Use Packet Details Tables

- You are already examining a specific packet.
- You want quick source/destination host context.
- You do not need full-window filtering or export.

### Host Properties Table

The Host Properties Table displays detailed information about each discovered host. If some of the fields below are missing, it just means that ShowShark hasn't yet discovered that information about the host.

| Field | Description |
| ----- | ----------- |
| **ID** | Unique identifier for the host. |
| **Hostname** | Device hostname. |
| **IP Address** | Current IP address. |
| **MAC Address** | Hardware address (shown at Advanced level). |
| **Manufacturer** | Device manufacturer (derived from protocols, MAC OUI, or other sources). |
| **MAC Manufacturer** | Manufacturer from MAC OUI lookup (shown at Advanced level). |
| **Derived Manufacturer** | Manufacturer derived from entertainment protocols (shown at Advanced level). |
| **Assumed Manufacturer** | Manufacturer assumed from packet data and metadata (shown at Advanced level). |
| **Device Type** | Type of device (e.g., lighting console, fixture). |
| **Additional Hostnames** | Other hostnames associated with the device. |

### Host Protocols Table

This table shows which protocols each host is using, with a cross (✕) in each relevant protocol column - for example, a device sending sACN packets will have a cross in the sACN column.

The protocols table will only show protocol columns for protocols that at least one host has been seen using.

## Troubleshooting Playbooks

### Device Missing from Host Table

1. Confirm packets are arriving for that device.
2. Let capture run longer to allow host discovery to populate metadata.
3. Check packet details tables on traffic from that device.
4. Verify any Host Table filters are not hiding the device.

### Manufacturer or Device Type Not Filled Yet

1. Keep capture running to gather more protocol metadata.
2. Review additional packets from that host.
3. Re-check Host Table after more traffic has been observed.

### Export Host Inventory for Reporting

1. Open main Host Table window.
2. Apply any filters needed for scope.
3. Export to CSV.
4. Attach CSV to troubleshooting notes or handover docs.

## Screenshot Placeholders

### Main Host Table Overview

![Main host table placeholder](/assets/images/placeholders/host-table-placeholder.svg)

### Host Table Filters and Export

![Host table controls placeholder](/assets/images/placeholders/host-table-placeholder.svg)

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/docs/watchers/">← Watchers</a></div>
  <div style="text-align: right;"><a href="/docs/filter-builder/">Filter Builder →</a></div>
</div>
{:/}
