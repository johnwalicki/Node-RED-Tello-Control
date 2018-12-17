# Use Visual Recognition on drone pictures

The Tello has a low level protocol that allows you to take pictures.  This flow sends the take picture command and receives / reconstructs the picture data from the Tello.  Ten it calls the Watson Visual Recognition service to classify what is in the image.

### Connect to the IBM Cloud
Use an ethernet cable to hardwire your laptop to your network so that it can reach the Internet.  Connect over WiFi to the Tello drone.

### Create a Watson Visual Recognition service instance
- Log into [IBM Cloud](http://cloud.ibm.com)
- Create a [Watson Visual Recognition service](https://cloud.ibm.com/catalog/services/visual-recognition)
- Returned to the [IBM Cloud Resources Dashboard](https://cloud.ibm.com/resources)
- Click on your Watson Visual Recognition instance
- Copy the Watson Visual Recognition API key to your clipboard.
- Paste the key into the Visual Recognition node in the flow.
![Watson Visual Recognition API Key](/docs/screenshots/Watson-Visual-Recognition-APIkey.png?raw=true "Watson Visual Recognition API Key")


### Solution

There is a [solution flow](/flows/solutions/part8_solution.json) available if you need help or want to check your solution.

![Tello Pictures Visual Recognition Dashboard Solution flow](/docs/screenshots/NodeRED-Tello-VisualRecognition-Solution-flow.png?raw=true "Tello Pictures Visual Recognition Dashboard Solution flow")

![Tello Pictures Visual Recognition Dashboard Solution flow](/docs/screenshots/NodeRED-Tello-VisualRecognition-Solution.png?raw=true "Tello Pictures Visual Recognition Dashboard Solution")

---

[Home](/README.md) | [Node-RED](/docs/PART1.md) | [Setup](/docs/PART2.md) | [Commands](/docs/PART3.md) | [Dashboard](/docs/PART4.md) | [Telemetry](/docs/PART5.md) | [Mission](/docs/PART6.md) | [Pictures](/docs/PART7.md) | **Visual Recognition**

---
