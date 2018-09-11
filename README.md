# Node-RED-Tello-Control
Node-RED flows to control the Ryze Tello Drone

This repository contains Node-RED flow examples that demonstrate how to control
the [Ryze Tello Drone](https://www.ryzerobotics.com/tello) using the [Node-RED visual editor](http://nodered.org).  This implementation is inspired by the [Tello Scratch node.js example](https://dl-cdn.ryzerobotics.com/downloads/tello/0222/Tello+Scratch+Readme.pdf)
but does not require those programs.

These Tello Node-RED examples showcase how to:
- Send individual commands to the Tello Drone
- Construct a mission flight plan that can be pre-programmed and then sent to
Tello drone for execution
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
### Node-RED Tello Dashboard Example
- This [flow](/flows/nodered-tello-dashboard.json) reads the telemetry data from the drone and displays some of the data in a Node-RED Dashboard.

![Tello Dashboard Gauges](/screenshots/NodeRED-Tello-Dashboard-gauges.png?raw=true "Tello Dashboard gauges")
![Tello Dashboard Flow](/screenshots/NodeRED-Tello-Dashboard-flow.png?raw=true "Tello Dashboard flow")
___
