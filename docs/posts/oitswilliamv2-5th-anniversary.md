---
date:
  created: 2026-06-15
  updated: 2026-07-20
links:
hero: /blogs/media/oitswilliamv2-is-going-5/oitswilliamv2-is-going-5.png

categories:
  - Hardware
tags:
  - hardware
  - OitswilliamV2
  - Voron mod
authors:
  - oitswilliam
---

# OitswilliamV2 is going 5

The printer, the computer. From June of 2026 to October of 2027, The BA concept is going 5. We will look at it's past, present and our future plans.
<!-- more -->

OitswilliamV2 was used to be just a small Voron 2 with my additions, but then something very ambitious happened, why not make it "live", by putting the advanced tech seen in fully-fledged computers in there?

## The early days

The early days of OitswilliamV2 has been nothing, but make it small. Sometime later, I added features that meant to be experimental, such as passive Power over Ethernet. However the most important part of it, as a concept, is: it should be portable, and should handle gaming.

<img src="/blogs/media/oitswilliamv2-is-going-5/gaming-on-v2.jpg" alt="Gaming on Voron 2?"></img>

The manipulated render shows it "in" Windows 10, just because I want to put a comedic material in, and it's because it's prior to the official release of Windows 11, but anyway. This is one of the machines where I intent to run Windows 11 on, where this is the first, but the last being my desktop computer.

## The concept

<img src="/blogs/media/oitswilliamv2-is-going-5/actual_oitswilliamsv2_starter_pack_idea_or_meme.jpeg" alt="The idea of OITSWILLIAMSV2, consisting of a shrunk down Voron 2, a 15-amp buck-boost converter, BigTreeTech Octopus, batteries with huge capacity, LattePanda SBC, a 5-inch touch-screen display, and of course, Windows. Might as well bundle it with Voron Stealthburner."></img>

The concept is simple, put Windows 11 inside the 3D printer, and then try to attach the battery to it. And of course and already said, be my first Windows 11 device, which sadly didn't, and so the battery.

### Someone imitated me, but sucked

Because of such ambitious project, there are imitations spawned, where they tried to run Minecraft, except on the spec-size Voron 2, which is not so portable. And in Raspberry Pi 3+, so it is insanely laggy running such software. And that plan has foiled. At least they are not running it on Windows.

### The logo

OitswilliamV2 used to be called as OITSWILLIAMSV2, until I was like, release it, but that name looks bad, so I removed the 's part of it, and is then called OITSWILLIAMV2, in full caps.

<img src="/blogs/media/oitswilliamv2-is-going-5/oitswilliamsv2-boot-screen.png" alt="OITSWILLIAMSV2 boot screen."></img>
I "ironically" added Voron Design logo, because it is in a Voron printer, but in reality they have nothing done in this project, and the logo for my group has no borders (the logo was before major change). Oh yea, and the 64, that's because during that time Raspberry Pi recommends 32-bit architechture operating systems on 64-bit architecture CPU-based SBCs, despite they have 64-bit version ones, and I want to chew on performance plus break 32-bit limits.

### The mini PC

During 2022, I decided to ditch the Pi 3+ with Morefine M6 that has quad-core Jasper Lake processor on it. Despite it's obviously different from LattePanda, it works, but can't do anything what I want and beyond. It only let it run Windows but still treat it like a printer, which means nothing on what I want. And on 2025 I ditched that due to Windows' issue (definitely, the later major version the more performance-demanding in background). I could run Debian physically but there are nonsense where there's more people using Windows than Debian / Ubuntu on desktops.

### Some considerations

There are considerations I want to implement, but gave up due to usability issues, especially the battery back. The battery back has two variants, one with the battery built-in, and one where two batteries can be swapped and are looked deceptively like 604s.
<img src="/blogs/media/oitswilliamv2-is-going-5/oitswilliamv2-battery-back.png" alt="OITSWILLIAMV2 battery back."></img>
This design lets users hot-swap batteries. There are some graphics at the left-hand side, such as Voron logo and a river-looking thing where it will be turned into stairs due to FFF layering, but the latter part might not work.
<img src="/blogs/media/oitswilliamv2-is-going-5/oitswilliamv2-battery-back-built-in-battery.png" alt="OITSWILLIAMV2 battery back, with a built-in battery."></img>
This design, on the other hand, has a built-in 4 to 6S, 1 to 3P, which prevented users from hot-swapping.

