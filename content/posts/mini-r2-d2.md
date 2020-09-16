---
title: "Mini R2-D2"
date: "2020-06-02"
author: "Stephanie Zepeda"
cover: "img/MiniR2D2.png"
description: "Construction of a R2-D2 at a scale of 45%, using Solidworks, Arduino and a 3D Printer."
---

# Frame Design

The design was made taking into account the multiple vents and panels of the robot seen on the films, so in a future it could have space to accomodate little sistems for their movemnt. The measurements took into account to make the frame where taken from the website wwww.astromech.com

{{< image src="/img/frame.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}

# Head mechanisim

- Solidworks design

The operation of this mecanism is simple it consist on a motor in the center of the head which gives action to a axial gear that moves smothly thanks to the help of a lazy sussan that is attached to the fram and the base of the head.

{{< image src="/img/head.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}



 - Arduino program

 ```
  else if (letter == 'E')
  {
    digitalWrite(LedR, LOW);
     randNumber = random(1, 16);
     digitalWrite(CABD, LOW);
     digitalWrite(CABA, HIGH);
     myDFPlayer.play(randNumber);
     Serial.println(randNumber);

     Serial.println(F("Cab Izq"));
     digitalWrite(LedA, HIGH);
     delay(10000);
     digitalWrite(LedA, LOW);
     digitalWrite(LedR, HIGH);
     digitalWrite(CABD, LOW);
     digitalWrite(CABA, LOW);
   }
   else if (letter == 'F')
   {
     digitalWrite(LedR, LOW);
     randNumber = random(1, 16);
     digitalWrite(CABD, HIGH);
     digitalWrite(CABA, LOW);
     myDFPlayer.play(randNumber);
     Serial.println(randNumber);
     Serial.println(F(" Cab Der"));
     digitalWrite(LedA, HIGH);
     delay(10000);
     digitalWrite(LedA, LOW);
     digitalWrite(LedR, HIGH);
     digitalWrite(CABD, LOW);
     digitalWrite(CABA, LOW);
   }
```

{{< video src="/video/r2" >}}

#  Center leg

Simple scissor mechanisim for the center leg to come up or down.

{{< image src="/img/centerfeet.png" >}}

# Results

{{< image src="/img/r2d2100.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}
