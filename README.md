# Formbot-V0
Details/Documentation for the Formbot V0 Kit

![Formbot V0 Kit](Images/Kit/formbot-v0-kit-main.jpg)

## Helpful info

Most of this is set in the `printer.cfg` file I've provided

### Max Motor Currents
- A/B - 1.5A
- Z - 0.65A
- E - 1.0A

### 65% Run Currents
Voron recommends 60-70% (0.6-0.7) to start
I chose 65%. Increase as needed but try to stay below 80-90%

Run Current = rated_motor_current * 0.707 * 0.65

Plug the max currents above into the equation with your desired percentage
- A/B - 0.69 (NICE!)
- Z - 0.3A
- E - 0.46A

### Thermistors
- Formbot Bed - "Generic 3950"
- Formbot V6 CHC Hotend - "ATC Semitec 104NT-4-R025H42G"
- Check Klipper docs for the correct sensor type based on your thermistor/hotend

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

The Kirigami bed frame is a great mod/upgarde that comes wiht the kit. I had some trouble with the provided bed around it's thickness and the placement of the thermal fuse. I was able to get through all the issues with small DIY fixes. Other people have also noted they've run into these issues on the Voron Discord as well as the Kirigami GitHub. YMMV

## BTT SKR Pico
GitHub: https://github.com/bigtreetech/SKR-Pico

Manual: https://github.com/bigtreetech/SKR-Pico/blob/master/BTT%20SKR%20Pico%20V1.0%20Instruction%20Manual.pdf

**Flashing (From Pi without PC)**: https://docs.vorondesign.com/build/software/skrPico_klipper.html

The SKR Pico is a nice small footprint Main Board. It trades some IO/connectivity capability for its compact size. Ex: there's no input of the chamber thermistor that comes on the V0 Umbilical frame PCB. Also there's no extra fan ports to hook up fans for something like the Nevermore filter. An Extra MCU like the Klipper Expander would be necessary to get some of this IO back.

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

Small simple display with a neopixel onboard to change the LCD Color.

## BTT Pi V1.2
GitHub: https://github.com/bigtreetech/BTT-Pi

Manual: https://github.com/bigtreetech/BTT-Pi/blob/master/BIGTREETECH%20Pi%20V1.2%20User%20Manual.pdf

Biqu Listing: https://biqu.equipment/collections/control-board/products/bigtreetech-btt-pi-v1-2

Aliexpress Listing: https://s.click.aliexpress.com/e/_DmQwZ0V

Useful features:
- ADXL SPI Port for Input Shaping
- 12-24V Power terminal input
- 5V USB-C Power input

The BTT Pi V1.2 is a nice alternative to Raspberry branded Single-Board-Computers that have frequently shot up in price. It has some nice 3D Printing specific features and numerous ways to power it.

### Flashing Image
The BTT Pi uses the same images as the BBT CB1 compute module. You can follow instructions for installing it.

BTT has 2 versions of the Kernal. A Minimal image and a Klipper image. The Klipper image has Klipper, Mainsail, Crowsnest and most other dependencies pre-installed. They just need to be updated after.
Images: https://github.com/bigtreetech/CB1/releases

By Default the host name for the image will be "btt-cb1" and it can be accessed with "btt-cb1.local" if you don't know the IP Address for it yet.

## Wiring

The Kirigami Bed Frame alows splitting the wiring coming out of the bed so that the bed can be removed and worked on without being tethered to the printer.

Voron recommends using Wago connectors to allow easily disconnecting the wires. The Kirigami bed mod includes mounts for the Wago connectors.

Since the Formbot kit bed heater doesn't include an integrated thermal fuse it needs to be connected inline with one side of the bed wires.

### Generic Formbot Wiring
![Generic Formbot Kirigami Wiring](Images/Wiring/Formbot-Kirigami-Generic.png)

An inline connector can be used to split the Thermistor wires under the bed.

### Formbot Wiring + LDO Kirigami Wiring Kit
![Generic Formbot Kirigami Wiring](Images/Wiring/Formbot-Kirigami-+-LDO-Wiring-Kit.png)

The LDO wiring kit includes 2 Wago mounts, a Thermistor breakout PCB and an LED PCB. A third wago is needed for the Formbot Thermal Fuse. The LDO V0 repo has stls for mounting its PCBs and the wagos. See the Kirigami Manual for more info.

## Products Used
### Phaetus Dragon HF
This is an optional upgrade on some Formbot listings. It offers single hand nozzle tightening and much higher Max Flow Rate compared to the default Formbot V6 CHC nozzle.

![Dragon HF](Images/Wiring/v0.2r1-dragon-hf-01.jpg)

### Bondtech 0.4 CHT Nozzle
This further increases the flow rate of the Dragon HF.

![CHT Nozzle](Images/Wiring/v0.2r1-cht-nozzle.jpg)

### Fabreeko cPIF V0.2 Printed Parts
https://www.fabreeko.com/collections/v0/products/voron-v0-2-s1-printed-parts-by-pif?variant=43678271570175

I found the cPIF parts pretty nice. I've since replaced a couple of of failed parts but I don't attribute the failures to the quality of the prints. More to some inherent issues in the part design

![cPIF Parts](Images/Wiring/v0.2r1-cPIF-parts.jpg)

### EP2 Grease
https://www.fabreeko.com/collections/v0/products/mobilux-ep2-grease

I originally greased the rails with White Lithium lubricant but bought this and regreased them when I redid the frame.

### GDS Time Fan Mini Stealthburner Fan Kit
https://dfh.fm/products/voron-mini-stealthburner-fan-kit?_pos=7&_sid=66ce4f1ac&_ss=r

