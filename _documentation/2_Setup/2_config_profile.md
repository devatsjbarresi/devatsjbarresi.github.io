---
layout: default
title: Configuration Profile
parent: Setup
nav_order: 2
permalink: /documentation/setup/configuration-profile/
---

<h1 align="center">Configuration Profile</h1>

---

Wireshark uses configuration profiles to manage settings like display, column layouts, packet colour filter other preferences.

### What's Included

The default ShowShark profile includes:

**Column Layout** - Designed specifically to show relevant entertainment information in the packet list. You can customise the columns to suit your needs or reset them at any time via _Tools > ShowShark > 2 Displays > Reset Columns_.

**Colour Rules** - A default set of colour rules that highlight packets based on protocol type, making it easier to visually distinguish different types of traffic as they appear in the packet list.

### Enabling the ShowShark Profile

When you first load the ShowShark plugin, a dedicated ShowShark configuration profile is automatically created. To activate it:

1. Go to **Edit > Configuration Profiles**

<p align="center">
  <img src="/assets/images/setup/setup_menu_config_profiles.png" alt="Configuration Profiles Menu"
       style="width: 50%;">
</p>

2. Select the **ShowShark** profile from the list
3. Click **OK** to apply the profile

<p align="center">
  <img src="/assets/images/setup/setup_window_config_profiles.png" alt="Configuration Profiles Window"
       style="width: 75%;">
</p>

Once activated, you'll notice the packet list columns change from Wireshark's default layout to ShowShark's customised view.

---

<div style="display: flex; justify-content: space-between; align-items: center;">
  <a href="/documentation/setup/installation/">< Installation</a>
  <a href="/documentation/guide/menus/">Menus ></a>
</div>
