### This is the live copy of Marlin I run on my personal printers, with my own mods plus code for MakersToolWorks printers, and configured for my own preferences.

#### Some of the mods I have done:

  * Status info GLCD screen for DOGM LCDs
    * display Z coordinates to hundreds, not just tenths
    * display SD print progress percentage numerically, not just with the bar.
    * display endstop state by toggling capitalization of X,Y,Z labels in the coordinate line
    * display 0% instead of --- when fan is off.
    * display long filename when printing from SD instead of short 8.3 filename
  * Makers Tool Works LED controller
    * send events to the MTwe LED controller introduced with the MendelMax 3 to display printer status. See bottom of Configuration.h
  * Fan control enhancements
    * Added a Fan Limit feature to constrain max fan speed using a panel menu item
    * Added Fan Ramping, to slowly spin up fan. Intended to avoid shocking PID to prevent temp drops when activating fan.

Things to be aware of about my configuration if you plan to use my version on your printer:

  * I may have FWRETRACT enabled in Configuration_adv.h
  * I probably have the X and Y endstop pins disabled in the board files for RAMBO and RAMPS
  * I probably have the MTWLED stuff enabled
  * If you have a MendleMax3, my esteps probably is way wrong for your printer
  * I have the kill pin disabled for my board configs
  * I have the beeper disabled for my board configs
  * I have my XY jerk set higher than most people use

# Marlin 3D Printer Firmware
<img align="right" src="Documentation/Logo/Marlin%20Logo%20GitHub.png" />

  * [Configuration & Compilation](/Documentation/Compilation.md)
  * Supported
    * [Features](/Documentation/Features.md)
    * [Hardware](/Documentation/Hardware.md)
    * [GCodes](/Documentation/GCodes.md)
  * Notes
    * [Auto Bed Leveling](/Documentation/BedLeveling.md)
    * [Filament Sensor](/Documentation/FilamentSensor.md)
    * [Ramps Servo Power](/Documentation/RampsServoPower.md)

##### [RepRap.org Wiki Page](http://reprap.org/wiki/Marlin)

## Quick Information

This is a firmware for reprap single-processor electronics setups.
It also works on the Ultimaker PCB. It supports printing from SD card+Folders, and look-ahead trajectory planning.
This firmware is a mashup between [Sprinter](https://github.com/kliment/Sprinter), [grbl](https://github.com/simen/grbl) and many original parts.

## Current Status: Bug Fixing

The Marlin development is currently revived. There's a long list of reported issues and pull requests, which we are working on currently.
We are actively looking for testers. So please try the current development version and report new issues and feedback.

[![Coverity Scan Build Status](https://scan.coverity.com/projects/2224/badge.svg)](https://scan.coverity.com/projects/2224)
[![Travis Build Status](https://travis-ci.org/MarlinFirmware/Marlin.svg)](https://travis-ci.org/MarlinFirmware/Marlin)

What bugs are we working on: [Bug Fixing Round 2](https://github.com/MarlinFirmware/Marlin/milestones/Bug%20Fixing%20Round%202)

## Contact

__IRC:__ #marlin-firmware @freenode ([WebChat Client](https://webchat.freenode.net/?channels=marlin-firmware), [Archive](http://energymonitor-dk.dns4e.net/marlin-firmware-log/))

__Mailing List:__ marlin@lists.0l.de ([Subscribe](http://lists.0l.de/mailman/listinfo/marlin), [Archive](http://lists.0l.de/pipermail/marlin/))

## Credits

The current Marlin dev team consists of:

 - Erik van der Zalm ([@ErikZalm](https://github.com/ErikZalm))
 - [@daid](https://github.com/daid)
 
Sprinters lead developers are Kliment and caru.
Grbls lead developer is Simen Svale Skogsrud.
Sonney Jeon (Chamnit) improved some parts of grbl
A fork by bkubicek for the Ultimaker was merged.

More features have been added by:
  - Lampmaker,
  - Bradley Feldman,
  - and others...

## Licence

Marlin is published unde the [GPL license](/Documentation/COPYING.md) because I believe in open development.
Please do not use this code in products (3D printers, CNC etc) that are closed source or are crippled by a patent.

[![Flattr this git repo](http://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=ErikZalm&url=https://github.com/MarlinFirmware/Marlin&title=Marlin&language=&tags=github&category=software)
