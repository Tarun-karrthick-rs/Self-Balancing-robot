# Self-Balancing Robot 🚀

This repository contains the design, implementation, and code for a **Self-Balancing Robot** built using an Arduino microcontroller, L298N motor driver, BO motors, MPU6050 sensor, and a lightweight foam board chassis. The project demonstrates the principles of robotics, control systems, and sensor integration.

## Project Overview 🌟

The self-balancing robot mimics the balancing mechanism of humans, maintaining its stability on two wheels. By utilizing a **Proportional-Integral-Derivative (PID)** control algorithm and real-time orientation data from the MPU6050 sensor, the robot adjusts motor speeds dynamically to remain upright.

### Key Features:
- **PID Control**: Ensures stable balance by dynamically adjusting motor speed and direction.
- **MPU6050 Sensor**: Provides precise real-time orientation data.
- **Lightweight Design**: Foam board chassis offers a sturdy yet portable framework.
- **Iterative Tuning**: Optimized PID parameters (`Kp`, `Ki`, `Kd`) for efficient locomotion.

---

## Components Used 🛠️

- **Arduino Uno**: Main microcontroller.
- **L298N Motor Driver**: Controls the BO motors.
- **BO Motors**: Provide mobility.
- **MPU6050 Sensor**: Measures orientation (yaw, pitch, roll).
- **Foam Board**: Frame and housing for components.
- Additional components: Wires, connectors, power supply.

---

## How It Works ⚙️

1. **Orientation Detection**:  
   The MPU6050 sensor detects the robot's orientation (yaw, pitch, roll) and sends this data to the Arduino.

2. **PID Algorithm**:  
   The Arduino processes sensor data and calculates corrections using the PID algorithm.  
   - **Kp**: Proportional gain for immediate response.  
   - **Ki**: Integral gain for reducing steady-state error.  
   - **Kd**: Derivative gain for anticipating future errors.

3. **Motor Adjustment**:  
   The calculated corrections adjust the speed and direction of the motors via the L298N motor driver.

4. **Balancing**:  
   The robot continuously self-adjusts to maintain balance, even while moving.

---

## Code Overview 💻

Key libraries used:
- **PID_v1.h**: Implements the PID algorithm.
- **LMotorController.h**: Simplifies motor control.
- **I2Cdev.h & MPU6050_6Axis_MotionApps20.h**: Interface with MPU6050 sensor.

### Core Functionality:
- **Setup**: Initializes MPU6050, PID controller, and motor drivers.
- **Loop**: Processes sensor data, computes PID output, and adjusts motors for balancing.

---

## Getting Started 🛴

### Prerequisites
- Arduino IDE installed.
- Components listed above.

### Steps to Build:
1. Assemble the hardware:
   - Connect Arduino, MPU6050, motor driver, and motors as per the circuit diagram.
2. Install required Arduino libraries.
3. Upload the code (`self_balancing_robot.ino`) to the Arduino.
4. Power up the system and tune the PID parameters (`Kp`, `Ki`, `Kd`) as needed.

---

## Challenges & Solutions 🧠

### Challenges:
- Achieving precise balance on uneven surfaces.
- Tuning PID parameters for dynamic responses.

### Solutions:
- Iterative testing and refinement of PID values.
- Lightweight chassis to minimize oscillations.

---

## Future Improvements 🔮

- Add Bluetooth control for remote operation.
- Incorporate obstacle detection using ultrasonic sensors.
- Enhance stability for rugged terrains.


