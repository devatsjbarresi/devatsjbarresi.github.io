---
layout: default
title: Capturing
parent: Guide
nav_order: 5
permalink: /docs/capturing/
---

<h1 align="center">Capturing Network Traffic</h1>

---
Wireshark captures network packets as they pass through your selected network interface. ShowShark analyses the captured data for entertainment-specific information. Capturing more packets gives ShowShark more to analyse, but larger captures take longer to process.

{: .note }
> The ShowShark download includes an example capture file you can open in Wireshark if you do not have live network traffic to capture.

## Quick Capture Steps

1. **Choose the interface:** Select the network interface carrying your entertainment traffic, such as Ethernet or Wi-Fi. See [Capture Interfaces](https://www.wireshark.org/docs/wsug_html_chunked/ChCapInterfaceSection.html).
2. **Start the capture:** Start capturing and let it run long enough to collect a useful sample. See the [Wireshark toolbar](https://www.wireshark.org/docs/wsug_html_chunked/ChUseMainToolbarSection.html).
3. **Stop the capture:** Stop capturing when you have the traffic you need.
4. **Open the Host Table:** Go to _Tools > 1 ShowShark Tools > 1 Host Table_ to view discovered devices. See [Host Table](/docs/host-table/).
5. **Explore the traffic:** Browse the [packet list](https://www.wireshark.org/docs/wsug_html_chunked/ChUsePacketListPaneSection.html) and [packet details](https://www.wireshark.org/docs/wsug_html_chunked/ChUsePacketDetailsPaneSection.html). Use display filters or the ShowShark [Filter Builder](/docs/filter-builder/) to focus on specific traffic.
6. **Save the capture:** Go to _File > Save As_ to keep it for later analysis.

## What You Will See

Without special switch configuration, you can still capture useful traffic, including:

- **Broadcast traffic** sent to everyone, such as discovery packets and broadcast Art-Net.
- **Multicast traffic** that your capture machine has joined, such as sACN.
- **Packets to or from your own machine**.

Protocols such as sACN and PSN are predominantly multicast, so your capture machine may need to join the relevant multicast groups before those streams are forwarded to it.

[ShowSquid](/docs/showsquid/) prompts devices to communicate and joins selected multicast groups, giving Wireshark more traffic to capture and ShowShark more information to analyse.

## What You Might Not See

Some traffic will not appear in a normal capture on a switched network:

- **Unicast traffic between two other devices**: the switch sends packets directly between those devices, so they are not forwarded to your machine.
- **Multicast streams not joined by your capture machine**.
- **Traffic on other VLANs or subnets** that never reaches your capture port.

{: .note }
> If you need to see traffic between two other devices, or traffic that would otherwise be filtered before reaching your machine, configure your switch to copy that traffic to your capture port. This is usually called port mirroring or SPAN. See your switch manufacturer's documentation for setup instructions.

{: .note }
> You can also use a TAP device between devices. This can be simpler, but it requires extra hardware and may mean altering your network setup.

## Explore ShowShark's Features

See the [Features](/docs/features/) section to find out more about the ShowShark tools available to help you inspect your network.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
	<div><a href="/docs/columns/">← Configure Columns</a></div>
	<div style="text-align: right;"><a href="/docs/features/">Features →</a></div>
</div>
{:/}
