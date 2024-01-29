## Problem

Blood pressure is one of the most important metrics for monitoring cardiovascular health. It can be used to identify numerous cardiovascular diseases like coronary artery disease and kidney disease, as well as alert people who are at increased risk of heart attack, stroke, and more. With such a key component of our health, it is important that we take the most accurate blood pressure measurements as possible, yet there are a variety of problems that healthcare professionals experience during their appointments that can hinder the proper diagnosis of their patient’s health issues. 
One of the most common issues with blood pressure monitoring is known as “white coat hypertension.” This occurs when blood pressure rises higher than normal because a patient is experiencing anxiety due to being in a medical setting, which can inflate blood pressure readings, making them inaccurate. According to a study on the proportion of American adults recommended Out-Of-Clinic Blood Pressure monitoring, roughly 93% of adults who measured high blood pressure in a medical setting met the criteria for white coat hypertension, as when monitoring blood pressure at home, their results fell within the normal range.
In contrast to white coat hypertension, “masked hypertension” occurs when patients feel more relaxed in a medical setting, causing blood pressure to fall within an appropriate range when it otherwise shouldn’t. Following the same study on the proportion of American adults recommended Out-Of-Clinic Blood Pressure monitoring, 33% of Americans met the criteria for masked hypertension, as their blood pressure when monitored at home was found to be more problematic than expected when measured in the medical office, 
Another issue comes from groups of people who are more sensitive to pain or discomfort, especially small children or elderly people. Most blood pressure readings are taken by wrapping a patient’s arm and inflating the wrap around the arm until the circulation in the arm is cut off, which can cause pain or discomfort. Pain and discomfort increase heart rate, which may result in inaccurate blood pressure readings. 

## Solution
With other at-home blood pressure monitors on the market, our blood pressure monitor is not the first at-home blood pressure monitoring system on the market, however, our monitor seeks to eliminate the stress and discomfort of checking blood pressure. Even when taking blood pressure at home using an upper-arm wrap, the sound and feeling of air being pumped into the wrap may still instigate feelings of stress and anxiety in users. By utilizing a string pulley system to monitor blood pressure, our device seeks to eliminate the all-too-familiar sound and feel of conventional blood pressure gauges. 
But what of wrist or finger blood pressure readers? Surely people who experience anxiety with upper-arm pressure monitors can use those. The issue with wrist and finger monitors is that these points of monitoring are further from the heart and main arteries where blood is being pumped. These “extremities” often result in less accurate readings. 
Our device creates a less stressful environment by allowing the patient to have control over the blood pressure monitor while also monitoring their blood pressure in an environment that feels safe. Not only will it allow patients to have control over their own limits, but it also allows a much more convenient option for those who regularly or frequently need to check their blood pressure without the worry of false measurements.


## Code Implementation:

The system allows the motor to be controlled in two modes:

Forward Rotation: When the command "1" is received through the Bluetooth connection, the motor rotates in the forward direction at a speed of 125 (adjustable).

Reverse Rotation and Slow Stop: When the command "0" is received through the Bluetooth connection, the motor reverses direction at a speed of 105 (adjustable). After a delay of 5 seconds, the motor gradually slows down and comes to a complete stop.

## Bluetooth Interface

The Bluetooth module (HC-05) is used to establish a wireless connection between the Arduino and a smartphone. The system interprets commands received through Bluetooth and adjusts the motor control accordingly.

## Implementation

The Arduino code utilizes the SoftwareSerial library to communicate with the Bluetooth module using UART protocol. The 5 Volt pin of the module is inserted into the 5V slot of the Arduino, and the GND pin on the module is inserted into the GND slot of the Arduino. This establishes a closed loop between the 2 devices and allows us to perform our motor control. 

The motor control functions (`motorControl`) adjust the speed and direction of the motor based on the received commands. The system is designed to provide flexibility for integration with custom smartphone applications.

Example: **motorControl(125, HIGH. LOW) - Parameter one establishes 125 rev / min, parameter two determines the direction1 of the wheel, in this case, clockwise. The final parameter determines the direction2**


## Possible enhancements to consider for future development:

1. Speed Control: Implement finer speed control options through Bluetooth commands.
2. Safety Features: Integrate emergency stop commands and safety checks.
3. User Interface: Develop a user-friendly smartphone application with a graphical interface for motor control.




## Outcome:

The proposed motor control system with Bluetooth interface aims to provide a versatile and remote-controllable solution for various applications. The project's modular design allows for future enhancements and customization based on specific requirements.

## Hardware Implementation:

Components Utilized:
Arduino Uno
L298N Driver
DC Motor
HC-05 Bluetooth Module
Moto G5
2 9V Batteries

The controller we used was the Arduino Uno, and utilizing the Arduino IDE, code was developed and programmed onto the microcontroller. Then, jumper cables were used to connect the L298N driver to the Uno, allowing the code from the microcontroller to be conveyed to the driver, which then supplies the proper voltage to the DC Motor, causing it to spin in whichever direction was supplied voltage. 
There are 3 pins on the driver that dictate the motor's clockwise rotation, counter-clockwise rotation, and rotational speed. To properly maintain a stable voltage within the system, a common ground was utilized between the Arduino Uno and the driver to prevent any electrical shortages. 
With regards to the Bluetooth module, the transmit pin of the module was connected to the receive pin of the microcontroller, and the receive pin of the module was connected to the transmit pin of the microcontroller, allowing the module to communicate instructions to the microcontroller, and vice-versa. 
The actual instructions that the module communicates to the microcontroller are based on the instructions that were put in the mobile terminal app that was utilized on the Moto G5. This specific phone was utilized as iOS devices do not allow certain unlicensed devices/modules to connect to their devices. 
Thus, the open-source nature of the Moto G5 allowed for the communication of instructions from a mobile terminal to the Bluetooth module, which then instructs the microcontroller to supply a certain instruction to the driver. 


## Limitations

A lack of motor power from the motor used didn’t fully allow for the arm band to constrict all the way through because the arm resistance was greater. Another problem was a lack of a pressure sensor to be able to measure blood pressure in the first place because there’s a specific one required. The buttons given were too sensitive, so it couldn’t be implemented in between the bands as an automatic response to 
unwrap as a safety net due to recommendations that it shouldn’t be too tight. 


## Conclusion

In conclusion, the project aims to tackle significant challenges in blood pressure monitoring by introducing an innovative blood pressure system that addresses issues like "white coat hypertension" and "masked hypertension." Utilizing a unique string pulley system, the blood pressure monitor seeks to eliminate the stress and discomfort associated with traditional upper-arm pressure monitors. 

The Arduino-based system, integrated with an HC-05 Bluetooth Module, allows remote control via a smartphone application, providing a convenient and stress-free experience for users. Despite hardware limitations impacting full arm band constriction and the absence of a pressure sensor, the project's modular design allows for future enhancements, such as finer speed control options and additional safety features. 

The proposed blood pressure monitoring system demonstrates versatility and potential for further development, offering an alternative solution for accurate and comfortable blood pressure measurements in various settings.


Citation
Booth III, John N., et al. “Proportion of US Adults Recommended Out-of-Clinic Blood Pressure Monitoring According to the 2017 Hypertension Clinical Practice Guidelines.” Hypertension (Dallas, Tex. : 1979), U.S. National Library of Medicine, pubmed.ncbi.nlm.nih.gov/31230550/. Accessed 28 Jan. 2024. 
