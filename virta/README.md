# Moraydular Virta #

A 100x200mm hybrid power supply design for Eurorack modular synthesizers.

Virta uses external SMPS DC wallwart as input, splits and regulates down to +-15V and +5V via standard 1x2 or 1x1 inch DC-DC blocks, then regulates +-15V down to +-12V using low dropout (LDO) linear regulators. Pi filters are included on the PCB between DC-DC stages for attenuating high frequency switching noise before final linear regulation stage. There is a provision for dummy load resistors for those DC-DC converters requiring a minimum load for stability. 

This should theoretically provide for a high quality power output without mains power inside the enclosure, at the expense of high parts cost (compared to a standard LM317/LM337 transformer-based power supply or plain SMPS) and less than ideal efficiency.

## Ordering and Building Notes ##

For now this is "at your own risk" type advanced project. I haven't exactly specified the part numbers to use because it hasn't been confirmed whether they're ideal and working for the limits I have specified. Furthermore, both DC-DC converters and LDOs may be a bit picky in auxiliary components.

Notes:

 - There is one error in v0.6 PCB: the ON/OFF pin of LM2991 should be tied to ground with a resistor leg or similar. MAY work without that modification.
 - For current V0.6 PCBs the 1"x1" footprint DC-DC holes are noticeably smaller than for the 1"x2" pinout, so all 1"x1" DC-DCs won't fit!
 - C31 should NOT be populated, it's there by mistake and will cause LM2991 to oscillate.

## Bill of Materials ##

 - 6x 100uF low ESR electrolytic (C1-C3, C16-C18)
 - 11x 0.1uF MLCC ceramic (C4-C6, C13-C15, C22-C24, C28-C29)
 - 9x 0.1uF 0805 SMD ceramic (C7-C12, C19-C21, optional, should improve switching noise filtering, may cause problems with some DC-DCs)
 - 3x 47uF low ESR electrolytic (C25-C27)
 - 3x 10uF (low ESR) electrolytic (C30, C32, C33)
 - 4x any of 1N4001 to 1N4007 (D1-D4)
 - 1x PCB mount 5x20mm fuse holder (F1 + a 5x20mm fuse according to your power use)
 - 3x 0.1" 2-pin headers for dummy load jumpers (J1-J3, may be left out if dummy load not used)
 - 4x ~10uH 2A+ radial / vertical inductor (L1-L4)
 - 3x standard 3mm led (LED1-LED3, pick a color and adjust resistors accordingly)
 - 2x isolated 15V DC-DC converter (ISOL 15v, specifications according to required power)
 - 1x isolated 5V DC-DC converter (ISOL 5V, specifications according to required power)
 - 14x PCB mount 6,3mm Faston / Abiko / quick disconnect terminals
 - 1x LM2991T (U1)
 - 1x LM1086CT-ADJ (U2, may use LM1084 or LM1085 but has to be -ADJ version)
 - 2x "fin" style TO220 heatsink (height according to required power)
 - 2x 1K "3296Y" style vertical multiturn trimmer (TR1, TR2)
 - 1x 220R 1/4W resistor (R6)
 - 4x 1K 1/4W resistor (R5, R7, R9, R10)
 - 2x 8.2K 1/4W resistor (R4, R8)
 - 2x 0.5R 5W power resistor (R1, R2)
 - 1x 0.22R 5W power resistor (R3)
 - 2x 56R 5W power resistors (RL1, RL2, optional, only if dummy load needed)
 - 1x 22R 5W power resistor (RL3, optional, only if dummy load needed)
 - 1x SMPS wall wart according to required power and chosen DC-DC converters
