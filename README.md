# Mod Mmm PCB for the IBM Model M

This project is designed to replace all internal compoents of an IBM Model M keyboard.  The only thing that needs to stay is the curved steel backplate for the PCB to be mounted on.

Typing test video: https://youtu.be/bYVQCdWaI7s

![modmmm-18](https://user-images.githubusercontent.com/800930/232109322-dad95236-db6f-4ee4-b8dc-26e65340556f.jpg)
![modmmm-17](https://user-images.githubusercontent.com/800930/232109356-5c60572b-d0c1-467e-a8aa-fb8bb116f13a.jpg)

## Features

* Hotswap PCB for MX switches
* Multiple layout support, including ISO, split spacebar, and 4x5 numpad. [KLE link](http://www.keyboard-layout-editor.com/#/gists/e5cd226119123328166c9ac3b0ec58fc)
* PCB mount stabalizers
* Under-switch LED for caps, scroll, and num lock
* Supports up to 3 rotary encoders
* Piezo buzzer
* Solenoid
* Vial firmware

<img width="600" alt="Mod-Mmm-Layout" src="https://user-images.githubusercontent.com/800930/232115156-ab874c28-675d-408f-9d1f-ddae8f0cc6cb.png">

## The Build "Stack"

The following is a table of measurements of everything that's stacked on top of the steel backplate.  The key spacing was taken from hires scans I made of the Model M's wiring membrane.  I recalculated the spacing for each decrease in radius except for the foam where I reused the numbers from the switch plate.  I was lazy and figured foam can stretch anyways.

| Part            | Thickness (mm) | Radius (mm) | Radius Start | 1u vertical spacing (mm) |
|-----------------|----------------|-------------|--------------|--------------------------|
| Steel backplate | 1.0            | 276.635     | inner        | 20.617
| Hex Standoffs   | 4.0            | n/a         | n/a          | n/a
| Mod Mmm PCB     | 1.0            | 272.135     | center       | 20.560
| Plate Foam      | 3.5            | n/a         | n/a          | n/a
| Switch Plate    | 1.5            | 267.385     | center       | 20.201

![modmmm-1-3](https://user-images.githubusercontent.com/800930/232261815-2a74097f-7007-439b-a1be-f1e9512ef58a.jpg)

## Parts List

| Part                        | Count | Notes |
|-----------------------------|-------|-------|
| Mod Mmm PCB                 | 1     | 1mm FR4 thickness
| Mod Mmm Daughterboard       | 1     | 1.2mm FR4 thickness
| Blackpill (STM32F411)       | 1     |
| M2.5x3mm Wafer Screw        | 116   | [Link](https://www.aliexpress.us/item/2255800885711092.html?spm=a2g0o.order_list.order_list_main.22.1875180223MOsy&gatewayAdapt=glo2usa&_randl_shipto=US)
| M2.5x4mm Hex Standoff       | 58    | [Link](https://www.aliexpress.us/item/2251832790997097.html?spm=a2g0o.order_list.order_list_main.23.1875180223MOsy&gatewayAdapt=glo2usa&_randl_shipto=US)
| M2.5x5.5 Insulated Washer   | 58    | Probably not needed (step 8).  [Link](https://www.aliexpress.us/item/2255801049052739.html?spm=a2g0o.order_list.order_list_main.24.1875180223MOsy&gatewayAdapt=glo2usa&_randl_shipto=US)
| BAV70 Diodoe                | 55    | [Link](https://www.mouser.com/ProductDetail/Nexperia/BAV70215?qs=me8TqzrmIYX%252B%2FJ6jIjzNeA%3D%3D&countrycode=US&currencycode=USD)
| Piezo Buzzer                | 1     | [Link](https://www.digikey.com/en/products/detail/tdk-corporation/PS1240P02BT/935924)
| 5v Solenoid                 | 1     | [Link](https://www.digikey.com/en/products/detail/sparkfun-electronics/ROB-11015/6163694)
| Kailh Hotswap Sockets       | 10    4 | More sockets for non-ansi layouts
| FFC Connector (30 pos)      | 2     | [Link](https://www.digikey.com/en/products/detail/omron-electronics-inc-emc-div/XF3M-1-3015-1B/4331813)
| FFC Cable (30 pos)          | 1     | [Link](https://www.digikey.com/en/products/detail/molex/0151670470/3281723)
| 3mm LED (green)             | 3     | For status panel. [Link](https://www.digikey.com/en/products/detail/w%C3%BCrth-elektronik/151031VS06000/4489988)
| 2mm LED (white)             | 3     | For keycap status. [Link](https://www.amazon.com/gp/product/B01C5HL0PO/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&th=1)
| 470Ω Resistor               | 3     | For panel LED |
| 10kΩ Resistor               | 3     | For keycap LED |
| 22kΩ Resistor               | 1     | Pullup for pin A10 |
| TIP120 Transistor           | 1     | For solenoid. [Link](https://www.amazon.com/gp/product/B08212F42Z/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)
| 1N4001 Diode                | 1     | For solenoid. Comes with above kit |
| 2.2kΩ Resistor              | 1     | For solenoid. Comes with above kit |
| Mill-Max 315 sockets (1x20) | 2     |
| Mill-Max 315 sockets (1x4)  | 1     |
| Mill-Max round pin (¼in)    | 44    | [Link](https://www.mouser.com/ProductDetail/Mill-Max/3320-0-00-15-00-00-03-0?qs=s8Nb1z4Wn%2FQ16WBIwCPrTw%3D%3D&countryCode=US&currencyCode=USD)
| 2u plate mount stabalizer   | 7     | Count varies based on layout
| 7u plate mount stabalizer   | 1     | For 7u spacebar
| EC11 Rotary Encoder         | 3     | Optional [Link](https://www.mouser.com/ProductDetail/Bourns/PEC12R-4222F-S0024?qs=%252B9%2Fcbd0IE0SDcVz9RehHSg%3D%3D)
| Rotary Encoder Knob (17mm)  | 3     | Optional [Link](https://www.amazon.com/dp/B07K8589MJ?ref=ppx_yo2ov_dt_b_product_details&th=1)
| Switch plate (9 piece set)  | 1     | Optional 1.5mm acrylic
| Plate Foam                  | 1     | Optional 3.5mm EVA foam (or 2mm + [1.5mm](https://www.aliexpress.us/item/3256804208838525.html?spm=a2g0o.order_list.order_list_main.5.21ef1802FA7EIC&gatewayAdapt=glo2usa&_randl_shipto=US))

For the Mill-Max 315 series low profile sockets, I found it more cost efficient to just buy a really long socket and cut the sizes I need with flush cutters.  [Here's an example of a 1x64 socket.](https://www.mouser.com/ProductDetail/Mill-Max/315-93-164-41-003000?qs=WZRMhwwaLl%252BIMh92Iwf2Uw%3D%3D&countryCode=US&).  The only thing is that the edges are rough after the cut, but it doesn't bother me.

## PCB Build Guild

To complete this build, you will need to get the main PCB and daughterboard manufactured.  The main PCB will need to be **1mm thick FR4**, and I made the daughterboard 1.2mm to match the thickness of the original one that came with the keyboard.  I personally like using [JLCPCB](https://jlcpcb.com/), so I've included a `zip` file in the each respective directory that you can upload to their service if you decide to go with them.  (FYI, you will need to order a minimum of 5 boards each).

### 1) Disassembly
The first step is to disassemble your Model M and clean it if neccessary.  There are lots of tutorials online on how to do this, and make sure you have a 7/32 inch (5.5mm) socket for the case screws.  I followed this one from YouTube: https://youtu.be/VsIr8dl_7Kk.

The hardest part is removing the plastic rivets that holds the frame assembly against the steel backplate.  I used a razor blade with a few pieces of electrical tape wrapped around the back for better grip and for safety (to easily tell which is the sharp side).  I would then rock the blade around a rivet in a "see-saw" motion while putting pressure on the blade until it popped off.  It'd be a good idea to place some type of "backstop" like tall box to prevent the rivets from flying everywhere.

### 2) Shape PCB

Using the hex standoffs and a few screws, mount the PCB onto the steel backplate for 24hrs.  You only need enough screws & standoffs for the PCB to hold its shape.  After you remove the PCB, you want there to be a slight curve to the FR4 before soldering on the components.  This way, the componenets and solder joints experience less stress when the PCB is bent into its final shape.

### 2) BAV70 Diodes

Flip the PCB over to the backside and solder on the BAV70 diodes (D1 - D55). Place a dab of solder on the single bottom pad of the diode on the PCB. Then using tweesers, position the diode so that the legs line up with the pads. Then using the point of one tweeser leg, gently hold the top of the diode in place while melting the dab of solder that was placed on the bottom pad previously. With the diode now held in position, solder the top two legs to their respective pads.

### 3) Kailh Hotswap Sockets & Rotary Encoders

![build-1](https://user-images.githubusercontent.com/800930/232109711-958a86d3-5982-4581-a192-f5908ceb8127.jpg)

Place some solder on one of the hot swap socket pads. There should be enough solder to make a small mound. Place the socket into position and melt the mound of solder that was previously added while pressing down on the center of the socket. Be sure to avoid touching any metalic parts to prevent burns. Keep the soldering iron on the pad long enough for the solder to flow around the socket connector (usually around 3 to 4 seconds). Now solder the other socket connector to the pad.

You can replace any of the keys in the Print Screen cluster with a rotary encoder.  Just make sure you don't place a hotswap socket there, and solder the EC11 encoder there instead.

### 4) Status Panel LEDs and resistors

These three LEDs go under the status panel (NUM1, CAP1, and SCRL1).  The short pin of the LED goes in the square pad.  As for the accompanying 470Ω resistors (R4, R5, and R6), orientation does not matter.  The LEDs here can be soldered in with extra height so that they sit closer to the "window" on the case, but I have not measered out what that distance should be yet.  Should be easy to do with some putty.

### 5) Switch LEDs and resistors (optional)

These LEDs go under the caps lock, scroll lock, num lock switches.  Depending on your switch, you may have to solder these in AFTER placing the switch into the socket.  You can tell by looking under the switch to see if there's a hole big enough for the LED to fit through.  If there are only 2 small holes for the LED pins, then the switch needs to go in first.  The short pin of the LED goes in the square pad.  As for the accompanying 10kΩ resistors (R1, R2, and R3), orientation does not matter.

### 6) Stabalizers

Install your stabalizers of choice onto the PCB.  For the vertical stabs, in order to counteract the curvature of the PCB, I use those adhesive stabalizer pads and cut them in half lengthwise (band-aids would work as well).  I then placed them on the inside half of where the stabs would sit.  The idea here is to angle the stabs back outwards so that they remain parallel.

![build-3](https://user-images.githubusercontent.com/800930/232109738-f275d87e-9415-4e2d-bade-86b1453beb47.jpg)

### 7) FFC Connector

![build-2](https://user-images.githubusercontent.com/800930/232109728-c4e8625a-e991-4d46-b60f-215ca8008962.jpg)

This can be a bit tricky to hand solder, so take it slow, and use plenty of flux.  Place a dab of solder on one of the large pads on the side.  Position the connector on top of the pads making sure that the small pins are centered relative to their respective pads.  While holding the connector in place, melt the dab of solder that was placed earlier so that the one side is held in place.  Now solder the other end of the connector so that it's held in position.  Moving on to the the small pins, I initally tried "drag soldering", but I ended up bridging a lot of pins.  If this happens, just clean it up with some solder wick.

I found that the better way to do this is to pull out the sharpest tip you have for your soldering iron, and placing a tiny dab of solder on each pad, while avoiding touching the adjacent pins with the iron tip.  Again, make sure you use plenty of flux.  This way, the solder will simply flow around the pin without bridging the neighboring pins.

### 8) Center and Install PCB

![build-4](https://user-images.githubusercontent.com/800930/232109754-c7a9d37d-ef82-4177-98dc-f5aee326c10b.jpg)

Starting with the steel backplate, insert a screw from the back and screw a standoff on from the other side.  Keep it loose enough so that the standoff can rattle around a bit.  Do this for all the mount holes on the steel plate, even if you end up not using them because they're still good for support.  (Note that in my photo, I skipped some holes.  I need to verify that placing a standoff there won't interfere with anything).  You should also put a standoff in corner top-right hole beneath the plastic post for added support.

Slip the steel backplate back into the bottom of the case.  You'll need to slide the bottom into the slots first, and then place the plastic case posts into the top-left and top-right corners of the steel backplate.

Line up the PCB over the holes and place 2 or 3 screws positioned horizontally from each other near the center of the PCB.  Push the center firmly down onto the standoffs to force the PCB to bend (this part is a bit nerve racking, especialy when you hear creaking noises), and secure it the screws while holding it in place.

Now place a switch + keycap at the corner of every section of the keyboard (ex: Esc, F1, ~, Ctrl, Print, Num-Lock, Num-Enter, etc).  Put the top of the Model-M case on, making sure it's aligned and fully seated with no gaps.  Carefully shift the PCB around slightly to get the keycaps to be in the correct position with equal amounts of spacing from the keycap to the case walls.  Basically you're trying to center the PCB by eye-balling the keycap gaps.

With the PCB now centered, remove the top of the case and begin screwing in all the mounting screws.  I'd suggest starting near the center and spiral outwards towards the edges.  These is where you'll probably need to shift the loose standoffs around to line the holes up.  Also, if you run into the problem where the top and bottom screws bump into each other inside the standoff, you'll need to add an insulated washer to the bottom screw.  Place the top case back on every once in a while to make sure the PCB didn't shift and is still centered.  After you're done, remove the steel backplate from the bottom of the case and tighten all the screws on the back.  If you feel that the standoffs are just spinning while you're turning the screw, just squeeze the PCB and backplate together so that it pinches the standoff and keeps it from spinning.

NOTE:  I noticed that the vertical 2u stabs in the numpad were blocking some of the screw holes in rev 1 of the PCB.  I flipped the stabs in rev 2 which is the version in the repo.

![build-5](https://user-images.githubusercontent.com/800930/232109792-ce302813-35ad-433c-9974-7e55c47346c5.jpg)

## Daughterboard Build Guide

![modmmm-15](https://user-images.githubusercontent.com/800930/232109547-0ac0f0de-39c2-4030-99ee-314af0cae293.jpg)

### a) Solenoid Components
Bend the narrow part of the pins on the TIP120 back towards the heatsink at a 90 degree angle.  Solder it into place.

The 2.2k resistor goes into the R2.2 spot (orientation does not matter).  The 1N4001 diode goes in to the 1N4001 position where the line matches the printed line on the board.  The solenoid wires don't have an orientation, and you can solder them directly into the holes or use a header/connector.

### b) 22k Pullup Resistor

In order to use pin A10 on the Blackpill, a 22k pullup resistor is needed (according to the [QMK docs](https://docs.qmk.fm/#/platformdev_blackpill_f4x1)). Solder this into the R1 position.  Orientation does not matter.

### c) Blackpill Development Board

It's probably best to flash the firmware onto the Blackpill first using `bin` file in the `firmware` directory. Hook it up to [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases) and push the following buttons to place it in bootloader mode before flashing:
* Press and hold the BOOT0 button
* Press and release NRST (reset) button
* Release BOOT0 button

Solder the Mill-Max 315 sockets onto the daughterboard.  Then place a piece of masking tape over the pin holes, and insert each pin though the tape and into its hole with tweezers.  Then set the Blackpill into place with the components facing UP and the USB port facing the top of the daughterboard.  Solder the pins into place, and then carefully and slowly remove the Blackpill.  If you pull too fast and hard, one edge will suddenly pop loose, bending the pins on the opposite side.  Remove the masking tape, and push the Blackpill back into place.

Lazy-man's short cut: skip the masking tape.  But note that using too much solder will cause it to flow down the pin and into the socket.  If you do, the keyboard will still work, but you won't be able to remove the Blackpill without desoldering.

### d) Piezo Buzzer

Solder this into the BZ1 position.  Orientation does not matter.

### e) Assembly

![modmmm-11](https://user-images.githubusercontent.com/800930/232109607-c60fbea1-3cc1-49ef-b7e6-3e4ca23203c4.jpg)
![modmmm-10](https://user-images.githubusercontent.com/800930/232109664-8749dece-aa71-459b-9a81-3c33fcf8f381.jpg)

Remove the steel backplate from the case if you haven't already.  If you have a Model M with the smaller PCB, you will need to clip away the plastic holder to make room for the larger footprint of the daughterboard.  Make sure the clamp on the FFC connector is lifted up, insert the FFC cable, and press the clamp back down.  Place the daughterboard into position inside the case bottom.  I don't have a good way to secure it to the case (I'm reluctant to drill holes), so a piece of tape or double-sided adhesive foam will do for now.

Put the steel backplate with mounted PCB back into place, and connect the other end of the FFC cable to the main board.  At this point, you can install your switches and keycaps, screw the case back together, and be done!

BUT, after some testing, I noticed that my Kailh Box White switches were not very stable.  This is probably due to the fact they they were 3 pin switches instead of 5, and the hot swap sockets didn't grip the switch pins that tightly.  This is why I opted to make a switch plate to better hold the switches in place.  This also meant I had to cut 3.5mm thick foam (technically 2mm + 1.5mm) to act as a spacer between the PCB and the switch plate.

Unfortunately, there was not enough room in the case to house a single switch plate that spanned the entire board, so I had to break the plate up into smaller sections (9 total), which ended up working pretty well.  The Esc key had its own little 1u switch plate, so the stability still wasn't great, but it'll have to do.  I also messed up the foam spacing for the top row, so I had to cut it off as a separate piece.  This is fixed in the repo version, which is in the `plate-ansi` directory.

![modmmm-9](https://user-images.githubusercontent.com/800930/232112496-89a89cb3-0163-47f3-b9e9-8124393ee40b.jpg)

## Inspiration

I want to mention all the projects/products that has inspired the creation of the Model Mmm:

* [Model-H](https://modelh.club/): Open source USB controller for the Model M
* [Class 80](https://geekhack.org/index.php?topic=118401.0) by [MMStudio](https://mmkeys.com/): Premium TKL retro-styled board with a solenoid and buzzer
* [Command 65](https://geekhack.org/index.php?topic=117715.0) by [Play Keyboard](https://www.play-keyboard.store/): Retro-styled wireless keyboard with buzzer based off the Commodore 64
