---
title: "Clock with logic gates"
date: "2019-04-10"
author: "Stephanie Zepeda"
cover: "img/12hrs-clock.png"
description: "Designing of a sequential circuit with counters, which would have the function of a 12-hour clock, where it would have an output that will indicate PM or AM, the clock could be started at any time and it could be reset."
---

## 12hrs clock using logic gates

>The 74LS90 decade counter is a counter that is capable of dividing the frequency each time it is connected with one another, therefore it was used to make it send a signal synchronized with the clock pulse so that the desired account, in addition a 74LS47 decoder was connected for the display outputs.

The logic circuits that were used for the construction of the clock were: 74LS90, counter to decades, to count the seconds and minutes; 74LS47, BCD decoder, to decode the counter outputs to outputs for the 7 segment display; 74LS190, synchronous BCD counter, to generate the sequence of the hours (1 to 12); 74LS73, JK flip-flop, to display if it is AM OR PM; 74LS08, 2-input AND; 74LS00, 2-input NAND; finally, 74LS04, NOT.

{{< image src="/img/Circuit.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}
