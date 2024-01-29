<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Smart Blood Pressure Monitor</title>
</head>

<body>

    <h1>🩸 Smart Blood Pressure Monitor</h1>

    <h2>Problem Statement 🚨</h2>

    <p>
        Blood pressure monitoring is crucial for cardiovascular health, yet common issues like "white coat hypertension"
        and "masked hypertension" can lead to inaccurate readings. Additionally, traditional monitoring methods may cause
        discomfort, especially in sensitive groups like children and the elderly.
    </p>

    <h2>Solution 💡</h2>

    <p>
        Introducing a revolutionary at-home blood pressure monitor! Our device eliminates stress and discomfort by
        utilizing a string pulley system, providing accurate readings without the familiar sound and feel of conventional
        gauges. It empowers users to control their monitoring environment, ensuring reliable results.
    </p>

    <h2>Code Implementation 🖥️</h2>

    <p>
        Our system, driven by an Arduino Uno, offers two modes via Bluetooth:
    </p>

    <ul>
        <li><strong>Forward Rotation:</strong> Command "1" for clockwise rotation at 125 RPM.</li>
        <li><strong>Reverse Rotation and Slow Stop:</strong> Command "0" initiates counterclockwise rotation at 105 RPM,
            gradually slowing to a stop after 5 seconds.</li>
    </ul>

    <h2>Bluetooth Interface 📱</h2>

    <p>
        The HC-05 Bluetooth module establishes a wireless link between the Arduino and a smartphone. Commands from a
        user-friendly app control motor speed and direction.
    </p>

    <h2>Possible Enhancements 🚀</h2>

    <ol>
        <li><strong>Speed Control:</strong> Implement finer speed adjustments through Bluetooth commands.</li>
        <li><strong>Safety Features:</strong> Integrate emergency stop commands and additional safety checks.</li>
        <li><strong>User Interface:</strong> Develop a graphical smartphone app for intuitive motor control.</li>
    </ol>

    <h2>Outcome 🎉</h2>

    <p>
        Our motor control system offers versatility and remote controllability, making it adaptable for various
        applications. The modular design allows for future enhancements, ensuring longevity and customization based on
        specific needs.
    </p>

    <h2>Hardware Implementation 🛠️</h2>

    <p>
        Components:
    </p>

    <ul>
        <li>Arduino Uno</li>
        <li>L298N Driver</li>
        <li>DC Motor</li>
        <li>HC-05 Bluetooth Module</li>
        <li>Moto G5</li>
        <li>2x 9V Batteries</li>
    </ul>

    <p>
        The system, powered by the Arduino Uno, communicates with the Bluetooth module, controlling the L298N driver
        and the DC motor. The Bluetooth module connects to a mobile terminal app on the Moto G5, allowing instructions
        to be conveyed to the microcontroller.
    </p>

    <h2>Limitations 🛑</h2>

    <ul>
        <li>Insufficient motor power impacted full arm band constriction.</li>
        <li>Lack of a pressure sensor prevented blood pressure measurement.</li>
        <li>Overly sensitive buttons hindered implementing an automatic safety response.</li>
    </ul>

    <h2>Conclusion 🌐</h2>

    <p>
        In conclusion, our project addresses challenges in blood pressure monitoring with an innovative, stress-free
        system. Despite limitations, the Arduino-based solution, coupled with Bluetooth control, shows promise for
        accurate and comfortable measurements. The modular design paves the way for future improvements, making it a
        viable alternative for various settings.
    </p>

    <h2>Citations 📚</h2>

    <p>
        Booth III, John N., et al. “Proportion of US Adults Recommended Out-of-Clinic Blood Pressure Monitoring
        According to the 2017 Hypertension Clinical Practice Guidelines.” Hypertension (Dallas, Tex. : 1979), U.S.
        National Library of Medicine, <a
            href="https://pubmed.ncbi.nlm.nih.gov/31230550/" target="_blank">pubmed.ncbi.nlm.nih.gov/31230550/</a>.
        Accessed 28 Jan. 2024.
    </p>

</body>

</html>
