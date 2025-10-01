---
layout: guide
title: Introduction
icon: home
header_title: Lemontron
---

Rev E documentation has not yet started! All there is, is the raw files. Please familiarize yourself with Rev A, then
leap to Rev E.

## Difficulty

The printing skill level either requires a recent enclosed printer or incredible skill by the operator! These tolerances
are tight and print quality must be high.

## Required Tools

### Screw Drivers

The Lemontron benefits from deep integration and thus only M3 (2mm Hex Bit) and a few M2.5 are used. I
recommend having a dedicated high quality M3 screwdriver, plus a bit for your drill. Add a countersink bit to clean up
the printed countersinks and to add countersinks to the probe.

<div class="bom-list">
{% include tool-item.html
title="Drill"
amazon="B003BEE2LU"
image="/assets/tools/drill.png" %}

{% include tool-item.html
title="Driver Bit"
amazon="B001553HD6"
image="/assets/tools/driver.png" %}

{% include tool-item.html
title="Screw Driver"
amazon="B00365EYJO"
image="/assets/tools/screwdriver.png" %}

{% include tool-item.html
title="Allen Keys"
amazon="B083BGVMB8"
image="/assets/tools/allen-keys.png" %}

{% include tool-item.html
title="Countersink"
amazon="B00LLGSZGS"
image="/assets/tools/countersink.png" %}
</div>

### 3D Printing Tools

You will need a modern, enclosed 3D printer to print the Lemontron parts. Razors for scraping. A craft knife for tidying
blemishes. Supa glue for the Lemonstruder parts (the "liquid" one not the thick one).
pesky wires.

<div class="bom-list">
{% include tool-item.html
title="Razor Blades"
amazon="B0BFHB3CXP"
image="/assets/tools/razor-blades.png" %}

{% include tool-item.html
title="Craft Knife"
amazon="B001A42CTW"
image="/assets/tools/craft-knife.png" %}

{% include tool-item.html
title="Supa Glue"
amazon="B0D2RP4B82"
image="/assets/tools/super-glue.png" %}

    <div class="bom-placeholder"></div>
    <div class="bom-placeholder"></div>

</div>

### Electrical Tools

A soldering iron is needed for soldering the edge connector and other wires. For the
motors, you'll need some wire cutters and a crimper. You may try your luck with a soldering iron.

<div class="bom-list">
{% include tool-item.html
title="Crimper"
amazon="B078WPT5M1"
image="/assets/tools/crimper.png" %}

{% include tool-item.html
title="Wire Strippers"
amazon="B000XEUPMQ"
image="/assets/tools/wire-strippers.png" %}

{% include tool-item.html
title="Soldering Iron"
amazon="B096X6SG13"
image="/assets/tools/soldering-iron.png" %}
<div class="bom-placeholder"></div>
<div class="bom-placeholder"></div>
</div>

### Trimming Tools

The motor shafts and X-Axis rail must be shortened. A Dremel with a cutoff wheel is recommended. Flush cutters are also
required, but 3d printers tend to come with those.

<div class="bom-list">
{% include tool-item.html
title="Dremel"
amazon="B0D2D28FSV"
image="/assets/tools/dremel.png" %}

{% include tool-item.html
title="Flush Cutters"
amazon="B00FZPDG1K"
image="/assets/tools/flush-cutters.png" %}
<div class="bom-placeholder"></div>
<div class="bom-placeholder"></div>
<div class="bom-placeholder"></div>
<div class="bom-placeholder"></div>
</div>

## About Rev E

Rev E builds on the previous versions of Lemontron with a geared extruder, refined geometry, cooling performance.

Previously, the Lemonstruder was an ender 3 extruder gear attached directly to the motor shaft. Without mechanical
leverage, it ran hot, and there was no room for error, something that almost everyone had trouble with. Rev E adds an
extensively tested 4.5:1 gear reduction, the Endgame Lemonstruder.

There is also a new 225 degree wraparound ducted cooling tool end. This wasn’t just slapped together — I went through
duct engineering hell: The result? High flow, unimpeded by complex ductwork, a sensible easy to picture flow that leaves
little to the imagination, and real world cooling performance that shows a clear advantage.

- E is also for CoolEEEng because this revision also implements art_nathan's motor cooling proposal, which buts the
  fans right up to the motors so that the air can brush the sides of the motors. As a bonus there's enough space to
  fix Vram cooling heatsinks to the motors for even more zest. So just look at it, that looks cool!

## Resources

{% include resources.html %}