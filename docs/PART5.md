# Receive telemetry data from the drone
In Part 4 you constructed a Node-RED Dashboard flow to send commands to the drone. In this Part 5 exercise, we will create a Node-RED Dashboard with gauges to display telemetry data from the drone.

The video below shows how gauge nodes can be configured to display the telemetry data from the drone.

<- Add video here ->

## Receiving Tello Telemetry Data

Open Port 8890/udp in laptop firewall to receive Tello telemetry data.

On Linux
```
$ sudo firewall-cmd --permanent --add-port=8890/udp
```

On Mac, use System Preferences to open the ports.
- Open System Preferences > Security & Privacy > Firewall > Firewall Options
- Click the + / Add button
- Choose 'node' application from the Applications folder and click Add.
- Ensure that the option next to the application is set to Allow incoming connections.
- Click OK.

## Task

Begin with the [Part5 starter flow](/flows/starter/part5_starter.json) and add gauge nodes to display telemetry:

- Temp
- Barometer
- Accel X
- Accel Y
- Accel Z
- Speed X
- Speed Y
- Speed Z

Add a Chart node to display
- Drone Height

Add a Text node to display
- Flight Time

![Tello Telemetry Dashboard Starter flow](/docs/screenshots/NodeRED-Tello-Telemetry-Starter-flow.png?raw=true "Tello Telemetry Starter flow")

### Solution

There is a [solution flow](/flows/solutions/part5_solution.json) available if you need help or want to check your solution.

![Tello Telemetry Dashboard Solution flow](/docs/screenshots/NodeRED-Tello-Telemetry-Solution-flow.png?raw=true "Tello Telemetry Dashboard Solution flow")

![Tello Telemetry Dashboard Gauges](/docs/screenshots/NodeRED-Tello-Telemetry-Dashboard-Solution.png?raw=true "Tello Telemetry Dashboard Solution")
---

---

[Home](/README.md) | [Node-RED](/docs/PART1.md) | [Setup](/docs/PART2.md) | [Commands](/docs/PART3.md) | [Dashboard](/docs/PART4.md) | **Telemetry** | [Mission](/docs/PART6.md) | [Pictures](/docs/PART7.md) | [Visual Recognition](/docs/PART8.md)

---
