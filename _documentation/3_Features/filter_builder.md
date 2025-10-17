---
layout: default
title: Filter Builder
parent: Features
nav_order: 3
---

<h1 align="center">Filter Builder</h1>

---

ShowShark includes a filter builder under **Tools > ShowShark** to help create Wireshark display filters without needing to know the full filter syntax.

The filter builder always works with the **current display filter**. When you select options, ShowShark updates the filter text in the display filter bar. The filter is **not automatically applied** until you apply it in Wireshark, and it can always be edited manually.

### How it works

The filter builder adds conditions to the existing display filter. New conditions are combined using ***and***. Multiple selections within the same category are grouped using ***or***. The resulting filter is written to the display filter bar for review or further editing.

### Manufacturer

The **Manufacturer** option opens a list of manufacturers that can be added to the display filter. Selecting a manufacturer, when none is currently selected, adds it to the current filter using ***and***. If multiple manufacturers are selected, they are grouped together using ***or***.

The filter matches either the source or destination host manufacturer. Manufacturers can be removed by manually editing the display filter bar.

### Protocol

The **Protocol** option opens a list of protocols that can be added to the display filter. Selecting a protocol, when none is currently selected, adds it to the current filter using ***and***. If multiple protocols are selected, they are grouped together using ***or***.

Some protocols, such as DMX, include sub-menus that allow more specific protocol variants to be selected. Protocols can be removed by manually editing the display filter bar.

### Host Filters

The **Host Filters** option opens a window for building filters based on source and destination hosts.

Within the same field, multiple values are combined using ***or***. Between different fields, filters are combined using ***and***.

**Host names** use *contains* matching and support comma-separated values.  
**IP addresses** support comma-separated values and ranges (for example `10.101.10.6–10.101.10.9`).  
**MAC addresses** support *contains* matching, comma-separated values, and partial MAC fragments.

The same rules apply to both source and destination hosts.

When applied, the generated filter is written to the display filter bar and can be edited manually.