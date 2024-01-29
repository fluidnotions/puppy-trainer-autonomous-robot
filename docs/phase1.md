**Project Objective**: 
To create an automated system that tracks a dog's movements within a flat and records videos of its actions for creating a dataset for supervised machine learning.

**Components**:
1. **ESP32W Rover with Camera**: 
   - Used for video recording and data transmission.
   - Equipped with ultrasonic sensors for obstacle avoidance.
   - Receives Bluetooth signals to track the dog.

2. **Dog Collar with Bluetooth Module**:
   - A lightweight Bluetooth Low Energy (BLE) module (like Nordic nRF Series or Adafruit Bluefruit) is recommended for its low power consumption and effective range.
   - The module sends out Bluetooth signals that the rover uses to locate and follow the dog.

**System Workflow**:
1. **Data Collection Setup**:
   - The dog wears a collar equipped with a BLE module.
   - The ESP32W rover is programmed to follow the Bluetooth signal from the collar.

2. **Tracking Mechanism**:
   - The rover uses the strength of the Bluetooth signal (Received Signal Strength Indicator, RSSI) to determine its proximity to the dog.
   - The system functions like a "hot and cold" game, where the rover moves towards stronger signals ("hotter") and away from weaker ones ("colder").

3. **Video Recording**:
   - The rover's camera continuously records video while it follows the dog.
   - The video stream is transmitted over Wi-Fi to a computer for storage and dataset creation.

4. **Obstacle Avoidance**:
   - The rover utilizes ultrasonic sensors to navigate around obstacles while tracking the dog.

5. **Power Management**:
   - The BLE module on the dog's collar should be set to a low power mode to conserve battery, waking up at intervals to transmit the Bluetooth signal.
   - The ESP32W rover should be equipped with a sufficient power source to handle extended periods of operation.

**Software Aspects**:
- Programming the rover for Bluetooth signal tracking and obstacle avoidance.
- Setting up the BLE module on the dog's collar for optimal power consumption and signal transmission.
- Implementing data transmission and storage solutions for the video feed.

**Testing and Calibration**:
- Thorough testing in the flat to calibrate the tracking accuracy and responsiveness of the rover.
- Adjusting the Bluetooth signal transmission frequency and power settings on the dog's collar for the best balance between tracking accuracy and battery life.

**Final Objective**:
The system will autonomously track the dog and record its actions, providing a rich dataset of video footage for training a machine learning model to recognize specific dog actions.
