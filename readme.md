
## Flsun V400/SR Overhaul in Accordance with Klipper Standards / Delta ## STATE UPDATING USE RELEASES. 


Configuration Variants:
1. OFFICIAL Klipper: Raspberry Pi , BTTPI PAD7 or general Linux device. Otherwse reinstalled Speeder-pad with OFFICIAL Projects. 
2. Flsun Speederspad Klipper: Includes many changes to core Klipper files. - conflicting docs i wont make any Further updates due to tramming disabled / official klipper project "ban" / docs conflicts among other false posts about Official project issues.
This is simply to much hastle for users , devs and, the official klipper team to deal with daily.  


Note:
On some printers, it may be necessary to temporarily increase 'minimum_z_position' to -10 for the initial setup to run 'probe_calibrate' due to varying quality control. Once "calibrate macro completes the nozzle will be babystepped 0.2 high to avoid scrapes on pei if user manual probe_calibrate went a bit wrong simply babystep down frist print. if all went well the values is typically some range of 0.05-0.0-0.1. The first 'save_config' will add a section to 'printer.cfg' with calibrated overrides such as 'zoffset', 'delta_calibrate', etc. Furhter note. tramming (delta_calibrate)  does have limits it expects the printer to be well assembled / square to work. only then will bed mesh be "accurate" mesh is only a "supplement" to deal with slight topograpy issues with the bed. 
a delta should never rely on this. Ideally on a fully settyp / fine tuned machine fade can be enabled and set to turn mesh off after the first few layers. this avoids the machine needing to constantly adjust z on every move. (this causes odd issues / artiiacts / dimension issues otherwise)

What's New?
1. V400 trams in accordance with delta docs. if using "vanila" klipper of the website is installed." Otherwise not much from the original sr configs. 

2. Calibrate button: Runs endstop calibration, delta_calibrate, and bed_mesh. Use this button ONLY after running 'probe_calibrate' to set up the probe offset. The order of events remains absolute: set up probe offset, run 'delta_calibrate' to apply zoffset/tram the arms, and then run 'bed_mesh'. Preheat the bed to the printing temperature before running the calibrate button. The process is automated and will reboot/save on its own. It completes once 'bed_mesh' has finished. Fluidd/Mainsail will display the running procedure. After completion, the (babystep) will be 0.6mm high to avoid scrapes if the Zoffset is wrong. Simply (babystep) down from Mainsail or Klipperscreen during the first print.

3. Spread cycle and stealth chops: According to TMC docs, spread cycle is the most accurate but also louder. The mode can be set in start G-code or manually selected.
4. Safe homing.
6. TMC spreadsheet tuning.
7. Auto-saving baby step based on Mental's XYZ offset macro.
9. Raspberry Pi Pico ADXL support.
11. Properly functioning bed mesh.
12. Revised macros to remove redundancy.
13. Effector LED turns on when running G28.
14. RGB EFFECTOR PCB support
15. Filament drying
16. Profile overrides
17. Multiple effector / extruder support.
18. Tool change
19. Thermal runaway....is renabled.
20. Z velocity cannot crash into the bed at 600-400mms........
21. built in flow / rotation distance calculators
23. Automated calibration (endstop, delta_calibrate, bed_mesh). Preheat the bed before using this. The probe must be on.



Note: Links are also provided to credit various authors and, view their pages. Credit for any specific code or collaboration efforts can be found in the corresponding .cfg files.
The Flsun Facebook community sr/v4 community pages, KevinOConnor's Klipper 0.s, mainsail/fluidd teams, and KlipperScreen are acknowledged.

To date i haven't aprooved any copy pasted versions from the sr/v400 regarding github.  I also won't support these on fb since they only offer user confusion or unrelated bugs / personal time waste looking for unrelated problems or, problems i can't personally solve in github.   


No collabs have been done unless explicitly listed by name in conigs other then rootiest with some jinja on the updated calibration button.  
Note Use and improvements of open-source code are encouraged and appreciated other then personal clout. Reminder Always thank developers for their work, time, and support. Happy printing 

Support Links / credits 
- For further support: Facebook Group (https://www.facebook.com/groups/1502404840209556)
- Klipper official website: klipper3d.org (https://www.klipper3d.org)
- Mainsail UI documentation: docs.mainsail.xyz (https://docs.mainsail.xyz)
- Moonraker repository: github.com/Arksine/moonraker (https://github.com/Arksine/moonraker)
- Kiauh repository: github.com/th33xitus/kiauh (https://github.com/th33xitus/kiauh)
- Private users / testers / feedback. 


