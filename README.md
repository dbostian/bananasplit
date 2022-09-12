# Banana Split

## Intro
Everyone’s favorite potassium packed, slightly radioactive, 105 calorie macropad is back! This time in a split wireless version. 3d print your own today!

![imgur](https://i.imgur.com/SoshcnY.jpg)
![imgur](https://i.imgur.com/ID31t6S.jpg)

## FAQ
**Q) [Again](https://github.com/dbostian/banana)?**

A) The opportunity was ripe for the taking.

**Q) How will I know if a split macropad is right for me?**

A) You’ll peel it in your bones.

**Q) Should I lube my switches?**

A) Go for it, but try not to slip!

**Q) Is this ortholinear?**

A) I would argue it is the most ortholinear of all the fruit.

**Q) How do I introduce myself in polite banana company?**

A) “Yellow, everyone.”

**Q) What’s your favorite programming language?**

A) Not sure if I have a favorite, but Javascript is `('b' + 'a' + + 'a' + 's')`

**Q) This FAQ is causing me physical pain.**

A) You can plantain all you want, but the puns will not stop.


## Thanks
A big thank you to [Keebio](https://keeb.io/) for releasing an [awesome set of KiCad libraries](https://github.com/keebio) for keyboard components. This saved me a ton of work.

## Tools + Materials
![imgur](https://i.imgur.com/d2F4gDC.jpg)

### Printed Parts
- [ ] 1x top_left.stl - [https://github.com/dbostian/bananasplit/blob/main/stls/top_left.stl](https://github.com/dbostian/bananasplit/blob/main/stls/top_left.stl)
- [ ] 1x top_right.stl - [https://github.com/dbostian/bananasplit/blob/main/stls/top_right.stl](https://github.com/dbostian/bananasplit/blob/main/stls/top_right.stl)
- [ ] 1x bottom_left.stl - [https://github.com/dbostian/bananasplit/blob/main/stls/bottom_left.stl](https://github.com/dbostian/bananasplit/blob/main/stls/bottom_left.stl)
- [ ] 1x bottom_right.stl  - [https://github.com/dbostian/bananasplit/blob/main/stls/bottom_right.stl](https://github.com/dbostian/bananasplit/blob/main/stls/bottom_right.stl)
- [ ] 2x fruit_slice.stl - [https://github.com/dbostian/bananasplit/blob/main/stls/fruit_slice.stl](https://github.com/dbostian/bananasplit/blob/main/stls/fruit_slice.stl)
- [ ] 1x battery_clip.stl - [https://github.com/dbostian/bananasplit/blob/main/stls/battery_clip.stl](https://github.com/dbostian/bananasplit/blob/main/stls/battery_clip.stl)

### Electronics
- [ ] 1x Banana Split PCBs - [https://github.com/dbostian/bananasplit/blob/main/pcbs/banana_split.zip](https://github.com/dbostian/bananasplit/blob/main/pcbs/banana_split.zip) - I ordered mine from Osh Park
- [ ] 1x nice!nano - [https://nicekeyboards.com/nice-nano/](https://nicekeyboards.com/nice-nano/)
- [ ] 1x 301230 Battery, with JST connector
- [ ] 1x JST Pigtail
- [ ] 1x SPDT Switch (PCM12SMTR - Digikey 401-2016-1-ND)
- [ ] 2x 12 pin Machine Sockets, Standard Length (Mill-Max 310 - Digikey ED11164-ND)
- [ ] 24x Machine Pins (Mill-Max 3320 - Digikey ED1134-ND) - order some extras
- [ ] 2x TRRS Jacks (PJ-320A)
- [ ] 8x Diodes (1N4148)

### Components
- [ ] 8x Switches - Cherry MX or compatible
- [ ] 8x Keycaps
- [ ] 1x TRRS Cable
- [ ] 1x USB C Cable
- [ ] 1x Sticker (not optional)

### Hardware
- [ ] 6x M3 x 16mm Socket Cap Machine Screw
- [ ] 6x M3 Heat Set Inserts

### Tools / Misc
- [ ] 3d Printer + Filament
- [ ] Soldering Iron + Solder
- [ ] Multimeter
- [ ] Wire Cutters / Strippers / Flush Cutters
- [ ] Hex Drivers

### Firmware
- [ ] ZMK Shield - [https://github.com/dbostian/bananasplitfirmware](https://github.com/dbostian/bananasplitfirmware)

![imgur](https://i.imgur.com/ZUsIklv.jpg)

## 3D Printing Notes
I printed mine in PETG at 0.20 mm layer height and with 15% infill. Enable support material for the shells. I used [ironing](https://help.prusa3d.com/article/ironing_177488) to get a nice finish on the fruit slices.

## Soldering Notes
The [nice!nano documentation](https://nicekeyboards.com/docs/nice-nano/getting-started) recommends a cool-ish soldering iron temperature - and also recommends triple checking your battery polarity. Please give this a read.

## Assembly
First, install the heat set inserts into the top shells. The ones nearest the middle should be installed deep enough so that they clear the PCB.

![imgur](https://i.imgur.com/LIgOknD.jpg)

Solder the diodes, TRRS jacks, and power switch to the PCBs.

![imgur](https://i.imgur.com/vXUvEQH.jpg)

Next, solder the machine headers to the board. I used the MCU to establish position as I soldered the corner pins into place, then removed it before soldering the remaining header pins. Then, solder the MCU to the pins. Use tape as suggested in [this socketing guide](https://www.40percent.club/p/socketing-pro-micro.html) to prevent permanently attaching things. Note that the tiny b+ and b- holes are not used.

![imgur](https://i.imgur.com/IKyvBmO.jpg)

Attach the JST pigtail to the PCB. Leave the battery disconnected during this step. Trim the back side of the wires flush.

![imgur](https://i.imgur.com/zQQ3jkQ.jpg)

Gently pry the MCU from its socket, and set aside. Snap your switches into the top shells and  solder the PCBs in place. Reinstall the MCU. 

![imgur](https://i.imgur.com/hDfkkjr.jpg)

Now’s the time to flash your favorite firmware and test. I am using [ZMK](https://zmk.dev/) - you can clone my sample firmware repo [here](https://github.com/dbostian/bananasplitfirmware). Running other firmware? The switches are wired into a 2x4 grid, connected to digital pins 8 & 9 (rows) and 4, 5, 6, & 7 (columns).

Connect the battery and secure it into the base with the clip. Assemble the 3d printed shells using M3 screws. Don’t forget the decorative fruit slices!

![imgur](https://i.imgur.com/Er1oeVY.jpg)

Lastly, add your keycaps, apply the sticker, connect the halves with the TRRS cable, and enjoy!

![imgur](https://i.imgur.com/XxVJOgu.jpg)


