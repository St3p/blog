---
title: "Slider Crank"
date: "2019-05-29"
author: "Stephanie Zepeda"
cover: "img/drogon1.png"
description: "This Mechanism is one of the most used systems in the mathematical field, it is an
arrangement of parts designed to make a rotary straight motion movement as the type of
movement that makes a piston engine, so me can define it as one type of four bar linkages
which has three revolute joints and one sliding joint"
---

## Simulation of a slide crank in ADAMS and MATLAB.

Slider-cranks are a commonly used type of mechanism translating a rotary movement
into a linear one, or the other way around. In this lab session, three slider-crank variations were
modelled using ADAMS software. Their movements were simulated and analyzed to find the
velocities and position for certain input angles. The obtained results were compared to manual
computations using the vector loop equations. With these two outcomes, it was attempted to
estimate the accuracy of the ADAMS software.

The main applications of it can be found in the industry as in the engines powered by
diesel or gasoline, also this type of mechanism has been used and analyzed over time for their
advantages as: low cost, few parts, weight and others.
The coordinate system to this type of mechanism should make the x-axis and the slider
one coincide, so we can associate a vector with each link also we can say that the magnitude of
this vector is the length of the link that is being analyzed, the direction of the vector is along the
link, so we can conclude that the system made a loop

{{< image src="/img/slider.png" >}}

{{< image src="/img/sliderADAMS.png" >}}
