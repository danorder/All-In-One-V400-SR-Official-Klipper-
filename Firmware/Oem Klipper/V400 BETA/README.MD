Current beta/overhaul. This will be added as "stable" upcoming, namely in this directory to avoid yet another repository. Currently "updating. start 10:24pm june 06 2023

Import Notes:
- `pid_tune` macros do not save_config to allow running both without double reboots.
- If `pid_bed` is enabled for "calibrate macro," both `virtual_sdcard` and `variables.cfg` locations may need to be changed. It depends on how Klipper was installed and what directories it's using. The assumption is it's using the `printer_data` directory and a "single install." Otherwise, tools like WinSCP or PuTTY can be used to find the "current" locations.

Since a clean config will have no calibration settings, a `bed_mesh` error will pop up and disappear when "calibrate" is run. To avoid cluttering macros, restore "mainsail" under settings with the provided layout to put macros under categories.

What's New?
- Filament dehydrate macro for use with a filament box or bed heater.
- SR firmware emulator/speed macros for non-dynamic acceleration or adjusting print speed during filament G-code. Use "active" in the pull-down menu to resume values after a reboot. These can also be used to speed up or slow down prints.
- Overhauled macros with pull-down menus available in Mainsail/Fluidd. Most macros use 1=on or 0=off.
- Filament flow/rotation distance calculators.
- 5 extruder/effector selection macros for quick swaps or common mod support. The default will be v400 effector on a fresh config.
- Rotation distance can be adjusted or saved with the `extrude_140` macro. A negative value will also reverse the motor direction.
- Most macros display errors/hints in the print stats section or terminal.
- Built-in flow profiles. By default, they are inactive until values are set. Profiles like PLA 100, PETG 94, etc., can be used by saving required changes in the machine.
- Firmware retraction values per flow profile can be saved and used when a specific filament is selected, such as PLA.

The `M500` macro lists "saved_variables" and displays things like current flow, rotation distance, input shaper, etc., in the terminal.

Calibrate Macro Update:
- The `calibrate` macro now attempts to run a `shaper_calibration`. If no shaper is found, it will display an error, reboot, and continue to the next calibration. The terminal will show this information if an ADXL is present or if the calibration failed.
- The `calibrate` macro has an option to change the default safe height in the pull-down menu. The default is 2mm high to avoid scrapes and should be lowered during the first print. The old default is 0.6mm high. The large height increase is to accommodate varying effectors/mods/probes.
- Regular `delta_calibrate`/`Probe_calibrate` behavior remains the same as on the website. If used in the terminal, these macros will not leave the nozzle high for the first print.
- The "Calibrate Settings" macro currently has the option to enable PID tuning of the bed during the calibration routine. The default behavior is off on a clean config with no variables file.

Prime blob extrude amount/length can now be adjusted with the `prime_blob_settings` macro, which also allows for extrude speed. Note that speed values are in mm/s instead of mm/min for simplicity.

Other updates include Prusa support macros, adjustable values in the pull-downs for PID bed/hotend macros, and fan speed override (`m106` adjustment). Refer to the documentation at https://github.com/garethky/klipper-voron2.4-config/blob/mainline/printer_data/config/part-cooling.readme.md (created by the original author) for details on overriding fan speeds.

