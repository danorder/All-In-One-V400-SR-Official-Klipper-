Flsun v400 overhaul in accordance to Klipper standards / delta. Page under construction.   

Whats new? 

v400 trams in acocradance to delta docs. 
Calibrate button which will run ,  Endstop calibration , Delta_calibrate , bed_mesh.  This button is to be used ONLY after Probe_calibrate has been run setting up the probe
offset.  The order of events remians absolute,  setup probe offset (probe_calibrate) delta_calibrae to apply zoffset / tram the arms only then will it be trammed allowing
mesh to work.  When running the calibrat button first preheat the bed to temp used for printing. The probe must be on. It is automated and will runn a routine rebooting /saving on its own
it will complete once bed_mesh has finished. Fluidd / Mainsail will also display what procedure is running. lastly once complete it will leave the (babystep) 0.6mm high
this is to avoid scrapes if Zoffseet is wrong. On the first print simply (babystep) down from mainsail or Klipperscreen.

Spread cycle and, stealth chops is possible. In accordance to tmc docs spreadcycle is the most accurate in theory howeverr it is degreeingly more loud. (not much) 
Safe homing 
Extruder in gear ratio 
1/254 stepping xyz
Tmc spreadsheet tuning 
autosaving Babystep based on Mental's xyz offset macro 
Heavy duty input shaper tuning 
Raspberry pi pico adxl support 
Idea maker profiles in accordance to delta / direct drive 
bed mesh works properly now..... 
