# Introduction
 
This is the draft online guide for MR-B3RB-M Pre-Production version. Please excuse our "dust" while this gitbook is under construction. Supportive feedback is welcome: [iain.galloway@nxp.com](mailto:iain.galloway@nxp.com)
 
You can expect frequent updates as the pre-production units become closer to production. We will try to address any questions about assembly here. Check back often.
 
Also, take a look at some of our other GitBooks:
- **NXP Mobile Robotics**: Quick reference and index for all our mobile robotics solutions.
- **MR-B3RB**: NXP Buggy3 Rev B platform using NavQPlus and MR-CANHUBK344
- **HoverGames**: Drone & rover dev. kits, with FMUK66 vehicle management unit.
- **NXP Cup**: Autonomous model car competition for students.
- **MR-CANHUBK344**: Small form factor CAN-FD to 100BASE-T1 ethernet bridge.
- **UCANS32K146**: CAN-FD node for mobile robotics applications.
- **RDDRONE-BMS772**: Battery management system (3-6 cells).
- **RDDRONE-T1ADAPT**: 100BASE-T1 ethernet adapter.
 
## Pre-Production MR-B3RB-M Block Diagram
 
### MR-B3RB System block diagram
 
### Block Diagram: Power Distribution
 
The PDB (Power Distribution board) is primarily a connector board and allows things like the specialized connectors on the motor and encoder to translate to the Dupont-style or standard DroneCode connector pinouts. It should be noted that the block diagram above does not show the power distribution connections, which are as follows:
- Battery input through a fuse
- Battery voltage and current measurement through the INA226
- 3x Battery voltage outputs on 5 pin JST-GH for NavQPlus, MR-CANHUBK344, Extra 5V regulating supply for LED lights, and powering PWM servo rail on MR-CANHUBK344 and therefore the Servo itself.
 
### Block Diagram: GPS Module
 
The GPS combines UART, I2C for Compass, and GPIO for switches, LED, and Beeper into a single large DroneCode standard connector.
 
### Block Diagram: Debugging interfaces
 
The DCD-LZ interface simply combines SWD and a UART on a single JST-GH Dronecode connector. Depending on your kit you may have any of the following debug adapter boards:
- FTDI USB-UART cable and adapter for UART/Console on the NavQPlus
- FTDI USB-UART cable + DCD-LZ adapter for MR-CANHUBK344 DCD-LZ interface
- NeuralProbe board with USBC interface and connectors for UART/Console AND DCD-LZ interface. This board includes a USB-UART converter and also includes a button that will toggle the RST pin on SWD/JTAG interface. There is a 3rd interface on this board for Pixhawk V6X debug+uart connectors (not used here, used with NXP MR-VMU-RT1176)

# What's in the Box
 
These pages are for REFERENCE; use the BUILD guide for actual assembly. Because the MR-B3RB is a "kit of kits," we will show what components are in the box, grouped with the sub-kit that it relates to. These sub-pages will describe the individual sub-kit. Each page contains a components table which enumerates all the parts that are included in the kit. The diagrams on the pages contain the pictures of the parts. The parts are labelled with their corresponding serial numbers, either directly in the diagram or in the heading of the diagram. To understand the possible configurations, please refer to the Naming and Versions page.
 
## WITB Cables and Screws
 
Because this is the pre-production version of the MR-B3RB, some cables and screws are not as clearly separated in the sub-kits as they could be. For clarity, we will mention them and their purpose here.
 
### Cables and Screws Components
 
The wires represented by rows with serial numbers 6 and 7 in the following table are not included in the current (Pre-Production) unit. Refer to the Errata on the Pre-Production unit. In their place, incompatible cables are included and their pictures are shown in the diagrams on this page for reference purposes.
 
| S.No. | Description                                                                                              | Quantity |
|-------|----------------------------------------------------------------------------------------------------------|----------|
| 1     | Cable, Lidar to NavQPlus 6-Pin JST-GH to 4-Pin JST-PH                                                    | 1        |
| 2     | Cable, XT60 PANEL MOUNT ADAPTER to XT60 Connector with Cover                                             | 1        |
| 3     | XT60 Connector with Cover                                                                               | 1        |
| 4     | Cable, Twisted, Black, 5-PIN JST-GH to 5-PIN JST-GH (With only 4 wires connected and middle wire unconnected) | 1        |
| 5     | Cable, 3 Pin Female Dupont Jumper to 6-PIN JST-GH                                                         | 1        |
| 6     | Cable, Back APA102 Strip (IN Port) to CANHUBK3, 7-PIN JST-GH to Stemma QT/Qwiic JST SH 4-Pin              | 1        |
| 7     | Cable, Back APA102 Strip (OUT Port) to Front APA102 Strip (IN Port), Stemma QT/Qwiic JST SH 4-Pin to Stemma QT/Qwiic JST SH 4-Pin | 1        |
 
