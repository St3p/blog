---
title: "Mini R2-D2"
date: "2020-06-02"
author: "Stephanie Zepeda"
cover: "img/MiniR2D2.png"
description: "Construction of a R2-D2 at a scale of 45%, using Solidworks, Arduino and a 3D Printer."
---

# Frame Design

The design was made taking into account the multiple vents and panels of the robot seen on the films, so in a future it could have space to accommodate little systems for their movement. The measurements took into account to make the frame where taken from the website wwww.astromech.com

{{< image src="/img/frame.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}

# Head mechanisim

- Solidworks design

The operation of this mechanism is simple it consist on a motor in the center of the head which gives action to a axial gear that moves smoothly thanks to the help of a lazy Susan that is attached to the from and the base of the head.

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
{{< youtube id="vOZ99ObCF2w" autoplay="true" color="white" yt_start="12" yt_end="24">}}


#  Center leg

- Solidworks Design

Simple scissor mechanism for the center leg to come up or down.

{{< image src="/img/centerfeet.png" >}}

- Arduino Code

```
if (letter == 'G')
    {
      randNumber = random(1, 16);
      digitalWrite(LedA, LOW);
      digitalWrite(APieCD, HIGH);
      digitalWrite(APieCA, LOW);
      digitalWrite(BPieCD, HIGH);
      digitalWrite(BPieCA, LOW);
      myDFPlayer.play(randNumber);
      Serial.println(randNumber);
      Serial.println(F("Pie Central Arriba"));
      digitalWrite(LedA, HIGH);
      delay(1500);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(APieCD, LOW);
      digitalWrite(APieCA, LOW);
      digitalWrite(BPieCD, LOW);
      digitalWrite(BPieCA, LOW);

    }
    else if (letter == 'H')
    {
      digitalWrite(LedR, LOW);
      randNumber = random(1, 16);
      digitalWrite(APieCD, LOW);
      digitalWrite(APieCA, HIGH);
      digitalWrite(BPieCD, LOW);
      digitalWrite(BPieCA, HIGH);
      myDFPlayer.play(randNumber);
      Serial.println(randNumber);
      Serial.println(F("Pie Central Abajo"));
      digitalWrite(LedA, HIGH);
      delay(300);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(APieCD, LOW);
      digitalWrite(APieCA, LOW);
      digitalWrite(BPieCD, LOW);
      digitalWrite(BPieCA, LOW);
    }
```
{{< youtube id="o6a2He_KXXc" autoplay="true" color="white" yt_start="12" yt_end="24">}}

# Foot

- Solidworks Design

System of gears to give the system more torque and pull force.

{{< image src="/img/foot.png" >}}

- Arduino Code

```
if (letter == 'C')
   {
     randNumber = random(1, 16);
     digitalWrite(LedA, LOW);
     digitalWrite(IZQD, LOW);
     digitalWrite(BIZQD, LOW);
     digitalWrite(IZQA, LOW);
     digitalWrite(BIZQA, LOW);
     digitalWrite(DERD, HIGH);
     digitalWrite(BDERD, HIGH);
     digitalWrite(DERA, LOW);
     digitalWrite(BDERA, LOW);
     myDFPlayer.play(randNumber);
     Serial.println(randNumber);
     Serial.println(F("Derecha"));
     digitalWrite(LedA, HIGH);
     delay(2500);
     digitalWrite(LedA, LOW);
     digitalWrite(LedR, HIGH);
   }
   else if (letter == 'D')
   {
     digitalWrite(LedR, LOW);
     randNumber = random(1, 16);
     digitalWrite(IZQD, LOW);
     digitalWrite(IZQA, HIGH);
     digitalWrite(DERD, LOW);
     digitalWrite(DERA, LOW);
     digitalWrite(BIZQD, LOW);
     digitalWrite(BIZQA, HIGH);
     digitalWrite(BDERD, LOW);
     digitalWrite(BDERA, LOW);
     myDFPlayer.play(randNumber);
     Serial.println(randNumber);
     Serial.println(F("Izquierda"));
     delay (2500);
           digitalWrite(LedA, LOW);
     digitalWrite(LedR, HIGH);

   }
else if (letter == 'A')
   {
     digitalWrite(LedR, LOW);
     randNumber = random(1, 16);
     digitalWrite(IZQD, HIGH);
     digitalWrite(IZQA, LOW);
     digitalWrite(DERD, LOW);
     digitalWrite(DERA, HIGH);
     digitalWrite(BIZQD, HIGH);
     digitalWrite(BIZQA, LOW);
     digitalWrite(BDERD, LOW);
     digitalWrite(BDERA, HIGH);
     myDFPlayer.play(randNumber);
     Serial.println(randNumber);
     Serial.println(F("Adelante"));
     digitalWrite(LedA, HIGH);
     delay(1000);
     digitalWrite(LedA, LOW);
     digitalWrite(LedR, HIGH);

   }

    else if (letter == 'B')
   {
     digitalWrite(LedR, LOW);
     randNumber = random(1, 16);
     digitalWrite(IZQD, LOW);
     digitalWrite(IZQA, HIGH);
     digitalWrite(DERD, HIGH);
     digitalWrite(DERA, LOW);
     digitalWrite(BIZQD, LOW);
     digitalWrite(BIZQA, HIGH);
     digitalWrite(BDERD, HIGH);
     digitalWrite(BDERA, LOW);
     myDFPlayer.play(randNumber);
     Serial.println(randNumber);
     Serial.println(F("Atras"));
     digitalWrite(LedA, HIGH);
     delay(1000);
     digitalWrite(LedA, LOW);
     digitalWrite(LedR, HIGH);

   }
   ```

   {{< youtube id="5Z0LixiRYLY" autoplay="true" color="white" yt_start="12" yt_end="24">}}

# Results

{{< image src="/img/r2d2100.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}

- Circuits

{{< image src="/img/R2D2CIR.png" alt="Circuit" position="center" style="border-radius: 8px;" >}}

- Arduino Code Complete
 ```
 #include "Arduino.h"
 #include "SoftwareSerial.h"
 #include "DFRobotDFPlayerMini.h"
 SoftwareSerial mySoftwareSerial(10, 11); // RX, TX
 DFRobotDFPlayerMini myDFPlayer;
 void printDetail(uint8_t type, int value);

 int IZQD = 2;
 int IZQA = 3;
 int BIZQD = A1;
 int BIZQA = A0;
 int DERD = 6;
 int DERA = 7;
 int BDERD = 12;
 int BDERA = 13;
 int CABD = 5;
 int CABA = 4;
 int LedR = 8;
 int LedA = 9;
 int APieCD = A3;
 int APieCA = A2;
 int BPieCD = A4;
 int BPieCA = A5;

 long randNumber;

 void setup() {

   pinMode(LedR, OUTPUT);
   pinMode(LedA, OUTPUT);
   pinMode(IZQD, OUTPUT);
   pinMode(IZQA, OUTPUT);
   pinMode(DERD, OUTPUT);
   pinMode(DERA, OUTPUT);
   pinMode(BIZQD, OUTPUT);
   pinMode(BIZQA, OUTPUT);
   pinMode(BDERD, OUTPUT);
   pinMode(BDERA, OUTPUT);
   pinMode(CABD, OUTPUT);
   pinMode(CABA, OUTPUT);
   pinMode(APieCD, OUTPUT);
   pinMode(APieCA, OUTPUT);
   pinMode(BPieCD, OUTPUT);
   pinMode(BPieCA, OUTPUT);
   mySoftwareSerial.begin(9600);
   Serial.begin(115200);

   randomSeed(analogRead(0));


   Serial.println();
   Serial.println(F("DFRobot DFPlayer Mini Demo"));
   Serial.println(F("Initializing DFPlayer ... (May take 3~5 seconds)"));
   Serial.println();
   Serial.println(F("=================================================================================================================================="));
   Serial.println(F(" [A] Adelante"));
   Serial.println(F(" [B] Atras"));
   Serial.println(F(" [C] Derecha"));
   Serial.println(F(" [D] Izquierda"));
   Serial.println(F(" [E] Cabeza Izq"));
   Serial.println(F(" [F] Cabeza Der"));
   Serial.println(F(" [G] Pie central Arriba"));
   Serial.println(F(" [H] Pie Central Abajo"));
   Serial.println(F(" [I] Stop"));
   Serial.println();
   Serial.println(F("================================================================================================================================="));

   if (!myDFPlayer.begin(mySoftwareSerial)) {
     Serial.println(F("Unable to begin:"));
     Serial.println(F("1.Please recheck the connection!"));
     Serial.println(F("2.Please insert the SD card!"));
     while (true) {
       delay(0);
     }
   }
   Serial.println(F("DFPlayer Mini online."));

   myDFPlayer.volume(10);  //Set volume value. From 0 to 30
 }

 void loop() {
   digitalWrite(LedR, HIGH);
   if (Serial.available() > 0)
   {
       digitalWrite(IZQD, LOW);
       digitalWrite(IZQA, LOW);
       digitalWrite(DERD, LOW);
       digitalWrite(DERA, LOW);
       digitalWrite(BIZQD, LOW);
       digitalWrite(BIZQA, LOW);
       digitalWrite(BDERD, LOW);
       digitalWrite(BDERA, LOW);
       digitalWrite(CABD, LOW);
       digitalWrite(CABA, LOW);
       digitalWrite(APieCD, LOW);
       digitalWrite(APieCA, LOW);
       digitalWrite(BPieCD, LOW);
       digitalWrite(BPieCA, LOW);      


     char letter = Serial.read();

     if (letter == 'C')
     {
       randNumber = random(1, 16);
       digitalWrite(LedA, LOW);
       digitalWrite(IZQD, LOW);
       digitalWrite(BIZQD, LOW);
       digitalWrite(IZQA, LOW);
       digitalWrite(BIZQA, LOW);
       digitalWrite(DERD, HIGH);
       digitalWrite(BDERD, HIGH);
       digitalWrite(DERA, LOW);
       digitalWrite(BDERA, LOW);
       myDFPlayer.play(randNumber);
       Serial.println(randNumber);
       Serial.println(F("Derecha"));
       digitalWrite(LedA, HIGH);
       delay(2500);
       digitalWrite(LedA, LOW);
       digitalWrite(LedR, HIGH);
     }
     else if (letter == 'D')
     {
       digitalWrite(LedR, LOW);
       randNumber = random(1, 16);
       digitalWrite(IZQD, LOW);
       digitalWrite(IZQA, HIGH);
       digitalWrite(DERD, LOW);
       digitalWrite(DERA, LOW);
       digitalWrite(BIZQD, LOW);
       digitalWrite(BIZQA, HIGH);
       digitalWrite(BDERD, LOW);
       digitalWrite(BDERA, LOW);
       myDFPlayer.play(randNumber);
       Serial.println(randNumber);
       Serial.println(F("Izquierda"));
       delay (2500);
             digitalWrite(LedA, LOW);
       digitalWrite(LedR, HIGH);

     }
  else if (letter == 'A')
     {
       digitalWrite(LedR, LOW);
       randNumber = random(1, 16);
       digitalWrite(IZQD, HIGH);
       digitalWrite(IZQA, LOW);
       digitalWrite(DERD, LOW);
       digitalWrite(DERA, HIGH);
       digitalWrite(BIZQD, HIGH);
       digitalWrite(BIZQA, LOW);
       digitalWrite(BDERD, LOW);
       digitalWrite(BDERA, HIGH);
       myDFPlayer.play(randNumber);
       Serial.println(randNumber);
       Serial.println(F("Adelante"));
       digitalWrite(LedA, HIGH);
       delay(1000);
       digitalWrite(LedA, LOW);
       digitalWrite(LedR, HIGH);

     }

      else if (letter == 'B')
     {
       digitalWrite(LedR, LOW);
       randNumber = random(1, 16);
       digitalWrite(IZQD, LOW);
       digitalWrite(IZQA, HIGH);
       digitalWrite(DERD, HIGH);
       digitalWrite(DERA, LOW);
       digitalWrite(BIZQD, LOW);
       digitalWrite(BIZQA, HIGH);
       digitalWrite(BDERD, HIGH);
       digitalWrite(BDERA, LOW);
       myDFPlayer.play(randNumber);
       Serial.println(randNumber);
       Serial.println(F("Atras"));
       digitalWrite(LedA, HIGH);
       delay(1000);
       digitalWrite(LedA, LOW);
       digitalWrite(LedR, HIGH);

     }
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
     if (letter == 'G')
     {
       randNumber = random(1, 16);
       digitalWrite(LedA, LOW);
       digitalWrite(APieCD, HIGH);
       digitalWrite(APieCA, LOW);
       digitalWrite(BPieCD, HIGH);
       digitalWrite(BPieCA, LOW);
       myDFPlayer.play(randNumber);
       Serial.println(randNumber);
       Serial.println(F("Pie Central Arriba"));
       digitalWrite(LedA, HIGH);
       delay(1500);
       digitalWrite(LedA, LOW);
       digitalWrite(LedR, HIGH);
       digitalWrite(APieCD, LOW);
       digitalWrite(APieCA, LOW);
       digitalWrite(BPieCD, LOW);
       digitalWrite(BPieCA, LOW);

     }
     else if (letter == 'H')
     {
       digitalWrite(LedR, LOW);
       randNumber = random(1, 16);
       digitalWrite(APieCD, LOW);
       digitalWrite(APieCA, HIGH);
       digitalWrite(BPieCD, LOW);
       digitalWrite(BPieCA, HIGH);
       myDFPlayer.play(randNumber);
       Serial.println(randNumber);
       Serial.println(F("Pie Central Abajo"));
       digitalWrite(LedA, HIGH);
       delay(300);
       digitalWrite(LedA, LOW);
       digitalWrite(LedR, HIGH);
       digitalWrite(APieCD, LOW);
       digitalWrite(APieCA, LOW);
       digitalWrite(BPieCD, LOW);
       digitalWrite(BPieCA, LOW);
     }
     else if (letter == 'I')
     {
       digitalWrite(LedR, LOW);
       randNumber = random(1, 16);
      digitalWrite(IZQD, LOW);
       digitalWrite(IZQA, LOW);
       digitalWrite(DERD, LOW);
       digitalWrite(DERA, LOW);
       myDFPlayer.play(randNumber);
       Serial.println(randNumber);
       Serial.println(F("Stop"));
     }
   }


   static unsigned long timer = millis();

   if (millis() - timer > 3000) {
     timer = millis();
   }
 }
 ```
