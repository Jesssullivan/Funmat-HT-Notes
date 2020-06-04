
## *misc notes, files for Funmat HT (late, pre-enhanced) 3d printer*

***a WIP @ the D&M Makerspace***

*or, skip ahead and declare war on small volume thermoplastics and win back months worth of free time (and also pass go, collect $200, etc etc)*



The core of most of our Funmat HT struggles stem from the poor location and quality of the extruder.

 It is pretty much a clone of a clone of a mk8 direct drive unit, complete with a standard 11mm copper hobb (~10.6* mm usable diameter).  The extruder assembly is directly above the v6 standard hotend (it uses a nice pt100 type optocoupler instead of the sheathed thermistor usually seen on lower temperature machines though, still all within e3d spec) coupled together with a bit of PEEK tube.

 All "regular" filaments including Nylons and Polcarbonates inevitably soften (even just a tiny can destroy a print!) at the exruder gear after a few dozen layers or so, not helped by the fantastically well insulated and heated chamber.  The extruder assembly is devoid of any cooling or fans (or even just a breeze), and the hobb itself can get quite hot (it's copper!) in conjunction with the high amperage, high accuracy microstepping (1/16+) stressing the extruder stepper one can expect from this machine.  

As a result, here are some observations when printing with the stock hardware and most materials floating around the makerspace:

prints are best sent via octoprint.  This provides excellent (and much needed) temperature monitoring, as well as the option for pre / post / whim gcode additions and modifications.  Best to send `G28 ;` homing command before each print among others currently configured for the the D&M's octoprint machine profile.  

- make sure fan  blower are properly addressed, blower should be `fan 0` in slicer.  This value  usually defaults to `1`.

-  upload file via "upload" button in [octoprint](http://octopi.local/) (while on the makerspace network)

- both top and side doors must be completely open

- make sure fans are on again via `control` tab, best to preheat temps too

- tighten idler.  the hot stepper does change the characteristics of the idler's pressure, and should start "almost too tight"

- *hope*

* * *


**Etc-**  


The D&M machine's firmware should be `FUNMAT HT_181126_B.hex`.  It is unknown if any other pre-enhanced machines shipped with these newer stepper drivers like ours did, but Intamsys has confirmed updating to this version was needed.  

See adjacent for setup documents, gcodes and cura profile.
