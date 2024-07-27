
# Filament Loading À la Prusa (FLÀP) 

### A set of Klipper macros with prompts for filament loading and more


## Description
This is a collection of Klipper macros for loading and unload filament and handleing filament runouts and color changes in a similar style to Prusa.

- When loading filament you are asked what material it is. The hotend and heatbed (optional) are then heated up to the temp defined for that material.
- When loading a filament you are asked if the material should be purged more after the intial purge.
- When unloading a material you are asked what material should be unloaded, if for some reason it is not saved.
- If the hotend cools down at anytime in load and unload beause of [Idle Timeout](https://www.klipper3d.org/Config_Reference.html#idle_timeout), then it is reheated before moving the extruder.
- If filament runs out during a printer, the printer is paused and unloads your filament. Then asks you to insert new filament.
- Checks if filament is actually present before trying to load


## Loading

## Unloading

## Filament runout / Color Change (M600)

Filament runout is one of the most ciritical and delicate operations for a 3D printer. A lot can go wrong and hours of a print and lots of filament can be trashed if it doesn't go right. With these macros I tried to make the process as bullet proof as possible with lots of checks to make sure everything goes as it should.


## Block Diagram


## Contributing
Bugs? Issues? Improvements? Open an issue or make a PR. 
