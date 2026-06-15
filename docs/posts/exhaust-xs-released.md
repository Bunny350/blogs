---
date:
  created: 2026-06-15
links:
hero: /blogs/media/exhaust-xs-released/oitswilliamv0-exs.png

categories:
  - Hardware
tags:
  - hardware
  - OITSWILLIAMV0
  - Voron mod
authors:
  - oitswilliam
---

# Exhaust XS released

Swooshing air filter for Voron 0 now available.

<!-- more -->

Oitswilliam Pang introduced Exhaust XS for Voron 0 to everyone under OITSWILLIAMV0 project. It is Oitswilliam's easiest-to-maintain exhaust filter.

## Philosophy

Exhaust XS has created as not much exhaust units for Voron 0 found, and those that exist require a big fan, which is why Oitswilliam decided to make on own.
The acronym, EXS, has popped in Oitswilliam's minds before it is ever designed.

## The toolless filter cartridge
<div class="clip">
<video loop autoplay muted playsinline src="/blogs/media/exhaust-xs-released/exs-filter-changing.mov">
    </video>
    </div>
    
The filter cartridge is made toolless. This is a major leap in Oitswilliam's hardware design, where replacing any element of the filter just require a hand to pull, whether it's the front HEPA, the activated pellets or the back HEPA filter. This design makes filter replacements significantly easy when compared to our ELG2 or some rivals.

## Dual-layer HEPA filter

We have contained two HEPA filters in a cartridge, to filter microplastics before the way to the activated pellets, and the back just for containing the dust of the activated pellets.

## 5010 blower-style fan, the point of the swooshing filter

<img src="/blogs/media/IMG_4367.jpeg" alt="A 5010 blower-style fan in V0.2378 being exposed for everyone to see" />

Exhaust XS uses 5010 blower-style dual-bearing fan, to make it different. This decision allows it to sound different, like a jet, while being powerful.

## The biggest gimmick - the hybrid filament sensor

<div class="clip">
<video loop autoplay muted playsinline src="/blogs/media/exhaust-xs-released/exs-tangle-sensing.mp4">
    </video>
    </div>

There is no exhaust unit made by Oitswilliam without some kind of filament sensor, until distant future. The hybrid filament sensor consists of the presence (or run-out) and tangle trigger. The design for EXS consists of the presence sensor placed on a unit that is then being checked by the tangle trigger[^material-tangle-sensing]. Although it can't detect extruder clogs, this is enough for the basic sensor.

We also like using our machines with abrasive filaments, but our machines' printed parts are not made with such or stronger materials. To solve this, the presence sensor has two MR85-ZZ or -2RS bearings that is in-between the incoming filament, just to prevent grinding.[^sensor-grinding-elg2] This is unseen in other filament run-out sensors.

## The profile
Exhaust XS is intended to be low-profile. With 3cm of bump, it already is the thinnest filtered exhaust unit made for Voron 0, and with chamfered corners, it certainly looks stealthy.

## What's the "reserved part" of the filter? And why did the front HEPA filter's punching right-side?

We are not telling you for now, as it will be a major breakthrough. Stay tuned by [following Oitswilliam in any applicable platforms](https://www.oitswilliam.com/media).

## Availability and compatibility

Exhaust XS was reserved for followers of Oitswilliam Pang and are happily using it under alpha-stage early access. Exhaust XS is being released today **June 15, 2026** under [OITSWILLIAMV0 project](https://github.com/Bunny350/OITSWILLIAMV0) repository. Assembly guide will also be updated today to meet the current materials. [Bill of materials](https://docs.google.com/spreadsheets/d/1qKHTR9wy5eDcJ8kGZrhbsqijIHyDv_TbETnKIMAwmbk/edit?usp=sharing) for EXS has released to the public.

Exhaust XS supports Voron 0 in revisions starting from V0.1. It can be mounted on and replaces the back panel of top hats from V0.1 and V0.2, printed and extrusion versions respectively. The main unit requires a fan header for the blower fan, and the hybrid sensor requires two digital signal pins and a ground pin.

Getting Exhaust XS physically requires a printer in print volume of at least 120x120x50mm, including Voron 0. There are parts of main unit that aren't split in left-right sides, these require a printer in print volume of at least 160x160x50cm, including Voron Trident & Voron 2 in at least 250mm spec, and Switchwire.

We have added an optional LED unit to EXS, currently only tinkerers with CAD knowledge can access this as there is none of it in manuals, this will be officially released later this year. And so, [**BabyDrone Back LED**](https://github.com/Bunny350/BabyDrone-Back-LED) has been released at the same time as EXS (not) just for this.[^babydrone-led-tou] 

[^material-tangle-sensing]: Materials softer than TPU 95A are recommended to have feed assistant installed. Even if the feed assistant is installed, the hybrid sensor normally cannot detect tangle for such filament material.
[^sensor-grinding-elg2]:  [https://github.com/Bunny350/OITSWILLIAMV2/issues/4](https://github.com/Bunny350/OITSWILLIAMV2/issues/4) This issue plagues run-out sensors with only switch rolling bearing over abrasive filaments grinding on run-out sensor shells in normal non-reinforced material.
[^babydrone-led-tou]: Usage of BabyDrone LED requires an agreement of Oitswilliam Pang Terms of Use.
