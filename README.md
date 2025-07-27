 
<h1>💙 CareBox : Smart Home Healthcare Assistant</h1>
CareBoxx is an integrated smart healthcare system designed to support disabled, elderly, and epileptic patients in home environments. It combines vital monitoring, automated medication delivery, and emergency seizure detection into a single connected ecosystem that ensures patients are cared for remotely and safely.

<h2>🩺 Overview</h2>
CareBoxx consists of three smart devices that work together:

<h2> 1.Wireless Health Monitoring System</h2>

<h3>🔹 Description</h3>
CareBoxx Vitals is a compact and smart wireless health monitoring system that helps patients—especially the elderly and those with chronic conditions—track their SpO2 (oxygen saturation), BPM (heart rate), and body temperature in real time. This module is a part of the broader CareBoxx ecosystem and is designed for seamless integration with mobile health applications.


<p align="center">
- Wireless Health Monitoring System - <br/>
<img src="https://i.imgur.com/DZUPfEp.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <img src="https://i.imgur.com/myMHlb0.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br />
<br />
<h3>🔸 How It Works</h3>
The system is composed of two interconnected BLE-enabled devices:

<h4>BLE Oximeter</h4>
A small sensor device that continuously measures:

- BPM (heart rate)

- SpO2 (blood oxygen level)

  
It then sends this data via Bluetooth Low Energy (BLE) to the second unit.

<h4>Vitals Receiver Unit (ESP32 Box)</h4>
This second, compact box includes:

 <h4> - ESP32 microcontroller</h4>

<h4> - MLX90614 infrared temperature sensor</h4>
It:

- Receives the BPM and SpO2 data over BLE

- Measures body temperature

- Packages all vitals data

- Sends it to the CareBoxx mobile app via BLE

<h3>App Integration & Auto-Diagnosis</h3>
Once the mobile app receives all vital data, it:

- Displays the current health stats

- Runs an auto-diagnostic based on thresholds to inform whether the values are within a healthy range or not

<p align="center">
- Application - <br/>
<img src="https://i.imgur.com/1QmlP1k.jpeg" height="25%" width="20%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/r7Au8yJ.jpeg" height="25%" width="20%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/NSi3FBj.jpeg" height="25%" width="20%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/g5oyHcm.jpeg" height="25%" width="20%" alt="Disk Sanitization Steps"/>
  <br />
<br />

<h3>🔹 Key Features </h3>

✅ Wireless BLE communication between sensors and central unit

✅ Real-time measurement of SpO2, BPM, and temperature

✅ Compact and low-power hardware setup

✅ Seamless BLE transmission to Android app

✅ Automatic diagnostic analysis of the vitals

✅ Patient-friendly interface

<h2> 2. RoboCare-lite </h2>

RoboCare-lite is a small automated box where the user (or caregiver) loads 3 doses of the day's pills—morning, afternoon, and evening. Here's how it functions:

🧠 BLE Connection: The device connects via Bluetooth Low Energy (BLE) to the CareBoxx mobile app.

📱 Smart Scheduling: The user opens the app and sets 3 medication reminders, each corresponding to a dose time.

🔕 Offline Operation: After setting the schedule, the app can be closed. The box stores the times internally.

⏰ Timed Alerts & Dispensing:

- When the set time arrives, RoboCare-lite triggers a buzzer alarm and blinks an LED.

- It then automatically distributes the correct dose using a servo-based mechanism.

- The system returns to idle mode until the next scheduled reminder.

<p align="center">
- Demo - <br/>
<img src="https://i.imgur.com/JTDzkSJ.jpeg" height="40%" width="40%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/WT7c73S.jpeg" height="40%" width="40%" alt="Disk Sanitization Steps"/>
  

  
 
  <br />
<br />

<h3>🔹 Key Features </h3>


✅ Bluetooth Low Energy (BLE) integration with mobile app

✅ Stores up to 3 pill doses for a full day

✅ Reminders can be programmed once daily

✅ Automatically dispenses pills at set times

✅ Buzzer + LED indicators for alarms

✅ Works without continuous app connection



<h2> 3. EpyCare </h2>

<h3>🔹 Description</h3>
EpyCare is a smart, wearable seizure detection system that leverages the onboard sensors of the Arduino Nano 33 BLE Sense to monitor user movement in real time. Designed for people with epilepsy or seizure-prone conditions, EpyCare aims to provide safety, autonomy, and peace of mind by detecting abnormal movement patterns and instantly notifying caregivers or family members.

This module is a part of the CareBoxx suite of assistive devices for health monitoring.

<h3>🔸 How It Works </h3>
<h4>- Motion Monitoring </h4>
- EpyCare uses the internal 9-axis IMU (accelerometer + gyroscope) of the Arduino Nano 33 BLE Sense to continuously analyze the user's movement.

<h4>Machine Learning Detection</h4>

</h5>A trained  model Using EdgeImpulse runs directly on the board to: </h5>

- Classify whether the current motion is normal or indicative of a seizure

- Avoid false alarms by intelligently distinguishing regular activity from seizure-like patterns

<h4>Seizure Alert Protocol </h4>
When a seizure is detected:

- A buzzer alarm is activated immediately to alert nearby people

- The board sends a BLE signal to the connected mobile app

<h4>App Response</h4>
The CareBoxx mobile app:

- Automatically retrieves the user’s GPS location

- Sends an SMS alert to pre-configured emergency contacts, including a message and location

<h3> 🔹 Key Features </h3>

✅ Real-time movement tracking with embedded IMU

✅ On-device Machine Learning with TinyML

✅ Immediate buzzer alarm for nearby awareness

✅ BLE communication with mobile app

✅ Location tracking and SMS-based emergency alert

✅ No internet required for detection or alerting




<h2>Components and Tools Used</h2>