### Cables and Screws Diagrams
 
- Cables and Connectors
- WITB MR-B3RB-BMF
 
## What's in the Box — Base Mechanical Frame
 
### Base Mechanical Frame Components
 
| S.No. | Item Number | Description                                                                                     | Quantity |
|-------|-------------|-------------------------------------------------------------------------------------------------|----------|
| 1     | 901-10008    | HW ACCESSORY, WLTOYS WL124017 CAR WITHOUT RADIO CONTROLLER, WITHOUT BATTERY AND WITHOUT RADIO RECEIVER and 1:12 Electric 4WD Climbing Car Instruction Manual for Model No. 124017 and USB Charger KX7V4-200 7.4V 2S with 3 Pin Connector | 1        |
| 2     | 901-77273    | HW ACCESSORY, J-LINK EDU MINI DEBUGGER                                                           | 1        |
| 3     | 700-31354    | PWA, DCD-LZ-ADAPT                                                                              | 1        |
| 4     | 600-77370    | CABLE, USB-TTL, FTDI TTL-232R-3V3, 6 PIN CONNECTOR, +3.3V, 0.70 M                              | 1        |
| 5     | 901-77364    | RC TOOLS 7 IN 1 HEX SCREWDRIVER SET HEXAGONAL                                                   | 1        |
| 6     | 280-77408    | PRE-CUT DOUBLE-SIDED FOAM SQUARES - 1/16" thick, 1/2 x 1/2"                                    | 10       |
| 7     | 901-77659    | HW ACCESSORY RC XT60 FEMALE TO MALE DEANS T PLUG ADAPTER                                        | 1        |
| 8     | 600-77612    | CABLE TIES, BLACK UV STABILIZED NYLON - 4", 18 LB                                               | 10       |
| 9     | 700-47472    | PX4ARMINGBRD Board                                                                             | 1        |
| 10    | 600-77546    | Cable for PX4ARMINGBRD (10-Pin JST-GH)                                                           | 1        |
| 11    | 901-10005    | HW ACCESSORY, DIRECT TIME OF FLIGHT LIDAR                                                       | 1        |
| 12    | 280-10004    | FASTENER, SCREW M2.5x10MM BLACK HEX SOCKET HEAD CAP                                             | 3        |
| 13    | 280-10006    | NUT, M2.5 x 0.45MM NYLON INSERTED HEX SELF LOCK NUT, BLACK ZINC PLATED, DIN985                    | 3        |
| 14    | 280-10007    | FASTENER, SCREW M3 X 0.5 X 8.0MM LONG, HEX DRIVE, BUTTON HEAD, PASSIVATED 18-8 SS                  | 3        |
| 15    | 280-10008    | NUT, M3 X 0.5 X 4MM NYLON INSERTED HEX SELF LOCK NUT, BLACK ZINC PLATED                            | 3        |
| 16    | 280-10009    | FASTENER, SCREW M3 X 0.5 X 5.0MM LONG, HEX DRIVE, BUTTON HEAD, PASSIVATED 18-8 SS                  | 16       |
| 17    | 280-10012    | FASTENER, SCREW M3 X 0.5 X 10MM LONG, HEX DRIVE, SOCKET HEAD, 18-8 SS                            | 8        |
| 18    | 280-10013    | FASTENER, SCREW M3 X 0.5 X 14MM LONG, HEX DRIVE, SOCKET HEAD, 18-8 SS                            | 4        |
| 19    | 280-10014    | FASTENER, SCREW M2.5 X 0.5 X 8MM LONG, PHILLIPS, FLAT HEAD TAPPING, 18-8 SS                      | 4        |
| 20    | 805-77575    | THE HOVERGAMES; COLOR LABEL Die Cut Sticker: 3.0" X 2.91"                                       | 1        |
| 21    | 805-10002    | LABEL, COGNIPILOT SMALL LOGO STICKER, 1" X 1"                                                   | 2        |
| 22    | 805-10001    | LABEL, NXP COLOR LOGO STICKER, 75MM X 30MM                                                      | 1        |
| 23    | 805-10003    | LABEL, COGNIPILOT LARGE LOGO STICKER, 50MM X 30MM                                               | 1        |
| 24    | 901-77605    | HW ACCESSORY, M3 NYLON SPACER KIT 180PCS M3 NYLON M-F HEX SPACERS SCREW NUT ASSORTMENT SET          | 1        |
| 25    | 901-77606    | HW ACCESSORY, M2/M2.5/M3 SCREW FASTENER KIT FOR WLTOYS 144001 1/14 RC                            | 1        |
| 26    | 600-10006    | CABLE, SERVO EXTENSION LEAD WIRING CABLE MALE TO MALE, 300 MM                                    | 2        |
| 27    | 600-77359    | CABLE, CUSTOM FOR DCD-LZ-ADAPT, 7 POSITION, JST-GH CONNECTOR, 100 MM                             | 1        |
| 28    | 901-10012    | HW ACCESSORY, XT60 PANEL MOUNT ADAPTER                                                            | 1        |
| 29    | 600-10009    | CABLE, CUSTOM PDB TO CANHUBK3 CABLE, 6 POSITION, JST-CH CONNECTOR, 10 INCHES                      | 1        |
| 30    | 590-10002    | FOAM, BLOCK 400MM WIDTH 600MM LENGTH X 200MM THICKNESS                                          | 1        |
| 31    | 280-77781    | FASTENER STANDOFFS 6x35MM & (TOP/BOTTOM) 3MMx5 SOCKET HEAD                                        | 1        |

