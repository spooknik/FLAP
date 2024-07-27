
# Filament Loading À la Prusa (FLÀP) 

### A set of Klipper macros for filament loading

## Description
This is a collection of Klipper macros for loading and unload filament and handleing filament runout in a similar style to how Prusa MK3 does it. What does this mean?

- When loading filament you are asked what material it is. The hotend and heatbed (optional) are then heated up to the temp defined for that material.
- When loading a filament you are asked if the material should be purged more after the intial purge.
- When unloading a material you are asked what material should be unloaded, if for some reason it is not saved.
- If the hotend cools down at anytime in load and unload beause of [Idle Timeout](https://www.klipper3d.org/Config_Reference.html#idle_timeout), then it is reheated before moving the extruder.
- If filament runsout during a printer, the printer is paused and unloads your filament. Then asks you to insert new filament.

These macros are build around the Orbiter Filament sensor, but can work with any filment runout switch you just need to define the pin. Most setups will not have a button to unload filament like the Orbiter Filament sensor but you can run the macro manually or make a simple button using a spare pin on your MCU.

## Loading

## Unloading

## Filament runout / Color Change (M600)

Filament runout is one of the most ciritical and delicate operations for a 3D printer. A lot can go wrong and hours of a print and lots of filament can be trashed if it doesn't go right. With these macros I tried to make the process as bullet proof as possible with lots of checks to make sure everything goes as it should.


## Block Diagram


## Contributing
Bugs? Issues? Improvements? Open an issue or make a PR. 
