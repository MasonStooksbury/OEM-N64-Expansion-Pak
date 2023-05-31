# OEM-N64-Expansion-Pak

![A picture of the custom OEM Expansion Pak running](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/Itdo.png?raw=true)

At long last! Here are the all the files you would need to create your own OEM Expansion Pak. All you would need to do is clone this repo, open the .kicad_pro file in KiCad, and you can poke around the files.

I use this plugin in KiCad to make it super easy to order boards with all the correct settings: [https://www.pcbway.com/blog/News/PCBWay_Plug_In_for_KiCad_3ea6219c.html](https://www.pcbway.com/blog/News/PCBWay_Plug_In_for_KiCad_3ea6219c.html)

## Some things to note:

 - ***Unless you have a 4MB RAM chip, this board will not do you any good***. Most of the old stock you will find are 2MB chips. Don't fret, I'm working on another open source board that will utilize two of these chips so that you can make your own Expansion Pak. This one is just for historical reference

 - The "ExpansionPak.pretty" folder is a library containing all the footprints needed for the project. Including the Edge Connector footprint created by Bigbass (check out more of his stuff here: [https://hachyderm.io/@bigbass](https://hachyderm.io/@bigbass) and here: [https://github.com/bigbass1997](https://github.com/bigbass1997/)). This saved me countless hours and pain, so a huge shoutout to him for allowing me to use it and release it

 - The schematic is probably not in an "official" format. But it's laid out in such a way that you can easily understand which pins on the Edge Connector are connected to which pins on the RAM chip. This was done on purpose as I feel it is a bit easier to understand for most people.

 - The pictured board and the render look different because I needed to change some things once I got the board. Namely, the corners were in the way of the original Expansion Pak mounting columns (if you look at an OEM one, they have cutouts). I also needed to modify the screw holes because the were too small.

Thank you so much to everyone who has followed along, commented, gave me feedback, and more. It's all very much appreciated and I'm excited to be able to give back. And another huge shoutout to Bigbass for allowing me to use their Edge Connector as it was a perfect fit and saved me countless revisions and lots of headache.

![KiCad view of the electrical schematic](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/schematic.png?raw=true)
![KiCad render of the front of the Expansion Pak](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/front.png?raw=true)
![KiCad render of the back of the Expansion Pak](https://github.com/MasonStooksbury/OEM-N64-Expansion-Pak/blob/main/back.png?raw=true)
