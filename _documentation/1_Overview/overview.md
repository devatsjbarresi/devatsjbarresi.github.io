---
layout: default
title: Overview
nav_order: 1
has_children: true
permalink: /documentation/overview/
---

<h1 align="center">Overview</h1>

---
ShowShark is a Wireshark plugin for entertainment networks that makes traffic more visual and easier to understand than Wireshark alone.

ShowShark learns about entertainment devices by observing the information they send over the network. It then uses this information to help you build a clearer picture of what is happening and who is talking to whom.

It runs entirely inside Wireshark with minimal setup and is read-only, meaning it never modifies packets or affects your network in any way.

ShowShark works with both live captures and saved capture files, requires no special hardware for most traffic types, and processes all data locally.

## Features

- **Entertainment Host Discovery** - ShowShark tracks entertainment devices on your network, detecting information such as hostnames, manufacturer, device type and discovery times based on information from their packets.
- **Host Tables** - View comprehensive tables of all discovered devices with their properties and supported protocols.
- **Enhanced Protocol Details** - See entertainment-specific information like universe numbers and priorities in the packet list columns.
- **Colour-Coded Display** - Visual colour rules to help you quickly distinguish different types of traffic.
- **Filter Builder** - Build complex Wireshark display filters without memorizing syntax using the built-in filter builder.

## Currently Supported Protocols

- **sACN (E1.31)** - Streaming ACN for DMX over IP
- **Art-Net** - Artistic Licence's lighting protocol  
- **IGMP** - Multicast group management
- **SLP** - Service Location Protocol for device discovery

## What ShowShark Does Not Do

- **Does not modify network traffic** - ShowShark is read-only; it does not interfere with your network, nor does it generate traffic.
- **Does not require special hardware to get started** - The most common protocols do not require any additional hardware.
- **Does not send data externally** - All processing happens locally.

**Get started**

- [Download](/download/) – Get the latest version.
- [Installation](/documentation/installation/) – Step-by-step setup.
