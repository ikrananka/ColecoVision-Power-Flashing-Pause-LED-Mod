# ColecoVision Power/Flashing Pause LED Mod

## Introduction

This mod for the ColecoVision has two functions.  The first is to provide a continuously lit red power LED.  This LED will illuminate whenever the ColecoVision is turned on and not paused.  The second function is to provide a hardwired, physical switch, to pause operation of the ColecoVision allowing you to pause a game at any point and resume play at your leisure.  A unique feature of this mod is that when paused the power/pause LED flashes to indicate that the system is paused.  The rate of flashing is user adjustable from 0.6 to 3.0Hz.  When pause is turned off the flashing LED reverts to being continuously lit (until the system is either paused again or is turned off).
The pause function is achieved by pulling the WAIT line of the ColecoVision’s Z80 CPU low.  This in effect pauses all Z80 processing and therefore pauses the game you’re playing.  However, the audio is not paused and will continue to emit the last note/tone which can be very annoying.  Therefore, this mod not only allows you to pause the Z80 processor but also disconnects the audio output whenever pause is engaged.

## FAQ

Q.	Will this work with Super Game Module (SGM1) games?

A.	Yes (if you wire the audio as recommended later in this document).  All SGM enhanced games still use the Z80 processor and so they will pause when the Z80 is paused just like any other ColecoVision game.  However, SGM enhanced audio is fed to the ColecoVision via the expansion port (EXAUD), bypassing the ColecoVision’s onboard sound from the SN76489A.  Therefore, it is important that when paused, audio is disconnected from a location after the point where audio from the SN76489A and EXAUD combine.  This is easy to do and instructions for this are provided later in this document.

Q.	Will this work with the upcoming Super Game Module 2 (SGM2)?

A.	Yes and No.  According to the latest information from Opcode Games, the SGM2 will be backwards compatible with SGM1 games and the pause mod will function in the same way as described in the answer above.  However, SGM2 specific games will use the new Z80 and/or 16-bit CPUs that are contained in the SGM2 unit and these cannot be paused using this mod.  However, Opcode Games has stated that “pause will be implemented in software for these games because of the dual CPU design” and so a hardware pause solution is not needed.  You never know, perhaps Opcode Games will make the SGM2s power LED flash when a game is paused!!!

Q.	Does this work with the Expansion Module #1?

A.	No.  The expansion module #1 uses its own processor and audio chip and like the SGM2 cannot be paused by this mod.  Be aware that moving the pause switch to the pause position while playing an expansion module #1 game may disconnect the audio so leave the switch in the normal position when playing these games.

Q.	Is the mod reversable?

A.	The mod is mostly reversable other than the fact that you must drill two large holes in the ColecoVision’s top housing.  These holes are obviously not reversable.

Q.	Can the switch and circuit board be removed for maintenance/troubleshooting?

A.	Yes.  Assuming you don’t use any glue during the installation, which isn’t necessary, then the switch and circuit board can be easily removed.

## The Kit
 
The installation kit contains the following items:
1.	ColecoVision Power/Pause LED Mod circuit board.
2.	Motherboard wire assembly.
3.	Pause switch wire assembly (includes pause switch).
4.	Circuit board custom spacer.
5.	Pause switch nut (used to hold switch and circuit board in place).
6.	LED holder.

## Tools Needed

- Phillips screwdriver
- Variable speed electric drill
- 1/4” drill bit
- Step drill bit up to 25/32” (alternatively a step drill bit up to 3/4” and a half round double-cut file)
- Anti-static mat with wrist strap (optional)
- Soldering iron and solder
- Xacto knife (or equivalent)
- Tin snips (to cut the bottom RF shield)
