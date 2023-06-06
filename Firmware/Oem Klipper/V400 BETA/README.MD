Current beta / overhaul. This will be added as "stable' upcoming namely this directory is to avoid yet another repo

Import Notes. 
pid_tune macros do not save_config. This is so both can be run to avoid double reboots. if pid_bed is enabled for "calibrate macro" 
Both virtual_sdcard and variables.cfg location may need to be changed. This will depend on how klipper was installed and, what directorys its using. it is assumed to be using the printer_data directory and "single  install" otherwise winscp or putty can be used to find the "current" locations"  
Since a clean config will have no calibration settings a bed_mesh error will popup and disappear appear "calibrate" is run. 
To avoid a bunch of macro clutter restore "mainsail" under settings with the provided layout this will put macros under catagories. 




Whats New ? 
1. Filament dehydrate macro for use with a filament box of some kind , or bed heater 
2.  SR firmwware emulator / speed macros if not using dynamic acceleration or to be called in perfilament gcode. The value to put in the pulldown is "active" these values do resume after a reboot. (printer will be using printer.cfg defaults) These can also be used if one wanted to speed things up otherwise slow them down during a print.  
3. Most macros have been overhauled and, now have a pull down menu availble in mainsail/fluidd. most macros use 1=on or 0 = off 
4. Filament flow / rotation distane calculators
5. 5 Extruder / effector selection macros. these set rotation distance rms current etc intended usage quick swaps or common mod support. on a fresh config v400 effector will of course be default. 
6. Rotatation distance can be adjusted or saved with extrude_140 macro a negative value will also reverse the motor direction 
7. Most macros will dispaly error / hints in the print stats section or terminal 
8. Built in flow profiles. by default this will not be in use until values are set. intended use profile flow is 100 and required changes are saved in the machine. eg pla 100 petg 94 etccc 
9. Firmware retrect values per flow profile can also be saved and will be use if for example Pla were to be selected" 
10. M500 macro to list "saved_variables" this will display things like current flow , rotation distance , input shaper etc in terminal. 

11. ##########################################################################################################################################################################################################
 CALIBRATE MACRO UPDATED: Calibratee will now attempt to run a shaper_calibration. If no shaper is found it will simply error reboot and continue on to the next calibration otherwise contine on error this will be 
 dispalyed in terminal if a adxl is present or it failed for whatever reason.  In additon the "calibrate" macro a option to change the default safe height in the pull down. by default this will be 2mm high to avoid 
 scrapes and, to be lowered during the first print. a large square is ideal. The old default is 0.6mm high The large height increase is to deal with varying effectors / mods / probes.  
 NOTE: regular delta_calibrate/Probe_calibrate behavior is the same as the website. if used in termianl these will not leave the nozzle high for the first print. 

FURTHER NOTE: MAINSAIL SAVE TO PROBE WILL NOT SET "BABYSTEP AKA SETGCODE OFFSET UNTIL DELTA_CALIBRATE IS RUN. AND, APPLY TO ENDSTOP IS ONLY TEMPORARY THE NET TIME DELTA_CALIBRATE IS RUN THIS OFFSET WILL BE GONE. 
FINNALLY THESE DO NOT ACCOUNT FOR FLSUN PRINTERS AND AUTOSAVING "ZOFFSET/BABYSTEP" ensure babystep was "reset" otherwise scapes etc could be possible. AS a disclaimer these are not recommended for use. 

Lastly "Calibrate settings" macro currently has the option to enable pidtuning of the bed during the calibration routine. again 1 = on 0 =off. The default behavior is off on a clean config and, no variables file. 
######################################################################################################################################################################################################################

12. Prime blob extrude ammount /length can now be adjusted with the "prime_blob_settings" macro this also alows for extrude speed. Note speed values are converted to mm/s intead of mm/min since this is generally simpler. 
14.Prusa support macro
15 pid bed / hotend macro now have adjustable values in the pull downs 
16 Fan speed override.(adjust m106) please see https://github.com/garethky/klipper-voron2.4-config/blob/mainline/printer_data/config/part-cooling.readme.md for docs (the creator) 
This is used to override fan speeds that the slicer would otherwise continue to reset if changed in mainsail. normally this would require a cancel print and slicer setting change. the need to know simple answer 
in usage would be to put in "=+20 or =-20" in the adjust box in the pull down of adjust m106 maco. Note it must have =.  - or + value in the box wont work without.  



