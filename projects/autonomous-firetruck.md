---
layout: page
tags: programming
category: ubc engineering competition
description: "competition robot for 2012 ubc engineering competition"
comments: yes
---

As part of the University of British Columbia's schoolwide engineering competition in 2012, all competitors were asked to build an autonomous robot that could travel from a starting location, pick up a can of water from a second location, put out a fire at the third location, and return to the starting location. The path connecting all these locations were marked by black tape and the terrain varied throughout the course, with several obstacles, ramps, and gaps that our robot had to avoid.

![Closely examining the course terrain prior to competition](/res/IMG_6440.JPG)
_Closely examining the course terrain prior to competition_

To build the robot, all teams were provided with the VEX robotic kit, consisting of a large number of mechanical components, sensors, and a microcontroller to control the robot autonomously.

The most essential problem was traveling through the course by following the black line connecting all the locations. To accomplish this, one light sensor was placed on each side of our robot. If our robot were to travel off the track, the light sensor will eventually sense the black line - This indicates our robot has travelled too far to the opposite side of the triggered light sensor. To account for this issue, we simply turn our robot in either a clockwise or counterclockwise direction (depending on which side the light sensor was triggered), and move forward again. This process is repeated until both light sensors are eventually untriggered, indicating that our robot is traveling in a straight line along the intended path.

![Back of the robot](/res/IMG_6457.JPG)
_Back of the robot. Blue rectangular box is the VEX microcontroller and red box on the side is the light sensor_

![Front of the robot](/res/IMG_6459.JPG)
_Front of the robot. Red box with with black spots is the ultrasonic sensor_

To pick up the water bottle, our team decided to use a ultrasonic sensor at the front of the robot to find the bottle of water. Once the waterbottle was within range of our sensor, the mechanical arm on our robot scooped the bottle of water up. Lastly, we travel to the destination and lower the mechanical arm to lower the bottle of water into the hypothetical fire, effectively putting it out. Our robot then turns around and returns to it's starting location.

To grade competitors, judges ranked all robots based on principles of design, functionality, and oral presentation. Taking all three areas into account, my team placed 3rd in the competition.

![Second Runner Ups](/res/IMG_6464.JPG)
_Presenting... Your UBC Engineering Competition Second Runnerups!_
