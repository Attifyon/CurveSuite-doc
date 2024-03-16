# ![icon](../img/icons/random_trim_curves.png) Random Trim Curves

[TOC]

---

## Overview
This modifier shortens curves by randomly trimming their roots or tips based on how the parameters are set

<iframe width="560" height="315" src="https://www.youtube.com/embed/DxPT-9JNdSw?si=6IuUgyUqYqd66SZP" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

---

## Parameters
![Parameters](params/random_trim_curves.PNG)

* **Root Min:** The minimum point's position along the curve that'll become the new root after trimming
* **Root Max:** The maximum point's position along the curve that'll become the new root after trimming
* **Root Trim Seed:** Determines the random number generated for the root trimming
* **Tip Min:** The minimum point's position along the curve that'll become the new tip after trimming
* **Tip Max:** The maximum point's position along the curve that'll become the new tip after trimming
* **Tip Trim Seed:** Determines the random number generated for the tip trimming

!!!warn "Trimming by Spline Factor"
    All of the trimming amount parameters are relative to the spline factor, where zero represents the root and one represents the tip. The default values will not trim the roots, and randomly trim the tips by up to 35%. In order to further trim the tips, you will need to actually reduce the tip trimming parameters

---

## Tips & Use Cases

* By setting the root trim seed and tip trim seed to be the same integer, you can have symmetrically trimmed curves.

* Modifiers like [Align Curve to Surface](align_curve_to_surface.md) and [Transfer Radius and Tilt](transfer_radius_and_tilt.md) also use spline factor for their internal calculations. When using this modifier alongside such modifiers, you may run into unexpected behaviour depending on their ordering. In such cases, make sure to try alternate orderings to see how they work together.