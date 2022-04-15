---
section: Hello Arduino 
nav_order: 4
title: Buzz!
gallery: true
topics: Piezo; Photoresistor; Tone Function
description: Time to make some buzz! Let's build a "light theremin" that changes pitch using a photoresistor. 
---

For this project you will need some jumper wires, a piezo, a 10k ohm resistor, and a photoresistor. 

{% include gallery-figure.html alt="parts needed: piezo, resistors, and wires" img="ther1.jpg" %}

This time we are adding a *sensor*, the photoresistor, so that UNO can get input from the outside world, i.e. UNO can get interactive! 
The piezo provides the buzzing (output) and we control it by having UNO read the photoresistor.

--------

## Light Theremin Circuit 

### Connect Piezo 

1. Gently insert the pins of your Piezo into row one and five (or any two separate rows that they fit into, the key is to try to leave enough space to fit your jumper wires!).

    {% include gallery-figure.html alt="piezo being inserted into breadboard" img="ther2.jpg" %}

2. Connect row one to the ground `-` rail with a wire jumper (i.e. piezo to GND)

    {% include gallery-figure.html alt="wire connecting breadboard GND to piezo" img="ther3.jpg" %}

3. Connect row five to pin `8` on the UNO using a wire jumper (i.e piezo to digital pin)

    {% include gallery-figure.html alt="wire connects piezo to UNO pin" img="ther4.jpg" %}

### Connect Photoresistor

4. Insert the pins from the photoresistor in rows twenty-five and twenty-eight (or any two separate rows that will provide some space to work).

    {% include gallery-figure.html alt="photoresistor added to breadboard" img="ther5.jpg" %}

5. Connect one leg of the photoresistor (row twenty-five) to the power `+` rail with a jumper wire. (i.e. photoresistor to 5V)

    {% include gallery-figure.html alt="wire connecting photoresistor to breadboard power rail" img="ther6.jpg" %}

6. Use 10k resistor to connect the other leg of the photoresistor (row twenty-eight) to ground `-` rail (i.e. photoresistor to GND). This is called the pull down resistor, used to ensure we have a stead signal for the input.

    {% include gallery-figure.html alt="resistor connects GND to photoresistor in breadboard" img="ther7.jpg" %}

7. Connect the same leg (row twenty-eight) to Pin `A0` on the UNO. (i.e. photoresistor to analog input)

    {% include gallery-figure.html alt="wire connects photoresistor to UNO pin" img="ther8.jpg" %}

### Connect Power 

9. Connect the ground `-` rail to a `GND` pin on the UNO with a power jumper wire.

10. Connect the power `+` rail to the `5V` Pin on the UNO with a power jumper wire.

    {% include gallery-figure.html alt="wires connect breadboard rails to UNO power pins" img="ther9.jpg" %}

All ready to program... 

-----------

## Theremin Code 

1. On the IDE, choose `File` > `Examples` > `StarterKit_BasicKit` > `p06_LightTheremin`

2. Plug UNO into the USB, and click the upload arrow to load the sketch. 

3. The first few seconds the program calibrates the photoresistor, so *move your finger over and back to change the amount of light falling on the sensor*. 

The buzzing will start soon - Enjoy!

### Make the Buzz Less Annoying!

Find at the line that says `int pitch = map(sensorValue, sensorLow, sensorHigh, 50, 4000);`

This function *maps* our photoresistor readings (`sensorValue`) to a number between `50` and `4000`, which will be output as a tone in the piezo.
The lowest possible sensor reading will translate to a tone of 50, the highest to 4000. 

Swap the range so that it says `4000, 0`. 
What does this do? 

### Experiment

Keep editing and experiment! 
Try changing a few values in the `loop()`, such as:

- range of pitch: change `4000, 0` to something else
- tone length: change the third number in the `tone()` function
- loop delay: change the final `delay()` time 

Try loading other sketch examples that work with this circuit:

- `File` > `Examples` > `Digital` > `toneMelody`
- Download [arduinoTeaching](https://github.com/evanwill/arduinoTeaching) examples. Look for `lightThereminBasic.ino`, a heavily annotated version of `p06_LightTheremin`.

-------------

## Extra Credit!

Put your vast knowledge of Arduino to use and build a new project based on what we did so far. 
Suggestions:

- Build a blinking lights display with multiple LEDs.
- Combine blinking LEDs and the light theremin *(note: tone() interferes with pin 11 and 3, delay() interferes with pin 5 and 6, so you can end up with odd results)*.

    {% include gallery-figure.html alt="UNO with light theremin circuit with LEDs added" img="blink_theremin.jpg" %}

- Use another sensor to set variables for blink or theremin, for example a potentiometer or temperature sensor.  

    {% include gallery-figure.html alt="temp sensor and LEDs added to light theremin circuit" img="temp_sensor.jpg" %}
