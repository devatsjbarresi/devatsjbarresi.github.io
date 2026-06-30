---
layout: default
title: Analysing
nav_order: 7
has_children: true
nav_fold: false
permalink: /docs/analysing/
---

<h1 align="center">Analysing</h1>

---

## What is Analysing?

Analysing is the process of looking at captured network traffic to understand what’s happening on the network. This can include inspecting packet contents and spotting what devices and protocols are active.

{: .note }
> Future documentation will include more detailed ShowShark and entertainment-specific analysis guidance.

{: .note }
> A companion app to ShowShark called **ShowSquid** is currently in development. The goal is to help prompt devices to “talk” to your Wireshark machine, so you have more to work with in ShowShark. See [ShowSquid](/docs/showsquid/).

## What You Will See

Without any special configuration, you can still see a lot of useful traffic, including:

- **Broadcast traffic** (sent to everyone) such as discovery packets and broadcast Art-Net.
- **Multicast traffic** that your capture machine has joined (e.g. sACN).
- **Any packets to/from your own machine**.

Protocols such as sACN and PSN are predominantly multicast, so your machine will need to join the relevant multicast groups before the stream will be forwarded to your capture machine.
An easy way to do this is with [sACNView](https://sacnview.org/): open it, browse for the universes you're interested in, and you should then see the sACN traffic arriving in Wireshark.

## What You Might Not See

Some traffic simply won’t show up from a normal capture on a switched network:

- **Unicast traffic between two other devices**: The switch sends packets directly between these two devices and it therefore won’t be seen by your machine.
- **Multicast streams (e.g. sACN) not joined by your capture machine**.
- **Traffic on other VLANs / subnets** that never reaches your capture port.

{: .note }
> If you need to see traffic between two other devices, or traffic that would otherwise be filtered before reaching your machine, you’ll need to configure your switch to forward (copy) that traffic to a specific port on your switch. This is called port mirroring or SPAN (Switch Port Analyser). See your switch manufacturer’s documentation for instructions on how to set this up.

{: .note }
> You can also use a TAP device that sits between the devices. This can be simpler, but it requires extra hardware and may mean altering your network setup.

## Explore ShowShark’s Features
{: .tip }
> If you don't have a capture to hand, open the example capture file from the ShowShark download zip in Wireshark to explore the features.
See the [Features](/docs/features/) section of the documentation to find out more about the ShowShark tools available to help you analyse your network.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
	<div><a href="/docs/capturing/">← Capturing</a></div>
	<div style="text-align: right;"><a href="/docs/features/">Features →</a></div>
</div>
{:/}

