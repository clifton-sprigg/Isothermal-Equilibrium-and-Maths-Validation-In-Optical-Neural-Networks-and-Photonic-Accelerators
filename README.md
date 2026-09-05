OK so you might think this is insane but when you delve into the physics and maths it all seems to work. Though admittedly this could just be the communism of computing (looks good on paper but doesn't work in practice). I had only looked into photonics for 2 days prior to writing this so I don't know. 

Some clarifications:

(**Note, I'm leaving this here to show my train of thoughts.** If you think the radiative maths vents add extra complexity to actually get the waves out of the block, then you need to learn that geometry is indeed your friend, because you can just make sure that they are 8 degrees to the surface. If this alone is insufficient then micro-prisms or serrated facets could be used at the ends of these waveguides to ensure a clean exit.)

I discovered the main flaw in this design, actually getting the radiative maths vents out of the block, and the sheer number of them. Far from thinking this makes it impossible instead it makes me think "seriously how is this the status quo?". So although geometric wiring is the industries bread and butter, to the point that they have you believing that a 12-18nm transistor is 2nm, lets try to solve this too. First group the gates into local clusters with a shared waste output line reducing the number of waveguides required by 10-100 times. Next move the waste waveguides onto a separate layer via vertical photonic vias to a completely passive "waste layer" of the chip. This layer should be made of a material that has a lower thermo-optic coefficient and lower propagation loss than the compute layer allowing the waste light to travel long distances across the chip and handle high optical power without degrading or heavily heating the substrate along the way. This then allows for combining these waveguides further as the small heat dissipation in this layer could be isolated from the compute layer with a small isolating layer and etched vacuum pockets (think silicon compute layer with a silicon oxide insulation layer and silicon nitride waste layer). These guides can then fan out as they approach the edge. To ensure there are no back reflections that could catastrophically disrupt calculations as the waste light moves between layers we again use simple geometry and make the vias tapered wedges so that any reflections are deliberately forced upward to scatter harmlessly out of alignment with the input waveguide. The final phase for the waveguides is, instead of trying to manufacture pristine edges that can't back scatter light, we place the absorbing pads at the peripoheral as an inner heating pad having the same effect as directly heating the thermal blanket. To fully wrap this up we separate the telemtry layers into the compute layer for catching the maths errors and the waste layer to actively know how much heat is being dumped into the thermal blanket. 

I mentioned the a-thermal polymers purely because there have been a lot of advancements in this area recently so wanted to make sure no one could just backfill with a new polymer and call it a "novel design" for patent purposes. Obviously at present using these would just be a recipe for delamination and cracking.

The active heating regime mentioned is a pointless waste of time! The reason it is there is 2 fold, first once again I don't want big tech pulling a fast one with patents, and there are always those who like to over engineer, so that one's for you. 

For the maths verification I mention you can "dump the current calculation as corrupt before it even arrives at the next calculation." I did not mean this to be extra "light speed switches" or anything at all more complex than not reading the data when it arrives as I didn't know those switches even existed!

The "zero cost implementation" is based on the fact they redesign and replace chips so regularly it would just be part of that process thus no additional costs. 


Things not noted:

By keeping the substrate at 70-75C you actually reduce the thermal gradient required for the microheaters to change the refractive index, thus lowering ΔT at the same time as consuming less power. 

Obviously this thermal control would never work for any chips with onboard lasers, however it would work for MZI's (Mach-Zehnder Interferometers) and MRR's (Micro-Ring Resonators).


Further clarifications (just so my ideas don't get misrepresented):

First I'm not suggesting that a thermal jacket will miraculously get rid of localised thermal spikes but rather it will keep a baseline clamped reducing the ΔT, thus making the substrate many factors more stable than present designs. (I'm not trying to create perfect, just better.)

Whilst it sounds counter intuitive to just "dump" data, when you factor in that this data packet can be resent immediately, whilst any data it goes with is held, and dealt with at a hardware level when an error is detected this is many many times faster than electronically checking every single output. (I'm not trying to make perfect, I'm just trying to make a new set of compromises for a new medium rather than applying the same compromises made in the 1950's for electronic computing.)

Finally it is obvious that this concept makes a chip physically thicker however for the Speed and power usage improvements this trade off is worth while. (It also allows the industry to do their favourite thing and optimise the geometry to make it smaller and eek out those 2% gains they've so loved for the last decade.)


If you think I'm insane please note, I'm not the one who came up with the idea to put heaters and absorbers in the middle of the chip then try to keep everything cool thus destroying lights determinism. That is all on the industry and is what they are doing right now.

Please stop treating photons like they are electrons, they are not! You cannot increase resistance or cause leakage by increasing temperature, all you actually achieve is stabilising the waveguide lengths thus assuring determinism again. This is a new medium that needs radically different compromises to those made for electrons so many years ago, please don't forget these were compromises for that specific medium. 


(Note: I, (Graham Clifton-Sprigg), the author hereby dedicate this entire work, including all architectural concepts, geometric wave-routing logic, thermal management loops, and real time error checking to the public domain under the Creative Commons CC0 1.0 Universal license. It is published openly to establish immediate prior art and ensure this technology remains free and un-patentable by any entity. And once again this is the concepts herein contained and in no way linked to Materials or specific geometries. So stop being devious, adding in 1 minor little thing doesn't make this your own "novel" concept!)