However, since it heavily relies on custom-built power components, only runs for less than an hour of printing, and I have never learned ways to convert the batteries of 4 to 6S to 24V constant output, I decide to scrap it, despite I can create a generic USB UPS driver for such unit, but that was years later.

SuperExpander port is another of my considered superpower feature, where it consists of the power input and USB signal pins. However as it is beyond complex, it was ultimately been scrapped.

<img src="/blogs/media/oitswilliamv2-is-going-5/oitswilliamv2-sxp-port.png" alt="OITSWILLIAMV2 SXP port."></img>

The SXP port is based around the JX6 / JX8 connector (but actually [optimized for JX8](https://www.facebook.com/share/p/15cLyyZsEVJ/)), which has 6 / 8 additional pins to play with, beside the power pins.

And not to mention about tracker mounting, it used to have magnetic mount, and after having the variant where it just sticked into the base color skirt parts via VHB tapes.

<img src="/blogs/media/oitswilliamv2-is-going-5/oitswilliamv2-airtag-mount-g1.png" alt="First generation of AirTag tracker mount made for V2.4(r1)."></img>

The first generation of AirTag tracker mount is just an extension to stick the tracker to the skirt and attaches AirTag via two M3x6mm BHCS and a bracket. That's it. But there are problems, since it is sticked via VHB tape, it may look unappealing and is either too difficult to change or remove batteries, or tape may disintegrate. These reasons are why the second generation of the tracker mount and the harder 60mm fan mount (that uses screws to secure) were made shortly.

<img src="/blogs/media/oitswilliamv2-is-going-5/IMG_5027.png" alt="First generation of AirTag tracker with an actual AirTag attached in."></img>
*[Yes, it was attached to my printer.](https://www.facebook.com/williampang.3363/posts/pfbid0kD782PY5aQFMNQEqGWKrmNf4WMdxfWSEWVPZKBHLEGzEeB2mWeBm67ifCbURsep7l)*

<img src="/blogs/media/oitswilliamv2-is-going-5/oitswilliamv2-airtag-mount-g2.png" alt="Second generation of AirTag tracker mount made for V2.4r2 (and Trident)."></img>
The second generation of the tracker mount has the back side hard-mounted to the fan mount. It uses magnets to secure the AirTag and can be secured with another M3x6mm BHCS. However, this bumped the screws (all M3x6) from 2 to 7 (and so the next generation).

However, I still did not like the way it attaches, or attached, as it will just be like "whopee", or prone to losing the tracker itself, if the tracker attachment screw securing the assembled tracker is not attached.

The third generation is where the tracker mount, at least AirTag version, for standard Voron printers released. I used to add a screw mount for between the assembled tracker unit and the inner bracket. However I removed the screw hole as it didn't appeal the simplicity. The third generation has a delicate alignment piece that is secured via M2x10mm self-tapping screw. 

And these three generations were made from February to July 2022 alone.

## RealEstate and Exhaust Lite
RealEstate and Exhaust Lite are the first two main parts of the mod I was optimized on. 

Exhaust Lite is intended to be small, however, in the first generation, the efficiency is too small, which is why I have made the second generaion of it. The second generaion is way bigger, and has built to have higher filtration efficiency, but still isn't what I have wanted. What I want is to have a very high filtration efficiency with another means.

<img src="/blogs/media/oitswilliamv2-is-going-5/IMG_9645.GIF" alt="RealEstate G2.1 in action."></img>

RealEstate, on the other hand, has been good. With the outer bezel of 1.2mm, making it the display mount for the flagship design. However, on the first generation, the frame joint is up, and the display joint is at the bottom, which made slight tilts easier, but can't tilt all the way where the screen face up, and the buttons are placed way too far on the side. So on generation 2, the buttons are placed on the top, and the joints are now bottom on the frame to top on the display. The next thing I want is the display with a rounded screen corners and some common features, such as having brightness adjustable through the computer settings, HDR compliant and HDCP, and might as well ditch the HDMI port for the flex cable connector that uses HDMI communication, but that needs driving up our innovation costs first. Another thing is I want new ways to physically interact.
 
## Current era
 
 Nowadays, OitswilliamV2 has mods that adds banger speakers, the thing that puts 30mm speaker raditators and 2-inch speakers into the printer, tracker mounts which allows to mount one of the trackers into the printer, and skirts made specifically for the single-board computers. But there is a thing that has changed my industry: The NUC mount. It is essentially the most ambitious part of the mod, and opened new gates.
 
## The future

OitswilliamV2 has not been finished yet, but there will be some exciting features where it bridges the great user experience. 

"Badass by design, intuitive on intent."

<img src="/blogs/media/oitswilliamv2-is-going-5/oitswilliamv2-logo-2026.svg" alt="OitswilliamV2 logo as of 2026." class="svg"></img>
This is the new chapter of OitswilliamV2, where we redefine the user experiences of the printer. From physical controls to on-screen, it will be the most significant change since the first FDM / FFF 3D printer.

### NUC skirt

The NUC skirt is the most insane part of OitswilliamV2. It is where indefinite possibilities made. The current mount allows mounting of short versions of NUC 12 Pro to 15 Pro. It will be the distant future of experiences.

### Neumorphism

Because we could drive graphics in real-time, we have introduced (partial) neumorphism to Mainsail [first through the custom CSS](https://gist.github.com/Bunny350/cf8a959f7bbcef1304f5af3403ffc4ca). But that isn't enough, and it is why we have decided to make tweaks to its internal layer, which is Vue, that adds living to the elements. At the same time, we will be making Mainsail more accessible with reduced motion, and reduced transparency, with forced settings available afterward. It is a mod, though, and I do enjoy the look of Apple's Liquid Glass physics, more than its looks.

### Next generation of tracker mounts

<img src="/blogs/media/oitswilliamv2-tracker.png" alt="OitswilliamV2 AirTag mount G4."></img>

The next generation of tracker mounts have simplified the design again. These mounts are made from scratch, due to previous generation's unoptimized parametric design scheme. Both AirTag and Galaxy SmartTag2 mounts were updated at the same time. The mounts have stashed screw requirements to just when attaching the inner bracket to the fan mount. For SmartTag2, the mount bracket is now the nut, just to make the tracker attachment easier and removal toolless, and for AirTag, the bracket can be attached or removed without any tools.

### RealEstate G2.3

A minor revision to RealEstate has released just to make the ports more accessible. It also renamed some obscure naming to more standardized ones.

### Exhaust Lite G3

The next version of Exhaust Lite is going to be the most significant, on the feature side, by adding the first Oitswilliam exclusive to the side of dirty air, which can rejuvenate the carbon pellets on every print finish. It will have a lock switch which makes filter changing easier yet toolless, and replacing the axial fan for the laptop blower fan. We might also try to insert the smoke detector just for the safety sake, and fit another temperature sensor just so it can report the environment temperature. When it comes with cross-compatibility, sadly, that is not cross-compatible with prior generations, as it is a major revision, except for the chamber cover, Bowden tube port, LED back and probably the camera mount.

## A new major category: Design

As I surf around the things, I decide to be like, why shouldn't I start my own design industry, and let others work for me and let me adjust them? And so, Oitswilliam Pang Design is born.
<img src="/blogs/media/oitswilliamv2-is-going-5/oitswilliam-pang-design-logo.svg" alt="Oitswilliam Pang Design." class="svg"></img>
This group, which included me, designs user interfaces for the future and provides icons made by everyone, adjusted by me. It is also responsible on making Mainsail with neumorphism makeover (as a mod). Users can view basic physics reference guides from such category next year. To those whose saying "Will Oitswilliam Pang Design replace (Oitswilliam Pang) Hardware and rival Voron Design?" I'm going to say "no," and which the Hardware can stay.

## Feeling staged, but it actually isn't

Before I unveil these to the public, I wanted to show these to some of certainly famous and infamous artists to see my neumorphism project. I'm still doing that, so [meet me while you still can.](/media) I am considered also meeting the lead developer of Mainsail and we at least say that will not apply to the base.

## Looking forward

The next generation of the tracker mounts were released. The NUC 12 Pro - 15 Pro skirt for Voron 2 150mm mod and RealEstate G2.3 is released today, under [OitswilliamV2 repository](https://github.com/Bunny350/OitswilliamV2). The new Mainsail mod is now in early-access, Oitswilliam Pang Design MKDocs will be released on fall of this year. Details of Exhaust Lite G3 with the first Oitswilliam exclusive feature from Hardware will be revealed next year and will go in alpha-EA (without Oitswilliam exclusive feature) within late of this year.

## Updates
* July 20, 2026 - Add an image for the tracker mount.
