Initial release. 

#1 If using the speederpad first ensure it is running the latest image which includes ssh and, root. Currently the simplest method is to simply delete the pi user account
and, remake it deleting anything "modified' Then reinstall with kiauh script. However this will also require enabling ssh with root user. Or b using kiauh to uninstall
everything. Moreover at this time there is a catch. Due to current moonraker changes not all projects are in sync. As a result things need to be done by hand. The most hastle free solution is either just reinstall "klipper" and KlipperScreen to return probe_calibrate buttons / other functions. This can be done with either kiauh or deleting the klipper folder then git cloning from klippers github. Note the update manager will claim "dirty" since its looking for the flsun repo this can be ignored. 

For the pi the setup remains the usual. using either mainsail or fluiddpi premade klipper images. notably mainsailos is now on the raspi flasher tool for download. 
 If using either image they need updates run or for advanced users its probably better to use a minimal raspiimage and install the projects from the website
instructions. Note kiauh can be hit and miss its often better to install using the manual way. eg  git clone whatever repo following the projects install instructions. 

Later for the pads depending on what happens with flsun images. I may make a simple cleanup script to fully run a clean klipper install for begginer users. currently its a bit of ssh terminal use.  

Note if coming from sr configs the functioality is basically the same / procedures. 
put files on , with mainsail / fluidd do not copy pate use the file.. this often leads to formating issues for whatever reason. 

REMINDER when running anything to do with "probing" put the probe on first. Using the Calibrate button probe on first same with probe_calibrate 
for extra clairity when using probe_calibrate once it probes the bed remove the probe then do the paper test. accept must be typed or hit before 
save_config. Further mainsail/fluidd "zoffset" buttons are a bit deceptive. these use gcode_offset aka babystep.  The testz commands must be used in terminal or ideally with the klipper screen zcalibrate button. Note: The zcalibrate button will list this as "probe" 

#1 Probe_calibrate with terminal or oem Klipper screen. Note: klipper screen has a slight bug atm when using the zcalibrate button it will not save_config and, the prompt will just dissapear seemingly freezing. Simply save_config from fluidd/main this will solve it for now. 

2. Preheat bed to temps used for actual printing. 

3. Hit calibrate macro. This will run a automated calibration routine saving / restarting on its own it will finish after bed_mesh. 

4. The calibrate button will leave the nozzle 0.6mm high lower this during a print. this is to avoid usererror or dimension issues with paper setting zoffset with Probe_calibratate. 

5. Make sure to run bed / hotend pid. 

