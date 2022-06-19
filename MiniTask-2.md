# Project-1: [Facial Recognition Door Using Windows IOT](https://www.hackster.io/windows-iot/windows-iot-facial-recognition-door-e087ce)

**Problem Statement:** Designing a device that unlocks itself if it recognizes the face in front of the door camera and stays locked if it doesnt recognize the face.

**Ideation and Planning:** Understanding the working of the device
- *Doorbell -> Webcam -> PC -> Facial recognition API -> Microcotroller -> Relay switch -> Door*

**Part of the pipeline to break**

| Part of the Pipeline   | Feasibility                                                                | Advantages                                                                                                                            | Disadvantages                                                                                         |
|------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Camera                 | Webcams are moderately expensive and very easy to set up                   | Webcams will provide very high quality images making the facial recognition very accurate                                             | Webcams can be hacked quite easily which gives rise to security issues                                |
| PC                     | For this project any PC with an internet connection and windows 10 will do | A PC will make setting up the code very easy and faces which are to be recognized by the camera can be registered without much hassle | It can be very expensive to buy a new PC in case someone doesnt have one from before                  |
| Facial recognition API | Face detection will become very easy using an API                          | Very easy to implement. Even people who have no idea about machine learning can use it.                                               | There is the risk of the data getting leaked thus breaching the privacy of people visiting your house |
| Microcontroller        | --                                                                         | --                                                                                                                                    | --                                                                                                    |
| Relay switch           | --                                                                         | --                                                                                                                                    | --                                                                                                    |