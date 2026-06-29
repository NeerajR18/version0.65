# version0.65

version0.65 is an almost 65% keyboard. It is a bluetooth keyboard, using the SuperMini nRF52840 board, which is pin compatible with the nice!nano v2.
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
|   |── Base/
|   |   |── version0.65-base-left.step
|   |   |── version0.65-base-middle.step
|   |   └── version0.65-base-right.step
|   |   
|   |──── Top/
|   |     |── version0.65-plate-left.step
|   |     └── version0.65-plate-right.step
|   |
|   |── version0.65-assembly.step
|   └── version0.65.f3z
| 
|── Production/   
|    |── gerbers.zip/
|    |
|    |── STL Files/
|    |   |─── version0.65-base/
|    |   |    |── version0.65-base-left.stl
|    |   |    |── version0.65-base-middle.stl
|    |   |    └── version0.65-base-right.stl
|    |   |
|    |   └─── version0.65-plate/
|    |        |── version0.65-plate-left.stl
|    |        └── version0.65-plate-right.stl
|    |
|    └── STEP Files/
|           |─── version0.65-base/
|           |      |── version0.65-base-left.step
|           |      |── version0.65-base-middle.step
|           |      └── version0.65-base-right.step
|           |
|           └──── version0.65-plate/
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
<img width="1016" height="549" alt="image" src="https://github.com/user-attachments/assets/34dda80b-e4b8-4236-bd8a-9264c9a206af" />

## PCB
##### PCB Front without GND Plane
<img width="979" height="347" alt="image" src="https://github.com/user-attachments/assets/2954b8de-9fa5-4e58-9e13-ef11f9f62b96" />

##### PCB Front with GND Plane
<img width="977" height="331" alt="image" src="https://github.com/user-attachments/assets/3d420cde-0ebe-418d-afc1-69940983a389" />

##### PCB Back without GND Plane
<img width="969" height="320" alt="image" src="https://github.com/user-attachments/assets/599930f8-021f-4ade-8995-a958e7287f5e" />

##### PCB Back with GND Plane
<img width="975" height="333" alt="image" src="https://github.com/user-attachments/assets/31202ad0-eb1e-44c1-bd29-3b3b04581050" />
 

## CAD
The case has been split to accomodate 3D printing. The plates and base have small pegs and holes for assembly.

#### Full Assembly
##### Top View
<img width="969" height="392" alt="image" src="https://github.com/user-attachments/assets/b764fcc6-3e90-40c2-b1d1-901356535a4f" />

#####  Side View
<img width="778" height="349" alt="image" src="https://github.com/user-attachments/assets/310366f0-f7fd-4fbb-a767-60109e995a82" />



#### Top Plate
##### Top View
<img width="977" height="348" alt="image" src="https://github.com/user-attachments/assets/471eedb7-97e5-437f-9a17-4e4bdbee15ed" />

#####  Side View
<img width="908" height="387" alt="image" src="https://github.com/user-attachments/assets/d9fc37f1-44ec-41a5-bd9b-b73f3cf80268" />

#### Base
##### Top View
<img width="962" height="338" alt="image" src="https://github.com/user-attachments/assets/2a15a90f-0293-4bd8-a7ad-860e2e9839a1" />

#####  Side View
<img width="1046" height="425" alt="image" src="https://github.com/user-attachments/assets/d2c979e7-7051-4633-84a1-f92e3291421a" />
 
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
| PCB from Robu | 5 | 8.83 | 44.28 | https://robu.in/ |
| Cherry Stabilizer Set (GEON AND C3) | 1 | 7.36 | 7.36 | https://neomacro.in/products/cherry-stabilizer-set-geon-and-c3?_pos=3&_sid=9a6134911&_ss=r |
| M3 Heatset Insert | 20 | 0.025 | 0.50 | https://onlyscrews.in/products/m3-x-3mm-brass-threaded-inserts |
| M3 × 16mm Screws | 20 | 0.023 | 0.46 | https://onlyscrews.in/products/hex-allen-csk-m3-x-16-screw-pack-of-20 |
| Shipping charges |-| - | 7 | - |
| **Total** |  |  | **107.07** |  |
