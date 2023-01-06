# 10DIN2VGA Multi-Purpose Dongle for Sega Saturn

<img src="./Pics/cover.jpg" width=800px>

This is a 10-pin mini DIN to VGA dongle that supports outputting RGBS or S-video & composite video signal, plus stereo audio, from a Sega Saturn.

The RGBS signal is compatible with 75-ohm terminated SCART video.

The S-video & composite video signals are directly output from the console.

## Functionality

You need to decide the configuration of this dongle during assembly, by closing corresponding jumpers on the PCBs.

Due to the incompatibilities between the two configurations and the possibility of causing damage by mixing up the dongle and adapter, I decided not to include switches inside the dongle, but instead solder jumpers and clear marking on the outer shell.

### RGBS Configuration

The RGBS mode is the primary objective of this project.

When configured to RGBS mode, you can opt to use C-Sync when using with an NTSC console, or use either Luma or composite video as sync for compatibility with PAL consoles.

### S-Video/Composite Video Adapter Configuration

When configured to adapter mode, you can use the widely available and cheap VGA to S-Video/CVBS adapter from Amazon to output the aformentioned video format.

<img src="./Pics/yc-c_adapter.jpg" width=600px>

Make sure the pinout of your adapter is as the following diagram:

<img src="./Pics/adapter_pinout.jpg" width=600px>

*It is possible to modify the solder jumpers to change the adapter between the two configurations. However it's not recommended to repeatedly taking this dongle apart for that purpose, as the structural integrity might become compromised.*

## Design Details

The 10-pin mini DIN connector on the Sega Saturn has several problems.

The biggest one is that there is only one correct way to insert it, and infinite wrong ways to attempt. There is also no easy way to tell whether you are holding it correctly without triple checking with your eyes. It's also very difficult to maintain the correct orientation during insertion, even after you've confirmed it.

Most 10-pin DIN ports on the Saturn are badly damaged due to bad attempts to insert a video cable. Combined with too much force applied, the connector is frequently broken.

Due to the position of the port, the strain from the video cable will stress the connector and reduce the life of the port.

The design of this dongle eliminates all the aforementioned problems.

<img src="./Pics/design_01_front.jpg" width=300px><img src="./Pics/design_02_top.jpg" width=300px>

The shape of the outside shell makes it easy to tell which way it's facing. Make sure the curve is in the 2nd quadrant and you know it's the correct way.

<img src="./Pics/design_03_side.jpg" width=300px><img src="./Pics/design_05_flush.jpg" width=300px>

The shape of the inside shell conforms to the indented area around the AV port on the console, with the bottom of the dongle flat and flush with the table. This will ensure there is only one way to plug in the adapter. Since the adapter tightly follows the outline of the shell, rotational stress and downward stress are effectively offloaded to the shell of the console, as well as making it impossible to insert the connector too far into the console.

<img src="./Pics/3d_demo_1.jpg" width=300px><img src="./Pics/3d_demo_2.jpg" width=300px><img src="./Pics/3d_demo_3.jpg" width=300px>

The VGA port stands vertically, which ensures that it's strong against downward stress itself, as well as avoiding a rotationally pulling tendency that could pull the 10-pin DIN connector out of the console.

The optional 3.5mm audio jack was carefully positioned so that it doesn't block the communication port.

The power jack was also avoided, including the launch version with a slightly protruding profile.

<img src="./Pics/design_04_avoidance.jpg" width=400px>

## Parts

