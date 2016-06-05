# Family Projects for Smart Objects
  
This is the companion website for the book, "Family Projects for Smart Objects" by [John Keefe](http://johnkeefe.net), due out in Fall 2016 from Maker Media. This is where you'll find links to ingredients for every project in the book, along with the copy-able code you'll need for each project.
  
  
# Kits

To make these projects, you'll need a handful of hobby electronics, which are relatively cheap and readily available. You can buy the parts for each project individually, or you can get "starter kits" that have almost all of the parts you'll need for this book. Here are some of the kits, with (TODO) additional notes about chapters where you may need to get some extra parts:

- [Adafruit Experimentation Kit for Arduino ($$)](https://www.adafruit.com/products/170)
- [Adafruit Starter Pack for Arduino ($$)](https://www.adafruit.com/products/68)
- [Adafruit Budget Pack for Arduino ($)](https://www.adafruit.com/products/193)
- [Make: Getting Started with Arduino Kit, Special Edition ($$)](http://www.makershed.com/products/make-getting-started-kit-arduino-uno-r3)
- [Sparkfun Invetor's Kit for Arduino ($$$$)](https://www.sparkfun.com/products/13844)
- [SparkFun Inventor's Kit for Arduino - V3.2 ($$$)](https://www.sparkfun.com/products/13154)


# Chapters  

## You Only Have to Do This Once

This is the kickoff chapter in the book, and all about getting your Arduino up and running. And you only have to do it once.

### Ingredients

- 1 Arduino Uno (Revision 3)
- 1 Arduino USB cable

You can buy just these parts from Adafruit or Sparkfun using the buttons below.

[Buy from Adafruit >](http://www.adafruit.com/wishlists/403572) [Buy from Sparkfun >](https://www.sparkfun.com/wish_lists/127673)

These ingredients are also found in all of the Arduino starter kits [I've listed](#kits).

### Installation Links

The book outlines how to install Arduino software on Mac, Windows or Ubuntu computers, but Arduino also works on various flavors of Linux. Here are additional resources:

- [Getting Started with Arduino on Mac OS](https://www.arduino.cc/en/Guide/MacOSX)
- [Getting Started with Arduino on Windows](https://www.arduino.cc/en/Guide/Windows)
- [Installing Arduino on Ubuntu](http://playground.arduino.cc/Linux/Ubuntu)
- [Installing Arduino for Debian](http://playground.arduino.cc/Linux/Debian)
- [Installing Arduino on Fedora](http://playground.arduino.cc/Linux/Fedora)

## Hello Blinky World

Traditionally, when people begin learning something new about computers, 
their first project is to make the computer say, "hello world." Among 
blinky makers, our "hello world" is making an LED flash on and off. That's what happens in this chapter.

### Ingredients

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino Uno (Revision 3)
- 1 Ardunio USB cable 
- 1 LED

These ingredients are also found in all of the Arduino starter kits [I've listed](#kits).

### Code

The code for this project actually comes with the Arduino software. The easiest way to use it is to open your Arduino software and navigate to the "Blink" sketch, starting at the menu bar and chosing _File_ &#8594; _Examples_ &#8594; _01.Basics_ &#8594; _Blink_.

You can also copy it from here:

```arduino
/*
  Blink
  Turns on an LED on for one second, then off for one second, repeatedly.

  Most Arduinos have an on-board LED you can control. On the Uno and
  Leonardo, it is attached to digital pin 13. If you are unsure what
  pin the on-board LED is connected to on your Arduino model, check
  the documentation at http://www.arduino.cc

  This example code is in the public domain.

  modified 8 May 2014
  by Scott Fitzgerald
 */


// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin 13 as an output.
  pinMode(13, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(13, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);              // wait for a second
  digitalWrite(13, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);              // wait for a second
}
```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

## A Dark-Detecting Light

For this project, we make an LED flash fast and urgently when the room is 
dark, and slow and calm when the room is bright.

### Ingredients

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino Uno
- 1 Arduino USB Cable
- 1 Breadboard
- 1 LED
- 3 jumper wires
- 1 Photoresistor
- 1 10K-ohm (10K&#937;) resistor

Most of these ingredients are also found in the Arduino starter kits [I've listed](#kits).

### Code

The code we use for this project comes with the Arduino software, so it's easy to load up. Navigate to the "Blink" sketch by going to the menu bar and choosing _File_ &#8594; _Examples_ &#8594; _03.Analog_ &#8594; _AnalogInput_.

Here it is written out:

```arduino
/*
  Analog Input
 Demonstrates analog input by reading an analog sensor on analog pin 0 and
 turning on and off a light emitting diode(LED)  connected to digital pin 13.
 The amount of time the LED will be on and off depends on
 the value obtained by analogRead().

 The circuit:
 * Potentiometer attached to analog input 0
 * center pin of the potentiometer to the analog pin
 * one side pin (either one) to ground
 * the other side pin to +5V
 * LED anode (long leg) attached to digital output 13
 * LED cathode (short leg) attached to ground

 * Note: because most Arduinos have a built-in LED attached
 to pin 13 on the board, the LED is optional.


 Created by David Cuartielles
 modified 30 Aug 2011
 By Tom Igoe

 This example code is in the public domain.

 http://www.arduino.cc/en/Tutorial/AnalogInput

 */

int sensorPin = A0;    // select the input pin for the potentiometer
int ledPin = 13;      // select the pin for the LED
int sensorValue = 0;  // variable to store the value coming from the sensor

void setup() {
  // declare the ledPin as an OUTPUT:
  pinMode(ledPin, OUTPUT);
}

void loop() {
  // read the value from the sensor:
  sensorValue = analogRead(sensorPin);
  // turn the ledPin on
  digitalWrite(ledPin, HIGH);
  // stop the program for <sensorValue> milliseconds:
  delay(sensorValue);
  // turn the ledPin off:
  digitalWrite(ledPin, LOW);
  // stop the program for for <sensorValue> milliseconds:
  delay(sensorValue);
}
```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

## Night Light

Night lights are awesome and useful, and the best ones save power by 
only lighting up when it's dark in the room. That's what we make with this project.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino
- 1 Arduino USB cable 
- 1 Breadboard
- 1 photoresistor
- 1 LED (white, if you have one)
- 3 Jumper wires

*Optional Items*

- 2 [Extension jumper wires (male-to-female)](https://www.sparkfun.com/products/9140)
- 1 Hollow, translucent toy
- 1 Arduino power supply

Except for the Optional Items, these ingredients are also found in the Arduino starter kits [I've listed](#kits).

The optional power supply allows you to untether your Arduino from your computer -- and let it run on its own. Arduinos get their power either from the USB port or from the round "barrel" jack next to the Arduino's USB outlet. If you kit doesn't come with a separate power supply, you can buy [one that fits the barrel jack](https://www.adafruit.com/products/276) or [this nifty version](https://www.adafruit.com/products/501) that uses your Arduino's USB cable instead.

Here's a link to the optional [extension jumper wires on Sparkfun](https://www.sparkfun.com/products/9140).

### Code

Here's the sketch used for this project.

```arduino
/*
 
 Night Light
 Lights an LED when the room is dark.

 By John Keefe, January 2016
 http://keefe.cc/night-light

 Based on example code created by David Cuartielles
 modified 30 Aug 2011 by Tom Igoe
 http://www.arduino.cc/en/Tutorial/AnalogInput

 This code is in the public domain.
 
 */

int sensorPin = A0;   // select the input pin for the photoresistor
int ledPin = 13;      // select the pin for the LED
int sensorValue = 0;  // variable to store the value from the sensor
int darkPoint = 0;    // if the sensor value is less than this, the room is "dark"

// This code runs once when Arduino is turned on or reset
void setup() {
  
  // declare the ledPin as an OUTPUT:
  pinMode(ledPin, OUTPUT);

  // this is needed to use the Serial Monitor
  Serial.begin(9600);
  
}

// This code loops forever
void loop() {
  
  // read the value from the sensor:
  sensorValue = analogRead(sensorPin);
  
  // if the sensorValue is less than the darkPoint
  // power the LED:
  if (sensorValue < darkPoint) {
    digitalWrite(ledPin, HIGH);
  }

  // if the sensorValue is greater than or equal to the
  // darkPoint, don't power the LED:
  if (sensorValue >= darkPoint) {
    digitalWrite(ledPin, LOW);
  }

  // output the sensor value to the Serial Monitor
  Serial.println(sensorValue);

  // add a little delay to help read the numbers!
  delay(100); 
}
```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

## Ice, Ice Binkly

This project makes an LED react to cold water.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino Uno
- 1 Arduino USB cable 
- 1 Breadboard
- 1 Thermistor
- 1 10k-ohm (10k&#937;) resistor
- A glass of ice water

Almost all of the Arduino start-up kits [I've listed](#kits) include a thermistor. Sometimes they are at the ends of long, wiggly wires; other times they have stiff wires, like an LED. Either one will work here.

### Code

This project uses the example code that comes with the Arduino software. So with the Arduino software 
running, go to: _File_ &#8594; _Examples_ &#8594; _03.Analog_ &#8594; _AnalogInput_.

You can use the code below, too, which is slight modified for the "Taking it Futher" part of the chapter -- where we add the ability to watch the sensor readings with the Serial Monitor.

```arduino
/*
  Analog Input
 Demonstrates analog input by reading an analog sensor on analog pin 0 and
 turning on and off a light emitting diode(LED)  connected to digital pin 13.
 The amount of time the LED will be on and off depends on
 the value obtained by analogRead().

 The circuit:
 * Potentiometer attached to analog input 0
 * center pin of the potentiometer to the analog pin
 * one side pin (either one) to ground
 * the other side pin to +5V
 * LED anode (long leg) attached to digital output 13
 * LED cathode (short leg) attached to ground

 * Note: because most Arduinos have a built-in LED attached
 to pin 13 on the board, the LED is optional.


 Created by David Cuartielles
 modified 30 Aug 2011
 By Tom Igoe

 This example code is in the public domain.

 http://www.arduino.cc/en/Tutorial/AnalogInput

 Further Modified by John Keefe May 2016
 to add Serial Monitoring
 
 */

int sensorPin = A0;    // select the input pin for the potentiometer
int ledPin = 13;      // select the pin for the LED
int sensorValue = 0;  // variable to store the value coming from the sensor

void setup() {
  // declare the ledPin as an OUTPUT:
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);  // < - - Added this line
}

void loop() {
  // read the value from the sensor:
  sensorValue = analogRead(sensorPin);
  // turn the ledPin on
  digitalWrite(ledPin, HIGH);
  // stop the program for <sensorValue> milliseconds:
  delay(sensorValue);
  // turn the ledPin off:
  digitalWrite(ledPin, LOW);
  Serial.println(sensorValue); // < - - New line is here
  // stop the program for for <sensorValue> milliseconds:
  delay(sensorValue);  
}
```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

## A Gentle Touch

When you tap a "button" on a smartphone's screen you obviously aren't 
pushing a button. The phone is detecting your finger on the glass. The 
same principles working on that screen to sense a finger can be used to 
make a touch-sensitive "button" with no moving parts. That's what we do in this project.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino Uno
- 1 Ardunio USB cable 
- 1 LED
- 3 jumper wires
- 1 resistor, with the highest resistance you have
- 1 square of aluminum foil, about the size of a cracker
- A piece of tape

All of the items in this project, besides the aluminum foil and tape, 
should be available in any of the Arduino starter kits [I've listed](#kits).

### Code

Here's the code used for this project:

```arduino
// Based on an example sketch originally written by Paul Badger 
// and now maintained by Paul Stoffregen
// https://github.com/PaulStoffregen/CapacitiveSensor
// Modified by John Keefe May 2016

#include <CapacitiveSensor.h>

CapacitiveSensor   cs_4_6 = CapacitiveSensor(4,6);   

int LED = 13;
long sensor_reading;

void setup()                    
{
   pinMode(LED, OUTPUT);
   Serial.begin(9600);
}

void loop()                    
{
    sensor_reading =  cs_4_6.capacitiveSensor(30);
    
    Serial.println(sensor_reading);
    
    if (sensor_reading > 100) {
      digitalWrite(LED, HIGH);
    } else {
      digitalWrite(LED, LOW);
    }

    delay(10);                             
}
```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

### Useful Links

In this chapter, I mention other fabrics you can use instead of foil and the ability to sew Arduinos right onto fabric -- so you could actually sew touch-sensitive "buttons" (and LEDs and lots of other things) into clothing. Here are some useful links to get you exploring:

- [Sewable -- and conductive! -- copper taffeta fabric](http://www.lessemf.com/fabric4.html#1212)
- [All about sewable Lilypad Arduinos & projects](http://lilypadarduino.org/)
- [Lilypad Arduinos and other parts at Sparkfun](https://www.sparkfun.com/categories/135?page=all)



## Someone Moved My Stuff!

This project uses a force, or pressure, sensor to detect when someone lifts an object from its place.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino
- 1 Ardunio USB cable 
- 1 Breadboard
- 5 jumper wires
- 1 [pressure sensor](https://www.sparkfun.com/products/9673)
- 1 [little buzzer](https://www.adafruit.com/products/160)
- 1 10k-ohm (10k&#937;) resistor
- a small object you cherish :-)

_Optional part_

- 1 [Arduino power supply](https://www.adafruit.com/products/276)

Most of these ingredients are also found in the Arduino starter kits [I've listed](#kits). Double check to make sure the kit you select has a pressure sensor. If you need one [here's a little version at Sparkfun](https://www.sparkfun.com/products/9673) and [here's a bigger one at Adafruit](https://www.adafruit.com/products/1075).

You'll also need a little buzzer, often called a piezo buzzer. If your kit doesn't have one, [you can buy one at Adafruit](https://www.adafruit.com/products/160).

The optional power supply allows you to untether your Arduino from your computer and keep it running. Arduinos get their power either from the USB port or from the round "barrel" jack next to the Arduino's USB outlet. If you kit doesn't come with a separate power supply, you can buy [one that fits the barrel jack](https://www.adafruit.com/products/276) or [this nifty version](https://www.adafruit.com/products/501) that uses your Arduino's USB cable instead.

### Code

Here's the code for this chapter.

```arduino
/*
 Analog Input
 http://www.arduino.cc/en/Tutorial/AnalogInput

 Created by David Cuartielles
 modified 30 Aug 2011 by Tom Igoe
 modified March 2016 by John Keefe

 This example code is in the public domain.

 */

int sensorPin = A0;   // set the input pin for the sensor
int buzzerPin = 13;   // set the pin for the buzzer
int sensorValue = 0;  // variable to store the sensor value
int movedValue = 100; // threshold value to trigger the buzzer

void setup() {
  // declare the buzzerPin as an OUTPUT:
  pinMode(buzzerPin, OUTPUT);

  // start up the Serial Monitor
  Serial.begin(9600);
}

void loop() {
  // read the value from the sensor:
  sensorValue = analogRead(sensorPin);
  
  // if the sensorValue is less than the movedValue,
  // turn the buzzer on (with HIGH power). 
  // Otherwise turn it off (with LOW power).
  if (sensorValue < movedValue) {
    digitalWrite(buzzerPin, HIGH);
  } else {
    digitalWrite(buzzerPin, LOW);
  }

  // print the sensor value to the Serial Monitor for calibration 
  Serial.println(sensorValue);
}
```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

### Useful Links

In the "Taking it Further" section of this chapter, I mention a cool material called Velostat that also has pressure-sensitive qualities. Lean more about [using (and buying) Velostat at Adafruit](https://www.adafruit.com/product/1361).

## Electric Candle

In this chapter, we use a "hot-wire" wind detector to make an electric candle you can actually blow out. 

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino Uno
- 1 Arduino USB cable 
- 1 Breadboard
- 1 push button 
- 1 LED
- 10 jumper wires 

_Special items_

- 1 [Modern Device Wind Sensor](https://moderndevice.com/product/wind-sensor/)
- [Soldering iron](https://www.sparkfun.com/products/9507)
- [Solder](https://www.sparkfun.com/products/9325)

_Optional Items_

- 1 Arduino power supply

Almost all of the ingredients you'll need come in Arduino starter kits [I've listed](#kits), with a notable exception &#8212; the [wind sensor from Modern Device](https://moderndevice.com/product/wind-sensor/). 

Assembling the wind sensor requires a small amount of soldering -- which requires a soldering iron and solder. If you don't have these at home, you can get them at a local hardware or hobby store, and of course from an online seller. Here's the Sparkfun links to a [soldering iron](https://www.sparkfun.com/products/9507) (they have many) and also some [lead-free solder](https://www.sparkfun.com/products/9325). 

The optional power supply allows you to untether your Arduino from your computer and keep it running. Arduinos get their power either from the USB port or from the round "barrel" jack next to the Arduino's USB outlet. If you kit doesn't come with a separate power supply, you can buy [one that fits the barrel jack](https://www.adafruit.com/products/276) or [this nifty version](https://www.adafruit.com/products/501) that uses your Arduino's USB cable instead.

### Code

```arduino
/* Modern Device Wind Sensor Sketch for Rev C Wind Sensor 
 * 
 *  
 Hardware Setup: 
 Wind Sensor Signals    Arduino
 GND                    GND
 +V                     5V
 RV                     A1    // modify the definitions below to use other pins
 TMP                    A0    // modify the definitions below to use other pins
 
 Paul Badger 2014
 Original at https://github.com/moderndevice/Wind_Sensor
 Licensed for use on official Modern Device hardware
 
 Revised by John Keefe 2016
 
 Hardware setup:
 Wind Sensor is powered from a regulated five volt source.
 RV pin and TMP pin are connected to analog inputs.
 
 */

#define analogPinForRV    1   // change to pins you the analog pins are using
#define analogPinForTMP   0

const float zeroWindAdjustment =  .2; 
int TMP_Therm_ADunits;  
float RV_Wind_ADunits;   
float RV_Wind_Volts;
unsigned long lastMillis;
int TempCtimes100;
float zeroWind_ADunits;
float zeroWind_volts;
float WindSpeed_MPH;

int led = 13;              // candle LED 
const int buttonPin = 2;   // the pushbutton pin
int buttonState = 0;       // variable for reading the pushbutton status

void setup() {
  
  // initialize the digital pin as an output.
  pinMode(led, OUTPUT); 
  
  // initialize the pushbutton pin as an input:
  pinMode(buttonPin, INPUT);    
  
  // turn LED on
  digitalWrite(led, HIGH);

}

void loop() {
  
  buttonState = digitalRead(buttonPin);

  if (millis() - lastMillis > 200){   
    
    TMP_Therm_ADunits = analogRead(analogPinForTMP);
    RV_Wind_ADunits = analogRead(analogPinForRV);
    RV_Wind_Volts = (RV_Wind_ADunits *  0.0048828125);

    // these are all derived from regressions from raw data as such they depend on a lot of experimental factors
    // such as accuracy of temp sensors, and voltage at the actual wind sensor, (wire losses) which were unaccouted for.
    TempCtimes100 = (0.005 *((float)TMP_Therm_ADunits * (float)TMP_Therm_ADunits)) - (16.862 * (float)TMP_Therm_ADunits) + 9075.4;  

    zeroWind_ADunits = -0.0006*((float)TMP_Therm_ADunits * (float)TMP_Therm_ADunits) + 1.0727 * (float)TMP_Therm_ADunits + 47.172;  //  13.0C  553  482.39

    zeroWind_volts = (zeroWind_ADunits * 0.0048828125) - zeroWindAdjustment;  
    
   WindSpeed_MPH =  pow(((RV_Wind_Volts - zeroWind_volts) /.2300) , 2.7265);   
    
    if (WindSpeed_MPH > 6) {
      douseCandle();
    }
    
    if (buttonState == HIGH) {
      lightCandle();
    }
    
    lastMillis = millis();    
  } 

}

void douseCandle() {

  // turn LED off
  digitalWrite(led, LOW);
  
}

void lightCandle() {

  digitalWrite(led, HIGH);
  
}
```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.


### Useful Links

Soldering is a great skill to have, and it's super easy to learn. Here's an excellent guide from Adafruit:

- [Adafruit Guide to Excellent Soldering](https://learn.adafruit.com/adafruit-guide-excellent-soldering?view=all)


## Invisible Ruler

Maybe you know how bats "see" with sound: Emitting high-pitched clicks 
and listening for how those sounds bounce off of things. It's called 
"echolocation" because the bats literally locate things using echoes. In this chapter, we make an Arduino do the same thing!

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino Uno
- 1 Arduino USB cable 
- 1 Breadboard
- 3 Jumper cables

_Special parts_

- 1 [Parallax Ping sensor](http://www.amazon.com/Parallax-Ultrasonic-Range-Sensor-28015/dp/B004SRTM0K)

_Optional parts_

- 1 LED

Almost all of the ingredients you'll need come in Arduino starter kits [I've listed](#kits), with a notable exception &#8212; the [Parallax Ping sensor](http://www.amazon.com/Parallax-Ultrasonic-Range-Sensor-28015/dp/B004SRTM0K), which you'll need to buy separately. These are common enough that you can sometimes find them in local hobby or electronics stores, too.

### Code

Here's the sketch used in this chapter:

```arduino
/* Ping))) Sensor

   http://www.arduino.cc/en/Tutorial/Ping
   
   created 3 Nov 2008
   by David A. Mellis
   modified 30 Aug 2011
   by Tom Igoe
 
   This example code is in the public domain.

 */

const int pingPin = 7;

void setup() {
  // initialize serial communication:
  Serial.begin(9600);
}

void loop()
{
  // establish variables for duration of the ping, 
  // and the distance result in inches and centimeters:
  long duration, inches, cm;

  // The PING))) is triggered by a HIGH pulse of 2 or more microseconds.
  // Give a short LOW pulse beforehand to ensure a clean HIGH pulse:
  pinMode(pingPin, OUTPUT);
  digitalWrite(pingPin, LOW);
  delayMicroseconds(2);
  digitalWrite(pingPin, HIGH);
  delayMicroseconds(5);
  digitalWrite(pingPin, LOW);

  // The same pin is used to read the signal from the PING))): a HIGH
  // pulse whose duration is the time (in microseconds) from the sending
  // of the ping to the reception of its echo off of an object.
  pinMode(pingPin, INPUT);
  duration = pulseIn(pingPin, HIGH);

  // convert the time into a distance
  inches = microsecondsToInches(duration);
  cm = microsecondsToCentimeters(duration);
  
  Serial.print(inches);
  Serial.print("in, ");
  Serial.print(cm);
  Serial.print("cm");
  Serial.println();
  
  delay(100);
}

long microsecondsToInches(long microseconds)
{
  // According to Parallax's datasheet for the PING))), there are
  // 73.746 microseconds per inch (i.e. sound travels at 1130 feet per
  // second).  This gives the distance travelled by the ping, outbound
  // and return, so we divide by 2 to get the distance of the obstacle.
  // See: http://www.parallax.com/dl/docs/prod/acc/28015-PING-v1.3.pdf
  return microseconds / 74 / 2;
}

long microsecondsToCentimeters(long microseconds)
{
  // The speed of sound is 340 m/s or 29 microseconds per centimeter.
  // The ping travels out and back, so to find the distance of the
  // object we take half of the distance travelled.
  return microseconds / 29 / 2;
}
```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.


## Get Your Arduino Online

In this chapter, we use an inexpensive wifi board to get an Arduino onto the internet. This project forms the foundation for the chapters in the rest of the book.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino Uno
- 1 Ardunio USB cable 

_Special items_

- 1 [Sparkfun Wifi Shield (ESP8266)](https://www.sparkfun.com/products/13287)
- 1 set of [Arduino R3 Stackable Headers](https://www.sparkfun.com/products/11417)
- [Soldering iron](https://www.sparkfun.com/products/9507)
- [Solder](https://www.sparkfun.com/products/9325)

_Optional items_

- 1 Breadboard
- 1 set of [Break-Away Headers](https://www.sparkfun.com/products/116)

The key part here is the [Sparkfun Wifi Shield (ESP8266)](https://www.sparkfun.com/products/13287), and also the [Stackable Headers](https://www.sparkfun.com/products/11417) needed to connect the wifi board to an Arduino.

The optional [Break-Away Headers](https://www.sparkfun.com/products/116) and breadboard really help to hold your wifi board in place while soldering. 

Soldering the stackable headers to the wif board requires a soldering iron and solder. If you don't have these, you can get them at a local hardware or hobby store, and of course from an online seller. Here's the Sparkfun links to a [soldering iron](https://www.sparkfun.com/products/9507) (they have many) and also some [lead-free solder](https://www.sparkfun.com/products/9325). 


### Code

To use the wifi board with the Arduino, we use a libary from Sparkfun, which is [available as a zip file](http://bit.ly/sparkfun-wifi). To add the library to your Arudino software ...

- Download the "wifi" library by [clicking this link](http://bit.ly/sparkfun-wifi).
- That should download a compressed file with a ridiculously long name called `SparkFun_ESP8266_AT_Arduino_Library-master.zip`. Don't unzip it!
- Start your Arduino software (if it's not running already).
- From the menu bar, select _Sketch_ &#8594; _Include Library_ &#8594; _Add .ZIP Library ..._
- Navigate to the place your browser saved `SparkFun_ESP8266_AT_Arduino_Library-master.zip` (it's very likely in your "Downloads" folder). 
- Select `SparkFun_ESP8266_AT_Arduino_Library-master.zip` and click the "Choose" button.
- Quit your Arduino software and restart it.

The library includes example code we need to get up and running. From the Arduino software menu bar it's at _File_ &#8594; _Examples_ &#8594; _SparkFun ESP8266 AT Library_ &#8594; _ESP8266_Sheild_Demo_. 

I've reproduced it here for reference: 

```arduino
/************************************************************
ESP8266_Shield_Demo.h
SparkFun ESP8266 AT library - Demo
Jim Lindblom @ SparkFun Electronics
Original Creation Date: July 16, 2015
https://github.com/sparkfun/SparkFun_ESP8266_AT_Arduino_Library

This example demonstrates the basics of the SparkFun ESP8266
AT library. It will show you how to connect to a WiFi network,
get an IP address, connect over TCP to a server (as a client),
and set up a TCP server of our own.

Development environment specifics:
  IDE: Arduino 1.6.5
  Hardware Platform: Arduino Uno
  ESP8266 WiFi Shield Version: 1.0

This code is released under the MIT license.

Distributed as-is; no warranty is given.
************************************************************/

//////////////////////
// Library Includes //
//////////////////////
// SoftwareSerial is required (even you do not intend on
// using it).
#include <SoftwareSerial.h> 
#include <SparkFunESP8266WiFi.h>

//////////////////////////////
// WiFi Network Definitions //
//////////////////////////////
// Replace these two character strings with the name and
// password of your WiFi network.
const char mySSID[] = "yourSSIDhere";
const char myPSK[] = "yourPWDhere";

//////////////////////////////
// ESP8266Server definition //
//////////////////////////////
// server object used towards the end of the demo.
// (This is only global because it is called in both setup()
// and loop()).
ESP8266Server server = ESP8266Server(80);

//////////////////
// HTTP Strings //
//////////////////
const char destServer[] = "example.com";
const String htmlHeader = "HTTP/1.1 200 OK\r\n"
                          "Content-Type: text/html\r\n"
                          "Connection: close\r\n\r\n"
                          "<!DOCTYPE HTML>\r\n"
                          "<html>\r\n";

const String httpRequest = "GET / HTTP/1.1\n"
                           "Host: example.com\n"
                           "Connection: close\n\n";

// All functions called from setup() are defined below the
// loop() function. They modularized to make it easier to
// copy/paste into sketches of your own.
void setup() 
{
  // Serial Monitor is used to control the demo and view
  // debug information.
  Serial.begin(9600);
  serialTrigger(F("Press any key to begin."));

  // initializeESP8266() verifies communication with the WiFi
  // shield, and sets it up.
  initializeESP8266();

  // connectESP8266() connects to the defined WiFi network.
  connectESP8266();

  // displayConnectInfo prints the local IP
  // and the network it is connected to.
  displayConnectInfo();

  serialTrigger(F("Press any key to connect client."));
  clientDemo();
  
  serialTrigger(F("Press any key to test server."));
  serverSetup();
}

void loop() 
{
  serverDemo();
}

void initializeESP8266()
{
  // esp8266.begin() verifies that the ESP8266 is operational
  // and sets it up for the rest of the sketch.
  // It returns either true or false -- indicating whether
  // communication was successul or not.
  // true
  int test = esp8266.begin();
  if (test != true)
  {
    Serial.println(F("Error talking to ESP8266."));
    errorLoop(test);
  }
  Serial.println(F("ESP8266 Shield Present"));
}

void connectESP8266()
{
  // The ESP8266 can be set to one of three modes:
  //  1 - ESP8266_MODE_STA - Station only
  //  2 - ESP8266_MODE_AP - Access point only
  //  3 - ESP8266_MODE_STAAP - Station/AP combo
  // Use esp8266.getMode() to check which mode it is in:
  int retVal = esp8266.getMode();
  if (retVal != ESP8266_MODE_STA)
  { // If it is not in station mode.
    // Use esp8266.setMode([mode]) to set it to a specified
    // mode.
    retVal = esp8266.setMode(ESP8266_MODE_STA);
    if (retVal < 0)
    {
      Serial.println(F("Error setting mode."));
      errorLoop(retVal);
    }
  }
  Serial.println(F("Mode set to station"));

  // esp8266.status() indicates the ESP8266 WiFi connect
  // status.
  // A return value of 1 indicates the device is already
  // connected. 0 indicates disconnected. (Negative values
  // equate to communication errors.)
  retVal = esp8266.status();
  if (retVal <= 0)
  {
    Serial.print(F("Connecting to "));
    Serial.println(mySSID);
    // esp8266.connect([ssid], [psk]) connects the ESP8266
    // to a network.
    // On success the connect function returns a value >0
    // On fail, the function will either return:
    //  -1: TIMEOUT - The library has a set 30s timeout
    //  -3: FAIL - Could not connect to network.
    retVal = esp8266.connect(mySSID, myPSK);
    if (retVal < 0)
    {
      Serial.println(F("Error connecting"));
      errorLoop(retVal);
    }
  }
}

void displayConnectInfo()
{
  char connectedSSID[24];
  memset(connectedSSID, 0, 24);
  // esp8266.getAP() can be used to check which AP the
  // ESP8266 is connected to. It returns an error code.
  // The connected AP is returned by reference as a parameter.
  int retVal = esp8266.getAP(connectedSSID);
  if (retVal > 0)
  {
    Serial.print(F("Connected to: "));
    Serial.println(connectedSSID);
  }

  // esp8266.localIP returns an IPAddress variable with the
  // ESP8266 current local IP address.
  IPAddress myIP = esp8266.localIP();
  Serial.print(F("My IP: ")); Serial.println(myIP);
}

void clientDemo()
{
  // To use the ESP8266 as a TCP client, use the 
  // ESP8266Client class. First, create an object:
  ESP8266Client client;

  // ESP8266Client connect([server], [port]) is used to 
  // connect to a server (const char * or IPAddress) on
  // a specified port.
  // Returns: 1 on success, 2 on already connected,
  // negative on fail (-1=TIMEOUT, -3=FAIL).
  int retVal = client.connect(destServer, 80);
  if (retVal <= 0)
  {
    Serial.println(F("Failed to connect to server."));
    return;
  }

  // print and write can be used to send data to a connected
  // client connection.
  client.print(httpRequest);

  // available() will return the number of characters
  // currently in the receive buffer.
  while (client.available())
    Serial.write(client.read()); // read() gets the FIFO char
  
  // connected() is a boolean return value - 1 if the 
  // connection is active, 0 if it is closed.
  if (client.connected())
    client.stop(); // stop() closes a TCP connection.
}

void serverSetup()
{
  // begin initializes a ESP8266Server object. It will
  // start a server on the port specified in the object's
  // constructor (in global area)
  server.begin();
  Serial.print(F("Server started! Go to "));
  Serial.println(esp8266.localIP());
  Serial.println();
}

void serverDemo()
{
  // available() is an ESP8266Server function which will
  // return an ESP8266Client object for printing and reading.
  // available() has one parameter -- a timeout value. This
  // is the number of milliseconds the function waits,
  // checking for a connection.
  ESP8266Client client = server.available(500);
  
  if (client) 
  {
    Serial.println(F("Client Connected!"));
    // an http request ends with a blank line
    boolean currentLineIsBlank = true;
    while (client.connected()) 
    {
      if (client.available()) 
      {
        char c = client.read();
        // if you've gotten to the end of the line (received a newline
        // character) and the line is blank, the http request has ended,
        // so you can send a reply
        if (c == '\n' && currentLineIsBlank) 
        {
          Serial.println(F("Sending HTML page"));
          // send a standard http response header:
          client.print(htmlHeader);
          String htmlBody;
          // output the value of each analog input pin
          for (int a = 0; a < 6; a++)
          {
            htmlBody += "A";
            htmlBody += String(a);
            htmlBody += ": ";
            htmlBody += String(analogRead(a));
            htmlBody += "<br>\n";
          }
          htmlBody += "</html>\n";
          client.print(htmlBody);
          break;
        }
        if (c == '\n') 
        {
          // you are starting a new line
          currentLineIsBlank = true;
        }
        else if (c != '\r') 
        {
          // you've gotten a character on the current line
          currentLineIsBlank = false;
        }
      }
    }
    // give the web browser time to receive the data
    delay(1);
   
    // close the connection:
    client.stop();
    Serial.println(F("Client disconnected"));
  }
  
}

// errorLoop prints an error code, then loops forever.
void errorLoop(int error)
{
  Serial.print(F("Error: ")); Serial.println(error);
  Serial.println(F("Looping forever."));
  for (;;)
    ;
}

// serialTrigger prints a message, then waits for something
// to come in from the serial port.
void serialTrigger(String message)
{
  Serial.println();
  Serial.println(message);
  Serial.println();
  while (!Serial.available())
    ;
  while (Serial.available())
    Serial.read();
}
```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

### Useful Links

Soldering is a great skill to have, and it's super easy to learn. Here's an excellent guide from Adafruit:

- [Adafruit Guide to Excellent Soldering](https://learn.adafruit.com/adafruit-guide-excellent-soldering?view=all)


## Sense the Internet

There's a ton of information on the Internet &#8212; and some of it is even useful! Now that we got an Arduino on the 'net, this project will use it to get some good data: weather conditions for the place you are now.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino
- 1 Ardunio USB cable 
- A home wifi network and the password for it
- A web browser

_Special items_

- The assembled [Sparkfun Wifi Shield (ESP8266)](https://www.sparkfun.com/products/13287) from the [previous chapter](#chapters-get-your-arduino-online). 

This project uses an assembled [Sparkfun Wifi Shield](https://www.sparkfun.com/products/13287). Details on its assembly, with [Arduino R3 Stackable Headers](https://www.sparkfun.com/products/11417), are on the product page and in the [previous chapter](#chapters-get-your-arduino-online).

### Code

The sketch for this project is here:

```arduino
/************************************************************
ESP8266_Shield_Demo.h
SparkFun ESP8266 AT library - Demo
Jim Lindblom @ SparkFun Electronics
Original Creation Date: July 16, 2015
https://github.com/sparkfun/SparkFun_ESP8266_AT_Arduino_Library

This example demonstrates the basics of the SparkFun ESP8266
AT library. It'll show you how to connect to a WiFi network,
get an IP address, connect over TCP to a server (as a client),
and set up a TCP server of our own.

Development environment specifics:
  IDE: Arduino 1.6.5
  Hardware Platform: Arduino Uno
  ESP8266 WiFi Shield Version: 1.0

This code is released under the MIT license.

Distributed as-is; no warranty is given.

Modified for use with OpenWeatherMap
by John Keefe, May 2016
************************************************************/

//////////////////////
// Library Includes //
//////////////////////
// SoftwareSerial is required (even you don't intend on
// using it).
#include <SoftwareSerial.h> 
#include <SparkFunESP8266WiFi.h>

//////////////////////////////
// WiFi Network Definitions //
//////////////////////////////
const char mySSID[] = "YourWifiNetworkNameGoesHere";
const char myPSK[] = "YourWifiPasswordGoesHere";

///////////////////////
// Weather Variables //
///////////////////////
const String apikey = "YourAPIKeyGoesHere";
const String latitude = "YourLatitudeGoesHere";
const String longitude = "YourLongitudeGoesHere";


//////////////////
// HTTP Strings //
//////////////////
const char destServer[] = "api.openweathermap.org";
String httpRequest = "GET /data/2.5/weather?lat=" + latitude + 
                           "&lon=" + longitude + "&APPID=" + apikey + " HTTP/1.1\n" +
                           "Host: api.openweathermap.org\n" +
                           "Connection: close\n\n";
   
// All functions called from setup() are defined below the
// loop() function. They modularized to make it easier to
// copy/paste into sketches of your own.
void setup() 
{
  // Serial Monitor is used to control the demo and view
  // debug information.
  Serial.begin(9600);
  serialTrigger(F("Press the Enter key to begin."));

  // initializeESP8266() verifies communication with the WiFi
  // shield, and sets it up.
  initializeESP8266();

  // connectESP8266() connects to the defined WiFi network.
  connectESP8266();

  // displayConnectInfo prints the Shield's local IP
  // and the network it's connected to.
  displayConnectInfo();

  clientDemo();
  
}

void loop() 
{
  // nothing here
}

void initializeESP8266()
{
  // esp8266.begin() verifies that the ESP8266 is operational
  // and sets it up for the rest of the sketch.
  // It returns either true or false -- indicating whether
  // communication was successul or not.
  // true
  int test = esp8266.begin();
  if (test != true)
  {
    Serial.println(F("Error talking to ESP8266."));
    errorLoop(test);
  }
  Serial.println(F("ESP8266 Shield Present"));
}

void connectESP8266()
{
  // The ESP8266 can be set to one of three modes:
  //  1 - ESP8266_MODE_STA - Station only
  //  2 - ESP8266_MODE_AP - Access point only
  //  3 - ESP8266_MODE_STAAP - Station/AP combo
  // Use esp8266.getMode() to check which mode it's in:
  int retVal = esp8266.getMode();
  if (retVal != ESP8266_MODE_STA)
  { // If it's not in station mode.
    // Use esp8266.setMode([mode]) to set it to a specified
    // mode.
    retVal = esp8266.setMode(ESP8266_MODE_STA);
    if (retVal < 0)
    {
      Serial.println(F("Error setting mode."));
      errorLoop(retVal);
    }
  }
  Serial.println(F("Mode set to station"));

  // esp8266.status() indicates the ESP8266's WiFi connect
  // status.
  // A return value of 1 indicates the device is already
  // connected. 0 indicates disconnected. (Negative values
  // equate to communication errors.)
  retVal = esp8266.status();
  if (retVal <= 0)
  {
    Serial.print(F("Connecting to "));
    Serial.println(mySSID);
    // esp8266.connect([ssid], [psk]) connects the ESP8266
    // to a network.
    // On success the connect function returns a value >0
    // On fail, the function will either return:
    //  -1: TIMEOUT - The library has a set 30s timeout
    //  -3: FAIL - Couldn't connect to network.
    retVal = esp8266.connect(mySSID, myPSK);
    if (retVal < 0)
    {
      Serial.println(F("Error connecting"));
      errorLoop(retVal);
    }
  }
}

void displayConnectInfo()
{
  char connectedSSID[24];
  memset(connectedSSID, 0, 24);
  // esp8266.getAP() can be used to check which AP the
  // ESP8266 is connected to. It returns an error code.
  // The connected AP is returned by reference as a parameter.
  int retVal = esp8266.getAP(connectedSSID);
  if (retVal > 0)
  {
    Serial.print(F("Connected to: "));
    Serial.println(connectedSSID);
  }

  // esp8266.localIP returns an IPAddress variable with the
  // ESP8266's current local IP address.
  IPAddress myIP = esp8266.localIP();
  Serial.print(F("My IP: ")); Serial.println(myIP);
}

void clientDemo()
{
  // To use the ESP8266 as a TCP client, use the 
  // ESP8266Client class. First, create an object:
  ESP8266Client client;

  // ESP8266Client connect([server], [port]) is used to 
  // connect to a server (const char * or IPAddress) on
  // a specified port.
  // Returns: 1 on success, 2 on already connected,
  // negative on fail (-1=TIMEOUT, -3=FAIL).
  int retVal = client.connect(destServer, 80);
  if (retVal <= 0)
  {
    Serial.println(F("Failed to connect to server."));
    return;
  }

  // print and write can be used to send data to a connected
  // client connection.
  client.print(httpRequest);

  // available() will return the number of characters
  // currently in the receive buffer.
  while (client.available())
    Serial.write(client.read()); // read() gets the FIFO char
  
  // connected() is a boolean return value - 1 if the 
  // connection is active, 0 if it's closed.
  if (client.connected())
    client.stop(); // stop() closes a TCP connection.
}


// errorLoop prints an error code, then loops forever.
void errorLoop(int error)
{
  Serial.print(F("Error: ")); Serial.println(error);
  Serial.println(F("Looping forever."));
  for (;;)
    ;
}

// serialTrigger prints a message, then waits for something
// to come in from the serial port.
void serialTrigger(String message)
{
  Serial.println();
  Serial.println(message);
  Serial.println();
  while (!Serial.available())
    ;
  while (Serial.available())
    Serial.read();
}
```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

### Useful links

Here are some of the links mentioned in this chapter, for easy reference:

- [OpenWeatherMap](http://openweathermap.org/) -- where we get the weather data.
- [Get an OpenWeatherMap Key](http://openweathermap.org/appid) -- the place to get your free API key.
- [LatLong.net](http://http://www.latlong.net/) -- to get the latitude and longitude where you are.
- [OpenWeatherMap's Current Conditions API](http://openweathermap.org/current) -- more details on the data we're getting.


## Do I Need an Umbrella Today?

The answer could be as simple as looking at your Arduino. In this chapter, we'll go beyond asking about the current weather &#8212; we'll get an Arduino to ask for a weather _forecast_ and use that information to determine whether you'll need an umbrella.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino
- 1 Ardunio USB cable 
- 1 LED
- A home wifi network and the password for it

_Special items_

- The assembled [Sparkfun Wifi Shield (ESP8266)](https://www.sparkfun.com/products/13287) from the [previous chapter](#chapters-get-your-arduino-online). 

This project uses an assembled [Sparkfun Wifi Shield](https://www.sparkfun.com/products/13287). Details on its assembly, with [Arduino R3 Stackable Headers](https://www.sparkfun.com/products/11417), are on the product page and in the [previous chapter](#chapters-get-your-arduino-online).

### Code

```arduino

// Code goes here

```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.


## Send Email with a Button

If making a computer say "Hello, world" is the first step of programming, and making an LED blink is the "Hello, world" of do-it-yourself smart objects, it's quite possible that making an "Internet Button" is the "Hello, world" of "Internet of Things" things. In this project, we make a button that send an email.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino Uno
- 1 Arduino USB cable 
- 1 Arduino power supply
- 1 Breadboard
- Push button
- A home wifi network and the password for it
- A web browser
- An email address

_Special items_

- The assembled [Sparkfun Wifi Shield (ESP8266)](https://www.sparkfun.com/products/13287) from the [previous chapter](#chapters-get-your-arduino-online). 

This project uses an assembled [Sparkfun Wifi Shield](https://www.sparkfun.com/products/13287). Details on its assembly, with [Arduino R3 Stackable Headers](https://www.sparkfun.com/products/11417), are on the product page and in a [previous chapter](#chapters-get-your-arduino-online).


### Code

```arduino

// paste code

```

Every sketch used in "Family Projects for Smart Objects" is also available in a zipped-up bundle [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

### Useful Links

This project uses the [IFTTT website](http://ifttt.com) to turn our button-press into an email. Here are some useful links:

- [IFTTT home page](http://ifttt.com)
- [IFTTT sign up page](https://ifttt.com/join)
- [Maker channel on IFTTT](https://ifttt.com/maker)


## Online Temperature Tracker

Arduinos are excellent at logging their observations. With this project, we get Arduino logging environmental data online.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino
- 1 Ardunio USB cable 
- 1 Arduino power supply
- 1 Breadboard
- A home wifi network and the password for it
- A web browser

*Special items*

- Your assembled [Sparkfun Wifi Shield](https://www.sparkfun.com/products/13287)
- 1 [Thermistor](https://www.adafruit.com/products/372)
- 1 10K Resistor

This project uses an assembled [Sparkfun Wifi Shield](https://www.sparkfun.com/products/13287). Details on its assembly, with [Arduino R3 Stackable Headers](https://www.sparkfun.com/products/11417), are on the product page and in a [previous chapter](#chapters-get-your-arduino-online).

A thermistor can be found in most of the Arduino starter kits [I've listed below](#kits). If you don't have one, you can get them [online](https://www.adafruit.com/products/372). 

### Code

```arduino

// paste code

```

Every sketch used in "Family Projects for Smart Objects" is also available as a zipped-up file [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads folder and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

### Useful Links

We post our code to a free data-gathering website made by Sparkfun, and also export it to another website called. [Analog.io](http://analog.io). Here are the key links:

- [data.sparkfun.com](http://data.sparkfun.com)
- [Analog.io sign up page](http://analog.io/users/sign_up)

