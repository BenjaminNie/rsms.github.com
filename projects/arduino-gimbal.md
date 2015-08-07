---
layout: post
category: arduino gimbal
description: "gimbal controlled with arduino"
comments: yes
---

For a school project, we were asked to design a self balancing gimbal that would automatically reposition itself using a combination of capacitors, servos, and an Arduino Uno microcontroller. For those of you unfamiliar with gimbals (like myself prior to this project), it is a mechanism used for keeping an instrument parallel to the ground regardless of how the surrounding environment changes.  For a detailed explanation of gimbals and their properties, check out this excellent [tutorial](http://science.howstuffworks.com/gimbal.htm).


Our gimbal consisted of a base and a top platform. The goal is to have the top platform parallel to the ground at all times, regardless of the base orientation. To achieve this, we needed a method to measure the angle of our base relative to the ground, so that we can adjust our top platform using a mechanical servo in the opposite direction to maintain parallellism with the ground.

The orientation of our base relative to the ground was measured using two capacitors. The capacitors were made of petri dishes filled half-full with water, and half the face of the petri dish would be covered in aluminum foil while the other half was clear. Whenever the base tilted, the water-to-aluminum ratio would change within each petri dish, which in turn modified the capacitance levels measured by our sensors. Using this data, the Arduino Uno can hypothesize how the orientation of the base has changed and rotate the top platform in the opposite direction using mechanical servos.

The two capacitors are mounted onto the base using two separate metal posts. One capacitor is oriented in the y-z plane and the other capacitor is oriented in the x-z plane. When the base is tilted in either direction the change in capacitance is interpreted by the Arduino as the base changing orientation, which in turn causes the servos to rotate and realign the top platform to a perfectly horizontal level.

The gimbal had two modes, automatic and manual mode. In automatic mode, the Active Gimbal responds to the movement of the base and adjusts the servo motors accordingly. This was made possible using a 555 timer, which sent out a square pulse to the Arduino at regular intervals. The width of this square pulse changes when the capacitance/angle changes. The Arduino had a built-in library to read the pulse width and based off this information, the base orientation can be calculated and used to readjust the top platform.

In manual mode, we could use our GUI to manually control the orientation of the top platform relative to the base. We had both a LCD GUI that was attached to our board, and also a Windows Application GUI that communicated to the Arduino using a serial port. In both the LCD GUI and the Windows App GUI, we could select angles ranging from -90 to 90 in both the X and Y axis for the top platform to rotate along.

**CLICK PICTURE BELOW TO WATCH A VIDEO OF OUR GIMBAL**
[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/jxidy6K0Rqk/0.jpg)](http://www.youtube.com/watch?v=jxidy6K0Rqk)
