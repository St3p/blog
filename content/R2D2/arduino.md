---
title: "R2-D2 Arduino Code"
date: "2020-06-02"
author: "Stephanie Zepeda"
cover: "img/arduino.jpg"
description: " "
---

```

#include <SoftwareSerial.h>  

SoftwareSerial R2D2(10, 11);  
char DATA = '0'; //Variable for the option choosen by the user is going to save     
int IZQD = 22;   //left foot first motor A
int IZQA = 24;   //left foot first motor B
int BIZQD = 26;  //left foot second motor A
int BIZQA = 28;  //left foot second motor B
int DERD = 30;   //right foot first motor A
int DERA = 32;   //right foot first motor B
int BDERD = 34;  //right foot second motor A
int BDERA = 36;  //right foot second motor B
int CABD = 42;   //head motor A
int CABA = 44;   //head motor B
int CP = 38;     //shoulder motor A
int CPA = 40;    //shoulder motor B
int LedR = 14;   //Red led pin
int LedA = 15;   //Blue led pin
int APieCD = 46; //central feet first motor A
int APieCA = 48; //central feet first motor B
int BPieCD = 50; //central feet second motor A
int BPieCA = 52; //central feet second motor B

void setup(){
  R2D2.begin(9600);  
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
  pinMode(CPA, OUTPUT);
  pinMode(CP, OUTPUT);
  pinMode(CABA, OUTPUT);
  pinMode(APieCD, OUTPUT);
  pinMode(APieCA, OUTPUT);
  pinMode(BPieCD, OUTPUT);
  pinMode(BPieCA, OUTPUT);
}

void loop(){


if (R2D2.available())
  DATA = R2D2.read();                   //stores in DATA de received character.

  if( DATA == 'A' ) {                   //forward feet
      digitalWrite(LedR, LOW);  
      digitalWrite(IZQD, HIGH);
      digitalWrite(IZQA, LOW);      
      digitalWrite(DERD, HIGH);
      digitalWrite(DERA, LOW);
      digitalWrite(BIZQD, HIGH);
      digitalWrite(BIZQA, LOW);
      digitalWrite(BDERD, HIGH);
      digitalWrite(BDERA, LOW);
      R2D2.println("Adelante");
      digitalWrite(LedA, HIGH);
      delay(100);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(IZQD, LOW);
      digitalWrite(IZQA, LOW);
      digitalWrite(DERD, LOW);
      digitalWrite(DERA, LOW);
      digitalWrite(BIZQD, LOW);
      digitalWrite(BIZQA, LOW);
      digitalWrite(BDERD, LOW);
      digitalWrite(BDERA, LOW);
}

  if( DATA == 'B' )   {                 //back feet

      digitalWrite(LedR, LOW);
      digitalWrite(IZQD, LOW);
      digitalWrite(IZQA, HIGH);
      digitalWrite(DERD, LOW);
      digitalWrite(DERA, HIGH);      
      digitalWrite(BIZQD, LOW);
      digitalWrite(BIZQA, HIGH);
      digitalWrite(BDERD, LOW);
      digitalWrite(BDERA, HIGH);
      R2D2.println(F("Atras"));
      digitalWrite(LedA, HIGH);
      delay(100);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(IZQD, LOW);
      digitalWrite(IZQA, LOW);
      digitalWrite(DERD, LOW);
      digitalWrite(DERA, LOW);
      digitalWrite(BIZQD, LOW);
      digitalWrite(BIZQA, LOW);
      digitalWrite(BDERD, LOW);
      digitalWrite(BDERA, LOW);
}
if( DATA == 'C' )   {              //right feet
      digitalWrite(LedA, LOW);
      digitalWrite(IZQD, LOW);
      digitalWrite(BIZQD, LOW);
      digitalWrite(IZQA, LOW);
      digitalWrite(BIZQA, LOW);
      digitalWrite(DERD, HIGH);
      digitalWrite(BDERD, HIGH);
      digitalWrite(DERA, LOW);
      digitalWrite(BDERA, LOW);
      R2D2.println(F("Derecha"));
      digitalWrite(LedA, HIGH);
      delay(100);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(IZQD, LOW);
      digitalWrite(IZQA, LOW);
      digitalWrite(DERD, LOW);
      digitalWrite(DERA, LOW);
      digitalWrite(BIZQD, LOW);
      digitalWrite(BIZQA, LOW);
      digitalWrite(BDERD, LOW);
      digitalWrite(BDERA, LOW);
    }
if( DATA == 'D' )   {                   //feet left
      digitalWrite(LedR, LOW);
      digitalWrite(IZQD, LOW);
      digitalWrite(IZQA, HIGH);
      digitalWrite(DERD, LOW);
      digitalWrite(DERA, LOW);
      digitalWrite(BIZQD, LOW);
      digitalWrite(BIZQA, HIGH);
      digitalWrite(BDERD, LOW);
      digitalWrite(BDERA, LOW);
      R2D2.println(F("Izquierda"));
      delay (100);
            digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(IZQD, LOW);
      digitalWrite(IZQA, LOW);
      digitalWrite(DERD, LOW);
      digitalWrite(DERA, LOW);
      digitalWrite(BIZQD, LOW);
      digitalWrite(BIZQA, LOW);
      digitalWrite(BDERD, LOW);
      digitalWrite(BDERA, LOW);

    }

    if( DATA == 'E' )   {                //head left

   digitalWrite(LedR, LOW);

      digitalWrite(CABD, LOW);
      digitalWrite(CABA, HIGH);    
      R2D2.println(F("Cab Izq"));
      digitalWrite(LedA, HIGH);
      delay(100);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);

      digitalWrite(CABD, LOW);
      digitalWrite(CABA, LOW);
 }

    if( DATA == 'F' )   {           //head right
digitalWrite(LedR, LOW);

      digitalWrite(CABD, HIGH);
      digitalWrite(CABA, LOW);
      R2D2.println(F(" Cab Der"));
      digitalWrite(LedA, HIGH);
      delay(100);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(CABD, LOW);
      digitalWrite(CABA, LOW);
    }
    if( DATA == 'G' )   {            //Central feet up

      digitalWrite(LedA, LOW);
      digitalWrite(APieCD, HIGH);
      digitalWrite(APieCA, LOW);
      digitalWrite(BPieCD, HIGH);
      digitalWrite(BPieCA, LOW);
      R2D2.println(F("Pie Central Arriba"));
      digitalWrite(LedA, HIGH);
      delay(1000);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(APieCD, LOW);
      digitalWrite(APieCA, LOW);
      digitalWrite(BPieCD, LOW);
      digitalWrite(BPieCA, LOW);

    }

     if( DATA == 'H' )   {        //central feet down
 digitalWrite(LedR, LOW);

      digitalWrite(APieCD, LOW);
      digitalWrite(APieCA, HIGH);
      digitalWrite(BPieCD, LOW);
      digitalWrite(BPieCA, HIGH);
      R2D2.println(F("Pie Central Abajo"));
      digitalWrite(LedA, HIGH);
      delay(1000);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(APieCD, LOW);
      digitalWrite(APieCA, LOW);
      digitalWrite(BPieCD, LOW);
      digitalWrite(BPieCA, LOW);
    }
    if( DATA == 'I' )   {         //shoulder up
  digitalWrite(LedR, LOW);

      digitalWrite(CP, HIGH);
      digitalWrite(CPA, LOW);
      R2D2.println(F("HOMBRO ARRIBA"));
      digitalWrite(LedA, HIGH);
      delay(100);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(CP, LOW);
      digitalWrite(CPA, LOW);
    }
    if( DATA == 'J' )   {             //shoulder down

      digitalWrite(LedR, LOW);
      digitalWrite(CP, LOW);
      digitalWrite(CPA, HIGH);
      R2D2.println(F("HOMBRO ABAJO"));
      digitalWrite(LedA, HIGH);
      delay(100);
      digitalWrite(LedA, LOW);
      digitalWrite(LedR, HIGH);
      digitalWrite(CP, LOW);
      digitalWrite(CPA, LOW);
    }
    if (DATA == 'K')                 //stops all the system
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
      digitalWrite(CPA, LOW);
      digitalWrite(CPA, LOW);

  }
    if (DATA == 'Z')            //main menu
 {
  R2D2.println();
  R2D2.println();
  R2D2.println("==================================================================================================================================");
  R2D2.println(" [A] Forward");
  R2D2.println(" [B] backwards");
  R2D2.println(" [C] Right");
  R2D2.println(" [D] Left");
  R2D2.println(" [E] Head Left");
  R2D2.println(" [F] Head Right");
  R2D2.println(" [G] Central Feet Up");
  R2D2.println(" [H] Central Feet Down");
  R2D2.println(" [I] Shoulder Up");
  R2D2.println(" [J] Shoulder Down");
  R2D2.println(" [K] Stop");
  R2D2.println(" [Z] Menu");
  R2D2.println();
  R2D2.println("=================================================================================================================================");

 }
}
```
