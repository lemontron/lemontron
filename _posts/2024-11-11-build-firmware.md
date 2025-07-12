---
layout: post
title:  "How to build Klipper"
category: guide
kofi: true
thumbnail: /assets/guide/intro---sd-card.jpg
permalink: /lemontron/:title
---

You can always download precompiled firmware, but building it yourself can be a good way to stay in control of the
process, for example to enable or disable extra features. This guide will give you a basic understanding of how to build
Klipper.

### Get up-to-date

SSH into the Raspberry Pi and run the following commands:

```bash
sudo apt update
sudo apt upgrade
```

### Build firmware

We're going to build the firmware on the Raspberry Pi, and then flash it to the SKR Pico.

```bash
cd klipper
git pull
make menuconfig
make
```

1. Set microcontroller to **Raspberry Pi RP2040**
2. Set interface to **UART0**

### Flash the SKR Pico

1. Using your computer, download the `klipper.uf2` file from the `klipper/out` directory to your computer.
2. Apply jumpers to the `BOOT` pins on the SKR Pico (located in the center, under the `TE` in `BIGTREETECH`) and the USB
   power selector next to the USB-C port.
3. Hold down the `BOOT` button on the SKR Pico and connect the SKR Pico to your computer over USB-C.