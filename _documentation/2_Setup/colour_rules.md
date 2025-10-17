---
layout: default
title: Colour Rules
parent: Setup
nav_order: 3
permalink: /documentation/colour-rules/
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

![Wireshark Colouring Rules dialog](/assets/colour_rules.png)


> **Note:** The colour rules file includes Wireshark's default colouring rules. It's safe to clear all existing rules before importing—no default colours will be lost.

