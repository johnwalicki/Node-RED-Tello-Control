# Use Visual Recognition on drone pictures

### Alert - **[Watson Visual Recognition service](https://cloud.ibm.com/docs/visual-recognition?topic=visual-recognition-index) has been discontinued**
The steps in this section are no longer available.

The Tello has a low level protocol that allows you to take pictures.  This flow sends the take picture command and receives / reconstructs the picture data from the Tello.  Then it calls the Watson Visual Recognition service to classify what is in the image.

## Task
### Connect to the IBM Cloud
Use an ethernet cable to hardwire your laptop to your network so that it can reach the Internet.  Connect over WiFi to the Tello drone.

### Create a Watson Visual Recognition service instance
- Log into [IBM Cloud](http://cloud.ibm.com)
- Create a [Watson Visual Recognition service](https://cloud.ibm.com/catalog/services/visual-recognition)
- Returned to the [IBM Cloud Resources Dashboard](https://cloud.ibm.com/resources)
- Click on your Watson Visual Recognition instance
- Copy the Watson Visual Recognition API key to your clipboard.

![Watson Visual Recognition API Key](/docs/screenshots/Watson-Visual-Recognition-APIkey.png?raw=true "Watson Visual Recognition API Key")

### Configure your Node-RED Flow to use Watson visual recognition
- Return to your Node-RED browser window
- Recall that in [Setup / Part 2](/docs/PART2.md) you installed the **node-red-node-watson** nodes which provide a collection of Node-RED nodes for IBM Watson services
- Import the [solution flow](/flows/solutions/part8_solution.json)
- Double-click on the **visual recognition** node
- Paste the API key from the clipboard into the Visual Recognition node
- Click on the Done button
- See screenshot:

![Tello Watson Visual Recognition API Key](/docs/screenshots/NodeRED-Tello-VisualRecognition-APIkey.png?raw=true "Tello Watson Visual Recognition API Key")

### Solution

There is a [solution flow](/flows/solutions/part8_solution.json) available if you need help or want to check your solution.

![Tello Pictures Visual Recognition Dashboard Solution flow](/docs/screenshots/NodeRED-Tello-VisualRecognition-Solution-flow.png?raw=true "Tello Pictures Visual Recognition Dashboard Solution flow")

Launch the Node-RED Dashboard by turning to the Dashboard tab in the right menu and then click on the launch button.

![Tello Pictures Visual Recognition Dashboard Solution flow](/docs/screenshots/NodeRED-Tello-VisualRecognition-Solution.png?raw=true "Tello Pictures Visual Recognition Dashboard Solution")

---

[Home](/README.md) | [Node-RED](/docs/PART1.md) | [Setup](/docs/PART2.md) | [Commands](/docs/PART3.md) | [Dashboard](/docs/PART4.md) | [Telemetry](/docs/PART5.md) | [Mission](/docs/PART6.md) | [Pictures](/docs/PART7.md) | **Visual Recognition** | [Custom Classifier](/docs/PART9.md)

---
