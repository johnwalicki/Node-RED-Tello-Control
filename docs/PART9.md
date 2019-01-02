# Fly the Tello drone with custom Visual Recognition of drone pictures

Now that the Tello is taking pictures and classifying images using the default classifier, in this final challenge the Tello will fly, take pictures, classify images using a custom classifier.

## Task

### Train a Watson Visual Recogition Custom Classifier

Follow the instructions in this [tutorial](https://developer.ibm.com/tutorials/detect-wildfire-damaged-homes-using-drone-images-watson-visual-recognition/) to train a Watson Visual Recognition custom classifier.  You might take drone images of balls in your yard, your dog playing in your yard, leaves in your gutters, bird nests in trees.  Anything your Tello Drone might see.

### Watson Visual Recogition Custom Classifier Model ID

- Train a Watson Visual Recogition Custom Classifier using images of your choice.
- After training has completed, turn to the Project Asset Visual Recognition model **Overview** tab.
- Copy the **Model ID** to your clipboard.


![Watson Visual Recognition Custom Classifier Model ID](/docs/screenshots/WatsonStudioVisualRecognitionCustomClassifier.png?raw=true "Watson Visual Recognition Custom Classifier")

### Configure your Node-RED Flow to fly your Tello while taking pictures and classifying images

- Return to your Node-RED browser window
- Import the [solution flow](/flows/solutions/part9_solution.json)
- Turn on your drone and connect to the drone Wifi
- Manually press the **TELLO_LOW_LEVEL_CONNECT** inject node.
- Turn to the Node-RED Dashboard - Tello Camera Dashboard.
- Paste the Model ID into the dashboard
- Press the button to start taking pictures every 10 seconds.
- TakeO-Off
- See screenshot:

![Tello Watson Visual Recognition API Key](/docs/screenshots/NodeRED-Tello-VisualRecognition-APIkey.png?raw=true "Tello Watson Visual Recognition API Key")

### Solution

There is a [solution flow](/flows/solutions/part9_solution.json) available if you need help or want to check your solution.

![Tello Custom Classifier Visual Recognition Dashboard Solution flow](/docs/screenshots/NodeRED-Tello-CustomClassifierVisualRecognition-Solution-flow.png?raw=true "Tello Custom Classifier Visual Recognition Dashboard Solution flow")

Launch the Node-RED Dashboard by turning to the Dashboard tab in the right menu and then click on the launch button.

![Tello Custom Classifier Visual Recognition Dashboard Solution Developer Selfie](/docs/screenshots/NodeRED-Tello-DeveloperSelfie.png?raw=true "Tello Custom Classifier Visual Recognition Dashboard Solution")

---

[Home](/README.md) | [Node-RED](/docs/PART1.md) | [Setup](/docs/PART2.md) | [Commands](/docs/PART3.md) | [Dashboard](/docs/PART4.md) | [Telemetry](/docs/PART5.md) | [Mission](/docs/PART6.md) | [Pictures](/docs/PART7.md) | [Visual Recognition](/docs/PART8.md) | **Custom Classifier**

---
