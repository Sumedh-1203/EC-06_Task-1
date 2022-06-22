# [Facial Recognition Door Using Windows IOT](https://www.hackster.io/windows-iot/windows-iot-facial-recognition-door-e087ce)

### Trouble shooting:
- The following is the order for working of the device:
  *Doorbell -> Webcam -> PC -> Facial recognition API -> Microcotroller -> Relay switch -> Door*
- If the device isnt working properly, there has to be a problem with one of the above components.
- Check each components one by one and find out which part of the device isnt working. Once you find where the error is, start debugging.

### Testing the doorbell:
- Here the doorbell is just the button which the user presses in order to activate the camera.
- Just make sure that the switch is working properly and that the PC recieves signals from the bell.

### Testing the webcam:
- If the facial recognition API isnt recieving the image of the person at the door then the webcam has some problem.
- Make sure that it is connected properly and the installation setup has been followed through completely and all the necessary drivers are installed.
- If the problem still persists, plug the webcam into another camera to see if its working. if the camera is not working on multiple computers then theres a fault in it and it needs to be changed. 
- If not, then see the antivirus settings on your computer which may be blocking acces to cameras for security reasons.

### Testing the PC:
- There is nothing as such to test here. Any decent PC with windows 10 and a reliable internet connection will work.

### Facial recognition API:
- Position the camera neatly so that the face of the person is clearly visible.
- Make sure that while setting up the code, the tutorial is followed thoroughly and go through the code once again if you think the code is wrong and cross verify.

### Testing the microcontroller: 
- The GPIO pins, pins to which the relay switch is connected doesnt have any inbuilt mechanisms to prevent shorting.
- So if the raspberry pie feels hot, it means you have shorted it.

### Testing the relay switch:
- Run the following code to check if the relay switch is working
```
Python
import RPi.GPIO as GPIO
GPIO.setmode(GPIO.BCM) # GPIO Numbers instead of board numbers
 
RELAIS_1_GPIO = 17
GPIO.setup(RELAIS_1_GPIO, GPIO.OUT) # GPIO Assign mode
GPIO.output(RELAIS_1_GPIO, GPIO.LOW) # out
GPIO.output(RELAIS_1_GPIO, GPIO.HIGH) # on
```
- If 0V is present at the relay pin, the corresponding LED lights up, at a HIGH level the LED goes out. So if you want the relay to open at a HIGH level, you need to connect the middle and left pins to the circuit. The LED is off there. If the relay is to open, if the LED is also on, middle and right OUT pins are connected.