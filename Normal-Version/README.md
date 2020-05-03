#### PCB (Voultar)

Voultar took the task and gave my old style PCB a modern look. He also includes some **new ideas** like a new jumper design to decide for low- or high-active reset respectively.

The repository offers the Gerber files including a component map picture in a Zip-file. The file is ready to _drag and drop_ into the [OSHPark](https://oshpark.com/) mask.

As far as I know the PCB will be also available on [Voultar's Mod Shop](https://voultar.com/index.php?route=common/home), soon.

#### PCB (Backup)

You can use the old style PCB if you want to. However, it's somehow outdated. Here is the old README I deleted with a previous commit.

```
Components:

IC1: PIC16F684 SOIC-14 with NESRGB-IGR code. Please choose whether you want to use a dual LED with a common anode or cathode in advance!
IC2: 74LVX125 SOIC-14

C1, C2: 100nF 0805
R1, R2: 220Ohm 0805

Jumper:

J1: 10kOhm 0805 -> set the reset type of your console there.
J2: Short the jumper you want to... '3' means that the PIC cycles only through the RGB modes; '4' als cycles through RGB off

PCB-order:

Please choose your preferred service.
You may order that PCB at OSHPark -> https://oshpark.com/shared_projects/C9jdssMN
```

#### Firmware

Grab the firmware for the PIC16F684 [here](https://github.com/borti4938/Switchless-Mods/tree/master/NES/IGR_for_NESRGB/)

-  current version: use the 'normal version' and flash the nesrgb_igr_684_var_led.hex. This 
-  older PCB version (with three 1k --10k resistors next to the 74*125): use the 'risky version' and flash nesrgb_igr_684_risky_var_led.hex

It is very important that the firmware is flashed on the PIC prior to assembly of the PCB as the ICSP pins are not directly available.



####  Installation

There are some pictures inside the installation folder. Most of them are for the NES front loader, two are for the NES-101 top loader and for the AV famicom as named by picture.

The most important task is the preparation of the reset line. Voultar has discovered that the NES needs some kind of a slow start. See some details and discussions can be found on [twitter](https://twitter.com/Voultar/status/1083441586967666688). For Voultars PCB version, you can add another capacitor on the PCB if you want to be sure - here is what he wrote me: "If you open the component map picture, you’ll see a green arrow pointing to two via’s. If people want to, they can move the 4.7uF reset cap on low-active reset consoles to this location so that all games will work correctly. "

The assembler file in the link (fw section) includes some additional installation notes mostly meant for the non-PCB install.

