---
layout: bom
title: Power Supply
qty: 1
orders: 1
total: 49.71
description: LOP-300-24
new: false
modification: true
links:
  - vendor: Digikey
    url: https://www.digikey.com/en/products/detail/mean-well-usa-inc/LOP-300-24/22040910
  - vendor: AliExpress
    url: https://www.aliexpress.us/item/3256807058463517.html
  - vendor: Mouser
    url: https://www.mouser.com/ProductDetail/MEAN-WELL/LOP-300-24?qs=Z%252BL2brAPG1J53tTb9OPXAA%3D%3D
optional: false
category: Electronics
---

The following substitute PSU's also work: LOP-300-27, LOP-200-24, LOP-200-24.
LOP and EPP variants are dimensionaly quite similar, but the EPP's are a bit taller.

If you are converting a JourneyMaker, you _can_ re-use the EPP-200-24 PSU, in fact the EPP model was used in the
announcement video and is in my Lemontron. However, the transformers tend to be installed sloppily at a slant, which
requires snipping off the top of the plastic casing to allow the top plates to sit flush.

## Required Modification

<ol class="steps">
    {% include step.html
    title = "Modify PSU"
    image = "psu---cut.jpg"
    content = "Bevel the two corners of the PSU that face outwards. The cut should bisect the screw post holes." %}
</ol>
