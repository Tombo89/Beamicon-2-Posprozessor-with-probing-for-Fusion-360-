# Beamicon-2-Posprozessor-with-probing-for-Fusion-360-
This is a Postprozessor für Fusion 360 and HSM Works, for the Beamicon 2 Control Soft- and hardware. It supports the Probing function of HSM and Fusion 360 Cam.

Most of the code is based on the Fusion 360 Postprozessor for Mach3 with probing functionality by mlm solutions. <a href>http://www.mlmsolutions.biz/fusion_post_mach3_probing.php
</a>. Thank you for your work, and well documented changes in the code so its easy to adopt.

As the code of mlm is free to use, and I am allowed to use it here, this code will also be free to use, change or adapt to your requirements.

## Please be carefull! This Postprozessor is still in developement and can cause serious harm to the machine or operator. Use it as a beta, to find issues, so that they can be eliminated. The Code is mostly copyed together from various resources an need to be clead up.

# Known Issues

- not all probing cycles are implemented. See the list of implemented cycles below.
- selection of other probe cycles can create unwanted moves on machine



# How to use this Postprozessor

This postprozessor is used as every other Fusion / HSM PP .cps file.
You can load it inside your software. You need to ad dthe hsm_probe_beamicon2_subroutine.txt file in your beamicon installations Macro folder.
This file contains Beamicon2 Macros, that where edited to fit the Postprozessors output.

With this postprozessor you will get 4 new settings in your software.

<a href="" target="blank"><img align="center" src="/images/hsmworks_pp_settings.PNG" height="250" /></a>

<ul>
    <li>Fast probing speed (mm/min) - sets the fast speed for the first fast measuring cycle</li>
    <li>Slow probe distance (mm)    - defines the distance that the probe should back up after beeing triggered</li>
    <li>Slow probing speed (mm/min) - sets the slow speed for backing up after first measuring cycle and sets the speed for the second slow cycle if selected</li>
    <li>Make second probe cycle     - can be set to yes or no. If set to yes a second probe cycle at a slower speed will be made to improve accuracy</li>
</ul>

Befor starting a created programm on your machine, make shure you set the origin of the touchprobe to roughly the same starting point, rellative to your workpiece like in the cam Simulaion.

The Machine will start the probing cycle with the fast speed, and will back up with the slow speed untill the probe is released. If the second probe cycle option is set, the probe will back out with the probe distance and start a second cycle with the slow speed for better accuracy.




# Currently implemented probing cycles that seem to work fine / variable #4
<ol>
    <li>Einzelfläche X</li>
    <li>Einzelfläche Y</li>
    <li>Einzelfläche Z</li>
    <li>X Steg</li>
    <li>Y Steg</li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li>Einzelner Flaechenwinkel Y</li>
</ol>

# Variables created by the Postprozessor

coming soon