# 10DIN2VGA Multi-Purpose Dongle



This is a 10-pin mini DIN to VGA dongle that supports outputting RGBS or S-video & composite video signal, plus stereo audio.

The RGBS signal is compatible with 75-ohm terminated SCART video. The S-video & composite video signals are directly output from the console.

## Functionality

When configured to RGBS mode, you can opt to use C-Sync when using with an NTSC console, or use either Luma or composite video as sync for compatibility with PAL consoles.

When configured to adapter mode, you can use the widely available VGA to S-Video/CVBS adapter to output the aformentioned video format.

It is possible to modify the solder jumpers to change the adapter between the two configurations. However it's not recommended to repeatedly taking this dongle apart for that purpose, as the structure integrity might become compromised.

## Design Details

The 10-pin mini DIN connector has several problems.

The biggest one is that there is only one correct way to insert it, and infinite wrong ways to attempt. There is also no easy way to tell whether you are holding it correctly without triple checking with your eyes. It's also very difficult to maintain the correct orientation during insertion, even after you've confirmed it.

Most 10-pin DIN ports on the Saturn are badly damaged due to bad attempts to insert a video cable. Combined with too much force applied, the connector are frequently broken.

Due to the position of the port, the strain from the video cable will stress the connector and reduce the life of the port.

The design of this dongle elimiates all the aformentioned problems.

The shape of the outside shell makes it easy to tell which way it's facing. Make sure the curve is in the 2nd quadrant and you know it's the correct way.

The shape of the inside shell conforms to the indented area around the AV port on the console, with the bottom of the dongle flat and flush with the table. This will ensure there is only one way to plug in the adapter. Since the adapter tightly follows the outline of the shell, rotational stress and downward stress are effectively offloaded to the shell of the console, as well as making it impossible to insert the connector too far into the console.

The VGA port stands vertically, which ensures that it's strong against downward stress itself, as well as avoiding a rotationaly pulling tendency that could pull the 10-pin DIN connector out of the console.

The optional 3.5mm audio jack was carefully located so that it doesn't block the communication port.