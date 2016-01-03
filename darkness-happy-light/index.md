# Family Projects for Smart Objects

Here's the spot to get the parts and code for the projects in "Family Projects for Smart Objects." This will be styled to be more beautiful in time for the book launch, but should function as-is now.

## Darkness-Happy Light 

### Ingredients 

- 1 Arduino Uno
- 1 Arduino USB Cable
- 1 Breadboard
- Your computer
- 1 LED
- 3 jumper wires
- 1 Photoresistor
- 1 10K-ohm resistor

All of the required parts for this project can be found in any of these Arduino starter kits:

- [Maker Shed Getting Started with Arduino Kit](http://www.makershed.com/products/make-getting-started-kit-arduino-uno-r3)
- [SparkFun Inventor's Kit](https://www.sparkfun.com/products/12060)
- [Adafruit Starter Pack for Arduino](https://www.adafruit.com/products/68)

If you'd like to buy any or all of the parts individually, you can use [this pre-populated shopping cart](https://www.sparkfun.com/wish_lists/121994) at SparkFun.

### Code

The code for this project comes with the Arduino software. Find it by going to *File* &#8594; *Examples* &#8594; *03.Analog* &#8594; *AnalogInput*

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



