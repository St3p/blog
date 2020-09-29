---
title: "Shift Registrers"
date: "2019-03-10"
author: "Stephanie Zepeda"
cover: "img/Shift-Registers.png"
description: "Four uses of shift registers. The first part consisted of simulating a mouse moving, that is, turning on a segment of the display at the same time with a given sequence; the second part, simulated a mouse growing until it became a worm, therefore, the display had to be turned on segment by segment according to the sequence given; for the third part, we had to simulate a viper in motion with two displays, turning on three segments per movement; finally, in the fourth part, a ball was simulated that bounced and traveled through nine displays, lighting four segments at the same time with a certain sequence."
---

## Screen Saver: Basic Scroll: The Mouse

For the first part, it was decided to use six JK flip flops (74LS76) connecting their outputs to the J inputs and the negated outputs to the K inputs, for the first flip flop a two input OR (74LS32) connected to the output of the last flip flop and to a pulse signal, so that, together with the clock signal connected to all the flip flops, a high signal would be passed through all the flip flops and with the outputs in parallel connect them to the display.

{{< image src="/img/mouse.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}


{{< image src="/img/mouse-Circuit.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}

## Screen Saver: Basic Shift: The Growing Mouse

In part two, we used seven D flip flops (74LS74) connecting their outputs to the D inputs, for the first flip flop a voltage signal was connected to the D input and a two input AND (74LS08) connected to the clock input To the clock signal and to a dip switch to be able to pause the circuit, the negated output of the last flip flop was also connected to the reset of the flip flops so that once the sequence was finished it would restart.

{{< image src="/img/growingmouse.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}


{{< image src="/img/growingmouse-circuit.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}

## Screen Saver: Sliding in two displays: The viper

The third part was made very similar to the first with twelve JK flip flops (74LS76) with the difference that each parallel output was connected to NOR's of five inputs (74LS260) and three inputs (74LS27), later the outputs of the NOR's were connected to NOT's (74LS04), since each segment of the sequence had to remain on for three and four clock times depending on the sequence. As in the second part, the clock input was connected with an AND with two inputs (74LS08) and a dip switch to be able to pause the sequence.

{{< image src="/img/viper.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}


{{< image src="/img/viper-circuit.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}

## Screen Saver: The Ball

For the last part, it was also very similar to activity 1, nine JK flip flops (74LS76) were used, where each parallel output was connected to four pins of the displays in such a way that the shape of a ball was generated and follow the sequence requested. In the same way, a dip switch was connected to the resets of all the flip flops in order to stop the sequence and restart it.

{{< image src="/img/ball.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}


{{< image src="/img/ball-circuit.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}
