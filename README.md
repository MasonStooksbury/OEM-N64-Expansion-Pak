[![License: CERN-OHL-P-2.0](https://img.shields.io/badge/Hardware_License-CERN--OHL--P--2.0-blue)](https://opensource.org/license/cern-ohl-p/)
[![License: MIT](https://img.shields.io/badge/Software_License-MIT-red.svg)](https://opensource.org/licenses/MIT)

# OEM-N64-Expansion-Pak | KiCad 8.0

![A picture of the custom OEM Expansion Pak running](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/pictures/Itdo.png?raw=true)

At long last! Here are the all the files you would need to create your own OEM Expansion Pak. All you would need to do is clone this repo, open the .kicad_pro file in KiCad, and you can poke around the files. [Here's a video of it working!](https://www.youtube.com/watch?v=sDxaTl5USwA)

I use this plugin in KiCad to make it super easy to order boards with all the correct settings: [https://www.pcbway.com/blog/News/PCBWay_Plug_In_for_KiCad_3ea6219c.html](https://www.pcbway.com/blog/News/PCBWay_Plug_In_for_KiCad_3ea6219c.html)

## Some things to note:

 - ***Unless you have a 4MB RAM chip, this board will not do you any good***. Most of the old stock you will find are 2MB chips. Don't fret, I have [another open source board](https://github.com/MasonStooksbury/Open-Source-N64-Expansion-Pak) that utilizes two of these chips so that you can make your own Expansion Pak. This one is just for historical reference. That being said, you can find instructions for ordering a board with the settings I use at PCBWay below in the "Making your own board" section if you happen to come across some 4MB modules, or you harvest them from a broken N64 (assuming you have the model with one 4MB chip as opposed to the ones with two 2MB chips)

 - The "ExpansionPak.pretty" folder is a library containing all the footprints needed for the project. Including the Edge Connector footprint created by Bigbass (check out more of his stuff here: [https://hachyderm.io/@bigbass](https://hachyderm.io/@bigbass) and here: [https://github.com/bigbass1997](https://github.com/bigbass1997/)). This saved me countless hours and pain, so a huge shoutout to him for allowing me to use it and release it

 - The schematic is probably not in an "official" format. But it's laid out in such a way that you can easily understand which pins on the Edge Connector are connected to which pins on the RAM chip. This was done on purpose as I feel it is a bit easier to understand for most people.

 - The pictured board and the render look different because I needed to change some things once I got the board. Namely, the corners were in the way of the original Expansion Pak mounting columns (if you look at an OEM one, they have cutouts). I also needed to modify the screw holes because they were too small.

Thank you so much to everyone who has followed along, commented, gave me feedback, and more. It's all very much appreciated and I'm excited to be able to give back. And another huge shoutout to Bigbass for allowing me to use their Edge Connector as it was a perfect fit and saved me countless revisions and lots of headache.


# Making your own board

## Installing necessary software, pulling the project, and uploading everything to PCBWay
 - First, download KiCad [here](https://www.kicad.org/download/)
 - Next, install the PCBWay plugin by following the instructions [here](https://www.pcbway.com/blog/News/PCBWay_Plug_In_for_KiCad_3ea6219c.html)
 - Clone this repository or download a ZIP of the files using the green button near the top right of the page
 - Open KiCad, then open this project by navigating to where you downloaded this repo and selecting the `.kicad_pro` file
   - ![Open project](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/pictures/instructions-01.png?raw=true)
 - Once open, click on the `.kicad_pcb` file to open up the PCB so we can begin to order it
   - ![Open project](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/pictures/instructions-02.png?raw=true)
 - From there, click the PCBWay button at the top right
   - ![Open project](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/pictures/instructions-03.png?raw=true)
 - KiCad should then automatically redirect you to a browser where it has opened up PCBWay and uploaded the necessary files so that you can begin ordering. Next we need to select all the correct options so that it will be made correctly.

## Selecting the correct options in PCBWay
 - Most of these options will be selected automatically, but be sure to set the ones in the red boxes as they are either structurally required or drastically affect cost
 - ![Open project](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/pictures/instructions-04.png?raw=true)
 - ![Open project](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/pictures/instructions-05.png?raw=true)
   - `Thickness`: This has to be 1.2 otherwise it will be too thick and you risk over-bending the receiver pins in the N64 
   - `Min hole size`: This tells PCBWay how small we need the holes for some of our vias
   - `Edge connector`: By far the most important setting. This tells PCBWay that we have what is called an `edge connector` (similar to how a RAM stick looks). That way they know to setup all the particular manufacturing stuff that is required to make these
   - `HASL lead free`: This is referring to the type of plating we want on our edge connector. Most commercial edge connectors are plated with a thin layer of hard material like gold since it can handle being seated/unseated multiple times better than most other materials. However, it's *really* expensive. I encourage you to select it just to see the price jump lol. That being said, `HASL lead free` is good enough for the Expansion Pak because you won't be removing it all that often, and even if you do, it's plenty hard enough to handle it. I pick the lead free variant cause I don't want to die early from lead poisoning
   - `Surface finish`: This is the plating that will appear on the pads where you will solder things to. `HASL lead free` is plenty good enough for this and also helps with cost
   - `Remove product No`: PCBWay adds a tracking number to the silkscreen of your boards so that their manufacturing process is a little easier. You can select the `Yes` option here and pay a little extra to have them not add that. It's not a huge deal, but something to be aware of.

![KiCad view of the electrical schematic](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/pictures/schematic.png?raw=true)
![KiCad render of the front of the Expansion Pak](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/pictures/front.png?raw=true)
![KiCad render of the back of the Expansion Pak](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/pictures/back.png?raw=true)
