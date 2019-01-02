# Create missions for your drone

You can create subflows in Node-RED.  A subflow acts like a function in other programming languages.  You can capture an existing flow, or part of a flow, into a subflow or create a subflow from scratch.  The subflows appear in the pallet and look like any other nodes in the pallet.  You can then drag the subflow nodes onto the pallet to run the flow within the subflow.

<- video here ->

## Task

Import the [part6 starter flow](/flows/starter/part6_starter.json), which provides you will all the subflow nodes as shown in the video.  You should create a patrol mission for your drone, which comprises of the following tasks:

- Take off
- Descend 1.5 meters
- Rotate 360º clockwise
- Complete a square by moving forward 50cm, then rotating 90º and repeating 4 times
- Land

Be sure to add sufficient delays into your solution to allow the drone to complete all the moves.  Add a new group to the dashboard and then create a button to allow you to start the mission from the dashboard.

You can import a [sample solution](/flows/solutions/part6_solution.json) if you need help or want to compare your solution with a sample solution.

![Tello Mission Starter flow](/docs/screenshots/NodeRED-Tello-Missions-Starter-flow.png?raw=true "Tello Missions Starter flow")

---

[Home](/README.md) | [Node-RED](/docs/PART1.md) | [Setup](/docs/PART2.md) | [Commands](/docs/PART3.md) | [Dashboard](/docs/PART4.md) | [Telemetry](/docs/PART5.md) | **Mission** | [Pictures](/docs/PART7.md) | [Visual Recognition](/docs/PART8.md) | [Custom Classifier](/docs/PART9.md)
---
