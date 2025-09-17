---
layout: guide
header_title: Lemontron
---

{% include youtube-video.html id="n6l3GvkE4QU" %}

Lemontron is a **DIY** project - there are no kits - you must buy the parts online and assemble them.

## About Rev E

Rev E builds on the previous versions of Lemontron with a geared extruder, refined geometry, cooling performance.

This is a major leap forward. Previously, the Lemonstruder was an ender 3 extruder gear attached directly to the motor
shaft. Without mechanical leverage, it ran hot, and there was no room for error, something that almost had trouble with.

- Extensively tested 4.5:1 gear reduction.
- Using a 16 tooth drive gear, 72 tooth reduction gear with a big extruder gear in the middle, what we have here is the
  endgame lemonstruder.
- It now handily maxes out the hotend, and we can absolutely pound filament. This bad boy beats some of the beefiest
  extruders and its shorter than the motor's shaft and that's pretty cool.
- Just to be clear, the extruder gear is no longer touching the motor, it can't get hot, it can only push filament hard
  and fast. You cannot win in a fight with this extruder. It's done, the extruder is finished and my god is it good.
  But did you think I was done? E is also for End as in tool end. New tool end!!!
- If you have a lemontron or Positron v3.2, you're familiar with the single duct cooling fan. however there's a dual
  duct mod by olli3d available the v3.2. Not to be outdone I aimed to bring something like that to the lemontron and now
  we have a 225 degree wraparound duct.
- This wasn’t just slapped together — I went through duct engineering hell:
    - I first designed a dual duct but wound up being a dead end once I realized the place where I built the 2nd duct
      was right where the box closes so that was just sad.
    - I tried a 180 deg, curved nozzle next, which although it worked, it was no better than stock, learning point was
      that thin ducts just don't work.
    - Suddenly I realized I could create a full 360 deg nozzle. However the internal ducting was too complicated and the
      fan choked. It was worse than stock, a beautiful failure.
    - And then, clarity. I eliminated the entire quadrant that was the hardest for the air to reach, and when I did, the
      design started designing itself, all the air restrictions let up, unlocking the wraparound duct concept.
    - The new design has characteristics of the first nozzle, most of the air still shoots out the front, but some of
      the air is delivered around to the back. I was able to modulate the air going to each section by calculating areas
      of the outlets which I took to be a fixed size vs the areas of the inlets which I could vary. The result? High
      flow, unimpeded by complex ductwork, a sensible easy to picture flow that leaves little to the imagination, and
      real world cooling performance that shows a clear advantage.
    - This tool end was released as an optional mod, since the plastic is uncomfortably close to the hotend. but look,
      it's there for you if you want to chase ultimate performance, and at this point I've been running it hard.
        - This tool end also has a refined probe mount, if you split yours while tightening it down, well don't fret,
          this one has reinforcement walls for a more rigid mount and to not only prevent cracking but also reinforce
          the tabs if they are already cracked.
        - One more tool end update is that I made it ever so slightly taller, to better clear the belts. The previous
          one had zero clearance so most people found that the belt rubbed on the probe mounts.
    - And just when you think that’s it… I got one more thing:
    - E is also for CoolEEEng because this revision also implements art_nathan's motor cooling proposal, which buts the
      fans right up to the motors so that the air can brush the sides of the motors. As a bonus there's enough space to
      fix Vram cooling heatsinks to the motors for even more zest. So just look at it, that looks cool!

## Resources

{% include resources.html %}