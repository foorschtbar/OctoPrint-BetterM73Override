# OctoPrint M73 ETA Override

Plugin that overrides OctoPrint ETA to values from last M73 gcode sent to the printer.

PrusaSlicer is able to calculate print estimates very accurately. Those estimates get injected into generated gcode as [M73 gcode](https://marlinfw.org/docs/gcode/M073.html) commands. This plugin reads the injected information to override what OctoPrint uses as default to calculate estimates. Improved estimates are displayed in OctoPrint, your printer display and in your favorite OctoPrint client.

This plugin will also work with other slicers that inject M73 gcode commands while slicing your STL files to produce gcode.

## Firmware

Prusa printers will display M73 estimates without any modifications. Printers that run on Marlin firmware might require their firmware to be properly configured to display M73 ETA on the printer display. If you are using Marlin 2.0.x then you will need to:
1. Uncomment #define SHOW_REMAINING_TIME in Configuration_adv.h
1. Uncomment #define USE_M73_REMAINING_TIME in Configuration_adv.h

## Setup

Install via the bundled [Plugin Manager](https://github.com/foosel/OctoPrint/wiki/Plugin:-Plugin-Manager)
or manually using this URL:

    https://github.com/gdombiak/OctoPrint-M73ETAOverride/archive/master.zip


## Configuration

No configuration required. Just install plugin and it will start to overriding OctoPrint ETA with last M73 gcode.

Please note that if printer is starting (heating or leveling bed) ETA will show less than one minute.

## Credits

This plugin was originally developed by Jakub Furman. I was no longer being maintained so I took ownership to keep it alive.