- Project PCB
  - [Main Board](https://oshpark.com/projects/ftX4cA6v)
  - [VGA Board](https://oshpark.com/projects/xInxeNXi)
  
- 3D Printed Shell
  - Front Shell (Universal)
  - Back Shell (Choose one according to your configuration)
    - [RGBS Marking](https://github.com/jeffqchen/10DIN2VGA/blob/main/3D%20Print/Shell%20Back-RGB.stl)
    - [Y/C & C Marking](https://github.com/jeffqchen/10DIN2VGA/blob/main/3D%20Print/Shell%20Back-YC.stl)
    - [No Marking](https://github.com/jeffqchen/10DIN2VGA/blob/main/3D%20Print/Shell%20Back.stl)

- VGA Port Slim, Female - [Link](https://github.com/jeffqchen/JeffParts/blob/main/Connectors/HD15/Slim/Female%20PCB/info.md)

- 10 pin Mini DIN Male Plug, Through-Hole Type - [Link](https://github.com/jeffqchen/JeffParts/blob/main/Connectors/Mini%20DIN/10Pin/Through%20Hole/info.md)

- [2x] SMD Capacitor, 10uF / 6.3V / Imperial 0603 Size

- M2-16mm screw and hex nut - [Link](https://github.com/jeffqchen/JeffParts/blob/main/Parts/M2%20M3%20Hex%20Screw%20%26%20Nut/info.md)


### Optional

For CSync configuration on NTSC console
- SMD Capacitor, 100uF / 6.3V / Imperial 1206 Size - [Link](https://github.com/jeffqchen/JeffParts/blob/main/Components/100uF%20SMD%20Cap/info.md)

- SMD Resistor, 470 Ohm / Imperial 0603 Size

## 3D Printing

Print the parts in the orientation shown below. Support is required and must be completely removed after wards.

<img src="./Pics/3d_print.jpg" width=400px>

### Preparing After Printing

#### Front Shell

There will be a small piece of support material stuck inside the cavity designed for a hidden nut.

You must extrac that support material in order for the nut to go in.

A dental pick will work nicely. A pair of tweezers with sharp tips might work as well.

<img src="./Pics/front_nut_1.jpg" width=400px>

After extracting ALL the support material (check with a flashlight), press and fit the M2 nut inside. It might be a tight fit.

<img src="./Pics/front_nut_2.jpg" width=300px><img src="./Pics/front_nut_3.jpg" width=300px>

#### Back Shell

Make sure the barrel cavity for the 10-pin DIN connector is smooth. If you see any artifact or blob sticking into the hole, trim with a sharp knife.

<img src="./Pics/back_barrel.jpg" width=400px>

## Assembly

### Preparing the PCB

Trim all the stubs sticking out side the PCB profile. Side cutters and files are your friends.

<img src="./Pics/prepare_01_pcb.jpg" width=400px>

### Combine the Two PCBs

The Two PCBs must be combined in a perfect perpendicular shape. With the help of the 3D printed insert piece, you can easily get this done.

Start by insert the VGA board all the way into the slot in the main board. There should be NO gap.

<img src="./Pics/assembly_pcb_0.jpg" width=400px>

Insert the combined PCBs into the slot in the printed insert piece.

<img src="./Pics/assembly_pcb_1.jpg" width=400px><img src="./Pics/assembly_pcb_2.jpg" width=400px>

Solder in one pin and check if the PCBs are perfectly perpendicular to each other and have no gap between each other. Adjust by re-melting the joint.

<img src="./Pics/assembly_pcb_3.jpg" width=400px>

After confirming, remove the insert and solder in the castellated vias, one side at a time.

<img src="./Pics/assembly_pcb_4.jpg" width=400px>

Add ample amount of solder and make sure all the joints are nice and full.

<img src="./Pics/assembly_pcb_5.jpg" width=400px><img src="./Pics/assembly_pcb_6.jpg" width=400px>

### Solder SMD Components

Tin SMD pads for the capacitors and resistors, and solder them in place.

**If you are planning to NOT use CSync, or if your console is PAL, do NOT populate the two components inside the "CSYNC NTSC" area.**

<img src="./Pics/assembly_smd_1.jpg" width=400px><img src="./Pics/assembly_smd_2.jpg" width=400px>
<img src="./Pics/assembly_smd_3.jpg" width=400px><img src="./Pics/assembly_smd_4.jpg" width=400px>


### Solder VGA Port

Nothing Special, just make sure it's all the way flush to the VGA board.

<img src="./Pics/assembly_smd_3.jpg" width=400px>

### Solder 10-pin Mini DIN Port

Pre-tin the two curvy ground pads around the 10DIN footprint on the "Saturn Side" of the main board with a small amount of solder, then wick them clean. Make sure the pads are as flat as possbile.

<img src="./Pics/assembly_pcb_0.jpg" width=400px>

Insert the 10DIN port **all the way** into the PCB from the "Saturn Side" of the main board. Make sure there is no gap between the 10DIN connector and the main board.

Solder down the tongue on the top of the DIN with some solder, so the connector stays in place.

<img src="./Pics/assembly_10din_01.jpg" width=400px>

Add some solder to the curvy ground pads around the 10DIN. Make sure the solder is well-wetted to both the pads and the metal shielding.

*You might have to raise the temperature of your iron by a few dozens of degrees in Celsius if you usually solder at a lower temperature. I went from 370 to 400.*

<img src="./Pics/assembly_10din_02.jpg" width=400px><img src="./Pics/assembly_10din_03.jpg" width=400px>

<img src="./Pics/assembly_10din_04.jpg" width=400px><img src="./Pics/assembly_10din_05.jpg" width=400px>

Solder in all the pins on the other side.

**Do NOT heat up these pins for too long or you risk melting plastic holding the pins inside the connector and destroying it.**

<img src="./Pics/assembly_10din_06.jpg" width=400px>

Add more solder to the top tongue and make sure solder creeps over to the other side of the PCB to form a strong joint by keeping the heat on for a bit longer.

<img src="./Pics/assembly_10din_07.jpg" width=400px><img src="./Pics/assembly_10din_08.jpg" width=400px>

### Configure The Jumpers

#### RGBS Mode

Close the jumpers to the lower position (with triangle) on the main board. Do NOT close the jumper on the VGA board.

If you wish to use alternative sync signals (Luma OR CVBS), close the corresponding jumper inside the "Alt-Sync" area as well. **Do NOT close both of them.**

<img src="./Pics/assembly_smd_2.jpg" width=400px>

#### Adapter Mode
Close the jumpers to the upper position (without triangle) on the main board. Close the jumper on the VGA board.

<img src="./Pics/assembly_jumper_03.jpg" height=400px>

### Solder 3.5mm Audio Jack

Insert the 3.5mm audio jack into the main PCB from the "Outside".

Make sure it's flush to the PCB, then solder in two pins with a small amount of solder.

<img src="./Pics/assembly_audio_01.jpg" height=400px>

Trim all the protruding legs. Make sure they are as short as possible, but there's no need to go crazy to make it flush.

<img src="./Pics/assembly_audio_02.jpg" height=400px>

Solder in all the pins with proper amounts of solder.

<img src="./Pics/assembly_audio_03.jpg" height=400px>

### Closing The Shell

Start by inserting the 10-pin DIN into the shell from the inside.

This will be a tight fit. Try pressing straight down from the back of the DIN connector to avoid lateral movements.

<img src="./Pics/assembly_shell_1.jpg" height=400px>

If it's difficult, use the insert piece as a thumb guard as below.

The insert piece should be left inside the shell as a support piece. It should be flush or below the shell interface. If it's sticking out, the board assembly is not in place.

<img src="./Pics/assembly_shell_2.jpg" height=400px>

Push down the PCB all the way. Use the 3.5mm jack as a reference. The port should touch the shell when the board assembly is in place.

<img src="./Pics/assembly_shell_3.jpg" height=400px>

Close the front shell onto the assembly. Hold the shells together with one hand, and put the M2-16mm screw in.

When it begins to feel harder to turn the screw driver, start using only 3 fingers to turn the screw driver in order to prevent over-tightening it and cracking the front shell.

The screw head should be flush or slightly below the back surface of the dongle as shown below.

<img src="./Pics/assembly_shell_4.jpg" height=400px>

And you have built the dongle!

<img src="./Pics/cover.jpg" width=800px>

#### Double Down On Strength

I've left a few gaps around the 10-pin DIN connector barrel. You may inject small amounts of super glue or even epoxy to make it indestructible. I didn't feel the necessity personally, but just in case your printer came out with a piece that's slightly loose.

<img src="./Pics/assembly_shell_4.jpg" height=400px>

#### If the 10-pin DIN Barrel Was Impossible To Push In

Your printer might give you a print with the barrel cavity being too tight. You can try using "Hole Horizontal Expansion" in Cura (or an equivalent option in other slicer software) to give it a 0.1mm expansion.

----------------
Shield: [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg