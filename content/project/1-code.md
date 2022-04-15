---
section: Hello Arduino
nav_order: 3
title: Blink!
gallery: true
topics: Code; Integrated Development Environment
description: Let's use code to make an LED blink! This mini project will get you oriented to the UNO, the IDE, and the code that makes it do *stuff*.
---

For this project all we need is an UNO board, a USB cable, and the IDE. 

The Arduino IDE is our "Integrated Development Environment" --> an application that allows you to edit/write code, compile it, and send it to Arduino devices.
This mini project introduces some of the features of the IDE and can help you test to ensure everything is set up correctly on your computer.

## First Arduino Program  

1. Open Arduino Software IDE.

    {% include gallery-figure.html alt="Arduino IDE window with blank sketch." img="arduinoIDE.png" %}

2. Click `File` > `Examples` > `01.Basics` > `Blink`. This will open a new window with the Blink program. These built in examples are a great way to learn. You don't need to write code from scratch: borrow. That is the power of code! 

    "Sketches" are programs written using the Arduino IDE. Each is saved in its own folder and has the extension `.ino`.

3. Take a first look at the code:
    - `//` means the line is a comment. The computer will ignore it - humans only! Multiple line comments are enclosed between `/*` and `*/`. For example, `/* this is a comment */`
    - Each Arduino program is made of two functions, `setup()` and `loop()`. Code in the `setup()` runs one time when the board starts up. Next, code in the `loop()` runs and then repeats until you pull out the plug! 

4. Plug your USB cable into your UNO and computer.

    {% include gallery-figure.html alt="UNO plugged in to USB with lights on." img="first_code.jpg" %}

5. On IDE, click `Tools` > `Board` > `Arduino UNO` to set up the correct board.

6. Click `Tools` > `Port` and select the port where your UNO appears. For example, you might seem something like "COM9 (Arduino Uno)". The number differs depending on where you computer mounts it.

7. Click the `Upload` arrow icon. The IDE will verify, compile, and upload your program to the UNO. Any errors will appear in the console window below the text editor.

8. Take a closer look at `Blink`:
- `pinMode()` is a set up function that tells our board to use a specific pin as an output or input.
- `LED_BUILTIN` is a special variable that refers to a LED built in to a board. 
-  `digitalWrite()` is like a switch: `HIGH` = on, `LOW` = off. 
- `delay()` is a timer that make the program wait. The delay is given in milliseconds.

9. Mod this code! Change the delay times or add more on/off's, then click the upload arrow to get it running on your board. Congrats: you are a <span class="term">programmer</span>!

{% capture more %}
The Arduino IDE v1 was based on the "sketchbook" created for [Processing](https://processing.org/) and [Wiring](http://wiring.org.co/), platforms originally designed for creating interactive projects in the visual arts. 

The Arduino programming language is a set of libraries in [C](https://en.wikipedia.org/wiki/C_(programming_language)) and [C++](https://en.wikipedia.org/wiki/C%2B%2B) designed for the boards. 
Arduino IDE hides some of the complexity of setting up, but be proud that you are writing C/C++ code!
{% endcapture %}{% include card.html text=more %}
