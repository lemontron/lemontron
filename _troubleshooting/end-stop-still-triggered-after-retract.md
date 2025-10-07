---
layout: troubleshooting
title: End stop still triggered after retract
---

1. Make sure you have a BLTouch jumper on your MCU. This connects an internal pull-up resistor which is critical to
   sensing the probe signals.
2. You were just testing it with your finger, you pushed it all the way in. Under normal probing, the build plate gently
   taps the probe.
3. Check the back of the probe for damage.