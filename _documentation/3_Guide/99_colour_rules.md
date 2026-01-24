---
layout: default
title: Colour Rules
parent: Guide
nav_order: 5
nav_exclude: true
permalink: /documentation/guide/colour-rules/
---

<h1 align="center">Applying Colour Rules</h1>

---
ShowShark includes a colour rules file which helps visualise different types of traffic in the packet list.

When the plugin is loaded, it places the colour rules file in the ShowShark documents folder. The folder can be accessed via **Tools > ShowShark > Open Documents Folder**.

## Apply Colour Rules

1. Open Wireshark
2. Go to **View > Coloring Rules...**
3. Click the **Clear all colouring rules** button.
4. Click the **Import...** button.
5. Navigate to the ShowShark documents folder and select `ShowShark_Colour_Rules_1.0.colours`.
6. Click **OK** to apply the colour rules.

<img src="/assets/images/colour_rules.png" alt="Wireshark Colouring Rules dialog" style="display: block; margin: 0 auto;">


> **Note:** The colour rules file includes Wireshark's default colouring rules. It's safe to clear all existing rules before importing—no default colours will be lost.

---

<div style="display: flex; justify-content: space-between; align-items: center;">
  <a href="/documentation/guide/filter-builder/">< Filter Builder</a>
  <a href="/documentation/capturing/">Capturing ></a>
</div>
