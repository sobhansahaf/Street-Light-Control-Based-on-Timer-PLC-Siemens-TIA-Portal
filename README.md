
# PLC-Controlled Street Lighting System

This project implements a **PLC-based street lighting control system** that activates lights automatically when a vehicle is detected. The system enhances visibility while conserving energy by running a timed lighting sequence only when needed.

---

## **Overview**

When a vehicle passes in front of the **vehicle-detection sensor**, the PLC initiates the following lighting sequence:

1. **Lights turn ON for 20 seconds.**
2. After the initial ON period, the lights enter a **10-second blinking mode**, flashing **once every 4 seconds** (2 seconds ON, 2 seconds OFF).
3. When the blinking sequence ends, the street lights **automatically turn OFF**.

---

## **System Sequence**

### **1. Vehicle Detection**

* A sensor detects an approaching vehicle.
* The PLC receives the detection signal and starts the program.

### **2. Continuous Lighting (20 seconds)**

* Street lights turn **fully ON**.
* A timer holds the lights ON for **20 seconds**.

### **3. Blinking Mode (10 seconds)**

* After the 20-second ON period, the lights begin **blinking**.
* Blink pattern:

  * **Light ON for 2 seconds**
  * **Light OFF for 2 seconds**
* This cycle repeats for a total blink duration of **10 seconds**.

### **4. Automatic Shutdown**

* After the blinking cycle, the lights turn **OFF**.
* The system resets to standby mode, waiting for the next vehicle trigger.

---

## **Functional Highlights**

* ⏱ Precise timer-controlled operation
* 🚗 Automatic activation from vehicle detection
* 💡 Energy-efficient lighting sequence
* 🔄 Blinking mode provides a gradual shutoff pattern
* ⚙️ Suitable for PLC ladder logic, function block, or structured text