# Description of Components
 
## J-Link EDU MINI DEBUGGER
 
### J-Link EDU MINI DEBUGGER Components
 
| S.No. | Description                                    | Quantity |
|-------|------------------------------------------------|----------|
| 1     | J-Link EDU Mini                                | 1        |
| 2     | 10-Pin 2x5 Socket-Socket IDC (SWD) Ribbon Cable | 1        |
| 3     | Micro-USB (Male) to USB-A (Male) Cable         | 1        |
| 4     | 20-Pin 2x10 Socket-Socket IDC (SWD) Ribbon Cable | 1        |
 
### M3 NYLON SPACER KIT
 
- 180PCS
- M3 NYLON M-F HEX SPACERS
- SCREW NUT ASSORTMENT SET (S.No. 24)
- M3 SPACER KIT
 
#### Outside View
- M3 SPACER KIT
 
#### Inside View
- M3 SPACER KIT
 
### M2/M2.5/M3 SCREW FASTENER KIT FOR WLTOYS 144001 1/14 RC
 
- SCREW FASTENER KIT (S.No. 25)
 
#### Outside View
- SCREW FASTENER KIT
 
#### Inside View
- SCREW FASTENER KIT
 
### MR-B3RB-PDB (Power Distribution Board)
 
- MR-B3RB-PDB Close-Up
- MR-B3RB-PDB Assembled
 
### Stickers and Accessories
 
- "THE HOVERGAMES" (S.No. 20)
- "NXP" (S.No. 22)
- "COGNIPILOT" (S.No. 23, 21) Stickers
- Cable Ties (S.No. 8)
- PRE-CUT DOUBLE-SIDED FOAM SQUARES (S.No. 6)
 
### Cables and Adapters
 
- DCD-LZ-ADAPT (S.No. 3)
- 7 POSITION JST-GH CONNECTOR (100 MM) (S.No. 27)
- XT60 FEMALE TO MALE DEANS T PLUG ADAPTER (S.No. 7)
- CABLE, CUSTOM PDB TO CANHUBK3 (S.No. 29)
- CABLE, USB-TTL, FTDI TTL-232R-3V3 (S.No. 4)
- CABLE, SERVO EXTENSION LEAD WIRING CABLE MALE TO MALE, 300 MM (S.No. 26)
- XT60 PANEL MOUNT ADAPTER (S.No. 28)
 
### Fasteners
 
- FASTENER, SCREW M3 X 0.5 X 5.0MM, HEX DRIVE, BUTTON HEAD (S.No. 16)
- FASTENER, SCREW M3 X 0.5 X 10MM, HEX DRIVE, SOCKET HEAD (S.No. 17)
- FASTENER SCREW M3 X 0.5 X 14MM, HEX DRIVE, SOCKET HEAD (S.No. 18)
- FASTENER, SCREW M2.5 X 0.5 X 8MM LONG, PHILLIPS (S.No. 19)
- FASTENER, SCREW M3 X 0.5 X 8.0MM LONG, HEX DRIVE, BUTTON HEAD (S.No. 14)
- NUT, M3 X 0.5 X 4MM NYLON INSERTED HEX SELF LOCK NUT, BLACK ZINC PLATED (S.No. 15)
 
### Additional Components
 
- 1:12 Electric 4WD Climbing Car Instruction Manual for Model No. 124017
- USB Charger KX7V4-200 7.4V 2S with 3 Pin Connector
- PX4ARMINGBRD Board (S.No. 9)
- Cable for PX4ARMINGBRD, 10-Pin JST-GH to 10-Pin JST-GH (S.No. 10)
- RC TOOLS 7 IN 1 HEX SCREWDRIVER SET HEXAGONAL (S.No. 5)

