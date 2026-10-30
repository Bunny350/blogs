---
date:
  created: 2026-10-24
  updated: 2026-10-30
hero: /blogs/media/v2-wire-breaking/IMG_2230.jpeg
categories:
  - Hardware
tags:
  - hardware
  - reactions
  - research
  - storylines
authors:
  - oitswilliam
---
# V2.3347 wire breaking and it's defective by design
Today's post is all about V2.3347 wire didn't stop breaking like mouse hunt and why Voron's cable recommendation on standard machines is defective by design.

<!-- more -->

!!! note
	This is still ongoing. Once done, I will make a video about it. Followers of Oitswilliam Pang who's joined in alpha-EA can view the BOM of V2.3347 painlessly, although that isn't the point.

I was going to publish this post early, but as I am lazy right now, I published it in conjunction with where the second generation of the banger speakers also release. Perfect times aside.

A long time ago, probably four years ago, when I decided to upgrade my V2 to revision 2 of V2.4, I decided to follow the recommended cable insulation material from the BOM of Voron Design. However, the cables went rough, constant breaking, so I've decided to [include the combs](https://www.thingiverse.com/thing:6415912) in TPU and organized the cable arrangement, but then the issue happened again, sometimes inside the comb, and other times in the position of the zip ties. I was like "what the hell," replaced the wires and then in one day, even went like mouse hunt, hunt down the broken cable, 5V, then GND and then got enough with one of the stepper motor wire.

## Standard machines have cable-chain unless it goes umbilical

Standard machines use cable chain, that's what the article is saying, and **no, [going with a CAN or USB toolhead alone does not help,](https://www.reddit.com/r/VORONDesign/comments/zaeyiw/comment/iyliqui/)** because you should, or will know that this is the cable's issue, although this is not where main MCU controls the extruder. The only way to solve the problem is to go umbilical where it allows for a larger bend radius, or go fine-stranded, which allows for a smaller bend radius. In this page, we're not working around with the umbilical because that is too easy and I would rather keep the cable chains.

## How many strands is it considered acceptable? Or should the strands' diameter be very small? Among other things that reduce breakage.

That is a question. I have checked the strand count and the strands' diameter of typical FEP wires from Voron BOM, which are lost, yipee! But there were previously, judged by its standard **UL1332** from [LDO Motors](https://docs.ldomotors.com/en/voron/toolhead_harness#the-toolhead-cable), like for example, 22AWG be 19 and 0.14mm, whereas the wires used by the Stealthburner toolhead PCB, including what V2.3347 do, 20AWG and 24AWG, are 19 & 0.18mm and 7 & 0.19mm respectively. Unfortunately, these wires broke during wear in the chain, some even after adding the combs and a greater amount of zip ties, which really pisses me off.

<img src="/blogs/media/v2-wire-breaking/IMG_5261.jpeg" alt="UL1332 FEP wire with its exposed conductor strands, in 24AWG." title="UL1332 FEP wire with its exposed conductor strands, in 24AWG." ></img>
*UL1332 FEP wire with its exposed conductor strands, in 24AWG.*

By the way, I have checked the igus' one, chainflex CF130.02.xx.UL, in 0.25mm2 (24AWG equivalent) where they probably have around 26 strands, equivalent to somewhere like 0.1mm, judging by the listing photos. I am lazy and don't want to completely fuss with it so I leave it, unless Voron decides to nominate this or something similar as the recommended cable for non-CAN or USB toolhead solutions.

And then there's [something enormous](https://www.chargerlab.com/teardown-of-apple-240w-usb-c-charge-cable-a2794) that's commonly seen in today's braided USB-C cables, and that's twisted wires in all and in-conjunction with the tensile cord. Although it seems that they are not using any of the FEP cables. I have these cables, probably many, but I am not gonna cut one of them for the sake of use until it stops working properly.

## There is a commonly-seen variant of fine-stranded FEP wire! Should I use it?

<img src="/blogs/media/v2-wire-breaking/IMG_5292.jpeg" alt="AFR250 with its exposed conductor strands, black in 24AWG and orange in around 20AWG." title="AFR250 with its exposed conductor strands, black in 24AWG and orange in around 20AWG."></img>

The wire in question is AFR250, the FEP wire with the fine-stranded conductor. However here is the issue: the insulator is wrapped, not something like "extruded", meaning that the cable may have a risk of getting unwrapped by external factors. I may be concerned that the insulation midway will be pulled. I've tried using it, but then it has its insulator suspiciously protruded after multiple chain bends. It is also not smooth either, as applying force to the wire moving side-to-side perpendicular against the edge can get the film stripped. I do not want to short electronics and potentially burn the hardware down.

Oh, and by the way, it has an acceptable strand diameter, which we'll learn after phases.

### How about the silicone?

I could have been used silicone wire and put them in 4\*4 array, but they are rough, and since its insulator is soft and weak on tensile strength, it can be peeled off easily.

## Phase 1, in 2025, trying to use the PUR-insulated chain cable

<img src="/blogs/media/v2-wire-breaking/IMG_2230.jpeg" alt="UL1332 wire broken before the first phase." title="UL1332 wire broken before the first phase."></img>

*UL1332 wire broken before the first phase.* The image was supposed to be on November of 2024. That time it was also before wire combs.

The first phase of it is to use the chain cable that claimed to be able to be rolled 30-million times, as the heater cable (20AWG) broke. It works, but because the chain end is popping off, I've decided against it.

<img src="/blogs/media/v2-wire-breaking/IMG_5322.jpeg" alt="The PUR-insulated cable for reference. This was made for my Voron 0 until I found out the problem before it gets installed." title="The PUR-insulated cable for reference. This was made for my Voron 0 until I found out the problem before it gets installed." ></img>
*The PUR-insulated cable for reference. This was made for my Voron 0 until I found out the problem before it gets installed.*

