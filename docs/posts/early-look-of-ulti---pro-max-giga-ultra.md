---
date:
  created: 2026-08-23
hero: /blogs/media/early-look-of-ulti---pro-max-giga-ultra/banner.jpeg
categories:
  - Hardware
tags:
  - hardware
  - mods
authors:
  - oitswilliam
---

# The ULTI****** Pro Max Giga Ultra

I don't want to say the **** part of it cuz somebody will cancel me. This is the early look of my mod and considerations of it. Oh yea, for me, I have to wait until when UltiMaker discontinue the machine I have been using. 

<!-- more -->

Today, Oitswilliam Pang is going to detail around plans of this project. This involves in turning an UltiMaker machine, whether it is 3, S3 or S5, into a CoreXY monster machine.

## The joint

<img src="/blogs/media/early-look-of-ulti---pro-max-giga-ultra/teh_joint.jpeg" />

The gantry joint is easy to make, which allows printing of the same part instead of one-side adjusted. It allows changing what the belt path's supossed just by rotating, like Prusa's, but since it also mounts 1515 Misumi extrusion via its back, the lefthand one should already be upside-down.

<img src="/blogs/media/early-look-of-ulti---pro-max-giga-ultra/joint_whole_x_gantry.jpeg" />
*The whole X gantry... except without the linear rail, which will do later. Only *wish* can tell*
Because of the joint design, belt location and limits, I will place an MGN12 or even MGN9 linear rail to the front of the gantry.

## The delosional hotend

I will opt-in hotends for Bambu Lab H series (which at the same time P2 and X2 series) for cost and simplicity reasons. I have the knockoff ones intended for this. And yes, don't worry, I will use two.

Unfortunately, I also need to figure out how to **switch** hotends. Ignore the hotend lifting? No! We have to copy one part of UltiMaker's Print Core switching... although patented so no commercial purpose, except that I want a bump that shifts which means the machine will require full range of X axis. This is the easiest route. The most difficult route is just imitate the Bambu H2's switching method, via separate motors, but it will be more difficult than any standard Voron builds with an optional Voron Tap.

## I want to use Bambu's way of homing and bed leveling

I want to have inductive bed leveling sensor, except that I want it to sense on the top of the hotend, which means Bambu. I can work around by using Prusa's method where the whole hotend detects bend, but that will be if Bambu method don't work. What I want is to hook these inductive Eddy current sensors to the TI LDC1612 Eddy current sensor controllers, and then use the tap probing.

By the way, I will also ditch all of the mechanical end-stops, except the Z axis which may have better use than XY. The XY ones shall go to the bin.

## Direct drive is my favorite filament driving method

Direct driving the filament to the nozzle of the hotend is already a trend since CoreXY explosion all thanks to Bambu Lab, and Prusa for when 3D printing for end-users become a trend. I want to snuck a NEMA14, and yes, **a,** meaning one, because we also need to make the hotend lighter, which means I will require some sort of cam setup that de-tensions the opposite gear when the current gear engages, and reverse the extruder motion if in direction opposite of the opposite.

By the way, the alternative solution is already like ten times easy, you'll know, the current may involve with screwing the firmware. 

## 3G-force shall be the shaping goal

3G-force (around 29,430mm/s2) might sound too insane, but the goal of my things is to be insane, insanely fast machines faster than Bambu Lab. What, I've [always wanted a fast DIY 3D printer](https://github.com/Bunny350/srabbit-2) even before Bambu Lab has founded or their X1 fundraiser campagin.

By the way to get 3G-force in XY axes and AB motors, I might require a beefier stepper motors, drivers that can handle high voltages and you guess it, a 48V PSU dedicated to these axes.

## Klipper firmware
Because it needs.

Joke aside, I need to change its controllers that lost RepRap philosophy to the boards that end-users enjoy. There will be BigTreeTech Kraken or LDO Leviathan MCU, because I am going to drive AB motors in 48V as mentioned above, and a host computer of either upcycled??? Or SBC that currently have no use (that shall not be Raspberry Pi 5).

Hey, the most chosen 3D printer brand right now, which is not Prusa, might not obey RepRap philosophy. I have both brands to constantly play around, so whatever.

## Something's related

I am also having minds of having my own adventure game of the Minecraft world, around the skit I showed four years ago, but since I am lazy, it might take forever to do... like my old [Bunny 350 Adventure games](https://github.com/Bunny350/Miscellaneous-projects/tree/main/Abandoned%20projects) that canned due to my laziness.

This mod aside, UltiMaker made RepStrap machines before S-line, in which case that had lost the RepRap philosophy.

## Last thing, which is not related, but I'm not ending the interview event

I am still ready to interview with all the artists, partically those who draw characters in own design. So if you are in these profession, [do let me know here](https://www.oitswilliam.com/support), and [I will give you these](https://www.oitswilliam.com/interview-with-oitswilliam.html).

## Availability

ULTI****** Pro Max Giga Ultra will be compatible with UltiMaker 3, S3 and S5. As long as they share the gantry, later generations of the predecessors will also be compatible.

The printable joints and idlers for ULTI****** Pro Max Giga Ultra has been [released to the public](https://github.com/Bunny350/ULTI---Pro-Max-Giga-Ultra), while the CAD files for it will be [made exclusive to the followers of Oitswilliam Pang](https://www.oitswilliam.com/alpha-ea) until the project in my side is complete. It might release in December, but I don't know. [Just follow me on Facebook, Instagram and YouTube for the announcements OK?](https://www.oitswilliam.com/media)
