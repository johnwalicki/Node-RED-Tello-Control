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
Before programming the Tello using Node-RED, several pre-requiste software packages need to be installed.
- [Node.js Installation Instructions](https://nodejs.org/en/download/)
- [Node-RED Installation Instructions](https://nodered.org/docs/getting-started/installation)

**Node-RED** is a flow-based programming environment from the JS Foundation. It provides a palette of nodes that allow
users to very quickly wire up IoT applications that can combine streams of both physical and digital events.
Its Node.JS runtime is easy to install on both devices and the cloud, and provides a framework for extending its capabilities.

Once Node-RED is installed, several additional Node-RED nodes will be necessary. Install the following nodes using the
Node-RED Manage Palette:
- node-red-Dashboard

Learn how to import flows into your Node-RED editor.

## Tello Node-RED Programming Examples
The Tello Node-RED examples in this repository showcase how to:
- Send individual commands to the Tello Drone
- Construct a mission flight plan that can be pre-programmed and then sent to
Tello drone for execution
- Build a Node-RED Tello Dashboard of control buttons to fly the drone
- Node-RED Tello Dashboard Example that displays the drone telemetry data

Get the Code by downloading and importing these Node-RED [flows](/flows) into your Node-RED editor.

Authors:
- [John Walicki](https://github.com/johnwalicki/)
- [Markus Van Kempen](https://github.com/markusvankempen)

## Node-RED flows in this repository:
### Send Commands to Tello Drone
- This [flow](/flows/nodered-tello-controls.json) demonstrates how to send individual commands to the Tello Drone

![Tello Control Flow](/screenshots/NodeRED-Tello-Controls-flow.png?raw=true "Tello Control flow")
___
### Execute a Pre-Programmed Flight Plan
- This [flow](/flows/nodered-tello-missions.json) sends a pre-programmed flight plan to the Tello Drone
  - Edit the Template nodes to construct your own pre-programmed Tello path.
  - Wire the Tello command set that you want to execute into the CSV split node.

![Tello Missions Flow](/screenshots/NodeRED-Tello-Missions-flow.png?raw=true "Tello Missions flow")
___
### Node-RED Tello Controls Dashboard Example
- This [flow](/flows/nodered-tello-controls-dashboard.json) builds a Node-RED dashboard of commands that control the drone.

![Tello Controls Dashboard Buttons](/screenshots/NodeRED-Tello-Controls-Dashboard.png?raw=true "Tello Telemetry Dashboard buttons")
![Tello Controls Dashboard Flow](/screenshots/NodeRED-Tello-Controls-Dash-flow.png?raw=true "Tello Controls Dashboard flow")
___
### Node-RED Tello Telemetry Dashboard Example
- This [flow](/flows/nodered-tello-telemetry.json) reads the telemetry data from the drone and displays some of the data in a Node-RED Dashboard.

![Tello Telemetry Dashboard Gauges](/screenshots/NodeRED-Tello-Telemetry-gauges.png?raw=true "Tello Telemetry Dashboard gauges")
![Tello Telemetry Dashboard Flow](/screenshots/NodeRED-Tello-Telemetry-flow.png?raw=true "Tello Telemetry Dashboard flow")
___