The cable requires a larger bend radius just to properly run, but because the standard cable chain in Voron requires a smaller bend, it created tension, which was why the chain end popped off.

Another reason on why I'm against it is because the 12-wire 0.25mm2 variant in conjunction with 2-wire 0.3mm2 stops fitting into the chain that V2.3347 was using properly.

<img src="/blogs/media/v2-wire-breaking/IMG_5320.jpeg" alt="The strands of the one wire of the PUR-insulated cable." title="The strands of the one wire of the PUR-insulated cable." ></img>
*The strands of the one wire of the PUR-insulated cable.*

By the way, why isn't there any phases from 2023 but before 2025? Well that's because the FEP cables were probably replaced during the MCU swap before the cables broke, or maybe I did not post insane cable breaking posts before.

<img src="/blogs/media/v2-wire-breaking/IMG_5264.jpeg" alt="The obscure fine-stranded PTFE wire from Mellow and Moons, with its exposed conductor strands." title="The obscure fine-stranded PTFE wire from Mellow and Moons, with its exposed conductor strands, in 24AWG."></img>

I've also seen the PTFE cable of what the included Moons' motor from Mellow for Clockwork 2, they are unlike what I was holding, they're fine-stranded. Unfortunately, their rarities are legendary, and I could not find them in common shopping platforms, although I got it... just read the rest of the page.

## [Phase 2](https://www.facebook.com/share/p/18LVhszSSM/), also in 2025, cable combs + zip tie
When my first phase got out, I've decided to implement the cable combs for V2.4 from Thingiverse, but I have a twist: print it in TPU, not any of it, but the hard TPU for AMS. This is then added with the zip ties on every two combs just so that it will not touch the chain.
It worked for a year, until one of the wires on the Y axis broke.

## Phase 3 - two zip-ties on one cable comb

This is when I've fed up with another one of the wires breaking and decided to implement two zip-ties per comb.

Well it worked for some time, until the other cables decided to break inside the comb.

<img src="/blogs/media/v2-wire-breaking/IMG_5211.jpeg" alt="One of the wire broken inside of zip ties, note that the zip tie did not have sharp corners but the wire still managed to break." title="One of the wire broken inside of zip ties, note that the zip tie did not have sharp corners but the wire still managed to break."></img>

*Note that I have added arrows and circles to the "supposed culprit" or innocent culprit and the broken wire, as not all people can find these.*

At this time, I am pissed off further as the 5V and ground cables break down in the comb, and so one of the extruder motor cables in the zip tie. Because of that, I really want to get the similar wire as what the Moons' extruder motor for Clockwork 2 has, and I am glad I did.

## Phase 4 - soft migration from UL1332 to fine-stranded PTFE wire (that isn't AFR250)

This phase is in, after the find of the fine-stranded PTFE wire that is legendary in terms of rarity by me, whatever that means, Because I am lazy, I have decided to migrate one wire then it breaks, however I will do the research on both of these wires. 
This is where I have to reprint the combs in normal TPU 95A as these in TPU for AMS broke as well.

<img src="/blogs/media/v2-wire-breaking/IMG_5258.jpeg" alt="AF46R-200 / AF200 with its exposed conductor strands, in 24AWG." title="AF46R-200 / AF200 with its exposed conductor strands, in 24AWG."></img>

The wire in question is AF200R, or **AF46R-200**. It has the best of both worlds, the insulation of UL1332, and the strands of AFR250. It can sustain most of the stress for the PUR-insulated cable that normal UL1332 FEP wire can't, although it is epic in terms of my rarity. Uhh do note that this is probably not the same as Moons or Mellow had (at least for Clockwork 2), despite them probably having the same strand diameter of 0.08mm and insulation method that aren't wrapped.

## But why is Voron's wire selection defective by design

The Voron's wire selection of UL1332 is defective by design, especially on what Stealthburner PCB recommend (24AWG), is because of its coarse strands. and a low strand count, also especially on what Stealthburner PCB recommended (7 strands). Because of these, the wires are not made for continuous moves inside the cable chain, doing that poses risk of wire breaking within 400 print hours, and thus that's why I do not recommend these wires inside cable chains ever, and marked the cable selection defective by design.

The cable combs helped, but the cables still managed to break; that isn't the comb's problem, but rather the wires themselves.

The moving cable in the chain is where wires or cables require a finer strand diameter (of 0.08mm). But that doesn't mean it can always use a fine strand as it could break for being too fine, as opposed to being too coarse in my cable breakage cases in V2.3347, so that's why people have set-up strand limits, such as 63... although they want people to acquire larger radii for cable chains with these strand-limited cables. Or very high gauge like 30AWG, as some cables using these were already broken by me just by typical bends. And oh yea, the fine-stranded wire can entangle much more prominently, as it is softer to flex, which is why I have decided to make the wire spools that can be made like Bambu's reusable spools, just to make sure it doesn't be tangled.

Wrapped insulation allows for denser wiring, it is, however, commonly seen in (not microwave oven) transformers, but for my application, it is on the speakers. I tried using it in the cable chain, only to be found that the insulation have risk of peeling off, which is why these, such as AFR250, are not recommended for being used or moved in the cable chain.
AF46R-200 will be the wire V2.3347 slowly stick on, as it has good insulation and strands, although it has the rarity of epic.

I hope the wire I choose lasts forever. The progress is still ongoing, once done, I will update the post and then upload the video. Thanks for reading.

## Updates
October 30, 2026 - upload the images of the PUR-insulated wires
