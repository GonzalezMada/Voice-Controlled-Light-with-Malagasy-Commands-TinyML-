<!-- mdformat off(b/169948621#comment2) -->

# Light Control using TinyML Application

This code run a 20 kB model that can recognize 2 keywords,
"mirehitra" and "maty", and control a light.
 “Mirehitra” (light on) and “Maty” (light off)

The application listens to its surroundings with a microphone and indicates
when it has detected a word by lighting an LED and switch on and of a light via relay module.


## Table of contents
<!--ts-->
* [Table of contents](#table-of-contents)
* [Deploy to Arduino](#deploy-to-arduino)
   * [Install the Arduino_TensorFlowLite library](#install-the-arduino_tensorflowlite-library)
   * [Load and run the example](#load-and-run-the-example)
<!--te-->

## Deploy to Arduino

The following instructions will help you build and deploy this example to
[Arduino](https://www.arduino.cc/) devices.

The example has been tested with Arduino Nano 33 BLE Sense Rev2. A relay module is connect to the arduino board via pin 2.
and everything is powered by a 6V battery but 5V battery can be used. 


### Install the Arduino_TensorFlowLite library

Downlaod the zip file contenining the TensorFlow Lite Micro Arduino library and
install it on Arduino IDE.


### Load and run the example

Once the library has been added, go to `File -> Examples`. You should see an
entry within the list named `Arduino_TensorFlowLite`. Select
it and click `micro_speech` to load the example.

Use the Arduino IDE to build and upload the example. Once it is running, you
should see the built-in LED on your device flashing. The built-in LED will flash on/off for each inference cycle. Saying the word "mirehitra" will
cause the green LED to remain on for 3 seconds. The current model has fairly low
accuracy, so you may have to repeat "yes" a few times. Saying the word "no" will cause the red LED to light up.  The blue LED will be lit for certain "unknown" sounds.

Word recognition should occur at a distance of approximately 1.5 feet in a low-noise environment.

The program also outputs inference results to the serial port, which appear as
follows:

```
Heard mirehitra (201) @4056ms
Heard maty (205) @6448ms
Heard unknown (201) @13696ms
Heard yes (205) @15000ms
```

The number after each detected word is its score. By default, the program only
considers matches as valid if their score is over 200, so all of the scores you
see will be at least 200.

When the program is run, it waits several seconds for a USB-serial connection to be
available. If there is no connection available, it will not output data. To see
the serial output in the Arduino desktop IDE, do the following:

1. Open the Arduino IDE
1. Connect the Arduino board to your computer via USB
1. Press the reset button on the Arduino board
1. Within 5 seconds, go to `Tools -> Serial Monitor` in the Arduino IDE. You may
   have to try several times, since the board will take a moment to connect.

If you don't see any output, repeat the process again.

