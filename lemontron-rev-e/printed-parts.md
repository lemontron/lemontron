---
layout: documentation
title: Printed Parts
icon: print
description: Settings & Materials
thumbnail: /assets/content/printed-parts.jpg
order: 1
---

{%- include tips/printing-tips.html -%}

## Chassis Inventory & Materials

<ul class="inventory">
{% include inventory-item.html
title="Top Plates"
id="top-plates"
settings="5 walls, 25% grid"
description="Mostly decorative, but need some thickness around the screw holes. Show off your printing
abilities with a flashy filament."
preferred_material="PLA" %}

{% include inventory-item.html
title="Unibody Chassis"
id="chassis"
description="The chassis should be made from a stiff material, and it does not experience savage heat."
settings="8 walls, 50% grid"
preferred_material="PLA" %}

{% include inventory-item.html
title="Mid Plates"
id="mid-plates"
description="High-temp material is required because these serve as the motor mounts."
settings="5 walls, 50% grid"
preferred_material="ABS" %}

{% include inventory-item.html
title="Tensioner"
id="tensioner"
description="High-temp material is required because this screws directly into the motor."
settings="5 walls, 50% grid"
preferred_material="ABS" %}

{% include inventory-item.html
title="Lemonstruder"
id="lemonstruder"
description="Made of two parts. Experiences compression from the spring, so a drift-resistant
material with good accuracy is preferred."
settings="5 walls, 50% grid"
preferred_material="CF-PETG"
other_material="ABS" %}

{% include inventory-item.html
title="Risers"
id="risers"
description="Raspberry Pi mounts to these, and they keep the SKR Pico pinned down. Material doesn't matter."
settings="5 walls, 50% grid"
preferred_material="PLA" %}

{% include inventory-item.html
title="Z-Tensioner"
id="z-tensioner"
description="High-temp material is required because this screws directly into the motor."
settings="5 walls, 50% grid"
preferred_material="ABS" %}

{% include inventory-item.html
title="Gantry Block"
id="gantry-block"
description="This links the X and Y rails together to create the XY plane. A stiff material, resistant to warping and
drift, is ideal."
settings="5 walls, 50% grid"
preferred_material="ABS" %}

{% include inventory-item.html
title="Fan Wire Guide"
id="fan-wire-guide"
description="No specific material requirements."
settings="3 walls, 25% grid, concentric top"
preferred_material="PLA" %}

{% include inventory-item.html
title="Filament Guide"
id="filament-guide"
description="No specific material requirements."
settings="3 walls, 25% grid"
preferred_material="PLA" %}
</ul>

## Z-Axis Inventory

<ul class="inventory">
{% include inventory-item.html
title="Z-Axis"
id="z-axis"
description="Choose any material for this part, just make sure it looks awesome."
settings="5 walls, 50% grid"
preferred_material="PLA" %}

{% include inventory-item.html
title="Bed Bracket"
id="bracket"
description="The bed bracket is made from two parts. A stiff material like CF-PETG would be ideal."
preferred_material="CF-PETG"
settings="5 walls, 50% grid"
other_material="PETG" %}

{% include inventory-item.html
title="Bed Holder"
id="bed-holder"
description="This is best printed in CF-PETG and the spine can be printed in whatever you want, I recommend matching
the tool head materials."
settings="8 walls, 50% grid"
preferred_material="CF-PETG"
other_material="PETG" %}

{% include inventory-item.html
title="Spool Holder"
id="spool-holder"
description="This has a captive nut, so make sure to add a pause! Layer adhesion is important here, so PLA is a good
choice."
settings="5 walls, 50% grid, concentric top/bottom"
preferred_material="PLA" %}

{% include inventory-item.html
title="Bed Holder Cups"
id="bed-holder-cup"
description="Holds up the bed! Print two of these."
settings="5 walls, 50% grid"
preferred_material="ABS" %}

{% include inventory-item.html
title="Spacer"
id="spacer"
description="Drop these into the Z axis to make the screws line up flush with the back side."
preferred_material="PLA" %}
</ul>

## Tool Head Inventory

<ul class="inventory">
{% include inventory-item.html
title="Tool Head"
id="tool-head"
description="The tool head houses the hotend and thus must be printed in ABS."
settings="5 walls, 50% grid, outer/inner wall order"
preferred_material="ABS" %}

{% include inventory-item.html
title="Clip"
id="clip"
description="Clips the belt to the tool end. Layer adhesion matters most, so I recommend PETG or PLA."
settings="5 walls, 50% grid"
preferred_material="PETG"
other_material="PLA" %}

{% include inventory-item.html
title="Clamp"
id="clamp"
description="No material requirements. Perhaps use ABS to match."
settings="5 walls, 50% grid"
preferred_material="ABS" %}
</ul>
