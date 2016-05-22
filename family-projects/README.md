# Family Projects for Smart Objects
  
This is the companion website for the book, "Family Projects for Smart Objects" by [John Keefe](http://johnkeefe.net), due out in Fall 2016 from Maker Media. This is where you'll find links to ingredients for every project in the book, along with the copy-able code you'll need for each project.
  
# Chapters  

## You Only Have to Do This Once

This is the kickoff chapter in the book, and all about getting your Arduino up and running. And you only have to do it once.

### Ingredients

- 1 Arduino Uno (Revision 3)
- 1 Arduino USB cable

You can buy just these parts from Adafruit or Sparkfun using the buttons below.

[Buy from Adafruit >](http://www.adafruit.com/wishlists/403572) [Buy from Sparkfun >](https://www.sparkfun.com/wish_lists/127673)

These ingredients are also found in all of the Arduino starter kits [I've listed below](#kits).

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

These ingredients are also found in all of the Arduino starter kits [I've listed below](#kits).

### Code

The code for this project actually comes with the Arduino software. The easiest way to use it is to open your Arduino software and navigate to the "Blink" sketch, starting at the menu bar and chosing _File_ &#8594; _Examples_ &#8594; _01.Basics_ &#8594; _Blink_.

You can also copy it from here:

```arduino
/*
  Blink
  Turns on an LED on for one second, then off for one second, repeatedly.

  Most Arduinos have an on-board LED you can control. On the Uno and
  Leonardo, it is attached to digital pin 13. If you're unsure what
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

Every sketch used in "Family Projects for Smart Objects" is also available as a zipped-up file [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads file and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

## A Darkness-Happy Light

For this project, we make an LED flash fast and happy when the room is 
dark, and slow and soothing when the room is in daylight.

### Ingredients

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino Uno
- 1 Arduino USB Cable
- 1 Breadboard
- 1 LED
- 3 jumper wires
- 1 Photoresistor
- 1 10K-ohm (10K&#937;) resistor

Most of these ingredients are also found in the Arduino starter kits [I've listed below](#kits).

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

Every sketch used in "Family Projects for Smart Objects" is also available as a zipped-up file [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads file and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

## Night Light

Night lights are awesome and useful, and the best ones save power by 
only lighting up when it's dark in the room. That's what we make with this project.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino
- 1 Arduino USB cable 
- 1 Arduino power supply
- 1 Breadboard
- 1 photoresistor
- 1 LED (white, if you have one)
- 3 Jumper wires

*Optional Items*

- 2 [Extension jumper wires (male-to-female)](https://www.sparkfun.com/products/9140)
- 1 Hollow, translucent toy

Except for the Optional Items, these ingredients are also found in the Arduino starter kits [I've listed below](#kits).

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

Every sketch used in "Family Projects for Smart Objects" is also available as a zipped-up file [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads file and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.

## Ice, Ice Binkly

This project makes an LED react to cold water.

### Ingredients 

In addition to your own computer, here's what you'll need for this chapter.

- 1 Arduino Uno
- 1 Arduino USB cable 
- 1 Breadboard
- 1 thermistor
- 1 10k-ohm (10k&#937;) resistor
- A glass of ice water

Almost all of the Arduino start-up kits [I've listed below](#kits) include a thermistor. Sometimes they are at the ends of long, wiggly wires; other times they have stiff wires, like an LED. Either one will work here.

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

Every sketch used in "Family Projects for Smart Objects" is also available as a zipped-up file [you can download here](https://github.com/jkeefe/family-projects-sketches/archive/master.zip). Once you do, navigate to your downloads file and unzip the file `family-projects-sketches-master.zip`, usually done just by clicking or double-clicking its icon. 

You'll find all of the sketches within "chapter" folders in that file. The sketches end in `.ino` (for Ardu_ino_) and have a blue Arduino icon. To use one, just double-click on it.



.
.
.
.

# Kits

To make these projects, you'll need a handful of hobby electronics, which are relatively cheap and readily available. You can buy the parts individually, or you can get "starter kits" that have almost all of the parts you'll need for this book. Here are some of the kits, with (TODO) additional notes about chapters where you may need to get some extra parts:

- [Adafruit Experimentation Kit for Arduino ($$)](https://www.adafruit.com/products/170)
- [Adafruit Starter Pack for Arduino ($$)](https://www.adafruit.com/products/68)
- [Adafruit Budget Pack for Arduino ($)](https://www.adafruit.com/products/193)
- [Make: Getting Started with Arduino Kit, Special Edition ($$)](http://www.makershed.com/products/make-getting-started-kit-arduino-uno-r3)
- [Sparkfun Invetor's Kit for Arduino ($$$$)](https://www.sparkfun.com/products/13844)
- [SparkFun Inventor's Kit for Arduino - V3.2 ($$$)](https://www.sparkfun.com/products/13154)

