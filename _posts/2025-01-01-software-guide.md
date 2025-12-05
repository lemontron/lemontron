---
layout: post
title: Software guide
thumbnail: /lemontron-rev-a/build-guide/intro---sd-card.jpg
categories: [guide]
---

Lemontron's official config: Mainsail OS on a Raspberry Pi

## Prepare the SKR Pico

Temporarily install `BOOT` and `USB Power` jumpers, connect it to your computer and press `BOOT`.

![SKR Pico Jumpers](/assets/content/skr-pico-jumpers.png)

{% include button.liquid
title="Download Firmware"
icon="download"
link="/assets/downloads/klipper.uf2" %}

Drag the firmware file to the PICO drive that appears. Remove the jumpers. Good to go!

{% include separator.html %}

## Prepare the Raspberry Pi

Burn Mainsail OS (64 bit) via [Raspberry Pi Imager](https://www.raspberrypi.com/software/) onto your SD Card, ensuring
you've added your SSH key and WiFi settings. No need to set a user/password.

The default user is **pi** and password is **raspberry**.

Use SSH to access the Raspberry Pi's terminal and paste this:

```bash
sudo apt update && sudo apt upgrade
cd ~/klipper/
make menuconfig
```

In the menu interface that appears...

1. Change microcontroller architecture to RP2040
2. Change communication interface to UART
3. Save Config
4. Run `make` in the terminal

## Configure Mainsail OS

1. Open up the Raspberry Pi webpage by navigating to the network name of the Raspberry Pi in your browser. If you named
   your printer "lemontron" then your URL would be `http://lemontron.local`
2. Update everything!
3. Click on the "Machine" tab (the last one) and
   upload [the config files](https://www.printables.com/model/1440115-lemontron-rev-e/files).

## Install AutoHotspot

[AutoHotspot](https://github.com/RaspberryConnect/AutoHotspot-Installer) can automatically put your Pi
in hotspot mode if your WiFi network is not around