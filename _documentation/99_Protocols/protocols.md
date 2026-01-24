<!-- ---
layout: default
title: Protocols
nav_order: 4
has_children: true
--- -->

# Protocols

ShowShark recognises and organises common entertainment‑networking protocols.  
This section explains how they appear in Wireshark and how to navigate between them inside the dissector.

---

## Viewing Protocol Layers

Each recognised packet adds protocol labels in the **Protocol** and **Info** columns.  
For example:  
- **sACN (Universe 1, Pri 100)**  
- **Art‑Net (OpOutput/DMX)**  
- **IGMP (Subscribe 239.255.0.1)**  

These layers are grouped in Wireshark’s packet tree under **ACN**, **Lighting**, or **Discovery**.

---

## Combined Traffic

When multiple protocols coexist (for example sACN + Art‑Net), ShowShark correlates them by device manufacturer, MAC, and IP.  
This keeps related frames linked and lets you trace one fixture’s behaviour across protocols.

---

## Expanding Detail

Each family has its own sub‑page for deeper options and examples:  
- [Lighting Protocols](/documentation/Protocols/lighting/) – DMX transport (sACN, Art‑Net)  
- [Discovery Protocols](/protocols/discovery/) – mDNS, SLP, E1.33  
- [General Protocols](/protocols/discovery/) – OSC, RDMnet, other control layers  

---

## Typical Use

Use this section when you want to:  
- Identify what protocols are active in a capture.  
- Confirm correct universe, priority, and multicast behaviour.  
- Jump to a specific family page for decoding tips.