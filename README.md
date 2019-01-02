# Node-RED-Tello-Control

Node-RED flows to control the Ryze / DJI Tello Drone

This repository contains Node-RED flow examples that demonstrate how to control
the [DJI Drone](https://www.ryzerobotics.com/tello) using the [Node-RED visual editor](http://nodered.org).

## Introduction

Flying the Tello drone with the Android/iOS mobile apps is amazing fun but the Tello has another fantastic feature.
The Tello includes a programming interface that developers can use to send commands to control the drone. Programming
APIs can also receive telemetry and video stream data from the Tello. Ryze and DJI provide
[SDK programming documentation](https://www.ryzerobotics.com/tello/downloads) to help developers learn how to program
the drone.  Tello programming has grown so popular that they have released a [Tello EDU](https://www.ryzerobotics.com/tello-edu)
version that has additional [SDK documentation](https://www.ryzerobotics.com/tello-edu/downloads).
An entire open source community has formed around programming the Tello. If you are a developer, a good place to start is the
[TelloPilots](https://tellopilots.com/) forums. There are dozens of [github repositories](https://github.com/topics/tello)
that have programming examples written in [Python](https://github.com/damiafuentes/DJITelloPy),
[Go](https://github.com/SMerrony/tello), [Swift](https://github.com/tranchis/TelloSwift) and
[Node.js](https://github.com/SovGVD/nodetello). This **Node-RED implementation** was inspired by the
[Tello Scratch node.js example](https://dl-cdn.ryzerobotics.com/downloads/tello/0222/Tello+Scratch+Readme.pdf).

## How this git repository is organised

To help you get familiar with Node-RED and how to control the Tello drone this git repository is split into a number of sections, where you have tasks to complete in each section.  If you just want to have fun with the drone and prefer not to do the tasks then jump into the flows folder and use the solutions.

## Tasks

1. [Learn about Node-RED](/docs/PART1.md)
2. [Install Node-RED](/docs/PART2.md)
3. [Send SDK commands to the drone](/docs/PART3.md)
4. [Build a Node-RED dashboard](/docs/PART4.md)
5. [Receive telemetry data from the drone](/docs/PART5.md)
6. [Create missions for your drone](/docs/PART6.md)
7. [Take pictures](/docs/PART7.md)
8. [Use Visual Recognition on drone pictures](/docs/PART8.md)
9. [Train a Visual Recognition Custom Classifier of drone pictures](/docs/PART9.md)

As a reminder, **Safety First!**  Take caution when flying your drone. Fly your drone indoors at your own risk.
Also, be respectful of your neighbors and public property when flying your drone outdoors.  When recording video
and taking pictures, be mindful of other people's privacy.  Obey all FAA regulatory restrictions posted about UAV
flight prohibitions.

### Authors

- [John Walicki](https://github.com/johnwalicki/)
- [Markus Van Kempen](https://github.com/markusvankempen)
- [Brian Innes](https://github.com/binnes)

___

Enjoy!  Give us [feedback](https://github.com/johnwalicki/Node-RED-Tello-Control/issues) if you have suggestions on how to improve this tutorial.

## License

This tutorial is licensed under the Apache Software License, Version 2.  Separate third party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1 (DCO)](https://developercertificate.org/) and the [Apache Software License, Version 2](http://www.apache.org/licenses/LICENSE-2.0.txt).

[Apache Software License (ASL) FAQ](http://www.apache.org/foundation/license-faq.html#WhatDoesItMEAN)
