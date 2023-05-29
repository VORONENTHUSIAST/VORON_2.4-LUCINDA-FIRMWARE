# VORON-2.4-r2-MKS-SKIPR-Build-CUSTOM-SIZE-

This is my Klipper Configuration for the Voron 2.4 r2.
<br>It contains the Macros I'm using, as well as basic printer settings, etc.
<br> I will always be working on this and finding new ways to arrange my configuration into different files, so you will find it changes. A lot!

This firmware will be used on three custom sized Voron 2.4 r2's. 1 is currently up and running printing the second.
<br>The second one will be finished by 10/05/2023.
<br>The third will probably happen late 2023 / early 2024.

**About this repository...**

With the help of the Voron Discord group, this firmware is running, thanks a lot!!

**USE AT YOUR OWN RISK!!**

**PLEASE NOTE!!** If you do intend to mess around, and have already got your printer up and running, **DO NOT** just copy and paste this until you are on the latest version of Klipper, Moonraker, etc. The SKIPR boards come with an old version of Moonraker, Klipper and Fluidd pre-installed and you will not be able to view any files / gcode files due to paths being depreciated!

**Goals for this printer:**

A printer that gets used for printing ABS 24/7 - I have always printed in ABS using bed slingers. I have acheived stunning prints, but enclosing anything larger than 235x235mm is a pain!

I wanted to have next gerneration printers with 300x300mm build plates and above for as cheap as possible!

Reliability, Usability - I wanted to build a couple of units that are easier to use than my old print farm. 
<br>Low Noise - Fans and motors can give you a headache!
<br>Print Speed - Knowing CoreXY units are inherrantly faster than Bed Slingers, I wanted to try and push a little further than the norm.
<br>Print Quality - I'm not going for Benchy Speed Records here, I still want parts to need minimal post-processing.

**About the Printer's Hardware...**

So far, the printer itself uses the standard inductive sensor and vanilla 3d printed parts. The Case is slightly different to standard.

As I initially planned to upcylce a broken SteadyTech Pro X for the first build, the following has been recycled on printer 1:

24v Heated Bed
<br>Bed Mount
<br>Motors 
<br>PSU 
<br>Power Switch
<br>Endstops

Sadly, I came into issues with other parts of the old printer that meant a lot got ditched into the local recycling centre, a fair bit was salvaged for other projects.

It utilises the following electronics hardware:

MKS SKIPR V1.0 Main Board
<br>MKS Pi TS-35 Touch Screen
<br>TMC2209 Stepper Drivers
<br>PL-08N2 Proximity sensor
<br>COMFAST CF-WU810N Wireless Dongle (Plug and play)
<br>ADXL345 Accelerometer 

**Klipper Software Customization...**

The following software customization has been added:

Klipper Cancel Object Preprocessor - Makes it possible to cancel objects to potentially save a print (Requires modifying your Slicer). 
<br>Print Area Bed Meshing (KAMPS) - A Macro that enables you to take a mesh of the area you will be printing on only (enabled in START_PRINT macro). **As of 1st May 2023, this is not working yet. For some reason my slicer is not processing my start_print Macro, I need to slow the error messages down on my screen to find out why!**

**Problems Experienced:**

The Initial MGN9 rails that I purchased for the Z were not machined correctly - this caused all sorts of binding issues, so they were returned. Buy cheap, buy twice!
<br>I started off with an incorrect sized frame from trying to re-use the SteadyTech extrusion. I tried to fix this by printing small bits of extrusion to place at either end - this DID NOT work!!
<br>I have since replaced with a full sized frame (all beit using printed corner cubes) and the printer mechanics now work flawlessly! Firmware, that's another story...

**Things I have learned:**

Klipper!! I was new to klipper at the start of my build, a month or so in and it feels like a familiar friend - far more intuitive than Marlin!
<br>Input shaping - Absolute blessing! Really helps to ramp up print speeds while maintaining quality!
<br>Cancel Object Pre-processor. I'm sorry, whaaaaaa?! So I can cancel prints on a multiple build if I don't like how they're going?! AMAZING!!! 
<br>KAMPS - this is now running, I was really tired when trying to implement this and foolishly got my macro name the wrong way around in the slicer, all now works and I am tweaking the adaptive purge line / Voron purge line to my liking!

**Things I'm still learning:**

Stepper Motor Tuning...

There is a guide on github (https://github.com/MakerBogans/docs/wiki/TMC-Driver-Tuning#example-for-an-extruder-motor) that I'm currently exploring.
I will be adding this into my printer when I'm comfortable with it.

KlipperScreen - I am making my own background and adding my own splash screen, whether the splash screen is 100% doable on the MKS PI-TS35 is another story, there seems to be a splash screen embedded in to the EEPROM that causes issues with my own image. Hopefully I can find a fix!!

**What I plan to do next...**

Finish building the second 310x310x300mm 2.4 r2
<br>Make a 600x600x1000mm version because I had a massive heat bed given to me that's sitting collecting dust (possible modification of parts for this to accomodate a larger frame).
