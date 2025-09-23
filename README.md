# RBN_soil_moisture_detector_Project1-2_LR
Building and Coding a Soil Detector P1

This project is a low-cost soil moisture detector built with Arduino. It measures soil moisture, temperature, humidity, and light, then displays the results on an LCD screen and uses LED indicators to signal soil water levels.  
 Repository Structure


---
## Repository Contents
| File / Folder                 | Description                                       |
| ----------------------------- | ------------------------------------------------- |
| `Assembly 1.zip`              | CAD / 3D Design files                             |
| `Assembly 1 (1).zip`          | Additional design files                           |
| `Bill of Material`            | Parts list                                        |
| `README.md`                   | Project documentation                             |
| `Soil Detector.pdf`           | Circuit wiring diagram in PDF format              |
| `Soil_Detector.png`           | Circuit schematic (image version)                 |
| `soil_detector.ino`           | Arduino source code for running the soil detector |
| `Laser Cutting Work`          | Pictures of Laser Cutting                         |

---
## Hardware Components

| Component              | Quantity | Notes                                  |
|------------------------|----------|----------------------------------------|
| Arduino Uno            | 1        | Microcontroller                        |
| Soil Moisture Sensor   | 1        | Analog output to A0                    |
| DHT11 Sensor           | 1        | Temperature & Humidity                 |
| Photoresistor (LDR)    | 1        | For light measurement                  |
| LCD 16x2 (I2C module)  | 1        | For displaying readings                |
| Green LED              | 1        | Soil moisture > 50%                    |
| Orange LED             | 1        | Soil moisture ~30%                     |
| Red LED                | 1        | Soil moisture < 10% (blinking)         |
| Breadboard             | 1        | For prototyping                        |
| Jumper Wires           | 10+      | Male-to-male / Female-to-male          |
| 9V Battery             | 1        | Power supply                           |

---
Assembly

<img width="876" height="586" alt="Screenshot 2025-08-20 090424" src="https://github.com/user-attachments/assets/28c09a8f-47e3-4b5f-b323-c1f7f8a0b123" />

---
## Software & Libraries

- **Arduino IDE**  
- Required libraries:  
  - `LiquidCrystal_I2C.h`  
  - `DHT.h`  

---
## Features

- Displays **Soil Moisture %, Temperature, Humidity, and Light** on LCD.  
- **LED indicators** for soil conditions:  
  - 🟢 Green = Moisture > 50%  
  - 🟠 Orange = Moisture ~30%  
  - 🔴 Red (blinking) = Moisture < 10%  

---
## How to Build  

1. Prepare Components  
Gather all items from the Bill of Materials above.  

2. Wiring Connections  

- **Soil Moisture Sensor** → A0 (analog pin)  
- **Photoresistor** → A1 (analog pin)  
- **Temperature Sensor [TMP36]** → Digital pin 2  
- **LCD 16x2 (I2C)** → SDA (A4), SCL (A5)  
- **LEDs**:  
  - Green → Pin 8  
  - Orange → Pin 9  
  - Red → Pin 10  
- **Power**: 9V battery  

---
## ASCII Wiring Diagram  

```
              +----------------------+
              |      Arduino Uno     |
              |                      |
      A0 <----| Soil Moisture Sensor |
      A1 <----| Photoresistor        |
       2 <----| DHT11 Sensor         |
       8 <----| Green LED            |
       9 <----| Orange LED           |
      10 <----| Red LED              |
      SDA <---| LCD SDA (A4)         |
      SCL <---| LCD SCL (A5)         |
              |                      |
     5V ------| VCC (Sensors + LCD)  |
    GND ------| GND (Common Ground)  |
              +----------------------+

        Power Options:
        - USB to PC
        - 9V Battery (Vin + GND)
```
## Circuit of diagram
<img width="1536" height="632" alt="Soil Detector" src="https://github.com/user-attachments/assets/16647565-e7f8-40eb-8a5c-ff4a8a42ae73" />

---
## Laser Cutting 
As part of my practice work, I explored laser cutting techniques to create custom casings and component holders. This exercise helped me gain hands-on experience with precision cutting, understanding material choices, and designing enclosures that improve both functionality and appearance of prototypes. It also gave me insight into how rapid fabrication tools can speed up iteration in hardware projects. I used CorelDraw to run the design that will be loaded to the machine.
<img width="673" height="317" alt="Screenshot 2025-09-23 163445" src="https://github.com/user-attachments/assets/2d8dc68b-5cfe-47ad-a5df-56c7898a186a" />

