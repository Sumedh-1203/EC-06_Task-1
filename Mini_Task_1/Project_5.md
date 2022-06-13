# Easy Motion and Gesture Detection by PIR Sensor & Arduino

### About
- In this project we use a PIR sensor and an arduino nano to detect the motion of the hand which is used to increase or decrease the volume of the speakers.

![Working of the device](https://hackster.imgix.net/uploads/attachments/586349/gesture_detection_QY3OQN8byq.gif?auto=format%2Ccompress&gifq=35&w=900&h=675&fit=min&fm=mp4)

### Working
- We can detect hand guesture using the TPA81 as PIR sensor which detects the thermal radiation emmitted by our hand.
- Instead of the TPA81, we can use 8 PIR sensors instead which is a much cheaper option and read the values from each of the PIR sensor one after the other.
- If we use the separate PIR sensors, we shouldnt connect the PIR power pins to the arduino 5V power supply and use an external power source.
- After setting up the TPA81, we write the code so that the device detects and prints the value of the temperature of the object in front of each of the 8 PIR sensors.
- Then we write an algorithm to detect a simple hand guesture of increasing and decreasing the volume.

### My suggestions
- I think that if we somehow implemented this module inside a laptop or a PC and added a bunch of more guestures to it then we can control the laptop/PC using hand guestures itself.