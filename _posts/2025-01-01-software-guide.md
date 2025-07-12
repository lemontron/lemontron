---
layout: post
title: Software guide
kofi: true
thumbnail: /assets/guide/intro---sd-card.jpg
permalink: /lemontron/software-guide/
categories: guide
---

Lemontron's official software stack is Mainsail OS on a Raspberry Pi.

## Prepare the SKR Pico

With the SKR Pico freshly unboxed, temporarily install two jumpers - On to the `BOOT` pins (located in the center, under
the "TE"in "BIGTREETECH") and `USB Power` pins (next to the USB port, to enable temporary power from USB instead of the PSU).
Then hold down the `BOOT` button and connect the SKR Pico to your computer.

![SKR Pico Jumpers](/assets/content/skr-pico-jumpers.png)

Drag [this firmware file](/assets/downloads/klipper.uf2) to the PICO drive that appears. Remove the jumpers. Good to go!

{% include separator.html %}

## Prepare the Raspberry Pi

Burn Mainsail OS (64 bit) via [Raspberry Pi Imager](https://www.raspberrypi.com/software/) onto your SD Card, ensuring
you've
added your SSH key and WiFi settings.

Use SSH to access the Raspberry Pi's terminal and paste this:

```bash
sudo apt update && sudo apt upgrade
cd ~/klipper/
make menuconfig
```

In the menu interface that appears...

1. Change microcontroller architecture to RP2040
2. Change communication interface to Serial
3. Save Config
4. Run `make` in the terminal

## Configure Mainsail OS

1. Open up the Raspberry Pi webpage by navigating to the network name of the Raspberry Pi in your browser. If you named
   your printer "lemontron" then your URL would be `http://lemontron.local`
2. Update everything!
3. Click on the "Machine" tab (the last one) and
   upload [the config files](/assets/downloads/config-20241223-175652.zip).

## Install AutoHotspot

AutoHotspot is a script that will automatically switch your Raspberry Pi between WiFi and Hotspot mode based on the
presence of your home network.
Check out
the [AutoHotspot documentation](https://github.com/RaspberryConnect/AutoHotspot-Installer/tree/master/AutoHotspot-Setup/Autohotspot)
for more information. Some AutoHotspot tutorials are outdated, you may need to replace the URL
with "https://www.raspberryconnect.com/images/hsinstaller/AutoHotspot-Setup.tar.xz"