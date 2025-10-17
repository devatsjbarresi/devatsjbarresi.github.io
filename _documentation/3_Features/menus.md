---
layout: default
title: Menus
parent: Features
nav_order: 1
nav_fold: false
---

<h1 align="center">Menus</h1>

---
ShowShark adds a menu under **Tools > ShowShark** in Wireshark, making it easy to access plugin features and settings.

## Display Level

ShowShark offers two display levels:

### Essential

- Simplified view with key protocol details and host information.
- Host Protocols and Host Properties are hidden by default for a cleaner interface.
- The Host Table can still be opened via Tools > ShowShark > Host Table.

### Advanced

- Adds more protocol fields and details to the packet list and window.
- Host Protocols and Host Properties are shown by default.
- The Host Table includes extra columns and counters.
- You can switch back to Essential at any time.

## Host Table

The Host Table displays all discovered devices and their properties. See the [Host Table](/documentation/3_Features/host_table/) page for detailed information.

## Options

### Display Level

- Set the default display level to Essential or Advanced.
- Change the display level from the main window or via Tools > ShowShark > Display level.
- The **Apply** button applies changes without closing the dialog.

### Attach Host Property Table

- Controls whether the Host Properties table appears in the packet details by default.
- Independent of display level.
- When disabled, the Host Properties table is hidden, but host information is still available via the Host Table.
- The **Apply** button updates the view without closing the dialog.

### Attach Host Protocol Table

- Controls whether the Host Protocols table appears in the packet details by default.
- Independent of display level.
- When disabled, the table is hidden, but protocol information is still available via the Host Table.
- The **Apply** button updates the view without closing the dialog.

### Open About Dialog at Startup

- Toggles whether the About window opens when Wireshark starts or when the plugin is reloaded.

## Filter Builder

The Filter Builder helps create Wireshark display filters without knowing the full syntax. See the [Filter Builder](filter_builder.md) page for detailed information.

---

## Notes

- ShowShark is read-only and does not alter packet data.
- It works with both live captures and saved capture files.
- No special capture options or hardware are required.
