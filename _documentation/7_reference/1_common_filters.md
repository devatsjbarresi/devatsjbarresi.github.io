---
layout: default
title: Common Filters
parent: Reference
nav_order: 1
permalink: /docs/common-filters/
---

<h1 align="center">Common Filters</h1>

---

Use these as quick copy-paste starting points in Wireshark's display filter bar. Many can also be created using ShowShark's [Filter Builder](/docs/filter-builder/).

## Protocol Filters

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-name"><code>show.acn</code></td><td>ACN packets, including sACN.</td></tr>
    <tr><td class="menu-name"><code>show.sacn</code></td><td>Just sACN packets.</td></tr>
    <tr><td class="menu-name"><code>show.artnet</code></td><td>Art-Net packets.</td></tr>
    <tr><td class="menu-name"><code>show.dmx</code></td><td>All types of DMX packets.</td></tr>
    <tr><td class="menu-name"><code>show.osc</code></td><td>OSC packets.</td></tr>
    <tr><td class="menu-name"><code>show.igmp</code></td><td>IGMP packets.</td></tr>
  </tbody>
</table>
</div>
{:/}

## Host and Manufacturer Filters

The Filter Builder can create [host filters](/docs/filter-builder/#host-filters) and [manufacturer filters](/docs/filter-builder/#manufacturer-filters).

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-name"><code>show.source.name contains "console"</code></td><td>Packets sent by hosts with <code>console</code> in their hostname.</td></tr>
    <tr><td class="menu-name"><code>show.dest.name contains "console"</code></td><td>Packets sent to hosts with <code>console</code> in their hostname.</td></tr>
    <tr><td class="menu-name"><code>show.source.manufacturer.etc</code></td><td>Packets sent by ETC devices.</td></tr>
    <tr><td class="menu-name"><code>show.dest.manufacturer.hp</code></td><td>Packets sent to HP devices.</td></tr>
    <tr><td class="menu-name"><code>show.manufacturer.ma_lighting</code></td><td>Packets sent from or to MA Lighting devices.</td></tr>
  </tbody>
</table>
</div>
{:/}

Packets sent by Carallon devices or sent to MA Lighting devices:

{::nomarkdown}
<div class="compact-filter-example"><code>show.source.manufacturer.carallon or show.dest.manufacturer.ma_lighting</code></div>
{:/}

## IP Address Filters

The [Host Filter window](/docs/filter-builder/#host-filters) creates these filters from the addresses you enter.

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-name"><code>show.source.ip == 10.5.4.1</code></td><td>Packets sent from this IP address.</td></tr>
    <tr><td class="menu-name"><code>show.dest.ip == 10.5.4.1</code></td><td>Packets sent to this IP address.</td></tr>
    <tr><td class="menu-name"><code>show.ip == 10.5.4.1</code></td><td>Packets sent from or to this IP address.</td></tr>
  </tbody>
</table>
</div>
{:/}

## DMX Filters

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-name"><code>show.sacn.dmx</code></td><td>sACN DMX packets.</td></tr>
    <tr><td class="menu-name"><code>show.artnet.dmx</code></td><td>Art-Net DMX packets.</td></tr>
    <tr><td class="menu-name"><code>show.dmx.universe == 1</code></td><td>DMX packets for universe 1.</td></tr>
    <tr><td class="menu-name"><code>show.sacn.universe == 1</code></td><td>sACN packets for universe 1.</td></tr>
    <tr><td class="menu-name"><code>show.artnet.universe == 0</code></td><td>Art-Net packets for universe 0.</td></tr>
  </tbody>
</table>
</div>
{:/}

## OSC Filters

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-name"><code>show.osc.address</code></td><td>Packets containing an OSC address.</td></tr>
    <tr><td class="menu-name"><code>show.osc.address contains "hello"</code></td><td>OSC addresses containing <code>hello</code>.</td></tr>
    <tr><td class="menu-name"><code>show.osc.value.int &gt; 1</code></td><td>OSC integer values greater than 1.</td></tr>
    <tr><td class="menu-name"><code>show.osc.value.bool.1 == true</code></td><td>Packets where the first OSC Boolean value is true.</td></tr>
  </tbody>
</table>
</div>
{:/}

## Combining Filters

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-name"><code>show.sacn and show.source.name contains "console"</code></td><td>sACN packets sent by hosts with <code>console</code> in their hostname.</td></tr>
    <tr><td class="menu-name"><code>show.artnet and show.ip == 10.101.10.50</code></td><td>Art-Net packets sent from or to one IP address.</td></tr>
    <tr><td class="menu-name"><code>show.sacn and show.sacn.universe == 1</code></td><td>sACN packets for universe 1.</td></tr>
    <tr><td class="menu-name"><code>show.osc and show.ip == 10.101.10.50</code></td><td>OSC packets sent from or to one IP address.</td></tr>
  </tbody>
</table>
</div>
{:/}

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/docs/reference/">← Reference</a></div>
  <div style="text-align: right;"></div>
</div>
{:/}
