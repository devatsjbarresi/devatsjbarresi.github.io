---
layout: default
title: About ShowShark
nav_order: 1
---

<h1 align="center">Welcome to ShowShark</h1>

---

ShowShark is a Wireshark plugin designed for entertainment technicians of all experience levels.

It makes network traffic more visual and easier to understand by discovering entertainment devices and displaying their information in a clear, accessible way.

Whether you're an experienced professional or just starting out, ShowShark provides practical tools for fault-finding and showing what's happening between devices on your network.

### Features

- **Entertainment Host Discovery** - ShowShark tracks entertainment devices on your network, extracting information such as hostnames, manufacturer and device type.
- **Host Tables** - View tables of all discovered devices with their properties and supported protocols.
- **Detailed Protocol Information** - See entertainment-specific information like universe numbers and priorities in the packet list columns.
- **Colour-Coded Display** - Colour coding will help you quickly distinguish different types of traffic.
- **Filter Builder** - Build complex Wireshark display filters without memorising syntax using the built-in filter builder.

### What ShowShark Does Not Do

- **Modify network traffic** - ShowShark is read-only; it does not interfere with your network, nor does it generate traffic.
- **Require special hardware to get started** - The most common protocols do not require any additional hardware.
- **Send data externally** - All processing happens locally on your computer.

### Supported Protocols

- **sACN (E1.31)** - Streaming ACN for DMX over IP (Internet Protocol).
- **Art-Net** - Artistic Licence's lighting protocol.
- **IGMP** - Multicast group management for things like sACN and device discovery.
- **SLP** - Service Location Protocol for working out which devices support which protocols.

<div style="text-align: center; margin-top: 2rem;">
  <a href="/download/" class="button" style="background-color: #1679a7; color: white; padding: 15px 30px; border-radius: 25px; text-decoration: none; font-weight: bold; display: inline-block;">Get Started</a>
</div>