# WITB MR-CANHUBK344
 
## What's in the Box — MR-CANHUBK344 Components
 
### MR-CANHUBK344 Components
 
| S.No. | Item Number | Description                                     | Quantity |
|-------|-------------|-------------------------------------------------|----------|
| 1     | 700-89377    | PWA, MR-CANHUBK344                             | 1        |
| 2     | 700-47294    | PWA, DRONE-CAN-TERM (CAN Bus Termination Resistor) | 1        |
| 3     | 336-77458    | HW ACCESSORY, 0.91 inch OLED Display Module IIC SSD1306 128x32 OLED | 1        |
| 4     | 600-77466    | CABLE, 4 PIN JST-GH TO 4 PIN JST-GH 300 MM      | 1        |
| 5     | 600-77467    | CABLE, ASSY, 4 PIN JST-GH TO 4 PIN JST-GH 50 MM | 1        |
| 6     | 600-77521    | DATA CABLE, 2 PIN JST-GH TO 2 PIN JST-GH 254 MM | 1        |
| 7     | 600-77602    | HW ACCESSORY, 5 PIN TO 5 PIN POWER INPUT CABLE | 1        |
| 8     | 600-77603    | HW ACCESSORY, POWER INPUT CABLE SYP TO DC5.5, 2.1 JACK | 1        |
| 9     | 600-77604    | HW ACCESSORY, POWER INPUT CABLE, SYR 2 PINS TO GHR 5 PINS | 1        |
| 10    | 600-77625    | HW ACCESSORY, XT60 Male to XT60 Female with SYP in parallel | 1        |
| 11    | 926-79071    | POSTCARD, MR-CANHUBK344, 6" X 4"               | 1        |
| 12    | -           | CABLE, 6 PIN JST-GH TO 6 PIN JST-GH 150 MM      | 1        |
 
# WITB MR-B3RB-PDB
 
## What's in the Box — MR-B3RB-PDB (Power Distribution Board) Components
 
- This board is being revised to include power measurement capability. The final version will look different than what is shown here.
 
### MR-B3RB-PDB (Power Distribution Board) Diagrams
 
- MR-B3RB-PDB Assembled
- MR-B3RB-PDB Close-Up
 
# WITB MR-B3RB-MUK
 
## What's in the Box — Mechanical Upgrade Kit Components
 
### Mechanical Upgrade Kit Components
 
#### Metal Parts
 
| S.No. | Description               | Quantity |
|-------|---------------------------|----------|
| 1.A   | Lidar "Arch"              | 1        |
| 1.B   | Decorative Top Cover      | 1        |
| 1.C   | Side Skirts               | 2        |
 
#### Plastic Parts
 
| S.No. | Description                           | Quantity |
|-------|---------------------------------------|----------|
| 2.A   | Side Plastic Panels                   | 4        |
| 2.B   | Front Plastic Shield with Mount for Camera | 1        |
| 2.C   | Back Plastic Shield                   | 1        |
| 2.D   | Covers for LEDs (Transparent)         | 2        |
| 2.E   | Front Plastic Panel for LEDs          | 1        |
| 2.F   | Back Plastic Panel for LEDs           | 1        |
 
#### Fasteners
 
| S.No. | Description                                    | Quantity |
|-------|------------------------------------------------|----------|
| 3     | Thumbscrew M3 X 0.5 X 15MM                     | 12       |
| 4     | FASTENER, SCREW M3 X 0.5 X 10MM LONG, PHILLIPS, FLAT HEAD TAPPING, 18-8 SS | 10       |
| 5     | NUT, M3 X 0.5 X 4MM HEX SELF LOCK NUT, 18-8 SS | 10       |
| 6     | FASTENER, SCREW M3 X 0.5 X 10MM LONG, HEX DRIVE, SOCKET HEAD, 18-8 SS | 9        |
 
### Description of Components
 
- Thumbscrew M3 X 0.5 X 15MM (S.No. 3)
- SCREW M3 X 0.5 X 10MM PHILIPS, FLAT HEAD (S.No. 4)
- NUT M3 X 0.5 X 4MM HEX (S.No. 5)
- SCREW M3 X 0.5 X 10MM HEX DRIVE, SOCKET HEAD (S.No. 6)
 
- Thumbscrew M3 X 0.5 X 15MM
- SCREW M3 X 0.5 X 10MM
- NUT M3 X 0.5 X 4MM HEX
- SCREW M3 X 0.5 X 10MM
