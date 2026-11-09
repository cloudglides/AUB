---
title: AUB
author: Cloudglides
description: Another USB Hub!!
---

### TOTAL TIME: 32 HOURS

## Day 1 | USB hub schematic | November 7th | 7 hours

okay so i've been working on a 4 port USB 2.0 hub!

the idea is to have a single USB C upstream connection and break that out into 4 USB A ports. started working on the schematic in kicad and got most of the main circuitry in place now.

for the actual hub controller im using the WCH CH334U. it handles all the USB communication and gives me the 4 downstream ports. got the upstream USB C connection wired up as well, including the CC resistors and the data lines.

one thing i wanted to get right was the power side of things. the hub is going to be bus powered, meaning it gets its power directly from the upstream connection. im using an AP2161 power switch for the downstream VBUS with overcurrent reporting. this should let the hub handle power distribution to the individual ports properly.

also added USBLC6 protection ICs for the USB data lines on all 4 downstream ports. figured its better to have some ESD protection rather than risk damaging the controller or whatever is connected to it.

got all 4 USB A connectors in place now, with their respective data lines and power connections. added the 12MHz crystal for the controller, decoupling capacitors, pull resistors and the status LEDs too.

heres the current schematic!

<img width="4961" height="3508" alt="AUB" src="https://github.com/user-attachments/assets/01fc35bc-d41d-4cce-be5b-2768802ad1cd" />


still need to go through the whole thing and double check the connections against the datasheets. especially the power switching and overcurrent bits. haven't moved onto PCB layout yet but the main circuit is looking damn good

pretty happy with the progress so far!

## Day 2 | getting the keyboard circuitry together | November 8th | 7 hours

back at it again! got quite a bit of the schematic done today, this time focusing on the actual keyboard circuitry.

started putting together the switch matrix. its an 8x8 matrix with individual diodes for each switch, so thats 64 switch positions in total. each row and column has its own net which should make things a lot easier when routing the PCB later.

also started working on the MCU side of things. got the GPIO connections mapped out for the matrix along with the other signals needed for the board. added the SWD and UART headers too so i have a way to flash and debug the firmware without having to mess around too much.

for power im using an AP2112K 3.3V regulator. added the input and output capacitors and started placing the decoupling capacitors around the rest of the circuit. also got the VBUS and 3.3V power connections sorted out.

another small thing i added was the three control buttons for cycle, mode and brightness. each has its own pull up and filtering capacitors. also added the reset circuitry and a few sensing lines for monitoring the power.

heres how the schematic is looking right now!

<img width="1227" height="762" alt="image" src="https://github.com/user-attachments/assets/23d35a1e-d110-4451-897a-e52cf17714d1" />


still have some checking to do before calling this part finished but the main switch matrix and controller connections are in place now. starting to look like an actual keyboard circuit instead of a bunch of disconnected components lol

next up is going through the connections properly and eventually moving towards the PCB layout.

## Day 3 | first PCB layout! | November 9th | 5 hours

finally started working on the PCB layout!

moved over from the schematic and started arranging all the components on the board. wanted to keep things reasonably organised so i've been grouping components based on what they actually do rather than just throwing everything wherever it fits.

got the upstream USB C connector on the left, followed by the power circuitry and the main hub controller. the 4 downstream USB A ports are placed together on the right side. also brought over the MCU section, buttons, LED driver and the entire switch matrix towards the bottom.

still experimenting with the placement rn. trying to figure out how to make everything fit while keeping the connections as reasonable as possible. there's quite a lot of components here and the ratsnest is already looking a little scary lol

also placed the mounting holes and started figuring out the general board arrangement. i haven't started routing anything yet, mostly just focusing on getting the components in the right places first.

heres what the board looks like so far!

<img width="791" height="701" alt="image" src="https://github.com/user-attachments/assets/82f54cf6-ff90-49a5-a171-1818d187e74f" />


definitely still a lot of work left to do. need to clean up the placement, think about the routing and make sure the USB data lines and power connections get enough attention.

## Day 3 | PCB routing progress | November 9th | 10 hours

spent some more time on the PCB today and started working on the actual routing!

this is my first time making a pcb with 4 layers, taking some time

redid the routing like 3 times :pf: its kinda hard idk

still a WIP rn and theres definitely a lot left to do. need to clean up the routing, check clearances and make sure everything is looking good before i can call this done.

heres where the PCB is at currently!

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/40f056e1-12b7-495a-a075-bf70c5ca009d" />


slowly getting there :p

## Some Day | 2h

worked on the github repo, zine and readme :p

<img width="1587" height="2245" alt="AUB (1)" src="https://github.com/user-attachments/assets/28c03436-d895-4e4f-8755-75446505a032" />
