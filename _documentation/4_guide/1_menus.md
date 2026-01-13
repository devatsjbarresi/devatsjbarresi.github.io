---
layout: default
title: Menus
parent: Guide
nav_order: 1
nav_fold: false
permalink: /docs/guide/menus/
---

<h1 align="center">Menus</h1>

---
ShowShark adds a menu under _Tools > ShowShark_ in Wireshark, making it easy to access plugin features and settings.

<p align="center">
  <img src="/assets/images/menus_overrview.png" alt="ShowShark Menu Overview"
       style="width: 65%;">
</p>

## 1. User Level

ShowShark offers two display levels:

### Essential

Essential is the default display level, designed to provide a clean and simple view of the most important information to get you started.

### Advanced

Advanced provides a more detailed view with additional details and information.

You can switch between Essential and Advanced at any time by going to _Tools > ShowShark > User Level_.

## 2. Displays

The Displays submenu provides quick access to reset display settings of the configuration profile (e.g. columns and colours).

See the [Columns](/docs/guide/columns/) page for more information on column settings.

## 3. Show Host Table

Opens the Host Table window displaying all discovered devices and their properties. See the [Host Table](/docs/guide/host-table/) page for detailed information.

## 4. Options

This opens the Options dialog where you can configure various ShowShark settings. You can't break anything from this window; however, most of the useful settings can be accessed from the menus anyway.

The dialog gives explanations of each setting and the options available.

## 5. Open Plugin Folder

Opens the folder where any additional files for ShowShark live (this may be empty).

## 6. Reload Wireshark Plugins

Reloads all Lua plugins in Wireshark without restarting the application. You should only really need to use this when updating the ShowShark plugin.

## 7. Visit ShowShark Website

Come here!

## 8. About ShowShark

Displays information about the current ShowShark version, including release notes.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
  <div><a href="/docs/capturing/">← Capturing</a></div>
  <div style="text-align: right;"><a href="/docs/guide/host-table/">Host Table →</a></div>
</div>
{:/}
