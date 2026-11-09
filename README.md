<h1 align="center">
  AUB
  <br>
</h1>
<h4 align="center">
Yet another USB HUB
</h4>
<div align="center">

![KiCad](https://img.shields.io/badge/kicad-%2300578F.svg?style=for-the-badge&logo=kicad&logoColor=white)
![STM32](https://img.shields.io/badge/STM32-03234B?style=for-the-badge&logo=stmicroelectronics&logoColor=white)

</div>
<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#pcb">PCB</a> •
  <a href="#credits">Credits</a> 
</p>


<p>&nbsp;</p>


# AUB

AUB is a 4-port USB 2.0 hub built around the WCH CH334U, with a USB-C upstream connection and 4 USB-A downstream ports.

wanted to build my own USB hub instead of buying another generic one. AUB is designed from scratch in KiCad, with proper power switching, ESD protection and a little CH32V003 MCU for the additional controls and status indicators.

the board also has 3 physical buttons and 5 status LEDs. everything is on one PCB, including the hub controller, power circuitry and the supporting MCU.

to build your own, grab the KiCad files, check out the schematics and BOM, and send the Gerber files to your preferred PCB manufacturer. the CH32V003 can be programmed through the SWIO header.

## Key Features

* **WCH CH334U** USB 2.0 hub controller with 4 downstream ports
* **USB-C** upstream connectivity
* **4x USB-A** downstream ports
* **CH32V003** MCU for additional controls and status indicators
* **Power management** using AP2161 with overcurrent reporting
* **ESD protection** on USB data lines using USBLC6-2SC6
* **3 physical buttons** for cycle, mode and brightness controls
* **5 status LEDs** for visual feedback
* **3.3V regulation** using AP2112K
* **4-layer PCB** designed in KiCad

## PCB

designed in KiCad with a 4-layer stackup. the layout includes the USB hub circuitry, MCU, power management and all the supporting components on a single board.

the USB connectors are positioned along the board edges, with the hub controller and its supporting circuitry grouped together. spent quite a bit of time adjusting placement and routing to keep things reasonably clean.

<img src="images/4-final-3d.png" alt="AUB final PCB 3D view" />

## Files

the repository includes the KiCad project files, schematics, BOM, Gerber exports and component placement files.

everything is open source, feel free to take a look, modify it or build your own!

### Schematic
<img width="1050" height="750" alt="image" src="https://github.com/user-attachments/assets/6c27fcf1-5ef9-4b3b-bda0-b4294381c30a" />
<img width="381" height="620" alt="image" src="https://github.com/user-attachments/assets/85f1fc95-866c-481b-8dc3-644a7626c3e7" />



---

### PCB Layers

#### F.CU
<img width="666" height="462" alt="image" src="https://github.com/user-attachments/assets/70b08e14-05eb-47e3-8718-415badf64f02" />


#### B.CU
<img width="666" height="462" alt="image" src="https://github.com/user-attachments/assets/7172b2c1-5a0e-4ab5-b356-8bb590a27ff7" />


## PWR
<img width="666" height="462" alt="image" src="https://github.com/user-attachments/assets/e0abf99c-ea5e-48e9-b6d3-5cc9de3a7e0f" />

## GND
<img width="666" height="462" alt="image" src="https://github.com/user-attachments/assets/27f2fe7a-0277-40ac-8f18-39fe009ece4a" />



---

### Board Views

#### Front
<img width="935" height="627" alt="image" src="https://github.com/user-attachments/assets/0266d833-d6d0-4061-b55c-3fcb3cb1a5b1" />


#### Back
<img width="935" height="627" alt="image" src="https://github.com/user-attachments/assets/91cb506c-03bd-481d-99fe-a4032e4b8ebe" />



### Zine
<img width="1587" height="2245" alt="AUB (1)" src="https://github.com/user-attachments/assets/cf1d1d43-9c01-4d94-9746-0c5bcf3a6205" />



## Credits

This project uses:
- [KiCad](https://www.kicad.org/)]
- [Hack Club Embassy](https://embassy.hackclub.com)

## License

GPL
