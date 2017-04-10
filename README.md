# FLTSIM2D
Longitudinal 3DOF Flight Simulator for 2017 BASIC Game 10-Liner

-------------------------------------------------------------------------------
## STARTING THE GAME
There are versions for two machines: The contest version is written in BBC 
BASIC and runs on a BBC Model B with 65C02 coprocessor. I feel this is a 
"legal" configuration because it utilizes standard hardware from the era. 
The ATARI TurboBASIC XL runs on a stock 800XL, but at about 25% realtime speed.
To run realtime, select a 65C816 @ 7.16 MHz from Altirra's System/CPU 
Options... menu. I don't feel this is legal because the 65C816 is not a 
standard upgrade available from Atari and it is an 8/16-bit processor.

### To start the game on BBC Micro Model B for BASIC 10-Liner Contest:

Run the BeebEm emulator.
Enable a 65C02 second processor in the Hardware menu.
Load the "fltsim2d.ssd" as Disc 0 from the File menu.
Enter LOAD "FLTSIM" at the prompt, then RUN and have fun!

### To start the game on Atari 800XL:

Boot the Altirra emulator as an 800XL in NTSC with the fltsim2d.atr file.
Select an 65C816 @ 7.16 MHz from the System/CPU Options... menu.
The emulator should auto reboot and run the program.
Have fun!

-------------------------------------------------------------------------------
## CONTROLS
The controls are arranged after the layout in SubLogic's "Flight Simulator II." 

Elevator:           B (nose up) and T (nose down) - changes in 0.5 degree steps.  
Flaps:              N (out/down) and Y (in/up) - changes in 10 degree steps.  
Throttle (BBC):     .> (increase) and ,< (decrease)  
Throttle (Atari):   right arrow (increase) and left arrow (decrease)  

-------------------------------------------------------------------------------
## INSTRUMENT DISPLAY
The display is organized in three four sections:

* There are four indicators:  

| Indicator | Description |
| --- | --- |
| KTAS  |    True airspeed in KNOTS. One knot is about 1/2 m/s or 2 kph. | 
| PITCH  |   Pitch in degrees. Positive pitch is nose up. | 
| ALT.   |   Altitude in feet. |   
| VRATE  |   Vertical rate with respect to the ground in feet per minute.  |

* There are three control setting readouts:  
ELEV.     Elevator position in degrees. Increments in 0.5 degree steps.   
POWER     Fraction of engine power in %. Controlled by the throttle.  
FLAPS     Flap position in degrees. Flap position changes slowly.  

* Next is the STALL warning indicator:  
STALL     A "!" and a BEEP mean you have dropped below the stall speed.  

* Finally are time and distance displays:  
DIST.     Distance over ground traveled in yards.  
TIME      Time elapsed in seconds and rate of game time relative to real time. The ATARI rate is correct for NTSC framerate and high for PAL.  

-------------------------------------------------------------------------------
## PLAYING THE GAME
The simulator is based on a Cessna 172. Does it fly like one? It stalls near 
the right speed. It climbs way too fast. It has about a 14000 ft ceiling.
There's a wicked phugoid - do not chase the VRATE.

Try to takeoff, level out and land. Crash once or twice. Here's a step-by-step
description for successfully complete a mission.

### Takeoff
Increase the power to 100% by repeatedly pressing the .> key 20 times.
Extend the flaps 10 degrees by pressing N once.
When KTAS hits 50 knots, pull back on the yoke by pressing B about 45 times. 
The elevator will be deflected more than -20 degrees. During this time, the
aircraft will rotate (pitch positive) and lift off the ground. 
Once off the ground, slowly bring the elevator down to increase KTAS while
keeping pitch positive and climbing. Once KTAS is around 90 knots, retract the
flaps by pressing Y once. Speed will increase.

### Flight
Climb to desired altitude. A fast rate of climb is achieved at about 100-110 
knots KTAS. Elevator up to slow down, elevator down to speed up. The maximum
altitude is maybe 14,000 ft. When approaching desired altitude slowly back off
on the power ,< to 75%. Slowly adjust the elevator (down) to level out. 

Stay below 125 KTAS. 

To descend, reduce the throttle for a VRATE of roughly -500 fpm. If you drop
too fast, your ears will pop! Keep KTAS < 125. Nose up the elevator to slow 
down. 

### Landing (or crashing!)
Descend to 1200 feet and slow to 85 knots. Extend flaps by 10 degrees. This 
should slow you down more. At 75 knots, extend flaps another 10 degrees. 
Slow to 70 knots. At 500 feet, extend flaps the final 10 degrees. Use pitch
to control your speed between 60-70 knots. Use power/throttle to maintain
a descent rate of >-500 fpm. Do not chase the VRATE or KTAS - the wicked 
phugoid will get you. At the desired speed and vertical rate, the aircraft 
will land itself.

## THINGS TO TRY
* Crash
* Find the altitude ceiling
* Stall and recover

 
