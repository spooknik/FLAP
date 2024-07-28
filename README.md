
# Filament Loading À la Prusa (FLÀP) 

### A set of Klipper macros with prompts for filament loading and more

https://github.com/user-attachments/assets/c1852419-f1c5-4ba8-8720-57148ebd5544

## Description
This is a collection of Klipper macros for loading and unload filament and handleing filament runouts and color changes in a similar style to Prusa.
What's unquie about these macros if they use Mainsail prompts as a helpful aide.

These macros where designed around the Orbiter Filament Sensor, but it will work with any filament sensor that is a switch. You just need to assign the pin in the config. The  Orbiter Filament Sensor also has a button for unload, which many filament sensors do not have. So in this case you would just call the unload macro in Mailsail or the like. 

The main features are:

- When loading filament you are asked what material it is. The hotend and heatbed (optional) are then heated up to the temp defined for that material.
- When loading a filament you are asked if the material should be purged more after the intial purge.
- When unloading a material you are asked what material should be unloaded, if for some reason it is not saved.
- If the hotend cools down at anytime in load and unload beause of [Idle Timeout](https://www.klipper3d.org/Config_Reference.html#idle_timeout), then it is reheated before extruding
- If filament runs out during a printer, the printer is paused, parked, waits for you to unload the filament. Then asks you to insert new filament.
- Checks if filament is actually present before trying to load

A video is worth a 1000 words:

## Install
1. Download ´flap_main.cfg´ and ´flap_temp_control.cfg´
2. Place both files in your Klipper config folder
3. Open ´flap_main.cfg´ and assign your pins
4. Have a look at the options in the config and customize to your liking
5. Open ´flap_temp_control.cfg´ and have a look at the material profiles and see if they are to your liking
6. Restart and try it out

## Todo
1. Long term testing
2. Testing on Klipper Screen (mind is in the mail)
3. Fixing bugs that will probably appear 🙃

## Loading

## Unloading

## Filament runout / Color Change (M600)

Filament runout is one of the most ciritical and delicate operations for a 3D printer. A lot can go wrong and hours of a print and lots of filament can be trashed if it doesn't go right. With these macros I tried to make the process as bullet proof as possible with lots of checks to make sure everything goes as it should.


## Contributing
Bugs? Issues? Improvements? Open an issue or make a PR. 

## Block Diagram

To help me understand the logic flow of what's going on at each step, I made block diagramd for each part of this project. 

### Loading and Unloading
![image](https://github.com/user-attachments/assets/5da8dd4b-1e0e-4c7b-b940-a42cfb83c0fc)

### Filament Runout
![image](https://github.com/user-attachments/assets/29a81ef2-a647-4c7f-974f-f8135eea212e)





