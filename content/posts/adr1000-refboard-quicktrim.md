+++
title = 'A Quick Update on Trimming the ADR1000 Reference Board'
date = 2024-07-28T17:33:37-04:00
draft = false
+++

### The update
Just a random update about the reference board, I did a quick trim to bring the output closer to 10V (At least according to my 34401A).

The math for the trim was pretty simple, just a some quick resistor combination formulas...
Ended up settling on a 1Meg resistor in parallel with the 10k resistor... which brings us to the following result for now:
![ADR1000 Quick Trim result](/posts/images/adr1000-refboard-quicktrim.jpg)

Ideally I would've used a 1.02Meg resistor to bring it even closer to 10V, I'll find the optimal extra resistance to add once the reference burns in a little more.