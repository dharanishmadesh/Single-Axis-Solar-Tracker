

# **Solar Tracker Using LDRs** 🌞

This project demonstrates how to use Light Dependent Resistors (LDRs) and a servo motor to create a solar tracking system that follows the sun. The LDRs detect the intensity of light on either side of the panel, and based on this data, the servo motor adjusts the panel's position to ensure it faces the brightest light source.

---

## **📂 Project Files**

- `SolarTracker.ino`  
  - Arduino code for the solar tracking system.

---

## **🔧 Hardware Required**

- **Arduino Uno / Nano** (or any compatible board)
- **1x Servo Motor**
- **2x LDRs (Light Dependent Resistors)**
- **2x 10kΩ Resistors**
- **Jumper Wires**
- **Breadboard**

---

## **🔨 Circuit Diagram**

- **LDR1** is connected to **Pin A0** of the Arduino.
- **LDR2** is connected to **Pin A1** of the Arduino.
- The **Servo motor** is connected to **Pin 9** of the Arduino.
- Use the resistors in a voltage divider configuration for the LDRs.

---

## **💻 Code Overview**

### **Setup**

1. The **Servo** is initialized to start at a position of **90 degrees** (centered).
2. The **LDR1** and **LDR2** pins are set as **INPUT** to read analog values corresponding to the light intensity on each LDR.

### **Loop**

1. The **LDR1** and **LDR2** values are read, representing the light intensity on each side of the solar panel.
2. The difference between the values is calculated to determine which side is receiving more light.
3. The servo adjusts its position based on which LDR is receiving more light. 
    - If the **left LDR (LDR1)** gets more light, the servo rotates left (decreases the angle).
    - If the **right LDR (LDR2)** gets more light, the servo rotates right (increases the angle).
4. The servo's position is updated every 100ms to follow the light source.

---

## **⚙️ Code Explanation**

- **LDR Values**: The analogRead() function is used to read the values of the LDRs. Higher values represent stronger light intensity.
- **Servo Movement**: The servo moves by adjusting the initial position (`initial_position`). The change is based on the difference in light detected by the LDRs.
- **Error Threshold**: The system has a tolerance level (`error`), which prevents the servo from moving unnecessarily if the light difference is minimal.

---

## **⚠️ Notes**

- Ensure the LDRs are placed in positions where they will receive light from the same source.
- The system works best when the servo has a range of movement that allows it to follow the light effectively.

---

## **💡 Future Improvements**

- Add more LDRs for better accuracy in tracking the light source.
- Use a more advanced control algorithm for smoother tracking.
- Integrate the system with a solar panel for real-world applications.

---

## **👨‍💻 Author**

- **Technical Tamizha**  
  - [Website](https://www.procreativehub.com)

