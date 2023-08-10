# Makertum MK1 - a 230 / 110 V~ PCB Heated Bed
The Makertum MK1 is a mains voltage heated bed for 3D printers with dual voltage support (230/110 V~), 500 W of heat output, 2 minutes heatup time (110 °C), power indicator LED and onboard thermal fuse. It is currently available to skilled beta testers all over the world.

![render of top side](https://cdn.hackaday.io/images/7579811449431756922.png)
![render of bottom side](https://cdn.hackaday.io/images/5494491449432442830.png)

## Caution
- this is highly experimental
- do not use this if you don't know what you're doing
- don't hold me responsible for the outcome of what you do with the information in this repository
- even if operated electrically correct this device is dangerous and can get hot enough to seriously injure humans and animals.

## Project status and compatibility
- [x] layoutet basic MK1 design
- [x] compatible to MK2/B heated bed in terms of dimensions / mounting hole spacing
- [x] compatible to most MK2/B heated beds in terms of endstop position
- [x] added 110 and 230 V~ compatibility by wiring options
- [x] added thermal fuse
- [x] added LED overcurrent fuse
- [x] added warnings, wiring and instructions to the silkscreen
- [x] added milled polycarbonat led/fuse cover
- [x] picked license [CC-BY-NC-SA](http://creativecommons.org/licenses/by-nc-sa/3.0/legalcode)
- [x] manufactured beta batch on FR4
- [x] stress tested beta batch (FR4) on 110 °C for 30 days, no visible damage, no deformation, observed slight darkening of solder mask
- [x] stress tested beta batch (FR4) on 130 °C for 30 days, no visible damage, no deformation, observed slight darkening of solder mask and slight yellowing of silkscreen
- [x] started shipping beta kits to beta testers now (get yours on [makertum.com/en/shop](http://www.makertum.com/en/shop))
- [ ] beta testing is in progress, but not completed
- [ ] cannot be considered safe yet, be cautious

## Specifications
- Power consumption:	500 W (230 V~) or 460 (110 V~) (beta PCBs may differ)
- Operation Voltages:	230 V~ (110 V~ over a center tap)
- Resistance:	~106 Ω (beta PCBs may differ)
- Trace length: about 402 x 200 mm = ~80,800 mm
- Copper thickness (on PCB):	1oz aka 1.37 mil aka 35 µm
- Trace width:	0.37 mm
- Safety features: onboard thermal fuse, fused power indicator LED with protective polycarbonat cover
- Mounting Holes: 209 mm center-to-center (RepRap compatible) + 3-point leveling

## Documentation
Board layout and BOM can be found in this repo, extensive assembly instructions are maintained on [hackaday.io](https://hackaday.io/project/8671/instructions)

## How to use
[RTFM](https://hackaday.io/project/8671/instructions). Know what you do. Solder components as described in the BOM, make sure no excess solder can cause shorts of any kind. Wire as instructed on the backside of the PCB, do not use without professional supervision and appropriate safety precautions. Do not use without closed loop temperature control, i.e. with a thermistor/thermocouple and SSR, since the thermal fuse is supposedly a safety feature rather than a means of temperature control.

## Why?
There are many benefits of a mains voltage PCB heated bed: I will be driven directly from mains, skips the need for an expensive power supply, high current heatsinked SSR and heavy wire. Instead, it can be driven by a cheap low current SSR without heatsink. It's also cheaper to manufacture and provides more structural support for your printing plate than silicone heater pads.
IMHO, it’s pretty much nuts to convert down mains voltage in a power supply to 12/24V just to drive a heating element, except that it „feels“ a bit safer. Also, it’s a false assumption, that a 12/24 V heated bed is actually safe, since in case of an unexpected malfunction it will still burn down your place - regardless of the voltage on the heating element. Using fuses, temperature feedback and considering failure scenarios cannot be omitted anyway.

## Disclaimer
I am not responsible for the outcome of what you do with this information. As said, this is a highly experimental and untested prototype.

## License
Created by Moritz Walter 2015, released under [CC-BY-NC-SA](http://creativecommons.org/licenses/by-nc-sa/3.0/legalcode)
