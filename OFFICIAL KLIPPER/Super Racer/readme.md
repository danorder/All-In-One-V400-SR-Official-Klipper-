Sr Firmware is identical to the v400 other then "build size / extruder" NOTE: GET BACKEND.CFG FROM THE PEVIOUS DIRECTORY THEY NEED THIS.  




If using extruderS macros use the printer.cfg MACRO THIS = default printer.cfg config values. everything else overrides printer.cfg unless set back to default with printer.cfg macro."



SETUP: 
Firstly rename xx sr board to printer.cfg. 2nd printer.cfg , backend , and, mainsail ui backup are required. simply drag and drop these on to mainsail. 
Due to varying hardware printer.cfg virtual sdcard and, variables location will most likely need to be adjusted. The old tutorial island aspect of the sr is now "depreciated" since forums have enough users now. 

Note calibration behavior / methods have not changed.  and, remainss  1. put on the probe 2. run probe_calibrate though terminal or klipperscreen (zcalibrate button) 3. preheat the bed 4. run "calibrate" wait for the
routines to complete. do not take off the probe it ends at "bed_mesh" rebooting a few times.  5. run pid hotend / bed. Note "babystep" will be left 2mm high. one the first print loweer this, this is to avoid scrapes. 
also Note only the calibrate button resets babystep. if using klipperscreen delta_calibrate/probe_calibrate. babystep must be reset prior as it does not do this otherwise the old value will be in affect. e.g if its stil
-2mm low this could be a scrape. 

refer to the main v400 folder release notes for further info since firmware is "unified" 



cura / prusa start gcode files have the required code. 
