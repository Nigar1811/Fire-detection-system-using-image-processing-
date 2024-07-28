# Smart and Green Fire Detection System with Image Processing

## Overview
The Smart and Green Fire Detection System is a fire detection and alerting system that leverages image processing techniques, sensors, and solar energy to provide an efficient, eco-friendly solution for detecting fires. This system is designed to offer quick detection and alert notifications, helping to minimize the damage caused by fire accidents.

## Features
- **Sensors:** Utilizes flame and smoke sensors to detect fire.
- **Image Processing:** Employs Raspberry Pi for background subtraction, color detection, segmentation, and Sobel edge detection.
- **Alerts:** Sends notifications via buzzer, SMS, email, and phone calls to concerned authorities and registered users.
- **Eco-Friendly:** Powered by solar panels, ensuring operation during power outages.
- **Cost-Effective:** Designed to be economically feasible and easy to install.

## System Architecture
The system architecture consists of four main modules:

1. **Power Supply:**
   - Solar panels charge a lithium-ion battery.
   - Ensures the system operates during power outages.

2. **Sensor Module:**
   - **Flame Sensor:** Detects fire using IR light.
   - **Smoke Sensor:** Detects smoke concentration using MQ6 sensor.

3. **Processing Module:**
   - **Arduino Uno:** Interfaced with sensors, sends data to Raspberry Pi.
   - **Raspberry Pi:** Performs image processing, sends alerts, and handles communication.

4. **Alerting Module:**
   - **Buzzer:** Alerts people nearby.
   - **GSM Module:** Sends SMS and makes calls.
   - **USB Camera:** Captures images and videos for analysis.
   - **Email Notifications:** Sends images to the fire department via email.

## Workflow

1. **Detection:**
   - Sensors detect the presence of fire.
   - If confirmed, the Raspberry Pi turns on the camera.

2. **Image Processing:**
   - Captures video frames and converts them from RGB to HSV.
   - Applies background subtraction and segmentation techniques.
   - Detects fire using color detection algorithms and Sobel edge detection.

3. **Alerting:**
   - Buzzer sounds to alert people nearby.
   - GSM module sends SMS and calls registered numbers.
   - Emails images to the fire department.

## Installation

### Hardware Requirements
- Arduino Uno
- Raspberry Pi B+
- Flame Sensor (IR-based)
- Smoke Sensor (MQ6)
- USB Camera (Quantum, 30 MP)
- Solar Panels
- Lithium-Ion Battery
- GSM Module (GSM900A)

### Software Requirements
- Arduino IDE
- Python 3.8
- Raspberry Pi OS
- Twilio API (for SMS and email notifications)
- Google Maps API (for location services)

### Steps to Install

#### Hardware Setup:
1. Connect sensors to Arduino Uno.
2. Interface Arduino with Raspberry Pi.
3. Attach USB camera to Raspberry Pi.
4. Set up the solar panel and connect it to the battery.

#### Software Setup:
1. Install Arduino IDE and upload sensor code.
2. Install necessary Python libraries on Raspberry Pi.
3. Configure Twilio and Google Maps API for notifications.
4. Write and upload image processing and alerting code to Raspberry Pi.

## Usage

### Register User:
- Register your mobile number with the system.

### Monitor System:
- The system will continuously monitor for fire and smoke.
- Alerts will be sent automatically in case of fire detection.

### Respond to Alerts:
- Follow the SMS and email instructions to respond to the fire incident.
- Use the location provided in the SMS to reach the affected area.

## Results and Performance
- **Efficiency:** 85%
- **Accuracy:** 94%
- **Test Cases:** 20

### Performance Metrics:
- **NTP:** Number of True Positives
- **NFN:** Number of False Negatives
- **NTN:** Number of True Negatives
- **NFP:** Number of False Positives

The system has shown to be highly efficient and accurate in detecting fires and sending timely alerts, minimizing the potential damage from fire accidents.

## Future Enhancements
- Increase the number of test cases for more robust performance analysis.
- Incorporate more sensitive sensors to improve detection accuracy.
- Expand the system to cover larger areas with multiple sensor modules.

## References
Refer to the full paper for detailed methodology, algorithms, and experimental results. The references used in this project are listed in the paper.
