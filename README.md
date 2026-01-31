Ultrasonic Radar System using Arduino and Processing
Project Description
This project implements a real-time ultrasonic radar system using an Arduino, an HC-SR04 ultrasonic sensor, a servo motor, and a Processing-based graphical interface. The ultrasonic sensor scans the environment by rotating on a servo motor, while Processing visualizes detected objects in a radar-style display.

System Overview
The Arduino controls the servo motor to rotate the ultrasonic sensor between 15° and 165°. At each angle, the distance to nearby objects is measured and transmitted over serial communication. The Processing application receives this data and renders a live radar visualization showing object position and distance.

Components Used
Hardware
  Arduino Uno
  HC-SR04 Ultrasonic Sensor
  Servo Motor (SG90 or equivalent)
  Jumper Wires
  USB Cable
Software
Arduino IDE
Processing IDE

Pin Configuration (Arduino)
| Component       | Arduino Pin |
| --------------- | ----------- |
| Ultrasonic Trig | 10          |
| Ultrasonic Echo | 11          |
| Servo Signal    | 12          |

Working Principle
The servo motor rotates the ultrasonic sensor from 15° to 165° and back.
At each angle, the ultrasonic sensor measures distance using time-of-flight.
Arduino sends angle and distance data via serial communication.
Processing reads the data and plots it on a radar-style GUI.
Objects within 40 cm are highlighted on the radar display.

Data Format (Serial Communication)
The Arduino sends data in the following format:
  angle,distance.
Example:
  90,23.
angle → Servo angle in degrees
distance → Measured distance in centimeters

Radar Visualization (Processing)
  Green arcs represent distance ranges (10 cm to 40 cm)
  A rotating sweep line shows the current sensor angle
  Red markers indicate detected objects
  Live angle and distance values are displayed on screen

Setup Instructions
Arduino
  Connect the ultrasonic sensor and servo motor according to the pin configuration.
  Upload the Arduino sketch to the board.
  Open the Serial Monitor and verify data output at 9600 baud.
Processing
  Open the Processing sketch.
  Update the serial port name (e.g., COM5) if required.
  Run the sketch to view the radar visualization.
  
Adjustable Parameters
  Servo sweep range: 15° – 165°
  Maximum detection range: 40 cm
  Serial baud rate: 9600
  Screen resolution: 1200 × 700

Applications
  Object detection and ranging
  Robotics and navigation systems
  Basic radar simulation
  Embedded systems and IoT learning projects

Learning Outcomes
  Arduino sensor interfacing
  Servo motor control
  Serial communication
  Real-time data visualization using Processing
  Coordinate transformation and trigonometry

Possible Enhancements
  Increase detection range
  Add obstacle classification
  Improve visualization scaling
  Integrate wireless communication
  Convert Processing UI to Python or Web-based visualization

Author
Raj
B.Tech Student
