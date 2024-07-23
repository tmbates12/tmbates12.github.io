+++
title = 'ADR1000 Refboard Intro'
date = 2024-07-22T20:49:50-04:00
draft = false
+++

# What's this all about???
Well, to be honest this is just a quick little project I cobbled together to have a semi-transferrable votlage standard for my 6.5digit multimeters I have.
Given that throwing a little board together using the [ADR1000](https://www.analog.com/en/products/adr1000.html) isn't all that hard, I figured I'd just go with it for now....
The [ADR1001](https://www.analog.com/en/products/adr1001.html) looks like a bunch of fun to use as well, but due to TCE (Temperature Coefficient of Expansion) differences between an LCC package and an FR4 PCB substrate, the tempco of the whole reference gets ruined.
However, the answer to this problem in the future may very well be to use a rigid-flex PCB and suspend the IC on a flex section of the board... I may pursue this at some point.

# The schematic and board design!
Here's the schematic, it's essentially the reference design, but with a few tweaks to fit what I was able to find on Digi-Key at the time of designing (July 2024) and what I was able to get as samples from VPG (The two "important" dividers).
![ADR1000 Reference Board Schematic](/posts/adr1000-refboard-schem.png)

As for the board design, I just did the bare minimum, and I still need to 3D print the plastic cap for the ADR1000 itself.
Here's some quick images of the board design in KiCAD, as well as IRL.
![ADR1000 Reference Board PCB Design](/posts/adr1000-refboard-board.png)
![ADR1000 Reference Board PCB Picture](/posts/adr1000-refboard-IRL.jpg)

# Some super quick measurements
I've taken some pretty quick measurements while the reference is still "fresh", but we'll see how it ends up after it burns in for a while.
Across three meters (My 34401A and 3457A, as well as the 34465A in the lab where I work) all the measurements were within ~10ppm (uV/V??? who cares) of each other without taking a large amount of care with the measurements.
All of the measurements were done on the 10V range @ 100NPLC. ACAL was performed on the 34465A before the measurement and all meters were allowed to warm up for well over a day before the measurement.

| Meter  | Voltage (V) |
| -----  | ----------- |
| 34401A | 9.96705     |
| 3457A  | 9.96701     |
| 34465A | 9.96696     |

# Afterword
Like a mentioned earlier, this was a fairly "low effort" project, so I'm not expecting amazing sub-ppm stability performance out of this thing, but it's much better than most of the cheaper off-the-shelf options.
I'm definitely interested in working on an ADR1001 design in the near future, so that may be the path forward for now....