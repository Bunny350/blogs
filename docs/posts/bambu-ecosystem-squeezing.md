---
date:
  created: 2025-01-21
  updated: 2025-01-22
tags:
  - reactions
  - ecosystem
categories:
  - Reactions
authors:
  - oitswilliam
---

# Bambu ecosystem squeezing, or is it?

Today is a talk about not just recent, but what I think is the biggest controversy that's bigger than A1 wire burning; its security enhancements, called Authorization Control System. Bambu claims that this will reduce remote attacks and exposures, and my thought, is in case if someone is stupid enough to open it via port forwarding. But people think it's a step ahead of squeezing the open ecosystem.

- Note that I am a [proud owner of Bambu's A1 Mini 3D printer](https://www.facebook.com/share/v/1Z2qqtiCfu/),  has two Voron printers (V2.3347 and V0.2378), but uses the normal Bambu Studio as it is ok to me. Other printers such as UltiMaker S3 and the 7-year old but *short-lived* idbox 3D printer that uses another slicer called UltiMaker Cura. And I am now designing a self-designed printer that is based of Voron Trident and FrankenVoron Tridex.

## Before this, let's take a look at other, valid controversies

* Bambu Lab sued by Stratasys with 8 patents, with half of them intended to troll Bambu and one of it being the same patent. [hope it's least controversal, but still ongoing]
* A1 wire burn [was the biggest before, addressed within two months].
    * The bed wire will burn if not properly bent. At least Bambu Lab recalled all pre-addressed A1 printers after two cases.
    * New batches after recall has addressed bed wires that no longer cause unintended burns.
* [Decryptable printer log](https://www.youtube.com/watch?v=f-IjIs4YA-4) [addressed].
    * Bambu Lab's printer control software aren't using GPL-licensed software, like Klipper or Marlin. Even though for X1, [Linux and the components are listed open-source](https://wiki.bambulab.com/en/knowledge-sharing/open-source-software).
    * You should see why Bambu Lab started development of their first printer on September of 2020 and unveiled it 20 months later, while others "copy" within five months and put open-source software, don't you?
* [Thermal runaway test "fail"](https://www.youtube.com/watch?v=6hS2dQX_RM4) [addressed]
    * The ceramic heater can add resistance and resist generation under heat. For this in X1 and P1, the ceramic heater can heat up to around 400˚C before it no longer heats due to excessive resistance. Although it's still high, it's better than the standard heater cartridge where it can glow so insane that it melt the aluminum off.
    * This was before any A-line printers release, but anyway, in A1 line of printers, and the future non-A-line printers that will use hotends for the A-line, they will predict if the hotend is present, and if it detects that the temperature rises up abnormally, it will stop heating. That is if you don't enable maintenance mode.
* Bambu Studio was based of PrusaSlicer [addressed].

## Now let's get back to current

The Authorization Control System is a feature that lets printer require keys before being controlled, It can only be from first-party slicer app and companion apps (unless otherwise if they change decisions). This feature does *not* limit statistical interactions or starting a print job that's already on the card, among other things, but it limits control-related interactions and other critical operations. Users who do not want this feature can keep their firmware, but not if they received the printer with this firmware from start, cause this does *not* let them downgrade the firmware.

## Why did it became controversal?

This has been fallen down to three sections, closing down the ecosystem, easy reverse engineering and dated terms.

### Closing down the ecosystem

This move has been known that it will affect community-maintained slicers, Home Assistant automations and dedicated controller devices (i.e. BTT Panda Touch). To address this, Bambu has unveiled a dedicated companion app called Bambu Connect that allows sending print jobs outside Bambu's own "unmodified-by-community" slicer and it's mobile companion app, and control the printer like on own slicer. I think not everyone likes this, as it adds three additional steps, and jogging the printhead will become cumbersome.

People have said that this is a step ahead of becoming the HP (inkjet) printers in 3D (or of 3D printing), where they will not do anything, including scanning if one ink was empty, or beg for subscription. Or even worse, they will no longer support generic or third-party filaments, I myself included, which Bambu said [they don't have intent on this](https://blog.bambulab.com/updates-and-third-party-integration-with-bambu-connect/) [or never; the other was over two years ago](https://blog.bambulab.com/to-open-or-not-to-open-that-is-the-question/). At least my Canon paper printer does anything, even print, and even if the ink is empty. I can also use non-Canon cartridges to print on papers, even though losing exclusive features that can only be accessed on the Internet, but I have never tried it.

### [Easy reverse engineering](https://wiki.rossmanngroup.com/index.php?title=Bambu_Lab_Authorization_Control_System)

Since Bambu Connect used Electron as it's base, and not using in-house encryption, people have figured out [how to crack down the keys used by Bambu Connect, within a day of it's beta release](https://www.reddit.com/r/BambuLab/comments/1i4k9m2/bambuconnect_has_been_pwned/). And has been shared to the wiki that's against companies abusing their customers. The key might be rotated later.

### Dated terms

[Louis flamed the responsibility of baseless allegations back to Bambu](https://www.youtube.com/watch?v=W6MybDJfmmY) when he got gaslit by Bambu's tactics of trying to remove archives captured by third-parties and the list of things that Bambu will not do when compared with the ToU.

I have pointed out that section 7.4 of the terms of use has explicitly said that users may no longer send new print jobs if new (stable, not beta) updates are found, but on the blog post regarding the controversy said (let's just say) this update is optional. This has confused a lot of people into thinking to update, per ToU, or not, for the sake of third-party integrations.

What I think is they missed the terms "Unless if explicitly specified," or "unless if the update is marked optional".

## Is this addressed?

Currently, I doubt it, but they have addressed most problems including solving LAN mode requirements being too strict by introducing developer mode in LAN mode. This allows third-party integrations to control the printer, but have to sacrifice for local intruders who play tricks with your printers remotely, yep "local" because there is no proof on this mode allowing remote attacks from the Internet.

They are also ready to talk with accessory vendors on gaining such restricted features.

Maybe this feature was made for users who have zero knowledge of networking, but still I doubt if this feature actually work against brute-force attack or something like that.

If you have things to point out, please send message on my Facebook [page](https://www.facebook.com/officialbunny350/), or email me yo [at] oitswilliam [dot] com.

*Short update*: add new links, clarify ownership and add suggestion information
*Short update 2*: forgot to add introduction and forgot about the actual name yeesh
*Update on January 22*: specified new reason on why Louis got gaslit
