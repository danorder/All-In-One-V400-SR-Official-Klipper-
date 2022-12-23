Ment to work with "pure stock' but namely the klipper files are "modified" and, Klipper screen cannot set zoffset properly its using the wrong commands. it needs to run 
Probe_calibrate to set the Probe zoffset" This can be done from terminal. or, Klipperscreen returned to oem via reinstall. naotaby the "zcalibibrate" button will have a 
Probe option. This is probe_calibrate and, will also have the lower by X ammount to run the paper test vs use terminal. https://www.klipper3d.org/Bed_Level.html#the-paper-test
once this is done delta_calibrate needs to be run to both tram and, apply the new probe_offset then lastly bed mesh can be used. Note bed level 1 and 2 are replaced with
Calibrate which will run everything except for probe_calibrate. The probe must be on first and bed temp should first be set to desired print temp. Running it will run all 
required calibration also savving / rebooting by itself. Lastly the Nozzle will be left 0.6mm high to avoid scrap potential. on the first print simply babystep dowwn to 
set the first layer. Generally if Probe_calibrate was on point the babystep / zoffset will be 0.00 or close. 

General instructions for files 

Simply rename or remove the current printer.cfg and, replace with github printer.cfg and, other_features files. The pico file / shaper file is optional but setup for a 
raspberry pi pico this can very depending on device. to enable there is a include near the top of printer.cfg 

