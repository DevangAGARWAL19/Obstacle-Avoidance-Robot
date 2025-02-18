# Obstacle-Avoidance-Robot
### **Smart Obstacle-Avoiding Robot using an Ultrasonic Sensor and Motor Driver**  

#### **Introduction**  
This project demonstrates a simple **obstacle-avoiding robot** that uses an **ultrasonic sensor (HC-SR04)** to detect objects in front of it. If the robot detects an obstacle **closer than 20 cm**, it automatically **stops and moves backward** to avoid collision. Otherwise, it continues moving **forward**. This is achieved using an **Arduino board** that controls **two motors** through a **motor driver circuit**.

---

### **Components Used**
1. **Arduino (Uno/Nano/MEGA)** – Acts as the brain of the robot.
2. **HC-SR04 Ultrasonic Sensor** – Measures the distance to obstacles.
3. **Motor Driver Module (L298N or L293D)** – Controls the motors.
4. **DC Motors** – Provides movement to the robot.
5. **Power Supply (Battery Pack)** – Powers the motors and Arduino.

---

### **Working Principle**
1. **Distance Measurement with Ultrasonic Sensor**  
   - The ultrasonic sensor sends a **high-frequency sound pulse** (triggered by `trigPin`).
   - The pulse travels forward, hits an object, and **bounces back**.
   - The sensor calculates the **time taken for the echo to return**.
   - Using the formula:  
     \[
     \text{Distance} = \frac{\text{Time} \times \text{Speed of Sound}}{2}
     \]
     where the **speed of sound** is **0.034 cm/µs**, the distance to the obstacle is determined.

2. **Motor Control Based on Distance**
   - If the **measured distance is 20 cm or more**, the robot **moves forward**.
   - If an obstacle is **detected within 20 cm**, the robot **stops for a moment**, then **moves backward** to avoid collision.
   - The motors are controlled using a motor driver, which allows **bidirectional movement**.

3. **Smooth Motion Handling**
   - The robot does not change direction suddenly; it **stops before reversing** to ensure smooth movement.
   - Functions are used to keep the code clean and well-organized.

---

### **Applications**
- **Autonomous obstacle-avoiding robots**
- **Smart vehicles** that navigate without human intervention
- **Industrial automation** to detect obstacles in warehouses
- **Educational robotics projects** to learn about sensors and motor control
