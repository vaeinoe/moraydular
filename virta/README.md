# Moraydular Virta #

A 100x200mm hybrid power supply design for Eurorack modular synthesizers.

Virta uses external SMPS DC wallwart as input, splits and regulates down to +-15V and +5V via standard 1x2 or 1x1 inch DC-DC blocks, then regulates +-15V down to +-12V using low dropout (LDO) linear regulators. Pi filters are included on the PCB between DC-DC stages for attenuating high frequency switching noise before final linear regulation stage. There is a provision for dummy load resistors for those DC-DC converters requiring a minimum load for stability. 

This should theoretically provide for a high quality power output without mains power inside the enclosure, at the expense of quite high parts cost (compared to a standard LM317/LM337 transformer-based power supply or plain SMPS) and less than ideal efficiency. 

At this point the project is work in progress. Prototype PCBs have been ordered but not yet built and verified functional.

## Ordering and Building Notes ##

TODO

## Bill of Materials ##

TODO
