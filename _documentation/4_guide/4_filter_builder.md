---
layout: default
title: Filter Builder
parent: Features
nav_order: 3
permalink: /docs/filter-builder/
---

<h1 align="center">Filter Builder</h1>

---

<style>
  .main-content img[src^="/assets/images/filter_builder/"] {
    display: block;
    margin: 2rem auto;
  }
</style>

[Wireshark display filters](https://www.wireshark.org/docs/wsug_html_chunked/ChWorkBuildDisplayFilterSection.html) allow you to show only the packets you want to see and hide the rest, but building them can be cumbersome and requires you to remember the filter syntax.

ShowShark’s Filter Builder allows you to create custom filters for hosts, manufacturers, protocols and [Watchers](/docs/watchers/) without requiring you to write the syntax by hand.

## Getting Started

1. Start a new capture, open an existing capture, or use the example capture included with the ShowShark download.
2. Open the Filter Builder from _Tools > 2 ShowShark Filter Builder_.

<img src="/assets/images/filter_builder/filter_builder_menu.png" alt="ShowShark Filter Builder menu" style="width: 55%;">

1. **Clear Filter:** Removes the current display filter.
2. **Host Filter Window:** Opens the [Host Filter Window](#host-filters) for building filters using hostnames, IP addresses and MAC addresses.
3. **Manufacturer:** Adds a filter for a selected [manufacturer](#manufacturer-filters).
4. **Protocol:** Adds a filter for a selected [protocol](#protocol-filters).
5. **Watcher:** Adds a filter for configured [Watchers](/docs/watchers/).

### Combining Filters

- Filters from different categories are combined using ***and***.
- Multiple selections within the same category are combined using ***or***.

{: .note }
> Filters may take longer to apply to large captures.

---

## Host Filters

Host Filter Window builds filters using source and destination host information.

Build host filters using:

<div class="menu-reference-container">
<table class="menu-reference">
  <tbody>
    <tr><td class="menu-name"><strong>Hostnames</strong></td><td>Device names detected by ShowShark.</td></tr>
    <tr><td class="menu-name"><strong>IP addresses</strong></td><td>Individual addresses, ranges or comma-separated lists.</td></tr>
    <tr><td class="menu-name"><strong>MAC addresses</strong></td><td>Full or partial addresses.</td></tr>
  </tbody>
</table>
</div>

You can specify criteria for **source hosts**, **destination hosts**, or both:

- Within the same field, multiple values are combined using ***or***
- Between different fields (source vs. destination), filters are combined using ***and***

### Hostname Filtering

The filter matches any hostname containing the text you enter. Matching is case-sensitive, and you can separate multiple entries with commas.

<p align="center">
  <img src="/assets/images/filter_builder/builder_host_eos_response.png" alt="EOS Host Filter Response"
       style="width: 75%;">
</p>

### IP Address Filtering

You can filter by a single IP address, a range or multiple addresses.

**Single IP address:**

<p align="center">
  <img src="/assets/images/filter_builder/builder_host_single_ip.png" alt="Single IP Address Filter"
       style="width: 75%;">
</p>

**IP address range:**

Enter the first and last address in the range, for example `10.101.10.6–10.101.10.9`.

<p align="center">
  <img src="/assets/images/filter_builder/builder_host_range_ip.png" alt="IP Range Filter"
       style="width: 75%;">
</p>

**Multiple IP addresses:**

Combine individual addresses and ranges, separated by commas.

<p align="center">
  <img src="/assets/images/filter_builder/builder_host_complex_ip.png" alt="Complex IP Filter"
       style="width: 75%;">
</p>

### MAC Address Filtering

Enter a full or partial MAC address. You can separate multiple entries with commas.

<p align="center">
  <img src="/assets/images/filter_builder/builder_host_mac.png" alt="MAC Address Filter"
       style="width: 75%;">
</p>

### Combining Host Filters

You can combine hostname, IP address and MAC address filters across the source and destination fields.

<p align="center">
  <img src="/assets/images/filter_builder/builder_host_big_filter.png" alt="Complex Host Filter Example"
       style="width: 90%;">
</p>

---

## Manufacturer Filters

Manufacturer filters show traffic to or from devices that ShowShark has identified as the selected manufacturer.

<p align="center">
  <img src="/assets/images/filter_builder/builder_menu_manu.png" alt="Opening Manufacturer Filter"
       style="width: 75%;">
</p>

Selected manufacturers appear in Wireshark’s display filter bar.

<p align="center">
  <img src="/assets/images/filter_builder/builder_filter_manu.png" alt="Manufacturer Filter Selection"    
       style="width: 75%;">
</p>

{: .warning }
> Manually editing manufacturer filters in the display filter bar may not update the Filter Builder correctly. See [Manual Editing](#manual-editing).

---

## Protocol Filters

The Protocol menu includes entertainment and general network protocols, with submenus for more specific options such as DMX and OSC.

<p align="center">
  <img src="/assets/images/filter_builder/builder_menu_protocols.png" alt="Protocol Filter Menu"
       style="width: 75%;">
</p>

{: .warning }
> Manually editing protocol filters in the display filter bar may not update the Filter Builder correctly. See [Manual Editing](#manual-editing).

### sACN Protocol Filter

<p align="center">
  <img src="/assets/images/filter_builder/builder_menu_sacn.png" alt="sACN Protocol Filter"
       style="width: 75%;">
</p>

### Universe Filter

<p align="center">
  <img src="/assets/images/filter_builder/builder_filter_universes.png" alt="Universe Filter Builder"
       style="width: 75%;">
</p>

---

## Manual Editing

You can use the syntax that Filter Builder creates as a starting point and edit it directly when you need more control over the filter logic or need to work around a known issue.

Click in the display filter bar to edit the filter. You can remove conditions, change `and` to `or`, or edit IP ranges, port numbers and hostnames. Press Enter to apply the filter. Wireshark highlights invalid filters in red.

To clear the display filter bar, click the **X** on the right, or delete all the text and press Enter.

See [Common Filters](/docs/common-filters/) for more filter examples.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/docs/watchers/">← Watchers</a></div>
  <div style="text-align: right;"><a href="/docs/showsquid/">ShowSquid →</a></div>
</div>
{:/}
