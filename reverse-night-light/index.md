# Family Projects for Smart Objects

Here's the spot to get the parts and code for the projects in "Family Projects for Smart Objects." This will be styled to be more beautiful in time for the book launch, but should function as-is now.

## Reverse Night Light 

### Ingredients 

- 1 Arduino
- 1 Ardunio USB cable 
- 1 Arduino power supply
- 1 Breadboard
- 1 photoresistor
- 1 LED (white, if you have one)
- 3 Jumper wires
- Your computer

*Special Items*

- 2 Extension jumper wires (male-to-female)
- 1 Hollow, translucent toy

Almost all of these parts are found in these Arduino starter kits:

- [Maker Shed Getting Started with Arduino Kit](http://www.makershed.com/products/make-getting-started-kit-arduino-uno-r3)
- [SparkFun Inventor's Kit](https://www.sparkfun.com/products/12060)
- [Adafruit Starter Pack for Arduino](https://www.adafruit.com/products/68)

Those kits don't generally include these [extension jumper wires](https://www.sparkfun.com/products/12794), which you need to buy separately.

If you'd like to buy any or all of the parts individually, you can use [this pre-populated shopping cart](https://www.sparkfun.com/wish_lists/121993) at SparkFun.

### Code

The code for this project comes with the Arduino software. Find it by going to *File* &#8594; *Examples* &#8594; *03.Analog* &#8594; *AnalogInput*

    /*
 
     Reverse Night Light
     Douses an LED when the room is dark.

     By John Keefe, January 2016
     http://keefe.cc/reverse-night-light

     Based on example code created by David Cuartielles
     modified 30 Aug 2011 by Tom Igoe
     http://www.arduino.cc/en/Tutorial/AnalogInput

     This code is in the public domain.
 
     */

    int sensorPin = A0;   // select the input pin for the photoresistor
    int ledPin = 13;      // select the pin for the LED
    int sensorValue = 0;  // variable to store the value coming from the sensor
    int darkPoint = 0;    // if the sensor value is less than this, it's "dark"

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
      // turn the LED off:
      if (sensorValue < darkPoint) {
        digitalWrite(ledPin, LOW);
      }

      // if the sensorValue is greater than or equal to the
      // darkPoint, turn the LED on:
      if (sensorValue >= darkPoint) {
        digitalWrite(ledPin, HIGH);
      }

      // output the value to the Serial Monitor
      Serial.println(sensorValue);

      // a little delay to help read the numbers!
      delay(100); 
}
