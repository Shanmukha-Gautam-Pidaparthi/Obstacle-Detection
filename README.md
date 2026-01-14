# Obstacle Detection Robot using Arduino

**Overview**

This project focuses on building an autonomous obstacle detection robot using an Arduino Uno, an ultrasonic distance sensor, and a motor driver module.
The robot detects obstacles in its path, stops, evaluates alternate directions, and navigates accordingly without human intervention.

Obstacle detection is widely used in autonomous robots, warehouse automation, assistive systems, and self-driving vehicles.
This build demonstrates the core principles behind such systems in a compact and cost-effective implementation.

<img width="960" height="447" alt="image" src="https://github.com/user-attachments/assets/1939af6f-ac47-4c96-a3fe-51573a8b7a52" />


**Features**

- Detects obstacles using an ultrasonic sensor
- Makes decisions to move forward, stop, reverse, or turn
- Uses servo-mounted sensor to scan left and right
- Fully autonomous movement
- Built entirely using open-source components and Arduino libraries

**Hardware Components**

- Microcontroller System
- Arduino Uno R3
- L298N Dual H-Bridge Motor Driver

**Locomotion**
- Chassis (wood or plastic)
- Two DC motors with wheels
- Servo motor for directional scanning

**Sensors**
- Ultrasonic sensor (HC-SR04)
- Supporting Electronics
- Battery (portable DC power supply)
- Connecting jumper wires

**Circuit Diagram**
- The wiring diagram includes connections between:
- HC-SR04 → Arduino trigger and echo pins
- L298N → Motor outputs and PWM pins
- Arduino → Servo control pin
- Battery → Motor driver power input

<img width="960" height="447" alt="image" src="https://github.com/user-attachments/assets/a69126ad-09db-4a37-a923-bd4849d2b8a6" />


**Software & Libraries**
- Arduino Libraries Used
- Servo.h — Servo motor control
- NewPing.h — Ultrasonic distance measurement

**Arduino Code**
The project consists of five major modules implemented in the Arduino sketch:
1. Initialization of pins and peripherals
2. Continuous distance measurement using ultrasonic sensor
3. Decision making inside loop() to choose movement direction
4. Movement functions (forward, backward, stop, left turn, right turn)
5. Scanning functions using servo for left and right look

Full runnable code is available in the project

**How It Works**

The ultrasonic sensor constantly measures the distance ahead.  
If no obstacle is detected within a threshold (15 cm), the robot moves forward.  
When an obstacle is detected, the robot:  
Stops  
Moves backward briefly  
Rotates its servo sensor to scan left and right  
Compares distance readings  
Turns towards the direction with more free space  
Movement resumes once a clear path is available.  


**Real-World Applications**

Obstacle avoiding robots are commonly used in:
- Warehouse logistics and inventory robots
- Self-driving vehicle perception systems
- Assistive medical delivery robots
- Search-and-rescue in unsafe environments
- Household robots like robotic vacuums

**Project Outcome**

During testing, the robot:  
Successfully detected obstacles within the preset range  
Made autonomous directional decisions  
Avoided collisions consistently  
Reacted within approximately 0.5 seconds  
