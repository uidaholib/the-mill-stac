---
section: Hello Arduino
nav_order: 2
title: Introducing Arduino UNO 
gallery: true
topics: Microcontrollers; Breadboard; Input & Output
description: Meet your Microcontroller!
---

{% include gallery-figure.html alt="Arduino board with parts labelled: USB for power and flashing; reset button; ATmega328P microchip; input/output pins; have fun!" img="arduino_intro1.jpg" %}

[<span class="term">Arduino UNO</span>](https://docs.arduino.cc/hardware/uno-rev3) is a simple prototyping board based on <span class="term">open source</span> hardware and software. 
It can be programmed using the [Arduino language](https://www.arduino.cc/reference/en/) to create interactive physical computing projects.
UNO is a great option because it is cheap, readily available (from official and unofficial manufacturers), well documented, and widely adopted.

The popularly has benefits--> help and ideas are always only a quick search away! 
For examples and inspiration check out the [Project Hub](https://create.arduino.cc/projecthub).

{% capture quote %}
"Arduino was born at the Ivrea Interaction Design Institute as a tool for fast prototyping, aimed at students without a background in electronics and programming." -- Learn more from the [Arduino Guide](https://www.arduino.cc/en/Guide/Introduction){% endcapture %}{% include card.html text=quote %}

## Breadboard 

That white thing attached to your UNO? 
Its a <span class="term">solderless breadboard</span>!

{% include gallery-figure.html alt="Solderless breadboard with parts labelled: Split; Row; Rail." img="breadboard.jpg" %}

A breadboard simplifies creating circuits, allowing you to link all your components together without soldering anything. 
The connection is made by inserting wire into the tiny holes: 

- Each pin hole on a <span class="term">Rail</span> is connected vertically.
- Each pin hole in a <span class="term">Row</span> is connected horizontally. 
- A <span class="term">Split</span> runs down the middle dividing the board in two.

## Inputs & Outputs

Arduino is designed to make interactive projects--that is, take input from the world and respond with outputs.
Arduino does not have any built in sensors or outputs, but it does have 20 <span class="term">Pins</span>.
We can connect inputs and outputs to the pins to bring projects to life.

<div class="row row-cols-1 row-cols-md-2">
<div class="col">
{% capture input %}
- button
- potentiometer (dial)
- temperature sensor
- accelerometer (motion sensor)
- photoresistor (light sensor)
- piezo mic (sound)
{% endcapture %}{% include card.html text=input header="Example inputs / sensors" extra-class="h-100 border-primary" %}
</div><div class="col">
{% capture output %}
- LED (light)
- piezo buzzer (sound) 
- Servo motor, DC motor (motion)
{% endcapture %}{% include card.html text=output header="Example outputs / actuators" extra-class="h-100 border-info" %}
</div></div>
