Obstacle Avoiding Robot Car using Arduino
Description
This project implements an autonomous obstacle-avoiding robot car using an Arduino microcontroller, an ultrasonic distance sensor, a servo motor, and an L298N motor driver. The robot scans its surroundings using a servo-mounted ultrasonic sensor and makes real-time movement decisions to avoid obstacles without human intervention.

Working Principle
The ultrasonic sensor is mounted on a servo motor that sweeps across multiple predefined angles. At each angle, the distance to nearby objects is measured and stored. If any obstacle is detected within a threshold distance of 30 cm, the robot performs an avoidance maneuver; otherwise, it continues moving forward.
A motor test routine runs at startup to verify proper motor operation and wiring.

Components Used
Arduino Uno
HC-SR04 Ultrasonic Sensor
Servo Motor (SG90 or equivalent)
L298N Motor Driver
Two DC Motors
Robot Chassis
Jumper Wires
External Power Supply / Battery Pack

Pin Configuration

Ultrasonic Sensor
| Signal | Arduino Pin |
| ------ | ----------- |
| Trig   | 13          |
| Echo   | 12          |

Servo Motor
| Signal  | Arduino Pin |
| ------- | ----------- |
| Control | 11          |

L298N Motor Driver
| Motor | Enable Pin | Direction Pins   |
| ----- | ---------- | ---------------- |
| Left  | 6          | IN1 = 7, IN2 = 5 |
| Right | 3          | IN3 = 4, IN4 = 2 |

Sensor Sweep Configuration
The ultrasonic sensor scans the environment at the following angles:
60°, 70°, 80°, 90°, 100°, 110°, 120°

This provides a wide forward field of view for obstacle detection.

Key Features
Servo-based ultrasonic scanning
Real-time obstacle detection
Independent control of left and right motors
PWM-based speed control
Automatic obstacle avoidance
Motor diagnostic test on startup

Distance Measurement
Distance is calculated using ultrasonic time-of-flight
Speed of sound assumed: 343 m/s
Distance output is in millimeters
Timeout handling returns a maximum distance of 4000 mm

Setup Instructions
Hardware Setup
  Assemble the robot chassis.
  Connect DC motors to the L298N motor driver.
  Mount the ultrasonic sensor on the servo motor.
  Connect all components according to the pin configuration table.
Software Setup
  Install the Arduino IDE.
  Ensure the Servo.h library is available.
  Upload the provided Arduino sketch to the board.
Execution
  Power on the robot.
  Observe the motor test routine.
  The robot will begin autonomous navigation.

Possible Enhancements
Implement PID-based motor control
Use weighted angle-based decision logic
Add Bluetooth or Wi-Fi control
Integrate additional sensors (IR, line sensors)
Log sensor data for analysis

Learning Outcomes
Arduino and Embedded C programming
Motor control using L298N
Servo and ultrasonic sensor integration
Real-time decision-making in robotics
Debugging hardware–software systems

Author
Raj
B.Tech Student