The stock fans are probably the most noticable lower quality parts of this kit. I found the plastic a bit brittle and the leads didn't tuck into the their slots on the body. This cause them to get pinched when I put them in the Mini SB.

## My Mods

### LDO Kirigami Wiring Kit

**Description**: "LDO Krirgami LED PCB, LDO Kirigami Breakout PCB, LDO Breakout Wire Kit, Wago 221-412 x 2 For use with Kirigami Beds"

**Link**: https://dfh.fm/products/voron-v0-kirigami-bed-wiring-and-led-kit

Since the Formbot Kit only comes with the frame I bought this wiring kit to get close to what comes in the LDO kit.

![LDO V0 Wiring Kit](Images/Wiring/v0.2r1-ldo-kirigami-wiring-kit.jpg)

### Nevermore V6

**Description**: 3D Printed Activated Charcoal Filter

**Link**: https://github.com/nevermore3d/Nevermore_Micro/tree/master/V6

2 5015 Fans
- Fabreeko - https://www.fabreeko.com/products/5015-blower-fan-by-honeybadger?_pos=1&_psq=50151&_ss=e&_v=1.0&variant=43628023152895
- DFH - https://dfh.fm/products/5015-24v-dual-ball-blower?_pos=1&_sid=426120d23&_ss=r

- 2 Wago 221-412 connectors (Optional)
- Activated Charcoal Pellets - https://www.fabreeko.com/products/nevermore-carbon?_pos=1&_sid=6691ede3b&_ss=r&variant=43205733449983

Printing ABS (as with most filament materials) can release VOCs (Volatile Organic Compounds) and has a noticabley more noxious smell than other materials like PLA. An active carbon filter can help clear absorb those orders/VOCs and move some air around the chamber for more efficient heating.

### Klipper Expander Board

Board allows increased IO and power for mods and upgrades limited by BTT SKR Pico board
- Neopixels
- Nevermore Fans
- Chamber Thermistor

![Klipper Expander Board](Images/Wiring/v0.2r1-klipper-expander-board.jpg)

**Links**:
- Fabreeko - https://www.fabreeko.com/collections/v0/products/klipper-expander-board
- DFH - https://dfh.fm/products/klipper-expander-for-voron-3d-printers?_pos=1&_sid=9323da715&_ss=r

### Fabreeko Honeybadger V0 Metal Toolhead Carriage

**Link**: https://www.fabreeko.com/collections/v0/products/v0-2-metal-toolhead-carriage-for-v0-2-by-honeybadger?variant=44164192338175

**Variation**: MGN7H

Requires - 4 M2x4 screws (for carriage mount), M3x8 (replaces rear M3x16 motor plate screw)

One of the parts I noticed failing was the X carriage. The hex nuts place on the front of the carriage started spinning in their slots. There was also a couple layer splits in the part when I removed it.

![Fabreeko Metal Carriage](Images/Wiring/v0.2r1-fabreeko-metal-carriage.jpg)

### Rainbow Matchstick LEDs

**Links**:
- DFH - https://dfh.fm/products/rainbow-stick?variant=43340753666270
- KB3D - https://west3d.com/products/rainbow-on-a-matchstick?_pos=10&_sid=57e17111c&_ss=r

**Mounts**: https://www.printables.com/model/408214-matchstick-diffusers

![Rainbow Matchsticks](Images/Wiring/v0.2r1-rainbow-matchsticks.jpg)

Becuase RGB LEDs

### Rainbow Barf LED Skirts

**Links**:
- Model By Maple Leaf Makers - https://www.printables.com/model/408741-v0-rgb-skirt-logo
- Fabreeko - https://www.fabreeko.com/products/rainbow-leds-pcb-by-whoppingpochard?_pos=1&_sid=cb992e68d&_ss=r
- https://west3d.com/products/steathburner-led-upgrade-rgbw?_pos=1&_sid=57e17111c&_ss=r

![Rainbow LED Skirts](Images/Wiring/v0.2r1-rainbow-led-skirts.jpg)

### Cable Management Tracks
These are printable versions of the tracks that LDO and other kits include.
I recomend printing them in PETG or a similar material that can flex a bit before snapping. I tried printing them in sever ABSs including Fusion Deep Water blue and the guide fingers were very brittle.

**Voron User Mod Link**: https://mods.vorondesign.com/detail/YTmSPTcWpctfTKQj3bOPg

![Cable Managment Ducts 1](Images/Wiring/v0.2r1-cable-management-03.jpg)

![Cable Management Ducts 2](Images/Wiring/v0.2r1-cable-management-04.jpg)

### Oriber Smart Filament Runout Sensor

**Project Link**: https://www.orbiterprojects.com/orbiter-filament-sensor/

![V0 Orbitor FRS](Images/Wiring/v0.2r1-orbitor-frs-01.jpg)

I thought it would be fun to modify the stock V0.2r1 FRS foot and use a smart sensor instead. With the use of a ball bearing and 2 push buttons the Orbiter sensor takes advantage of Klipper Macros to allow features like pausing/resuming, auto extruder heating, auto purging and quick unloading with the press of a button.

I'll upload the files and/or modifications when I feel it's in a good place.

### V0 Hinged Spool holder and Rear Panel

**Mod Link**: https://www.printables.com/model/548771-voron-0-hinged-back-panel-w-hinged-filament-spool-

I found that I was frequently taking off the rear panel and often had to lay the printer on its back. This combo of mods makes it easy to work on the electronics of the printer and move it around without undoing a lot of screws.
