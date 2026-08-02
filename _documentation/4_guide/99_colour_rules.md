---
layout: default
title: Colour Rules
nav_exclude: true
published: false
permalink: /docs/colour-rules/
---

<h1 align="center">Applying Colour Rules</h1>

---
ShowShark includes a colour rules file which helps visualise different types of traffic in the packet list.

## Apply Colour Rules

1. Open Wireshark
2. Go to _View > Coloring Rules..._
3. Click the **Clear all colouring rules** button.
4. Click the **Import...** button.
5. Select `ShowShark_Colour_Rules_1.0.colours`.
6. Click **OK** to apply the colour rules.

<img src="/assets/images/colour_rules.png" alt="Wireshark Colouring Rules dialog" style="display: block; margin: 0 auto;">


> **Note:** The colour rules file includes Wireshark's default colouring rules. It's safe to clear all existing rules before importing—no default colours will be lost.

---

{::nomarkdown}
<div style="display: flex; justify-content: space-between; align-items: center; width: 100%;">
	<div><a href="/docs/filter-builder/">← Filter Builder</a></div>
	<div style="text-align: right;"><a href="/docs/capturing/">Capturing →</a></div>
</div>
{:/}
