---
layout: default
title: Capturing
nav_order: 4
has_children: true
nav_fold: false
permalink: /documentation/capturing/
---

<h1 align="center">Capturing Network Traffic</h1>

---
Wireshark captures network packets as they travel across your network interface. ShowShark then analyzes this captured data to provide entertainment network-specific insights.
The more packets you capture, the more complete ShowShark's analysis becomes, but on the flip side, larger captures require more processing time.

## Very Quick Capture Steps

1. **Choose the Interface** - Open Wireshark and on the main screen, select the network interface where your entertainment traffic is flowing (Wi-Fi, Ethernet, etc.)
2. **Let it Run** - Allow captures to run for a representative time period (usually a minute will do) to build a complete picture of network activity.
3. **Stop the Capture** - Click the red square button in the toolbar to stop capturing packets.
4. **Save Important Captures** - Use _File > Save As_ to keep capture files for later analysis
5. **Use Display Filters** - ShowShark's [Filter Builder](/documentation/filter-builder/) helps you focus on specific traffic types.
6. **Open Host Tables** - View discovered devices and their properties via _Tools > ShowShark > Host Table_. See the [Host Table](/documentation/host-table/) documentation for more details.

## Learning to Capture

For detailed information on capturing network traffic with Wireshark, refer to the official Wireshark documentation:

[Wireshark User's Guide - Capturing Live Network Data](https://www.wireshark.org/docs/wsug_html_chunked/ChCapCapturingSection.html)

---

<div style="display: flex; justify-content: space-between; align-items: center;">
  <a href="/documentation/guide/filter-builder/">< Filter Builder</a>
  <span style="visibility: hidden;">></span>
</div>
