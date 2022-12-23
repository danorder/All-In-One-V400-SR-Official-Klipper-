Initial release. 

#1 If using the speederpad first ensure it is running the latest image which includes ssh and, root. Currently the simplest method is to simply delete the pi user accont
and, remake it deleting anything "modified' Then reinstall with kiauh script. however this will also require enabling ssh with root user. Or b using kiauh to uninstall
everything. Hoever at this time there is a catch. Due to current moonraker changes not all projects are in sync. As a result things need to be done by hand. The most hastle
free solution is either just reinstall "klipper" and Klipper screen to return probe_calibrate buttons / other functions. This can be done with either kiauh or deleting 
the klipper folder then gitcloning from klipper github. Note the update manager will claim "dirty" since its looking for the flsun repo. 

For the pi the setup remains the usual. using either mainsail or fluiddpi premade klipper images. notably mainsailos is now on the raspi flasher tool for download. 
 If using either image they need updates rum or for advanced users its probably better to use a minimal raspiimage and install the projects from the website
instructions. Note kiauh can be hit and miss its often better to install using the manual way. eg  git clone whatever repo following the projects install instrucitons. 

Later for the pads depedning on what happens with flsun images. I may make a simple cleanup script to fully rudn a clean klipper install for begginer users. 

