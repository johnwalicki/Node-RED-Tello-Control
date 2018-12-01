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

## Pre-Requistes

**Node-RED** is a open source project and flow-based programming environment from the
[JS Foundation](https://js.foundation/community/projects). It provides a palette of nodes that allow users
to very quickly wire up IoT applications that can combine streams of both physical and digital events.
Its Node.JS runtime is easy to install on both devices and the cloud, and provides a framework for
extending its capabilities.

Before programming the Tello using Node-RED, several pre-requiste software packages need to be installed.
- [Node.js Installation Instructions](https://nodejs.org/en/download/)
- [Node-RED Installation Instructions](https://nodered.org/docs/getting-started/installation)

Once Node-RED is installed, several additional Node-RED nodes will be necessary. Install the following nodes
using the Node-RED Manage Palette or via the npm command line:
- [node-red-dashboard](https://flows.nodered.org/node/node-red-dashboard) - A set of dashboard nodes for Node-RED
- [node-red-node-watson](https://flows.nodered.org/node/node-red-node-watson) - A collection of Node-RED nodes for IBM Watson services

Learn how to [import flows](https://github.com/binnes/esp8266Workshop/blob/master/en/part3/NODERED.md#step-3---how-to-install-additional-node-red-nodes)
into your Node-RED editor.

As a reminder, **Safety First!**  Take caution when flying your drone. Fly your drone indoors at your own risk.
Also, be respectful of your neighbors and public property when flying your drone outdoors.  When recording video
and taking pictures, be mindful of other people's privacy.  Obey all FAA regulatory restrictions posted about UAV
flight prohibitions.

## Tello Node-RED Programming Examples

The Tello Node-RED examples in this repository showcase how to:
- Send individual commands to the Tello Drone
- Construct a mission flight plan that can be pre-programmed and then sent to Tello drone for execution
- Build a Node-RED Tello Dashboard of control buttons to fly the drone
- Node-RED Tello Dashboard Example that displays the drone telemetry data

Get the Code by downloading and importing these Node-RED [flows](/flows) into your Node-RED editor.

#### Authors:
- [John Walicki](https://github.com/johnwalicki/)
- [Markus Van Kempen](https://github.com/markusvankempen)

## Node-RED flows in this repository:

### Send Commands to Tello Drone
- This [flow](/flows/nodered-tello-controls.json) demonstrates how to send individual commands to the Tello Drone.
  - Each **inject** node, will send a single command to the Tello.  Units are in centimeters or degrees.
  - A list of commands can be found in the [Tello SDK documentation](https://dl-cdn.ryzerobotics.com/downloads/Tello/Tello%20SDK%202.0%20User%20Guide.pdf)

![Tello Control Flow](/screenshots/NodeRED-Tello-Controls-flow.png?raw=true "Tello Control flow")
___
### Execute a Pre-Programmed Flight Plan
- This [flow](/flows/nodered-tello-missions.json) sends a pre-programmed flight plan to the Tello Drone
  - Edit the Template nodes to construct your own pre-programmed Tello path
    - Double click on the Template nodes to enter the list of Tello commands
    - Recall that the SDK pdf has a list of valid commands
    - Each line should contain the following instructions:<br/>
     *command*,*distance (cm)|rotation degrees*,*optionally the delay time (milliseconds) until next command is sent*<br/>
     eg.
      ```
      command,0,250
      takeoff,0
      up,25,5000
      cw,90
      land,0
      ```
    - The command *command* initializes the drone to receive instructions.
    - A *0* for the distance just tells the flow that no units are necessary and is
  - Wire the Tello command set that you want to execute into the **Initialize Mission** and **Split** nodes.
  - Start the mission by pressing the **inject** node labeled **Run Mission**
  - If the Tello goes out of control, click on the **Abort Mayday Abort** inject node.

![Tello Missions Flow](/screenshots/NodeRED-Tello-Missions-flow.png?raw=true "Tello Missions flow")
___
### Node-RED Tello Controls Dashboard Example
- This [flow](/flows/nodered-tello-controls-dashboard.json) builds a Node-RED dashboard of commands that control the drone
  - The Inject nodes from the prior flow have been replaced with Node-RED dashboard **Button** nodes
  - Node-RED dashboard **Button** nodes can be customized with colors and Font Awesome icons
  - Each Node-RED dashboard group contains a column of related Tello commands
  - Each **Flight Path** button sends the Tello command and 50cm distance - which is a reasonable compromise for indoor testing but could be extended for outdoor flight
  - The **Rotation** buttons send the specified degrees rotation
  - the **Flips!** buttons flip the drone in the direction specified

![Tello Controls Dashboard Buttons](/screenshots/NodeRED-Tello-Controls-Dashboard.png?raw=true "Tello Telemetry Dashboard buttons")
![Tello Controls Dashboard Flow](/screenshots/NodeRED-Tello-Controls-Dash-flow.png?raw=true "Tello Controls Dashboard flow")
___
### Node-RED Tello Telemetry Dashboard Example - Experimental
- This [flow](/flows/nodered-tello-telemetry.json) reads the telemetry data from the drone and displays some of the data in a Node-RED Dashboard.
  - The complete command set of telemetry data has not been fulled documented
- This flow is experimental and does not fully function. Patches are welcome.

![Tello Telemetry Dashboard Gauges](/screenshots/NodeRED-Tello-Telemetry-gauges.png?raw=true "Tello Telemetry Dashboard gauges")
![Tello Telemetry Dashboard Flow](/screenshots/NodeRED-Tello-Telemetry-flow.png?raw=true "Tello Telemetry Dashboard flow")
___

Enjoy!  Give me [feedback](https://github.com/johnwalicki/Node-RED-Tello-Control/issues) if you have suggestions on how to improve this tutorial.

## License
This tutorial is licensed under the Apache Software License, Version 2.  Separate third party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1 (DCO)](https://developercertificate.org/) and the [Apache Software License, Version 2](http://www.apache.org/licenses/LICENSE-2.0.txt).

[Apache Software License (ASL) FAQ](http://www.apache.org/foundation/license-faq.html#WhatDoesItMEAN)
