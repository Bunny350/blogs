---
date:
  created: 2026-08-05
hero: /blogs/media/elic/elic.jpeg
categories:
  - Hardware
  - Announcement
tags:
  - hardware
  - alpha-EA
  - OITSWILLIAMV2
  - Exhaust Lite
  - Voron mod
authors:
  - oitswilliam
---

# The Exhaust Lite Integrated Controller

The One Unit That Zaps All The Wiring.

<!-- more -->

Today, Oitswilliam Pang announced Exhaust Lite Integrated Controller. The unit that allows one-cable installations, perfect for maintenances.

ELIC is the microcontroller board that allows simpler connections of the exhaust units for Klipper-ran printers. Turning the printer sideways or upside-down for exhaust mainentance or add-ons will be the past.

## Small and affordable

The dimension of ELIC is up to 45x45mm, with maximum possible thickness of 6mm. This allows the installations on exhaust units that are not the next generation of Exhaust Lite. With larger round on the bottom-right, this is our way of keying the placement.

With STM32F070 microcontroller unit, the cost of ELIC is budget-friendly and can fit on budget 3D printers as a convenient exhaust accessory.

## The ports

<img src="/blogs/media/elic/elic-front.png" alt="Front side of ELIC"/>

ELIC has 9 connection ports, two of which is made exclusive to the Pro version.

On the left there is a port for the filament sensors, it is optimized with our hybrid filament sensor which will be in the next generation of Exhaust Lite, but also has 3.3V pin that allows connection to virtually all run-out and tangle sensors available. Then the thermometer below, for chamber monitoring or our gimmick. The fan port, also below, is where it can be universal. ELIC will use the low profile fan in ELG3, but since it also needs to be universal, we have made such port accept either PicoBlade 1.25 or JST-PH 2.0, and accepts hardware PWM at up to 25KHz.

On the top is where two MOSFET drivers place, which accepts software PWM at up to 25KHz, and the NeoPixel LED port for those that prefer using NeoPixel LEDs.

On the right is the Pro-version exclusive USB ports, via JST-PH 2.0. It allows further expansion with a camera and the port of your imagination.

ELIC uses USB-C port for everything it does, such port provides power to the LEDs, fan and other USB units. This is the goal of ELIC.

## Accessible bootloader and reset buttons

ELIC has highly accessible buttons just so it can be pressed even when installed on the exhaust units. Accessing in these options only require paper clips or SIM ejector pins instead of disassembling the entire machine.

## The unit does not exist without true OitswilliamV2 integration, but something has stopped this from happening

Yep, that's the title of initalization vows. We have found that ELIC got the virtual machine stuck on not-ready state, and then found out that is the software issue based of another board that uses different MCU, and you've already knew that, obviously different board. The solution we found is delayed restart, and then we, I mean I myself, managed to make a delayed bootloader that allows delaying initalization just to solve the stuck issue, and that did. It also has a gimmick that tells users that is working using the fan.

Because of that, we have also created two variants of Klipper flashing configurations. One with 8Kib bootloader offset, and one without that (no bootloader). 

## Debugging port issues

We are trying to deal the issue where the debug pins weren't working as expected. On completely internal prototypes, there is the debug pin accessible as through-hole, but we could not access its debug. So during the alpha-stage prototype, we have moved the debug pins to the back and turned them into solder pads.

## Availability and requirements

ELIC is now available to be tested by the followers of Oitswilliam Pang via [alpha-EA](https://www.oitswilliam/com/alpha-ea), while the bootloader software for ELIC is [available now to all users](https://github.com/Bunny350/Bootloader-firmware/blob/ELIC-G1-F070).

Integrator files of ELIC for non-followers will be available on October of this year, and the ELIC & the CAD source files will be available in Christmas December.  

ELIC, including normal and Pro versions, require the power of at least 5V 1A, or recommended 5V 1.5A, fan power shall not exceed 3.75W, LED and output powers shall not exceed the total power of 5W. Thermometer for ELIC is 100-kiloohm NTC thermistor. ELIC accepts NeoPixel LEDs that require 5V logic. ELIC requires a free USB port with at least USB 2.0 standard.

Note: the thumbnail shown is prototype II, while the release has no debug pins at the front.
