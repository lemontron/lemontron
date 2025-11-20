---
layout: post
title: Lemontron "Endgame Revision" Annoucement
categories: [ news ]
thumbnail: /assets/content/endgame-announcement-video.jpg
excerpt: |-
  After a full year of design, testing, and refinement, the Lemontron has reached the Endgame milestone.
---

After a full year of design, testing, and refinement, the Lemontron has reached what I'm calling the "Endgame"
milestone. The Lemontron has upgraded into a far more capable machine: Stronger, cooler, easier to build, and
dramatically more rigid & repeatable.

{% include youtube-video.html id="FU5CCRJrfcg" %}

This update is the cumulative one-year overview of changes across Revisions B through E, driven by community feedback,
discoveries, and a relentless attempt to squeeze more performance out of the space-constrained form factor.

Below is an overview of what's changed:

## A New Extruder: The Endgame Lemonstruder

The biggest leap forward is the new 4.5:1 geared extruder. Earlier versions relied on a hob mounted directly to the
motor shaft. That approach worked-sometimes-but it also ran hot, offered very little mechanical margin, and behaved
inconsistently depending on the motor.

The new design uses a 16-tooth drive gear, a 72-tooth reduction gear, and a larger intermediate gear riding on a
post. The result is:

- High torque with stable grip
- Minimal heat transfer to filament
- Faster flow rate, exceeding 43mm³/s
- Good thermals even after long heat soaks

It's compact, powerful, and finally feels like the extruder this printer deserved from the beginning.

## The 225-Degree Wraparound Cooling Duct

Strong part cooling airflow has always been a challenge in such a cramped tool head. After multiple failed
designs—including dual ducts, a 180-degree curved outlet, and even a full 360-degree "ring" duct, I
landed on a 225-degree wraparound that unlocks the fan's full cooling abilities.

This design:

- Delivers most airflow to the front where it matters
- Routes a controlled amount to the sides and rear
- Avoids internal restrictions that choke the fan
- Has large directed outlets

## Full Chassis Cooling Overhaul

Paired with larger fans, this system outputs 8× the airflow of earlier prototypes.

- Fans directly cool the motors, design inspired by art_nattanon- a fan is touching each motor
- Quad nearly-chassis-height fans
- Optional copper VRAM-style heatsinks for additional surface area

This helps the motors, especially the extruder, stay cool and stable during long prints, which directly fixes most print
issues.

## Structural Improvements Everywhere

Many of the most impactful changes are subtle: geometry tweaks, reinforced features, and progressively more thoughtful
design-for-manufacturing decisions. A few highlights:

- Stronger Z-Block: Shifting the motors outward allows more material where it matters most, reduces flex, and enables
  the use of preferred
  bearing sizes.
- New Lead Nut Seat: A taller, reinforced seat prevents Z-offset drift—even when printed in PETG.
- Probe Mount: Revised walls prevent cracking of the probe's mounting tabs and improves durability.
- Relocated Tensioner: Instead of hollowing out the critical Z-block, the tensioner now sits at the front and pivots
  around the motor screw. Cleaner,
  stronger, and simpler.
- Updated Bracket + Edge Connector Fix: A new receiving channel fully restrains the PCB tab in the edge connector,
  eliminating the up/down play that caused
  Z-offset shifts.
- One-Handed Bed Assembly: Added guide rails allow you to drop the bed holder into place with a single hand.

## The Screw Elimination Saga

From Rev A through E, I've been slimming down the BOM. Every unnecessary fastener is one more part to track, buy, and
install. Over time:

- Screw types dropped from 13 to 7
- Various countersinks were swapped for stronger alternatives
- Short screws were replaced with longer ones + printed spacers
- Raspberry Pi mounting switched from M3 to M2.5
- Heat-set insert geometry was optimized while reducing screws as a side-effect

It's not glamorous! But the payoff is a printer that gets ever closer to building itself.

## A Genuinely Useful Tool

All of these improvements translate to genuinely better prints. Rev E is capable of strong, reliable, repeatable
outputs, even on long prints or with challenging materials. This machine has become a real daily driver.

## What's Next?

There are still frontiers I'm exploring:

- Full direct drive: likely impossible within the current folding geometry, but still on my mind.
- Vertical fine artifact (VFA) reduction: possibly belt-related; a 6 mm belt experiment is on the horizon.

No promises on timelines. This project has been a labor of passion, often at the expense of more practical
opportunities. As I'm currently between jobs, but Patreon support sure helps.

## Time For You To Build One

If you've been waiting for a moment to start your build, this is it.

Video breakdown, files, and community links are available on the site.

{% include button.liquid
icon="link"
title="Check out my Rev E documentation here!"
link="/lemontron-rev-e/" %}