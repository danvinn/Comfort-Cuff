## 🩸 Smart Blood Pressure Monitor | ComfortCuff

### Problem Statement 🚨

Blood pressure monitoring is crucial for cardiovascular health, yet common issues like "white coat hypertension" and "masked hypertension" can lead to inaccurate readings. Additionally, traditional monitoring methods may cause discomfort, especially in sensitive groups like children and the elderly.

### Solution 💡

Introducing a revolutionary at-home blood pressure monitor! Our device eliminates stress and discomfort by utilizing a string pulley system, providing accurate readings without the familiar sound and feel of conventional gauges. It empowers users to control their monitoring environment, ensuring reliable results.

### Code Implementation 🖥️

Our system, driven by an Arduino Uno, offers two modes via Bluetooth:
- **Forward Rotation:** Command "1" for clockwise rotation at 125 RPM.
- **Reverse Rotation and Slow Stop:** Command "0" initiates counterclockwise rotation at 105 RPM, gradually slowing to a stop after 5 seconds.

### Bluetooth Interface 📱

The HC-05 Bluetooth module establishes a wireless link between the Arduino and a smartphone. Commands from a user-friendly app control motor speed and direction. 

### Possible Enhancements 🚀

1. **Speed Control:** Implement finer speed adjustments through Bluetooth commands.
2. **Safety Features:** Integrate emergency stop commands and additional safety checks.
3. **User Interface:** Develop a graphical smartphone app for intuitive motor control.

### Outcome 🎉

Our motor control system offers versatility and remote controllability, making it adaptable for various applications. The modular design allows for future enhancements, ensuring longevity and customization based on specific needs.

### Hardware Implementation 🛠️

Components:
- Arduino Uno
- L298N Driver
- DC Motor
- HC-05 Bluetooth Module
- Moto G5
- 2x 9V Batteries

The system, powered by the Arduino Uno, communicates with the Bluetooth module, controlling the L298N driver and the DC motor. The Bluetooth module connects to a mobile terminal app on the Moto G5, allowing instructions to be conveyed to the microcontroller.

### Limitations 🛑

- Insufficient motor power impacted full arm band constriction.
- Lack of a pressure sensor prevented blood pressure measurement.
- Overly sensitive buttons hindered implementing an automatic safety response.

### Conclusion 🌐

In conclusion, our project addresses challenges in blood pressure monitoring with an innovative, stress-free system. Despite limitations, the Arduino-based solution, coupled with Bluetooth control, shows promise for accurate and comfortable measurements. The modular design paves the way for future improvements, making it a viable alternative for various settings.

### Citations 📚

Booth III, John N., et al. “Proportion of US Adults Recommended Out-of-Clinic Blood Pressure Monitoring According to the 2017 Hypertension Clinical Practice Guidelines.” Hypertension (Dallas, Tex. : 1979), U.S. National Library of Medicine, pubmed.ncbi.nlm.nih.gov/31230550/. Accessed 28 Jan. 2024. 
