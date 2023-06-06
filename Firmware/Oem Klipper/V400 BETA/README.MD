Current beta / overhaul. This will be added as "stable' upcoming namely this directory is to avoid yet another repo

Whats New ? 
1. filament dehydrate macro for use with a filament box of some kind , or bed heater 
2. 2. sr firmwware emulator / speed macros if not using dynamic acceleration or to be called in perfilament gcode 
3. 3. Most macros have been overhault and, now have a pull down menu availble in mainsail/fluidd. most macros use 1=on or 0 = off 
4. Filament flow / rotation distane calculators
5. 5 Extruder / effector selection macros. these set rotation distance rms current etc intended usage quick swaps or common mod support. on a fresh config v400 effector will of course be default. 
6. rotatation distance can be adjusted or saved with extrude_140 macro a negative value will also reverse the motor direction 
7. Most macros will dispaly error / hints in the print stats section or terminal 
8. Built in flow profiles. by default this will not be in use until values are set. intended use profile flow is 100 and required changes are saved in the machine. eg pla 100 petg 94 etccc 
9. Firmware retrect values per flow profile can also be saved and will be use if for example Pla were to be selected" 
10. M500 to list "saved_variables" this will display things like current flow , rotation distance , input shaper etc. 
11. CALIBRATE MACRO UPDATED. calibratee will now attempt to run a shaper_calibration. If no shaper is found it will simply error reboot and continue on to the next calibration otherwise contine on error this will be 
12. dispalyed in terminal if a adxl is present or it failed for whatever reason. 
13. Prime blob extrude ammount /length can now be adjusted with the "prime_blob_settings" macro this also alows for extrude speed. Note speed values are converted to mm/s intead of mm/min since this is generally simpler. 
14. 
