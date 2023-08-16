# VORON GREEN

The Voron Green is a 300mm Voron 2.4, built around an LDO Kit ([LDO Motors Voron 2.4 300 Kit - 3DJake Nederland](https://www.3djake.nl/ldo-motors/voron-24-300-kit?sai=12016))



## Configuration

The basis of the configuration of Voron Green is done around Klippain. For further configuration details see the klipper folder in this repo.

[GitHub - Frix-x/klippain: Generic Klipper configuration for 3D printers](https://github.com/Frix-x/klippain)

## Mods

The following mods / adaptions have been made to make this printer even better:

### Display

The default graphic display is not very useful. On the voron green this has been replaced with a Waveshare 4.3" Touch Screen:

[Waveshare 4.3" Touch Screen on Amazon](https://www.amazon.nl/gp/product/B083Q8YLVP/)

This is mounted using the following mod:

[Touch Screen Mount on GitHub](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/jeoje/4.3_Inch_Touchscreen_Mount)

**Note:** The new LDO revC kit already contains a nice 4.3" Touch Screen so no need to buy this one for future builds.

### Gantry Backers

On the Y extrusions gantry backers are installed to combat bending of the Y-Rails under temperature changes:

[Voron V2.4/Trident 300 Titanium Backers](https://lecktor.com/en/v2x-frames/1002-voron-v24trident-300-titanium-backers-01002.html)

**Note:** The X backer of this kit is not used as it is not needed on X due to the rail orientation. Installing this on top of the X extrusion will only make things worse!

### Kinematic Mount

To give the bed proper room for thermal expansion, without stress from the mounting a kinematic mount is used:

[Kinematic mount for V2.4](https://lecktor.com/en/v2x-buildplate/1032-kinematic-mount-for-v24-01032.html)

### Reinforced Gantry Mount

I don't like the way the gantry is mounted originally. I'm also not a huge fan (anymore) of the GE5C mod as it can have too much play. The Annex Reinforced Gantry mounts give a much more solid mounting of the gantry:

[Annex Reinforced Gantry Mounts](https://github.com/Annex-Engineering/Annex-Engineering_User_Mods/tree/main/Printers/Non_Annex_Printers/VORON_Printers/VORON_V2dot4/annex_dev-Reinforced_Gantry_Mounts)

[Needed ball end screws on Amazon](https://www.amazon.nl/dp/B07VYXTRL1)

### Front Idlers / Tensioners

On the Voron Green I'm using Rama's idlers:

[Rama's Idlers on GitHub](https://github.com/Ramalama2/Voron-2-Mods/tree/main/Front_Idlers)

However on a future build I would recommend the BFI (Beefy Front Idlers) from Clee as they are better:

[GitHub - clee/VoronBFI](https://github.com/clee/VoronBFI)

### Z Idlers / Tensioners

On the Voron Green I'm using the Z idlers from Hartk1213's pins mod:

[GitHub - Voron 2.4 Pins Mod](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/hartk1213/Voron2.4_Trident_Pins_Mod)

However on a future build I would recommend the ZFI (Beefy Z Idlers) from Clee as they are better:

[GitHub - clee/VoronBFI](https://github.com/clee/VoronBFI)

### AB Motor Mounts

For the motor mounts the Hartk1213's pins mod is used:

[GitHub - Voron 2.4 Pins Mod](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/hartk1213/Voron2.4_Trident_Pins_Mod)

### XY Joints and X-Beam

For the XY joints and X-Beam I've used the Trailhead from Armchair Engineering. This gives much more stiffness and reduces moving mass. I've used the 6mm / 1515 / MGN9 variant.

[GitHub - Armchair-Engineering/Trailhead-XY-Joints: Modified XY joints for the Voron 2.4 and Trident](https://github.com/Armchair-Engineering/Trailhead-XY-Joints)

For the X-Rail I've used a CPC rail from Fermio as we want the best possible rail on X as that is the only axis that is only constrained by 1 rail.

[Fermio - CPC MR 9ML 350mm](https://fermio.xyz/chieftek-precision-co.-ltd/cpc-mr-9ml-350-mm/)

### Toolhead

For the toolhead I'm using the XOL toolhead from Armchair Engineering. This is a stripped down toolhead, so the moving mass will be optimal, but still is very stiff.

[GitHub - Armchair-Engineering/Xol-Toolhead](https://github.com/Armchair-Engineering/Xol-Toolhead)

Along with the toolhead the following choices have been made:

#### Extruder

As extruder I'm using the Orbiter 2.0 as this one has the optimal balance between grip and motor torque. This one will skip steps instead of strip the filament when something goes wrong in the extrusion path. It also provides enough grip, as with some Glass Filled Nylons I've had issues getting good grip with the standard BMG gears of the StealthBurner. Don't go for the LGX lite. It has more grip, but at the cost of less torque.

[LDO Motors Orbiter Extruder V2.0 - 3DJake Nederland](https://www.3djake.nl/ldo-motors/orbiter-extruder-v20)

#### Hotend

For the hotend the Voron Green is using the Phasetus Rapido Plus (PT1000) in combination with Bondtech CHT bi-metal nozzles. This gives the best possible flow rate.

I did not choose to go with the E3D Revo. The Revo has issues with the heatbreak bending, and also does not have a high flow nozzle for abbraisive filaments.

[Phaetus Rapido Plus Hotend HF - 3DJake Nederland](https://www.3djake.nl/phaetus/rapido-plus-hotend-hf)

[BondTech CHT BiMetal RepRap Nozzle - 3DJake Nederland](https://www.3djake.nl/bondtech/cht-bimetal-reprap-nozzle?sai=14008)

#### Toolhead PCB

For the toolhead PCB I'm using a custom PCB that uses the pinout of the Stealthburner PCB so the existing wiring of the LDO kit can be re-used. The custom PCB has the options to wire 12V to the fans, which is needed when the Delta Fans are used for the XOL Toolhead.

[GitHub - XOL PCB](mods/XOL%20Breakout)

#### Z-Probe

The Voron Green uses the Euclid Z-Probe. Kicky PCB is a good alternative. Avoid the normal Klicky or Klicky-NG as they are not as stable.

[Lecktor - Euclid probe](https://lecktor.com/en/sensors/1143-euclid-probe-01143.html)

[Printables - Euclid Gantry Dock with Magnet](https://www.printables.com/model/388004-longer-euclid-dock-arm-with-magnet-for-retention)

### Z-Endstop

The Sexbolt mod is used as Z-Endstop as this gives the best force on the nozzle to squeeze away any plastic before probing.

[Z endstop Sexbolt - Lab4450.com](https://lab4450.com/product/z-endstop-sexbolt/)

### Front Door

I personally don't like the double front doors of the original Voron, so I instead went with a 6mm thick, single panel door:

[GitHub - BeunHaas34 Annex Door](https://github.com/Annex-Engineering/Annex-Engineering_User_Mods/tree/main/Printers/Redoubt/BeunHaas34-Annex_Door)

However recently a new mod was released with an even sturdier door. You might want to consider this one for future builds:

[GitHub - Whopping Clicky Clacky Door](https://github.com/tanaes/whopping_Voron_mods/tree/main/clickyclacky_door)

### Panel Mounts

I'm using Annex's panel mounts as they make it so much easier to remove the panels.

[GitHub - Annex Panel Clips](https://github.com/Annex-Engineering/Annex-Engineering_User_Mods/tree/main/Printers/All_Printers/annex_dev-Panel_2020_Clips_and_Hinges)

### Purge Bucket

The following purge bucket / nozzle brush holder / plate stopper is used. You can use the nozzle brush from the LDO kit with this one:

[GitHub - Decontaminator Purge Bucket & Nozzle Scrubber](https://github.com/VoronDesign/VoronUsers/tree/master/orphaned_mods/printer_mods/edwardyeeks/Decontaminator_Purge_Bucket_%26_Nozzle_Scrubber)

### Camera

A Logitech C920 camera is mounted on the top of the gantry using this mod:

[GitHub - Voron 2.4 C920 Mount](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Koios/C920_Mount)

### Umbilical

The X/Y cable chains have been removed. It adds weight and is not supported with the XOL toolhead and/or TrailHead 1515 XY Joints. The XOL toolhead natively supports the umbilical, but the following mod is used on the A motor drive to support the umbilical:

[Printables - Voron V2.4 Rear Umbilical](https://www.printables.com/model/363657-voron-v24-rear-umbilical)

Note that the Voron Green uses sensorless homing, so no need to print anything related to the endstops.

### Filament Sensor

The BTT filament sensor (REV1) is used to sense movement of filament. This will detect filament runout as well as filament blockage.

[Amazon - BTT SFS](https://www.amazon.nl/dp/B089NYC6JL)

The sensor is mounted at the rear top of the Voron with a modified exhaust cover:

[GitHub - Voron Exhaust Cover for BTT SFS](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Fiction/Exhaust_cover_SFS)

### Extra Thermistors

Two extra thermistors are mounted in Voron Green:

- In the Z Cable chain to measure chamber temperature

- In the rear right Z extrusion to measure frame temperature

### ADXL

Nozzle mount accelerometer gives the best results for input shaper. To use the LDO ADXL board in this way I'm using the Nozzle Mount adapter (using an M6 bolt to hard fasten it to the hotend):

[GitHub - Armchair Engineering's Rapido ADXL Nozzle Thread Mount](https://github.com/Armchair-Engineering/ADXL-Mounts/blob/main/STLs/RapidoADXL_v14%20-%20Nozzle%20Thread%20Mount.stl)
