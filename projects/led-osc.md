---
layout: post
category: arduino gimbal
description: "gimbal controlled with arduino"
comments: yes
---

For my second year project course, my team and I built a electro-mechanical LED display that reads an analog voltage wave produced by a signal generator as input and outputs the exact same wave onto a row of LEDs. The device is designed to display the waveform produced by the function generator by rapidly moving a column of 16 LEDs back and forth in a linear fashion using a mechanical arm powered by a DC motor. The device must operate at a constant speed that is fast enough so the human eye can perceive the waveform.

The Scotch-Yoke mechanism was chosen to guide our mechanical arm since it is more efficient in converting circular motion produced by the motor into linear movement of the cart along the rail. It consists of a pin attached to the wheel that moves down a slot, pushing the form to move in a straight line.

The logic was implemented using a analog-to-digital converter. The analog signal ranged from 5V to -5V, and our ADC translated this value into an 8 bit binary figure. An analog voltage value of 5V (highest) would translate to 255 (1111 1111 in binary) digital output, while a -5V input voltage would translate to a 0 (0000 0000 in binary) digital output. This digital output value is then processed with an Altera FPGA board, mapping these into a row of 16 LEDs. Depending on the input value at the time, a different LED is lit up, and this calculation is repeated many times in parallel with the movement of the mechanical arm, to make the LEDs display an identical wave to what is produced by the signal generator.

As an extra feature, our team built the capability to vary the voltage per division and also the time per division of the waveform displayed. By pressing push buttons on our Altera FPGA board, we could control the scale in both the X and Y axis that were displayed by our LEDs.

**CLICK PICTURE BELOW TO WATCH A VIDEO OF OUR OSCILLOSCOPE**
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/z46cDl2nidg/0.jpg)](http://www.youtube.com/watch?v=z46cDl2nidg)
