
# Filament Loading À la Prusa (FLÀP) 

### A set of Klipper macros with prompts for filament loading and more

https://github.com/user-attachments/assets/c1852419-f1c5-4ba8-8720-57148ebd5544

## Description
This is a collection of Klipper macros for loading and unload filament and handleing filament runouts and color changes in a similar style to Prusa.
What's unquie about these macros if they use Mainsail prompts as a helpful aide.

These macros where designed around the Orbiter Filament Sensor, but it will work with any filament sensor that is a switch. You just need to assign the pin in the config. The  Orbiter Filament Sensor also has a button for unload, which many filament sensors do not have. So in this case you would just call the unload macro in Mailsail or the like. 

Macros included:

- Filament Load
- FIlament Unload
- Filament Runout
- Color Change M600 (WIP)
- Pause
- Resume
- Cancel

The main features are:

- Lots of helpful [prompts](https://docs.mainsail.xyz/overview/features/macro-prompts) that guide you through the process
- Material temperature profiles. Add custom material profiles for whatever you might be printing.
- Optional Beep (M300) command can be played at stages of load and unload
- Temperture Checks and temperature recovery if [idle timeout](https://www.klipper3d.org/Config_Reference.html?h=idle#idle_timeout) is reached.
- Filament Checks during loading to make sure there is acutally filament loaded

A short demo because [a video is worth a 1000 words](https://www.youtube.com/watch?v=ou3CjtsuDTo)

## Install
1. Download ´flap_main.cfg´ and ´flap_temp_control.cfg´
2. Place both files in your Klipper config folder
3. Open ´flap_main.cfg´ and assign your pins
4. Have a look at the options in the config and customize to your liking
5. Open ´flap_temp_control.cfg´ and have a look at the material profiles and see if they are to your liking
6. Restart and try it out

## Todo
1. Long term testing
2. Testing on Klipper Screen (mine is in the mail)
3. Optimize macros by using lists 
4. Fixing bugs that will probably appear 🙃

## Contributing
Bugs? Issues? Improvements? Open an issue or make a PR. 

## Block Diagram
To help me understand the logic flow of what's going on at each step, I made block diagramd for each part of this project. 

### Loading and Unloading
![image](https://github.com/user-attachments/assets/5da8dd4b-1e0e-4c7b-b940-a42cfb83c0fc)

### Filament Runout
![image](https://github.com/user-attachments/assets/29a81ef2-a647-4c7f-974f-f8135eea212e)





