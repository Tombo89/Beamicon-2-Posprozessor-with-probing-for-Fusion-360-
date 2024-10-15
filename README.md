# Beamicon-2-Posprozessor-with-probing-for-Fusion-360-
This is a Postprozessor für Fusion 360 and HSM Works, for the Beamicon 2 Control Soft- and hardware. It supports the Probing function of HSM and Fusion 360 Cam.

## Please be carefull! This Postprozessor is still in developement and can cause serious harm to the machine or operator. Use it as a beta, to find issues, so that they can be eliminated.

# Known Issues

- not all probing cycles are implemented. See the list of implemented cycles below.
- Y axis angle rotation doesnt work and needs to be fixed.
- very slow Feedrate for probe moving distance
- lot of useless G0 Z0 inside subroutine file
- <b>Probe crashes into origin at the end of Y axis angle rotation</b>


# How to use this Postprozessor

This postprozessor is used as every other Fusion / HSM PP .cps file.
You can load it inside your software. You need to ad dthe hsm_probe_beamicon2_subroutine.txt file in your beamicon installations Macro folder.
This file contains the original Beamicon2 Macros, that where edited to fit the Postprozessors output.

Befor starting a created programm on your machine, make shure you set the origin of the touchprobe to roughly the same starting point, rellative to your workpiece like in the cam Simulaion.



var GV_PROBE_SPEED_FAST = 1; // Probe Feedrate schnell laut einstellung im PP in HSM Works
var GV_PROBE_SPEED_SLOW = 2; // Probe Feedrate langsam laut einstellung im PP in HSM Works
var GV_PROBE_SLOW_DISTANCE = 3; // Wie weit soll sich die probe im slow modus bewegen laut einstellung im PP in HSM Works
var GV_PROBE_TYPE = 4; // Nummer des ausgewÃ¤hlten Probetypen in HSM Works
var GV_X = 5; 
var GV_Y = 6; 
var GV_Z = 7; // Einstellung Rohteil Oberkante HSM Works
var GV_TOOL_DIA = 8;
var GV_FEEDRATE = 9; // HSM Works Einfahrvorschub
var GV_DEPTH = 10; // Rueckzugshoehe + Messtiefe+1mm
var GV_APPROACH1 = 11;
var GV_APPROACH2 = 12;
var GV_CLEARANCE = 13; // Abstand 1 HSM Works rÃ¼ckzug vom WerkstÃ¼ck
var GV_OVERTRAVEL = 14; // Abstand den der Taster Ã¼ber den erwarteten Weg hinausfahren darf laut HSM Works Einstellung
var GV_RETRACT = 15; // RÃ¼ckzughÃ¶he in HSM Works
var GV_WCS = 16;
var GV_WIDTH1 = 17; // Breite anzutastendes Objekt in Richtung Y
var GV_WIDTH2 = 18;
var GV_PROBE_SPACING = 19; // Abstand 2 in HSM Works zwischen den TastPunkten
var GV_TOL_POSITION = 20;  //the tolerance for the position
var GV_TOL_ANGLE = 21;  //the tolerance for the angle
var GV_TOL_SIZE = 22;  //the tolerance for the size
var GV_PAR_CIRC_ANG_A = 23; //the angle of the touch point relative to the WCS
var GV_PAR_CIRC_ANG_B = 24; //the angle of the touch point relative to the WCS
var GV_PAR_CIRC_ANG_C = 25; //the angle of the touch point relative to the WCSc


Value 4 Ausgewähltes Programm HSM Works

1 Einzelfläche X
2 Einzelfläche Y
3
4 X Steg
5 Y Steg
6
7
8
9 
10
11
12
13
14
15
16
17
18
19