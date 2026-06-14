# version0.65

version0.65 is a 65% keyboard which follows the Leopold FC660M layout. It is bluetooth keyboard, using the SuperMini nRF52840 board, which is pin compatible with the nice!nano v2.
It has a built in battery along with a On/Off switch.

The keyboard is hotswap, with gateron hotswap sockets and Gateron Blue switches.

The PCB was designed in KiCad and the case was designed in Autodesk Fusion. The footprints for the switches have been taken from the marbastlib library - https://github.com/ebastler/marbastlib

This Keyboard was made for Hack Club KEEB.

Note: This is still a WIP. Please copy at your own risk.

## Repository Guide
```
version1/
|── PCB/
|   |── version0.65.kicad_pro
|   |── version0.65.kicad_pcb
|   |── version0.65.kicad_sch
|   └── fp-lib-table
|
|── CAD/
|   |──── Full/
|   |     |── version0.65-assembly.step
|   |     |── version0.65-base.step
|   |     |── version0.65-plate.step
|   |     |── version0.65-top.step
|   |     └── version0.65.f3z
|   |
|   └──── Split/
|         |──── Base/
|         |     |── version0.65-split-base-left.step
|         |     |── version0.65-split-base-middle.step
|         |     └── version0.65-split-base-right.step
|         |
|         |──── Top/
|         |     |── version0.65-split-plate-left.step
|         |     └── version0.65-split-plate-right.step
|         |
|         |── version0.65-splitcase-assembly.step
|         └── version0.65-splitcase.f3z
| 
|── Production/   
|    |── gerbers.zip/
|    |
|    |── STL Files/
|    |   |─── version0.65-split-base/
|    |   |    |── version0.65-base-left.stl
|    |   |    |── version0.65-base-middle.stl
|    |   |    └── version0.65-base-right.stl
|    |   |
|    |   └─── version0.65-split-plate/
|    |        |── version0.65-plate-left.stl
|    |        └── version0.65-plate-right.stl
|    |
|    └── STEP Files/
|           |─── version0.65-split-base/
|           |      |── version0.65-base-left.step
|           |      |── version0.65-base-middle.step
|           |      └── version0.65-base-right.step
|           |
|           └──── version0.65-split-plate/
|                   |── version0.65-plate-left.step
|                   └── version0.65-plate-right.step
|
|── Assets/
|    |── Keycaps/
|    |── MX Switch/
|    └── nice!nano/
|
|── Firmware/
|
|── BOM.csv
|── journal.md
└── README.md
```

## Schematic
##### Overall Schematic
<img width="1173" height="590" alt="image" src="https://github.com/user-attachments/assets/be4c3ac6-c0e7-4de7-b0e6-379787bbe178" />


## PCB
##### PCB Front without GND Plane
<img width="977" height="384" alt="image" src="https://github.com/user-attachments/assets/23c2b1fd-b6c8-4a7c-af8a-d6974c13d283" />


##### PCB Front with GND Plane
<img width="977" height="391" alt="image" src="https://github.com/user-attachments/assets/57820a6e-4209-488c-8803-2c2926cd3979" />


##### PCB Back without GND Plane
<img width="971" height="392" alt="image" src="https://github.com/user-attachments/assets/97b8eee5-cec2-4163-9a00-d16fc9b1aa2f" />


##### PCB Back with GND Plane
<img width="976" height="390" alt="image" src="https://github.com/user-attachments/assets/e2bd9c74-a955-4613-98e0-10c432ee3128" />
 

## CAD
The case has been split to accomodate 3D printing. A non-split case also is included in the CAD folder. The plates and base have small pegs and holes for assembly.

#### Full Assembly
##### Top View
<img width="650" height="308" alt="image" src="https://github.com/user-attachments/assets/8e1746bd-6edd-469d-a3be-1ba8b31f15f2" />


#####  Side View
<img width="933" height="469" alt="image" src="https://github.com/user-attachments/assets/e2f9ff12-cade-47cd-99c5-76d34e2467e2" />


#### Top Plate
##### Top View
<img width="694" height="336" alt="image" src="https://github.com/user-attachments/assets/fa34da71-14a1-4e33-82a6-0fa6f81e0634" />

#####  Side View
<img width="883" height="441" alt="image" src="https://github.com/user-attachments/assets/6c679788-67d3-4bc4-9893-a2ef8e4960fc" />

#### Base
##### Top View
<img width="775" height="425" alt="image" src="https://github.com/user-attachments/assets/84f09af4-b6f0-470c-a972-abbd8e1f0ca1" />


#####  Side View
<img width="784" height="292" alt="image" src="https://github.com/user-attachments/assets/8e11c721-c2f7-4a05-b6d7-7e89447e8563" />
 
## Firmware
version0.65 uses ZMK firmare. While the firmware has not been tested IRL, it can be found in a separate repository.

Firmware repository- https://github.com/NeerajR18/zmk-config-version0.65


## Bill of Materials
| Part Name | Quantity | Unit Price (USD) | Ext. Price (USD) | Link |
|-----------|---------:|-----------------:|-----------------:|------|
| nRF52840 Development Board (Compatible with nice!nano) | 1 | 8.00 | 8.00 | https://robu.in/product/promicro-nrf52840-development-board/ |
| Gradient Keycaps | 1 | 13.66 | 13.66 | https://stackskb.com/store/veekos-gradient-keycaps-cherry-profile-135-keys/ |
| Gateron Hotswap Sockets | 66 | 0.11 | 7.00 | https://stackskb.com/store/gateron-hotswap-sockets/ |
| Gateron G Pro 3.0 Switch (Pack of 10) | 7 | 2.10 | 14.71 | https://meckeys.com/shop/accessories/keyboard-accessories/key-switches/gateron-g-pro-3-0-switch/ |
| OS102011MA1QN1 | 1 | 0.38 | 0.38 | https://robu.in/product/os102011ma1qn1-ck-100ma-single-pole-double-throw-spdt-12v-10000-times-plugin-slide-switches-rohs/ |
| S2B-PH-SM4-TB | 1 | 0.42 | 0.42 | https://robu.in/product/s2b-ph-sm4-tblfsn-jst-1x2p-2p-ph-tin-2-25%E2%84%8385%E2%84%83-2a-1-2mm-copper-alloy-horizontal-attachment-smdp2mmsurface-mount%EF%BC%8Cright-angle-wire-to-board-connector-rohs/ |
| 1N4148W-T4 | 66 | 0.015 | 0.99 | https://sharvielectronics.com/product/1n4148w-t4-high-speed-fast-switching-diode-sod-123-package/ |
| YY503040-JST-PH | 1 | 2.31 | 2.31 | https://sharvielectronics.com/product/3-7v-1100mah-lipo-rechargeable-battery-with-jst-ph-2mm-connector/ |
| PCB from Robu | 5 | 8.05 | 48.35 | https://robu.in/ |
| Cherry Stabilizer Set (GEON AND C3) | 1 | 7.36 | 7.36 | https://neomacro.in/products/cherry-stabilizer-set-geon-and-c3?_pos=3&_sid=9a6134911&_ss=r |
| M3 Heatset Insert | 20 | 0.025 | 0.50 | https://onlyscrews.in/products/m3-x-3mm-brass-threaded-inserts |
| M3 × 16mm Screws | 20 | 0.023 | 0.46 | https://onlyscrews.in/products/hex-allen-csk-m3-x-16-screw-pack-of-20 |
| **Total** |  |  | **104.14** |  |
