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

## Telemetry Data
The drone will send telemetry data to port 8890.  The **Parse Status into an object** change node uses a JSONata expression to parse the telemetry data into an JSON Object. 

- **pitch** : the degree of the attitude pitch.
- **roll** : the degree of the attitude roll.
- **yaw** : the degree of the attitude yaw.
- **vgy** : the speed of the “y” axis.
- **templ** : the lowest temperature in degree Celsius.
- **temph** : the highest temperature in degree Celsius
- **tof** : the time of flight distance in cm.
- **h** : the height in cm.
- **bat** : the percentage of the current battery level.
- **baro** : the barometer measurement in cm.
- **time** : the amount of time the motor has been used.
- **agx** : the acceleration of the “x” axis.
- **agy** : the acceleration of the “y” axis.
- **agz** : the acceleration of the “z” axis.

JSON Object example output:
```
{"pitch":7,"roll":33,"yaw":-29,"vgx":0,"vgy":0,"vgz":0,"templ":61,"temph":62,"tof":10,"h":0,"bat":43,"baro":39.96,"time":22,"agx":307,"agy":-324,"agz":-930}
```

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
