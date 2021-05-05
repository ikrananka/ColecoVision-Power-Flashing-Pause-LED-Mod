# ColecoVision Power/Flashing Pause LED Mod

## Introduction

This mod for the ColecoVision games console has two functions.  The first is to provide a continuously lit red power LED.  This LED will illuminate whenever the ColecoVision is turned on and not paused.  The second function is to provide a hardwired, physical switch, to pause operation of the ColecoVision allowing you to pause a game at any point and resume play at your leisure.  A unique feature of this mod is that when paused the power/pause LED flashes to indicate that the system is paused.  The rate of flashing is user adjustable from 0.6 to 3.3Hz.  When pause is turned off the flashing LED reverts to being continuously lit (until the system is either paused again or is turned off).
The pause function is achieved by pulling the WAIT line of the ColecoVision’s Z80 CPU low.  This in effect pauses all Z80 processing and therefore pauses the game you’re playing.  However, the audio is not paused and will continue to emit the last note/tone which can be very annoying.  Therefore, this mod not only pauses the Z80 processor but also disconnects the audio output whenever pause is engaged.

The Finished Product
![](https://github.com/ikrananka/ColecoVision-Power-Flashing-Pause-LED-Mod/blob/main/images/Installed%20Mod.JPG)

## FAQ

Q.	Will this work with Super Game Module (SGM1) games?

A.	Yes (if you wire the audio as recommended later in this document).  All SGM enhanced games still use the Z80 processor and so they will pause when the Z80 is paused just like any other ColecoVision game.  However, SGM enhanced audio is fed to the ColecoVision via the expansion port (EXAUD), bypassing the ColecoVision’s onboard sound from the SN76489A.  Therefore, it is important that when paused, audio is disconnected from a location after the point where audio from the SN76489A and EXAUD combine.  This is easy to do and instructions for this are provided later in this document.

Q.	Will this work with the upcoming Super Game Module 2 (SGM2)?

A.	Yes and No.  According to the latest information from Opcode Games, the SGM2 will be backwards compatible with SGM1 games and the pause mod will function in the same way as described in the answer above.  However, SGM2 specific games will use the new Z80 and/or 16-bit CPUs that are contained in the SGM2 unit and these cannot be paused using this mod.  However, Opcode Games has stated that “pause will be implemented in software for these games because of the dual CPU design” and so a hardware pause solution is not needed.  You never know, perhaps Opcode Games will make the SGM2s power LED flash when a game is paused!!!

Q.	Does this work with the Expansion Module #1?

A.	No.  The expansion module #1 uses its own processor and audio chip and like the SGM2 cannot be paused by this mod.  Be aware that moving the pause switch to the pause position while playing an expansion module #1 game may disconnect the audio so leave the switch in the normal position when playing these games.

Q.	Is the mod reversable?

A.	The mod is mostly reversable other than the fact that you must drill two large holes in the ColecoVision’s top housing.  These holes are obviously not reversable.

Q. Can the top and bottom halves of the ColecoVision console shell be separated during system maintenance/troubleshooting?

A. Yes.  A pair of 6-pin Molex connectors ae included in the design that when disconnected from each other allow the top and bottom halves of the ColecoVision console shell to be completely separated from each other.

Q.	Can the switch and circuit board be removed for maintenance/troubleshooting?

A.	Yes.  Assuming you don’t use any glue during the installation, which isn’t necessary, then the switch and circuit board can be easily removed.

## The Kit
 
The installation kit contains the following items:
1.	ColecoVision Power/Pause LED Mod circuit board.
2.	Motherboard wiring harness.
3.	Pause switch wiring harness (includes pause switch).
4.	Circuit board custom spacer.
5.	Pause switch nut (used to hold switch and circuit board in place).
6.	LED holder.

## Bill of Materials

Please download and refer to the Bill of Materials contained in this repository.

## LED Installation

Note that when installing the LED onto the PCB it must be slightly raised above the PCB surface..........

## Construction of the Wiring Harnesses
### Tools Needed

- Soldering iron and solder
- Wire cutter
- Wire stripper
- Crimping tool (I use a [Waldom W-HT-1921 crimping tool](https://www.digikey.com/en/products/detail/gc-electronics/W-HT-1921/26396)).

### Wire

Note that my preference is to use multistrand (7/32) 24AWG wire for this kit.  Nevertheless, 22AWG multistrand wire would also likely work fine.

### Wire Lengths and Connections

Refer to the following wiring diagram and photographs for details.  Use the appropriate crimps (from the Bill of Materials) for wires that are part of the Molex connectors.  I recommend soldering the wires to the four connections on the back of the rocker switch.

![](https://github.com/ikrananka/ColecoVision-Power-Flashing-Pause-LED-Mod/blob/main/images/Wiring%20Harness.png?raw=true)

## The Custom Spacer

dsfgsdfsdgsdg

## The Pause Switch Nut

The pause switch nut is included with the purchase of the Radio Shack DPDT switch from the bill of materials.  However, the nut needs to be modified slightly by lightly sanding down the ridges that will press against the PCB when installed.  To do this I typically use 300 grit sandpaper and hold the nut flat as shown in the first photo below.  I then slide the nut over the sandpaper in a circular motion while pressing down.  The second photo below shows the finished article and should give you a good idea of how much of the ridges you need to sand off.  Note that if you don't sand down these ridges then you will find that you won't be able to screw the nut onto the switch when it is installed in the ColecoVision with the spacer and PCB installed.  Sanding down the ridges allows the nut to get close enough to the thread on the switch so that it can be tightened up.

Ready to sand the nut:

Photo here......

Finished sanding:

Photo here......

## Installation Instructions

Refer to the installation instructions pdf included with this repository.

## Pause Flashing Frequency

The installation instructions include details of how to adjust the flashing frequency.  I have also provided video to illustrate what different flashing frequncies look like.  You can view the video [here](https://youtu.be/l38Kgi8KPcs).


