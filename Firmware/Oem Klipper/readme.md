MARKING : LEGACY IN FAVOR OF A MORE ADVANCED VERSION / UNIFIED SR / V400 REPO.  Most general help / support can be found at.  https://www.facebook.com/groups/1502404840209556

KNOWN STABLE CURA 5.22 , 4.10 , 4.8XX 
IDEAMAKER V4.31XXXX 
PRUSA 2.50. 
prusa/sl3er rebrands/derivativess neither supported/none supported. stable versions can be hit and miss / frequently change. consider these "advanced" and require page github bug reports read / releese notes.  

########################################################################################################################################################################################################################
Reminder its heavily suggested to at a minimum have "vanilla" klipper and, klipperscreen. since "stock" pads have no ability to tram the effector to the bed or correct "probe_calibrate commands" refer to (klipper websites probe_calibrate / delta calibration docs for the why.)   This could work in a perfect qc / user assembly world  however every machine is ultimately different so the solution to seemingly "unsolvable " mesh / tramming issues is either find the tiny off alignemnt section / loose scree etc Or b vanilla unmodified klipper to tram out slight dimensional issues / alignemnt. Keep  in mind a delta unlike corexy/cartesian runs on "softwaremagic" to print linear, so calibration being on point is a must otherwise mesh is either, 1 the bed is bowed/whatver topography issues or B, the effector is moving that way adding to the troubleshooting difficulty.   

########################################################################################################################################################################################################################
For general in depth instructions. Its always the Klipper website or coresponding projects "klipperscreen mainsail etc. These change regularly and, are always the most accurate/current souce being the creators vs random guides / youtube. which typically may be accourate or accurate under X time period.  Keeping in mine these can be useful however its always a handful vs a world of devs making X changes to docs / settings daily to every few weeks. other current info is often found on github discussions for X particular feature.  


########################################################################################################################################################################################################################
#1 If using the speederpad first ensure it is running the latest image which includes ssh and, root. Currently the simplest method is to simply delete the pi user account
and, remake it deleting anything "modified' Then reinstall with kiauh script. However this will also require enabling ssh with root user. Or B. just using kiauh to uninstall
everything. Moreover at this time there is a catch. Due to current moonraker changes not all projects are in sync. As a result things need to be done by hand. The most hastle free solution is just reinstall "klipper" and KlipperScreen to return probe_calibrate buttons / other functions. This can be done with either kiauh or deleting the klipper/klipperscreen folder then git cloning from klippers / klippersScreens github. Note the update manager will claim "dirty" since its looking for the flsun repo this can be ignored.  

########################################################################################################################################################################################################################
For the pi the setup remains the usual. using either mainsail or fluiddpi premade klipper images. Notably mainsailos is now on the raspi flasher tool for download. 
 If using either image they need updates run or for advanced users its probably better to use a minimal raspiimage and install the projects from the website by hand using their 
instructions. Note kiauh can be hit and miss its often better to install using the manual way. eg  git clone whatever repo following the projects install instructions its just a quick tool nothing more. 
Later for the pads depending on what happens with flsun images. I may make a simple cleanup script to fully run a clean klipper install for begginer users. currently its a bit of ssh terminal use.  

Note if coming from sr configs the functioality is basically the same / procedures. 
put files on , with mainsail / fluidd do not copy paste use the file.. this often leads to formating issues for whatever reason. 

########################################################################################################################################################################################################################
REMINDER when running anything to do with "probing" put the probe on first. Using the Calibrate button probe on first same with probe_calibrate 
for extra clairity when using probe_calibrate once it probes the bed remove the probe then do the paper test. accept must be typed or hit before 
save_config. Further mainsail/fluidd "zoffset" buttons are a bit deceptive. these use gcode_offset aka babystep.  The testz commands must be used in terminal or ideally with the klipper screen zcalibrate button. Note: The zcalibrate button will list this as "probe" for general safety on any nuew printer build its suggested to also use somthing like cardboard to avoid pei sheet damages. 

#1 Probe_calibrate with terminal or oem Klipper screen. Note: klipper screen has a slight bug atm when using the zcalibrate button it will not save_config and, the prompt will just dissapear seemingly freezing. Simply save_config from fluidd/main this will solve it for now. 

2. Preheat bed to temps used for actual printing. 

3. Hit calibrate macro. This will run a automated calibration routine saving / restarting on its own it will finish after bed_mesh. 

4. The calibrate button will leave the nozzle 0.6mm high lower this during a print. this is to avoid usererror or dimension issues with paper setting zoffset with Probe_calibratate. 

5. Make sure to run bed / hotend pid. 

