---
layout: page
tags: programming
category: ubc engineering competition
description: "competition robot for 2013 ubc engineering competition"
comments: yes
---

Having learned from the previous year's mistakes and triumphs, our team was back at UBC's annual engineering competition. This year, we were asked to build a robot to mimic an autonomous garbage truck whose responsibility was to guide itself from a starting location to a garbage can, pick up the garbage can, and proceed to tour a row of homes to pick up trash.
Like last year, all teams were provided with the VEX robotic kit, which was a kit consisting of many mechanical components, sensors (ultrasonic, IR, etc), and a microcontroller with a C compiler. All locations that needed to be traveled to were connected together with black tape, and there were a few misleading trails of black tape and numerous ramps placed along the track to test our robot's software complexity and mechanical capabilites. 

When we entered the previous year's competition, our robot only had two light sensors mounted. The light sensors were mounted facing the ground, and were arguably the most crucial sensor in our system since they kept track of the black tape and ensured our robot doesn't steer off course. The problem with two sensors was the massive amount of zigzagging done by the robot as it tried to correct it's course, since the correction didn't occur until the robot was very crooked. This year, we added a third light sensor in the center, which heavily reduced the zigzagging of our robot. An ultrasonic sensor was placed at the front of the vehicle to detect the garbage. When the garbage was close enough, our robot would use a mechanical arm to sweep down and place the garbage inside the garbage can.

![Aeriel view of robot](/res/IMG_8824.JPG)
_Aeriel view of robot.  Three light sensors face the bottom and ultrasonic sensor faces the front._
![Side view of robot](/res/IMG_8827.JPG)
_Side of the robot. Servos were used to control back wheel._

Due to the 5 hour limitation of the competition, we were unable to complete our robot's mechanical garbage arm. However, most teams competing were in a similar situation, and we were asked to demo our robot on portions of the obstacle course it could complete. The judges loved the design principles our team used to build this robot, especially the rapid prototyping process we used to finetune the path adjustment algorithm using our three light sensors. Ultimately, our team came just short, and we finished 2nd place in the competition.

![Cracking a smile(x4) after our presentation](/res/IMG_8823.JPG)
_Cracking a smile(x4) after our presentation_
