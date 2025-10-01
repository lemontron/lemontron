---
layout: post
title: Troubleshooting
thumbnail: /lemontron-rev-a/images/intro---sd-card.jpg
categories: [guide]
---

## "End stop still triggered after retract"

Make sure you have a BLTouch jumper. Check the back of the probe for damage.

## M3 Screws are not passing through the holes properly / Filament doesn't make it through the extruder

This problem is caused by overextrusion on the printed parts. Holes will be sized too small and this makes assembly harder, as well as causes the problem where filament is stuck in the path across the extruder gear or filament is hard to load. Calibrate the flow rate and reprint the affected parts.

## Prints are coming out mirrored

You swapped your A and B motor wires.

## The belts are rubbing on the left top plate

Your top plate is bowed due to wires trapped underneath. Make sure you've bound your wires in kapton tape. Loosen the top and mid-plates and give the wire bundle a good wank to settle them into the wire channels

## The belt is rubbing on the right top plate

1. Some non-MeanWell, alternate PSU's such as from AME, have a taller capacitor. Carve out your top plate.
2. The wires in the PSU cavity are too springy or your have a clearance issue and are pushing the top plate up. Redo the wiring so that it's cleaner.

## The screws on the carriage are bottoming out

Your X rail is 6mm rather than the standard 6.5mm. Drop some spacers (the ones for the Z rail) into the two holes and tighten again.

## The sharp X rail is chewing up the belts

Your X rail cuts were cut too close to the holes. Not to worry, there are printable pulleys to hold the belt clear of the rail.