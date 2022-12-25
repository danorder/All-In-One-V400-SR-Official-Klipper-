Designed to work with "pure stock speeder pads' (Flsun firmware)

Note: The klipper files are "modified" and, Klipper screen cannot set PROBE zoffset.  its using babystep which is just a workaround for slight probe_offset measurement issues with paper etc.  This will lead to strange deviation numbers due to not knowing the hardware offset. it will need to run  Probe_calibrate to set the Probe zoffset" This can be done from terminal. or, Klipperscreen returned to oem via reinstall.  Stock KlipperScreen will have a "zcalibrate" button with a Probe option. This is probe_calibrate which  will include  lower by X amount buttons to run the paper test vs use terminal. https://www.klipper3d.org/Bed_Level.html#the-paper-test
once this is done delta_calibrate needs to be run to both tram and, apply the new probe_offset then Bed mesh can be used afterwards. Note bed level 1 and 2 are replaced with Calibrate which will run everything except for probe_calibrate. The probe must be on first and bed temp should first be set to desired print temp. Running it will run all required calibration also saving / rebooting by itself. Lastly the Nozzle will be left 0.6mm high to avoid scrap potential. on the first print simply "babystep" down to set the first layer. Generally if Probe_calibrate was on point the babystep / zoffset will be 0.00 or close. 

General instructions for files 

Simply rename or remove the current printer.cfg and, replace with github printer.cfg and, other_features files. The pico file / shaper file is optional but setup for a 
raspberry pi pico this can very depending on device. to enable there is a include near the top of printer.cfg removing the # will enable the file however after shaper is run using a pico the file will need to be disabled again otherwise the pico would need to be plugged into he pad at all times. (It would see the pico as another required printer mcu otehrwise)    



Initial startup will not have a "save_section at the bottom of printer.cfg" probe_calibrate will be required to run first , Then calibibrate button. note unless a nozzle is changed or somthing that would affect the probe / hotend height. Probe_calibrate generally doens't need to be run again just the calibrate button for general leveling or changing bed temps to account for mesh / height changes with thermal  expansion.  

Note if coming from sr configs the functioality is basically the same / procedures. 
put files on , with mainsail / fluidd do not copy paste use the file.. this often leads to formating issues for whatever reason. 


REMINDER when running anything to do with "probing" put the probe on first. Calibrate button probe on first same with probe_calibrate 
for extra clairity when using probe_calibrate once it probes the bed remove the probe then do the paper test. accept must be typed or hit before 
save_config. 

#1 Probe_calibrate with terminal or oem Klipper screen. Note: klipper screen has a slight bug atm when using the zcalibrate button it will not save_config and, the prompt will just dissapear seemingly freezing. Simply save_config from fluidd/main this will solve it for now. 

2. Preheat bed to temps used for actual printing. 

3. Hit calibrate macro. This will run a automated calibration routine saving / restarting on its own it will finish after bed_mesh. 

4. The calibrate button will leave the nozzle 0.6mm high lower this during a print. this is to avoid usererror or dimension issues with paper setting zoffset with Probe_calibratate. 

5. Make sure to run bed / hotend pid. 

