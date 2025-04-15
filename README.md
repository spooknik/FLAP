
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
- [Optional] Beep (M300) command can be played at stages of load and unload
- Temperture Checks and temperature recovery if [idle timeout](https://www.klipper3d.org/Config_Reference.html?h=idle#idle_timeout) is reached.
- Filament Checks during loading to make sure there is acutally filament loaded
- [Optional] Auto Resume after runout
- Persistence storage of material temps; material is remembered even after reboot
- "Retry" feature during filament loading, which unloads the filament if something is wrong.
- [Optional] cooldown hotend to a specific temp after loading
- [Optional] heats bed during loading
- [Optional] homes Z before loading, to make room for purge
- Customizable purge length, purge speed, unload distance, park postion, park lift and park retraction
- Works 100% with Klipperscreen

## Install
[See the wiki for a step by step guide.](https://github.com/spooknik/FLAP/wiki/Installation)

Also check out [extras](https://github.com/spooknik/FLAP/wiki/Extras)

## Todo
1. Long term testing
3. Fixing bugs that will probably appear 🙃
4. Continuous beep alert during runout / color change
5. High temp to low temp material transition - [Explained here](https://www.reddit.com/r/klippers/comments/1ee8ewb/comment/lgfh9ue/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button)
6. Prevent bed from cooling down during print pause
7. Faster "purge more" - It's a bit slow at the moment

## Changelog
- V1.0 - Intital Release
- V1.1 - Optimized material load and unload prompt.
- V1.2 - Added cooldown after loading function. Optimized prompt text and layouts.
- V1.3 - Added working color change (M600), Improved pruge dialogue, Added auto-resume after runout and color change.
- V1.4 - Added persistent storage of temps, "Retry" during filament purge, home Z during loading, tested working with klipper screen

## Contributing
Bugs? Issues? Improvements? Open an issue or make a PR. 

## Block Diagram
To help me understand the logic flow of what's going on at each step, I made block diagramd for each part of this project. 

### Loading and Unloading
![image](https://github.com/user-attachments/assets/5da8dd4b-1e0e-4c7b-b940-a42cfb83c0fc)

### Filament Runout
![image](https://github.com/user-attachments/assets/29a81ef2-a647-4c7f-974f-f8135eea212e)





