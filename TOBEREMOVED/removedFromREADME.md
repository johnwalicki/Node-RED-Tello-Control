# TO BE REMOVED OR REFACTORED INTO DOCS FOLDER CONTENT

This content has been removed from the readme.md file.  Rather than deleting it, it has been temporarily moved here until it can be reused.

## Node-RED flows in this repository

### Send Commands to a Tello Drone

- This [flow](/flows/nodered-tello-controls.json) demonstrates how to send individual commands to the Tello Drone.
  - Each **inject** node, will send a single command to the Tello.  Units are in centimeters or degrees.
  - A list of commands can be found in the [Tello SDK documentation](https://dl-cdn.ryzerobotics.com/downloads/Tello/Tello%20SDK%202.0%20User%20Guide.pdf)

![Tello Control Flow](/docs/screenshots/NodeRED-Tello-Controls-flow.png?raw=true "Tello Control flow")

___

### Execute a Pre-Programmed Flight Plan

- This [flow](/flows/nodered-tello-missions.json) sends a pre-programmed flight plan to the Tello Drone
  - Edit the Template nodes to construct your own pre-programmed Tello path
    - Double click on the Template nodes to enter the list of Tello commands
    - Recall that the SDK pdf has a list of valid commands
    - Each line should contain the following instructions:  
     *command*,*distance (cm)|rotation degrees*,*optionally the delay time (milliseconds) until next command is sent*  
     eg.
      ```text
      command,0,250
      takeoff,0
      up,25,5000
      cw,90
      land,0
      ```
    - The command *command* initializes the drone to receive instructions.
    - A *0* for the distance just tells the flow that no units are necessary and is only required if you want to set a delay.
  - Wire the Tello command set that you want to execute into the **Initialize Mission** and **Split** nodes.
  - Start the mission by pressing the **inject** node labeled **Run Mission**
  - If the Tello goes out of control, click on the **Abort Mayday Abort** inject node. It will send a *emergency* command to the Tello to immediately stop the propellers.

![Tello Missions Flow](/docs/screenshots/NodeRED-Tello-Missions-flow.png?raw=true "Tello Missions flow")

___

### Node-RED Tello Controls Dashboard Example

- This [flow](/flows/nodered-tello-controls-dashboard.json) builds a Node-RED dashboard of commands that control the drone
  - The Inject nodes from the first flow have been replaced with Node-RED dashboard **Button** nodes
  - Node-RED dashboard **Button** nodes can be customized with colors and Font Awesome icons
  - Each Node-RED dashboard group contains a column of related Tello commands
  - Each **Flight Path** button sends the Tello command and 50cm distance - which is a reasonable compromise for indoor testing but could be extended for outdoor flight
  - The **Rotation** buttons send the specified degrees rotation in the clockwise or counter-clockwise directions of the button icon
  - The **Flips!** buttons flip the drone in the direction specified

![Tello Controls Dashboard Buttons](/docs/screenshots/NodeRED-Tello-Controls-Dashboard.png?raw=true "Tello Telemetry Dashboard buttons")
![Tello Controls Dashboard Flow](/docs/screenshots/NodeRED-Tello-Controls-Dash-flow.png?raw=true "Tello Controls Dashboard flow")

___

### Node-RED Tello Telemetry Dashboard Example - Experimental

- This [flow](/flows/nodered-tello-telemetry.json) reads the telemetry data from the drone and displays some of the data in a Node-RED Dashboard.
  - The complete command set of telemetry data has not been fulled documented by Ryze.
- This flow is experimental and does not fully function. Patches are welcome.

![Tello Telemetry Dashboard Gauges](/docs/screenshots/NodeRED-Tello-Telemetry-gauges.png?raw=true "Tello Telemetry Dashboard gauges")
![Tello Telemetry Dashboard Flow](/docs/screenshots/NodeRED-Tello-Telemetry-flow.png?raw=true "Tello Telemetry Dashboard flow")