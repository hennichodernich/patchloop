# patchloop
Design files for the PatchLoop PCB

The files patchloop2.kicad_* contain the version with RJ45 jacks on opposite sides. This allows for neat short traces between the jacks.

I needed to rework the files patchloop.kicad_* (jacks on same side) because the first version contained a bug so that only one loop was used effectively.

PCB manufacturer Aisler will directly accept the KiCad file for manufacturing, but you can find zipfiles with the gerbers for both variants in the gerbers/ subdirectory. Any PCB manufacturer (e.g. BetaLayout, JLCPCB, PCBWay, OSHPark) should be able to accept those.

Licensed under CC BY-SA 3.0

# Note on the choice of balun

While in the schematic (and in the BOM) you will find an M/A-COM ETC4-1-2, this might not be the optimal choice for all possible patch cables. For cables with a length of 2-3 meters, an ETC1-1-13 usually works better to achieve ~50 ohms on the coax connector. The ETC4-1-2 is advantageous for very long cables (and thus higher impedances). I also tried Coilcraft WBC4-4 to transform from very low impedances to 50 ohms (take care of its orientation), but this only makes sense for very short cables: A 1m cable exposed approximately 10 ohms to my NanoVNA.

In general the same holds for selfwound baluns, an 1:1 balun will work best in most of your applications.
 
