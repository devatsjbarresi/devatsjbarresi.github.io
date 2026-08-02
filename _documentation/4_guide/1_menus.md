---
layout: default
title: Menus
parent: Guide
nav_order: 3
nav_fold: false
permalink: /docs/menus/
---

<h1 align="center">Menus</h1>

---

ShowShark adds five menu groups under Wireshark's _Tools_ menu.

## Menu Structure

1. **[Tools](#1-tools)**
2. **[Filter Builder](#2-filter-builder)**
3. **[Displays](#3-displays)**
4. **[Options](#4-options)**
5. **[ShowShark](#5-showshark)**

{: .note }
> Some changes require Wireshark to reload packets. ShowShark will warn you when this is needed.

## 1. Tools

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-number">1.</td><td class="menu-name"><strong>Host Table</strong></td><td>Opens the <a href="/docs/host-table/">Host Table</a> window.</td></tr>
    <tr><td class="menu-number">2.</td><td class="menu-name"><strong>Watchers</strong></td><td>Opens the <a href="/docs/watchers/">Watchers</a> editor.</td></tr>
  </tbody>
</table>
</div>
{:/}

## 2. Filter Builder

These options use the [Filter Builder](/docs/filter-builder/) to create Wireshark display filters without typing the full filter syntax manually.

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-number">1.</td><td class="menu-name"><strong>Clear Filter</strong></td><td>Clears the current display filter.</td></tr>
    <tr><td class="menu-number">2.</td><td class="menu-name"><strong>Host Filter Window</strong></td><td>Opens the Host Filter editor to build filters using hostnames, IP addresses, or MAC addresses.</td></tr>
    <tr><td class="menu-number">3.</td><td class="menu-name"><strong>Manufacturer</strong></td><td>Adds a filter for the selected device manufacturer.</td></tr>
    <tr><td class="menu-number">4.</td><td class="menu-name"><strong>Protocol</strong></td><td>Options for adding protocol filters.</td></tr>
    <tr><td class="menu-number">5.</td><td class="menu-name"><strong>Watcher</strong></td><td>Adds a filter for configured <a href="/docs/watchers/">Watchers</a>.</td></tr>
  </tbody>
</table>
</div>
{:/}

## 3. Displays

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-number">1.</td><td class="menu-name"><strong>Colour Filters</strong></td><td></td></tr>
    <tr class="menu-subitem"><td class="menu-number">1.</td><td class="menu-name"><strong>Colour Filter 1</strong></td><td>Applies colour filter set 1.</td></tr>
    <tr class="menu-subitem"><td class="menu-number">2.</td><td class="menu-name"><strong>Colour Filter 2</strong></td><td>Applies colour filter set 2.</td></tr>
    <tr class="menu-subitem"><td class="menu-number">3.</td><td class="menu-name"><strong>Colour Filter 3</strong></td><td>Applies colour filter set 3.</td></tr>
    <tr><td class="menu-number">2.</td><td class="menu-name"><strong>Column Layout</strong></td><td></td></tr>
    <tr class="menu-subitem"><td class="menu-number">1.</td><td class="menu-name"><strong>Lighting</strong></td><td>Applies the ShowShark lighting <a href="/docs/columns/">column layout</a>.</td></tr>
  </tbody>
</table>
</div>
{:/}

## 4. Options

These options control ShowShark's behaviour and display preferences. They can also be edited in the ShowShark Options window.

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-number">0.</td><td class="menu-name"><strong>Options Window</strong></td><td>Opens the ShowShark Options window.</td></tr>
    <tr><td class="menu-number">1.</td><td class="menu-name"><strong>User Level</strong></td><td>Selects Essential or Advanced mode.</td></tr>
    <tr><td class="menu-number">2.</td><td class="menu-name"><strong>Hosts</strong></td><td>Selects whether ShowShark displays only hosts identified as entertainment devices or all hosts on the network.</td></tr>
    <tr><td class="menu-number">3.</td><td class="menu-name"><strong>Sort By</strong></td><td>Selects how hosts are sorted throughout ShowShark: IP address, hostname, or MAC address.</td></tr>
    <tr><td class="menu-number">4.</td><td class="menu-name"><strong>DMX Display</strong></td><td>Selects how DMX values are displayed throughout ShowShark: percent, decimal, hexadecimal, or not shown.</td></tr>
    <tr><td class="menu-number">5.</td><td class="menu-name"><strong>Attach Host Protocol Table</strong></td><td>Shows or hides the host protocol table in each packet dissection.</td></tr>
    <tr><td class="menu-number">6.</td><td class="menu-name"><strong>Attach Host Property Table</strong></td><td>Shows or hides the host property table in each packet dissection.</td></tr>
    <tr><td class="menu-number">7.</td><td class="menu-name"><strong>Show About Dialog on Startup</strong></td><td>Selects whether the About dialog appears when ShowShark starts.</td></tr>
  </tbody>
</table>
</div>
{:/}

## 5. ShowShark

{::nomarkdown}
<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-number">1.</td><td class="menu-name"><strong>Reload Wireshark Plugins</strong></td><td>Reloads Lua plugins in Wireshark.</td></tr>
    <tr><td class="menu-number">2.</td><td class="menu-name"><strong>Visit ShowShark Website</strong></td><td>Opens the <a href="/">ShowShark website</a>.</td></tr>
    <tr><td class="menu-number">3.</td><td class="menu-name"><strong>About ShowShark</strong></td><td>Opens the About dialog.</td></tr>
    <tr><td class="menu-number">4.</td><td class="menu-name"><strong>Check for Updates</strong></td><td>Checks whether a newer version of ShowShark is available.</td></tr>
  </tbody>
</table>
</div>
{:/}

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/docs/configuration-profile/">← Configuration Profile</a></div>
  <div style="text-align: right;"><a href="/docs/columns/">Configure Columns →</a></div>
</div>
{:/}
