# Formbot-V0
Details/Documentation for the Formbot V0 Kit

![Formbot V0 Kit](https://github.com/SrgntBallistic/Formbot-V0/blob/v0.2/Images/Kit/formbot-v0-kit-main.jpg?raw=true)

## Helpful info

Most of this is set in the `printer.cfg` file I've provided

### Max Motor Currents
A/B - 1.5A
Z - 0.65A
E - 1.0A

### 65% Run Currents
Voron recommends 60-70% (0.6-0.7) to start
I chose 65%. Increase as needed but try to stay below 80-90%

Run Current = rated_motor_current * 0.707 * 0.65

Plug the max currents above into the equation with your desired percentage
A/B - 0.69 (NICE!)
Z - 0.3A
E - 0.46A

### Thermistors
Formbot Bed - "Generic 3950"
Formbot V6 CHC Hotend - "ATC Semitec 104NT-4-R025H42G"
Check Klipper docs for the correct sensor type based on your thermistor/hotend

## Features
- Kirigami Bed Kit
- BTT Pi V1.2
- BTT SKR Pico
- BTT V0 Display
- CHC V6 Hotend (Upgradeable to Dragon/HF)
- Double Sided PEI Sheet
- Crimped Wiring Looms
- Moons Motors
- Stainless Steel Rails
- MIC6 Cast Aluminum Build Plate
- Polycarbonate Panels
- Gates Belts
- Vivedino 60W Silicone Bed Heater
- Stainless Steel Hardware
- Umbilical Board + Harness
- Makerbeam XL Extrusion
- Meanwell 150W PSU

Aliexpress Listing: https://s.click.aliexpress.com/e/_Dk19GYN

## Kirigami Bed
![Kirigami Bed](https://github.com/christophmuellerorg/voron_0_kirigami_bed/blob/master/Images/stealth_beta.png?raw=true)
GitHub: https://github.com/christophmuellerorg/voron_0_kirigami_bed

Manual: https://github.com/Kagee/kirigami-bed-manual

## BTT SKR Pico
GitHub: https://github.com/bigtreetech/SKR-Pico

Manual: https://github.com/bigtreetech/SKR-Pico/blob/master/BTT%20SKR%20Pico%20V1.0%20Instruction%20Manual.pdf

**Flashing (From Pi without PC)**: https://docs.vorondesign.com/build/software/skrPico_klipper.html

## BTT V0 Display
GitHub: https://github.com/VoronDesign/Voron-Hardware/tree/master/V0_Display

Flashing Docs: https://github.com/VoronDesign/Voron-Hardware/blob/master/V0_Display/Documentation/Setup_and_Flashing_Guide.md

Biqu Listing: https://biqu.equipment/products/voron-display-v1-0

Ali Express Listing: https://s.click.aliexpress.com/e/_DBvhC7R

Features:
- 1.3" OLED Display
- Rotary Encoder
- Neopixel
- STM32F042F6P6 MCU
- USB Connector

## BTT Pi V1.2
GitHub: https://github.com/bigtreetech/BTT-Pi

Manual: https://github.com/bigtreetech/BTT-Pi/blob/master/BIGTREETECH%20Pi%20V1.2%20User%20Manual.pdf

Biqu Listing: https://biqu.equipment/collections/control-board/products/bigtreetech-btt-pi-v1-2

Aliexpress Listing: https://s.click.aliexpress.com/e/_DmQwZ0V

Useful features:
- ADXL SPI Port for Input Shaping
- 12-24V Power terminal input
- 5V USB-C Power input

### Flashing Image
The BTT Pi uses the same images as the BBT CB1 compute module. You can follow instructions for installing it.

BTT has 2 versions of the Kernal. A Minimal image and a Klipper image. The Klipper image has Klipper, Mainsail, Crowsnest and most other dependencies pre-installed. They just need to be updated after.
Images: https://github.com/bigtreetech/CB1/releases

By Default the host name for the image will be "btt-cb1" and it can be accessed with "btt-cb1.local" if you don't know the IP Address for it yet.

## Products Used
### Fabreeko cPIF V0.2 Printed Parts
https://www.fabreeko.com/collections/v0/products/voron-v0-2-s1-printed-parts-by-pif?variant=43678271570175

### EP2 Grease
https://www.fabreeko.com/collections/v0/products/mobilux-ep2-grease

### GDS Time Fan Mini Stealthburner Fan Kit
https://dfh.fm/products/voron-mini-stealthburner-fan-kit?_pos=7&_sid=66ce4f1ac&_ss=r

## My Mods

### LDO Kirigami Wiring Kit

**Description**: "LDO Krirgami LED PCB, LDO Kirigami Breakout PCB, LDO Breakout Wire Kit, Wago 221-412 x 2 For use with Kirigami Beds"

**Link**: https://dfh.fm/products/voron-v0-kirigami-bed-wiring-and-led-kit

### Nevermore V6

**Description**: 3D Printed Activated Charcoal Filter

**Link**: https://github.com/nevermore3d/Nevermore_Micro/tree/master/V6

2 5015 Fans
https://www.fabreeko.com/products/5015-blower-fan-by-honeybadger?_pos=1&_psq=50151&_ss=e&_v=1.0&variant=43628023152895
https://dfh.fm/products/5015-24v-dual-ball-blower?_pos=1&_sid=426120d23&_ss=r

2 Wago 221-412 connectors (Optional)
Activated Charcoal Pellets - https://www.fabreeko.com/products/nevermore-carbon?_pos=1&_sid=6691ede3b&_ss=r&variant=43205733449983

### Klipper Expander Board

Board allows increased IO and power for mods and upgrades limited by BTT SKR Pico board.
Neopixels
Nevermore Fans


**Links**:
https://www.fabreeko.com/collections/v0/products/klipper-expander-board
https://dfh.fm/products/klipper-expander-for-voron-3d-printers?_pos=1&_sid=9323da715&_ss=r

### Fabreeko Honeybadger V0 Metal Toolhead Carriage

**Link**: https://www.fabreeko.com/collections/v0/products/v0-2-metal-toolhead-carriage-for-v0-2-by-honeybadger?variant=44164192338175

**Variation**: MGN7H

Requires - 4 M2x4 screws (for carriage mount), M3x8 (replaces rear M3x16 motor plate screw)

### Rainbow Matchstick LEDs

**Links**:
https://dfh.fm/products/rainbow-stick?variant=43340753666270

**Mounts**: https://www.printables.com/model/408214-matchstick-diffusers

### Cable Management Tracks
These are printable versions of the tracks that LDO and other kits include.
I recomend printing them in PETG or a similar material that can flex a bit before snapping. I tried printing them in sever ABSs including Fusion Deep Water blue and the guide fingers were very brittle.

Voron User Mod Link: https://mods.vorondesign.com/detail/YTmSPTcWpctfTKQj3bOPg
