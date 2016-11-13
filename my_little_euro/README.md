# Moraydular My Little Euro #

A compact (50x250mm) combined linear halfwave power supply and 7-way power distribution PCB for Eurorack modular synthesizers. A convenient way to get your first DIY euro system or a small tabletop setup going for not too much money.

The maximum output current depends on the capacitance of the big reservoir capacitors, heatsinking of the regulators, and current rating of the external transformer. In any case, do not expect to get more than roughly 500mA of +-12V with any configuration - this is meant to be a simple and cheap supply for a couple of modules, not something for big systems. The +5V regulator draws power from the +12V rail so this has to be taken into consideration if your system uses a lot of +5V.

![Populated PCB](http://vae.fi/moraydular/my_little_euro_v1.jpg)

## Ordering and Building Notes ##

The file moraydular\_my\_little\_euro\_v1.dip contains the PCB design in DipTrace format. The Gerber files in gerber directory are for ordering a 5x25cm 2-layer PCB. I have successfully received prototypes from DirtyPCBs and the files should be fine as-is for other prototype PCB services like OSHPark, iTead or Seeed. Please specify 2 oz copper traces (or even thicker if you can get it for decent price).

Populating the PCB should be relatively straightforward. 

 * The LED polarity follows standard convention: the short leg / cathode / notched side of LED goes where there's a notch in the silkscreen
 * You should use heatsinks for regulators according to your estimated current draw - Tayda sells decent unfinished aluminum ones, for example

## Bill of Materials ##

 * **1x** External 12V AC-AC transformer. Note that AC-DC will NOT work! Something like 1A would fit the maximum intended purpose best. These aren't available everywhere these days, but bigger electronics stores usually stock them, and you can often find suitable ones for super cheap at flea markets and surplus stores.
 * **1x** DC power connector matching the connector for the transformer. Should be isolated from case's metal parts as it will carry AC. The large holes should fit a standard PCB mount 2.1mm or 2.5mm center DC connector (if you don't need a power switch), or you can wire a panel mount one to the smaller holes on the sides of the connector footprint.
 * **7x** 16-pin (2x8) 0.1" shrouded box header (eg. Reichelt WSL 16G) OR unshrouded pin strip
 * **3x** 3mm LEDs
 * **3x** Current limiting resistors according to LEDs you've chosen. 2x 1K, 1x 220R as indicated on PCB silkscreen should be fine at least for normal red or green leds
 * **8x** standard rectifier diodes, any of 1N4001...1N4007 will do
 * **1x** 7805 voltage regulator + heatsink
 * **1x** 7812 voltage regulator + heatsink
 * **1x** 7912 voltage regulator + heatsink
 * **3x** 10uF electrolytic capacitors, 16V or higher voltage rating
 * **5x** 100nF ceramic capacitors
 * **4x** 4700uF 25V+ electrolytic capacitors (unmarked on the PCB). Bigger caps would be able to supply larger currents more reliably, so if you can find and fit even bigger capacitance (6800uF?) with 7.5mm lead pitch and 25V or higher voltage rating, go for it.
