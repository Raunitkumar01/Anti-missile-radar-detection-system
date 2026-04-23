# Anti-missile-radar-detection-system

This project creates a radar system using an ultrasonic sensor and a servo motor connected to Arduino. The Arduino sends angle and distance data to Processing, which displays it as a radar screen.

⚙️ Working Principle
The servo motor rotates from 15° to 165°
angle,distance.

At each angle, the ultrasonic sensor (HC-SR04) measures distance

Arduino sends data in format:
Processing Code Functionality
 1. Serial Communication
Uses processing.serial.* library

Reads incoming data from Arduino

Extracts:

Angle

Distance

2. Radar Display
Draws semi-circular arcs like a real radar

Displays angle lines

Creates a green scanning effect

3. Sweep Line
A rotating green line shows current scanning angle

Moves according to servo position
Visual Representation
Red Line → Object is present

Green Line → No object detected

Distance is converted from cm → pixels for display
4. Object Detection Logic
The key part of your code:

if (iDistance > 2 && iDistance < 80)

