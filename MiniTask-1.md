# Project-1: Facial Recognition Door Using Windows IOT

### Decsription:
- Home security is a growing concern for a lot of people these days. To overcome this concern and to put home owners at ease, this door is designed such that it unlocks itself using facial recognition.
- If the software recognizes the face of the person standing in front of the door, the door automatically unlocks but if it doesnt recognize the face, the door stays locked.
- We can use either a Raspberry Pie or a Minnowboard MAX for this project though the later one is recommended.
- Facial recognition is done through Microsoft Face APIs hosted on microsoft azure.
- The brains of this solution runs on windows 10 IOT core running on Minnowboard MAX hardware.
- A standard USB camera is attached to the device's USB port along with a monitor and speaker attached to the devices HDMI port.
- The GPIO pin is used to control a relay switch which in turn locks and unlocks the door lock. The doorbell button is attached to the GPIO pin as well.
- Finally, a cloud based API, Project Oxford Face API is used for facial recognition.
- After assembly of the project, first step is to register the faces of the people which you want to have access to your house i.e. family members, relatives, close friends etc.
- Whenever someone wants to enter, they will press the doorbell. Then the camera will capture a photo of their face and the software will run the photo through its data base.
- If it finds a match, the door will open and the guest will be greeted via the speaker attached.
- If the software doesnt find a match, the door will remain locked and the guest will be told to step back.

### Personal notes:
- Along with a speaker, we can also add an OLED screen to display the welcome or the warning message.
- Instead of a normal webcam, we should use something like Intel RealSense Depth camera because a normal webcam cannot tell the difference between a photo and an actual person.
- We can also integrate an app with the system which notifies the owner whenever someone tries to access the door. And if any suspicious activity is detected by the camera, the app will alert the owner immediately.


# Project-2: Easy Motion and Gesture Detection by PIR Sensor & Arduino

### Description:
- In this project a PIR sensor and an Arduino nano is used to detect the motion of the hand which is used to increase or decrease the volume of the speaker.
- Hand guestures are detected using the TPA81 as PIR sensor which detects the thermal radiation emmitted by our hand.
- Instead of the TPA81, 8 PIR sensors can be used which is a much cheaper option. In this case the values from each of the PIR sensors are read one after the other.
- If separate PIR sensors are used, the PIR power pins shouldnt be connected to the arduino 5V power supply and an external power source is to be used.
- After setting up the TPA81, code is written in order to read the values from each of the 8 PIR sensors and the 8 element array is printed on the serial monitor.
- Then using an algorithm which detects a simple hand guesture of increasing and decreasing the volume, we can control the volume of the speakers.

### Visuals:
![gif](https://hackster.imgix.net/uploads/attachments/586349/gesture_detection_QY3OQN8byq.gif?auto=format%2Ccompress&gifq=35&w=900&h=675&fit=min&fm=mp4)

### Personal notes:
- I think that if we somehow implemented this module inside a laptop or a PC or any electronic device for that matter and added a bunch of more guestures to it then we can control the device entirely using hand guestures itself.


# Project-3: Density Based Traffic Signal System using Microcontroller

### Description:
- Nowadays controlling the traffic has become a major issue in every city because of exponential increase in the number of automobiles and time delays between traffic lights.
- In order to rectify this problem, this project has desiged a density based traffic light system.
- The traffic density is measured using IR sensors which inturn are connected to the microcontroller which controls the traffic lights.
- In this project the ATmega8 controller is used. Along with the controller, 4 IR sensors and 4 traffic lights are also needed.
- If there is traffic on the road then that particular IR sensors outputs zero otherwise it outputs 1.
- If a particular IR sensor outputs 0, green signal is given to that particular path and red signal is given to all other parts.
- We can allow a time delay of 1 minute for each path.
- Sometimes the device can be malfunctioning. The most commmon reason for ths is that sometimes the sensor also absorbs normal light.
- Another limitation of the project is that the IR sensor can only detect objects at short distances. So in an actual traffic light system, a different approach should be implemented in order to measure the traffic density.

### Schematic:
![Circuit](https://www.electronicshub.org/wp-content/uploads/2014/06/Density-Based-Traffic-Lights-System-Circuit-Diagram.jpg)

### Personal notes:
- In order to calculate the traffic density, instead of an IR sensor,a normal camera can be used to get a view of the road and using computer vision, we can count the number of cars on the road to get the traffic density.