---
layout: default
title: About ShowShark
nav_order: 1
---

<h1 align="center">Welcome to ShowShark</h1>

---

ShowShark is a Wireshark plugin that makes entertainment networks easier to visualise and understand.

ShowShark adds more information about entertainment protocols to Wireshark, making traffic easier to read and showing useful details such as DMX universe and OSC values.

As traffic passes through Wireshark, ShowShark gathers information about devices, including hostnames, manufacturers and device types. It also shows which protocols devices are using and which other devices they are communicating with.

## Features

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference about-reference">
  <tbody>
    <tr><td class="menu-name"><strong>Device Discovery</strong></td><td>ShowShark identifies entertainment devices and collects details such as their hostnames, manufacturers, and device types.</td></tr>
    <tr><td class="menu-name"><strong>Host Table</strong></td><td>View discovered devices, their properties, and the protocols they support.</td></tr>
    <tr><td class="menu-name"><strong>Protocol Details</strong></td><td>See entertainment-specific information like universe numbers and priorities in the packet list columns.</td></tr>
    <tr><td class="menu-name"><strong>Colour-Coded Display</strong></td><td>Colour coding helps you quickly distinguish different types of traffic.</td></tr>
    <tr><td class="menu-name"><strong>Filter Builder</strong></td><td>Build complex Wireshark display filters without memorising syntax using the built-in filter builder.</td></tr>
    <tr><td class="menu-name"><strong>Watchers</strong></td><td>Track specific DMX and OSC values over time in dedicated watcher columns.</td></tr>
    <tr><td class="menu-name"><strong><a href="/docs/showsquid/">ShowSquid App</a></strong></td><td>Prompts devices to communicate, joins selected multicast groups, and listens for traffic, giving ShowShark more information to analyse.</td></tr>
  </tbody>
</table>
</div>
{:/}

## Supported Protocols

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference about-reference">
  <tbody>
    <tr><td class="menu-name"><strong>sACN (E1.31)</strong></td><td>DMX over IP; ShowShark displays details such as universes, priorities, and DMX values.</td></tr>
    <tr><td class="menu-name"><strong>Art-Net</strong></td><td>DMX and device discovery over IP; ShowShark displays node details, universes, and DMX values.</td></tr>
    <tr><td class="menu-name"><strong>IGMP</strong></td><td>Multicast subscriptions; ShowShark identifies the querier and clearly labels subscription traffic with entertainment details such as sACN universe numbers.</td></tr>
    <tr><td class="menu-name"><strong>mDNS</strong></td><td>Local host and service discovery; ShowShark identifies device names and advertised services.</td></tr>
    <tr><td class="menu-name"><strong>OSC</strong></td><td>Open Sound Control; ShowShark displays message addresses and values and lets you track them with Watchers.</td></tr>
    <tr><td class="menu-name"><strong>SLP</strong></td><td>Service Location Protocol; ShowShark identifies advertised services and uses them to show which protocols devices support.</td></tr>
  </tbody>
</table>
</div>
{:/}

<div style="text-align: center; margin-top: 2rem;">
  <a href="/download/" class="button" style="background-color: #1d71c4; color: white; padding: 15px 30px; border-radius: 25px; text-decoration: none; font-weight: bold; display: inline-block;">Get Started</a>
</div>
