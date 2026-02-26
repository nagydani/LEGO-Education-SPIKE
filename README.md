# LEGO Education SPIKE

In this reporsitory, you'd find the results of reverse-engineering efforts aimed at 
SPIKE Essential and SPIKE Prime kits, discontinued by LEGO in June 2026.

## Introduction

As of February, 2026, SPIKE is the most recent line of LEGO Robotics sets, targeted 
for the education market. SPIKE Essential is for younger children (6+ by LEGO 
classification), SPIKE Prime is for older children (10+ by LEGO classification). 
Both sets include one *hub*, a microcontroller brick running MicroPython and various 
peripherials to be attached to them. Both the hub and the peripherials use 
exclusively LEGO Technic couplings through holes and pins in a studless fashion. 
All the peripherials of both sets are compatible with both hubs. Both sets have an 
optional "Personal Learning Kit" that can be purchased separately, neither of which 
has additional electronic components.

The only recommended use is through the same LEGO SPIKE app (available both as a web-app 
for desktop/laptop computers and as an installable app for Android and iOS tablets), 
which is quite limiting, especially for the SPIKE Essential kit.
Although LEGO did not include any technical measures to enforce this and even documents 
some aspects of the inner workings, this documentation is nowhere near sufficient to 
use these sets without relying on LEGO SPIKE app. This project aims to rectify the 
situation.

## SPIKE Essential

This set has contains a small hub with 2 ports, an inertial sensor package a single 
controllable color LED and one button. With its LEGO-supplied firmware, it must be connected 
to a host computer at all times either though USB or Bluetooth. If connection is lost, 
the hub shuts down in 10 seconds and it has no facilities for presisting user-supplied 
software.

The supplied peripherials are two *small motors*, one 3x3 *LED matrix* and one 
*color sensor*.

The rest of the set contains a small selection of LEGO Technic elements, some of them 
for interfacing with LEGO System bricks. In particular, it contains no gears. The models 
are supposed to be built mostly using simple LEGO System brick stacking techniques. Given 
the low torque of the small motors and the lack of elements for compounded mechanical 
advantage (except levers), this building technique is quite adequate.

In addition to structural parts, the set contains a very large number of decorative parts, 
including four minifigures representing child characters with names for story-telling. 
For optical experiments, the set contains a plastic magnifying lens with a focal distance 
of 3 FLU (24mm) of fairly low quality.

The "Personal Learning Kit" contains two more teacher mini-figures (one male, one female) 
and a selection of additional parts, including LEGO Technic parts missing from the 
main set, such as two frames and two double-bevel cogwheels (20 and 12 cogs, respecitvely) 
that can be used at angles between 0 and 90 degrees for simple geared mechanisms. 
It also contains an additional lens identical to the one in the main set for more 
sophisticated optics experiments.

## SPIKE Prime

*To be continued...*
