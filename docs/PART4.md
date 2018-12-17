# Build a Node-RED dashboard

In Part 3 you constructed a Node-RED flow to send commands to the drone. In this Part 4 exercise, we will create a Node-RED Dashboard with buttons that send the SDK commands. Recall in Part 1, you installed the node-red-dashboard nodes and you should find the Node-RED Dashboard nodes in your palette.

The video below shows how button nodes can be configured to send the SDK commands to the drone.

<- Add video here ->

## Task

Begin with the [Part4 starter flow](/flows/starter/part4_starter.json) and add button nodes to the following commands:

- emergency
- up 50cm
- down 50cm
- right 50cm
- left 50cm
- forward 50cm
- back 50cm
- rotate clockwise 90º
- rotate counter-clockwise 90º
- rotate clockwise 360º
- flip forward

![Tello Control Dashboard Starter flow](/docs/screenshots/NodeRED-Tello-Dashboard-Starter-flow.png?raw=true "Tello Control Dashboard Starter flow")

Launch the Node-RED Dashboard by turning to the Dashboard tab in the right menu and then click on the launch button.

![Tello Controls Dashboard Buttons](/docs/screenshots/NodeRED-Tello-Controls-Dashboard-Starter.png?raw=true "Tello Controls Dashboard Starter")


### Solution

There is a [solution flow](/flows/solutions/part4_solution.json) available if you need help or want to check your solution.

![Tello Control Dashboard Solution flow](/docs/screenshots/NodeRED-Tello-Dashboard-Solution-flow.png?raw=true "Tello Control Dashboard Solution flow")

![Tello Controls Dashboard Buttons](/docs/screenshots/NodeRED-Tello-Controls-Dashboard-Solution.png?raw=true "Tello Controls Dashboard Solution")
---

[Home](/README.md) | [Node-RED](/docs/PART1.md) | [Setup](/docs/PART2.md) | [Commands](/docs/PART3.md) | **Dashboard** | [Telemetry](/docs/PART5.md) | [Mission](/docs/PART6.md) | [Pictures](/docs/PART7.md) | [Visual Recognition](/docs/PART8.md)

---
