---

date:
  created: 2026-04-01
links:
categories:
  - Announcement
  - Hardware
  - Oitswilliam Pang
tags:
  - 3D printing accessories
  - filament desiccant
  - announcements
authors:
  - oitswilliam
hero: /blogs/media/hd-desiccant/IMG_3933.jpg

printer_serial: V2.3347
printer_make: voron
printer_features: 
  - render

---

# HD desiccant holder - The new calibration model

The most banger calibration print that will rival every other single calibration prints, where this will shine.

<!-- more -->

Today, we are going to nominate HD desiccant as our standardized calibration model. This model is basically a useful thing that protects filaments from being too hygroscopic that cause in poor / garbage quality prints or even jam, but it has elements of torturing printers and filaments. This calibration model has cutouts, text and notches intended to test the printer quality.

<img src="/blogs/media/hd-desiccant/banger-render.png" />

## The chamfered top lid

The chamfered top lid is made for ease of assembly and disassembly. It is also a great way to test the printer's bed level, adhesion and -to-nozzle distance. The distance between the knurl edges are 1.2mm, perfect for checking whether the printer over-extruded. The lid also has a thin wall of 0.4mm, so it will force you to use Arachne slicer engine / wall generator instead of classic.

## The bottom holder

The bottom holder has 27 wide grilles around the perimeter, making sure that it has the maximum evaporating performance by airflow when being dried. It has 9 wide grilles on the inside, which also improves the drying performance. Not only that, due to the simple design, the top and bottom of the desiccant has nine grilles cutout (totaling 18 on both sides).

## The top cover

<img src="/blogs/media/hd-desiccant/IMG_3936.jpg" />

The top cover used to only have one variant, but until now. We have created a version that is foolproof, where it has large hexagonal brim intended to support / suspend the desiccant to the filament's inner roll.

## Mating, clicking and removal

<div style="display: flex; justify-content: center;">

<blockquote class="instagram-media" data-instgrm-captioned data-instgrm-permalink="https://www.instagram.com/reel/DVqocWHkwL2/?utm_source=ig_embed&amp;utm_campaign=loading" data-instgrm-version="14" style=" background:#FFF; border:0; border-radius:3px; box-shadow:0 0 1px 0 rgba(0,0,0,0.5),0 1px 10px 0 rgba(0,0,0,0.15); margin: 1px; max-width:540px; min-width:326px; padding:0; width:99.375%; width:-webkit-calc(100% - 2px); width:calc(100% - 2px);">

<a onCLick="loadIgScript()" href="#reels-loaded"><p style="text-align: center"> Load Instagram Reel </p></a>


<a href="https://www.instagram.com/reel/DVqocWHkwL2" target="_blank" style="font-size: 12px">If the embed did not load, or JavaScript for this browser or this website is disabled, please visit here to watch this video.</a>


</blockquote>

<script>
function loadIgScript() {
  console.log("test")
  var igScript = document.createElement("script");
    igScript.type = "text/javascript";
    igScript.src = "https://www.instagram.com/embed.js";
    igScript.async = true;
    document.body.appendChild(igScript);
}

  </script>
</div>

*Snappy sounds demo (Instagram)*

The unit has notch and cutout intended to secure the desiccant holder. The mating procedure seems simple, but the top cover has a cutout, and the bottom case has a small notch just for it. This allows making of snapping sound, but when you could not lock it or broke it while locking, it respectively means that the part has under-extruded or over-extruded, or the pressure advance values and / or input shaper are wrong.

## Intense R&D

HD desiccant has been torture-tested to make sure it is durable, even when printed in ABS. The previously released units had sharp top corners but these were not made optimized for FDM / FFF as it get weakened, except it in PC, but we don't want to require such exotic material. To solve this, the top is now chamfered and might as well make the bottom rounded.

## Material requirements

<img src="/blogs/media/hd-desiccant/IMG_3950.jpg" />

*Image may contain the unit in older revision.*

Don't get me started without saying this. This part requires a material that can endure in at least 60°C, meaning PLA can be out (unless if it's from Polymaker, and is HT version). ABS and ASA are the recommended materials for this part, but it's smelly when being melted, so PETG / PCTG are considerable. Although give PC <s>and PA</s> a try, but it will suck on the first try. They can be with or without composites (i.e. carbon or glass fiber, et cetera) For the desiccant, silica gel with diameters of 3 to 5mm is recommended.

## Drying / rejuvenation

To dry or rejuvenate the desiccant with the holder in, you can rejuvenate it by heating it in at least 6 hours, under medium heat settings, or 60°C. This is probably a major breakthrough when compared to rivaling desiccant holders with smaller or tighter meshes where it sometimes require  high heat settings while keeping the same drying time of six hours, or sometimes require longer.

## Customization

These holders are parametric, meaning we can adjust values on-the-fly, this is no exception. When you have some filaments that are in thicknesses thinner than usual, you can get its f3d source file[^fusion], or go to its MakerWorld site online[^bambu-account] and change the height to your desired.

Be noted that the height must be at least 35mm, otherwise the model will break. Although you can set it to virtually the printer's maximum allowed height, if you want to see whether the printer's Z axis sag, or slot it into multiple filaments.

## Availability

<img src="/blogs/media/hd-desiccant/IMG_3958.jpg" />

HD desiccant holder has already been released through [GitHub](https://github.com/Bunny350/HD-desiccant) for geeks and enthusiasts, including Voron users and has released recently in [MakerWorld](https://makerworld.com/models/2565724-hd-desiccant-holder#profileId-2827543) with starter packs[^bambu-account] for absolute beginners and Bambu users. Invasion to other printing platforms and OpenSCAD are considered but that would be in forseeable future. Users can even modify it with their liking, right now! And we have many of them made as well. Consider following Oitswilliam Pang on Facebook and Instagram after reading[^elaborate-scam-for-advertising-alpha-ea].

[^fusion]: Requires Autodesk Fusion. Despite Fusion can export STEP file, it is non-parametric.
[^bambu-account]: Requires Bambu Lab + MakerWorld account. Otherwise you may get them through GitHub. We want this model to be obtainable as easy as it can.
[^elaborate-scam-for-advertising-alpha-ea]: Hey, there are [upcoming](https://makerworld.com/community/post/1716971) [hardware](https://www.instagram.com/p/DWZXI-8EldR/) to be released within this year. Impatience? Follow Oitswilliam Pang in Facebook and Instagram and message in either platform to grant access to alpha-EA repository. Steps required, but testing needed!
