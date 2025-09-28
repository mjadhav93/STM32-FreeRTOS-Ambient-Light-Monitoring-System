# STM32-FreeRTOS-Ambient-Light-Monitoring-System
Developed an embedded system on STM32 using FreeRTOS multitasking to monitor ambient light intensity. The system integrates a TSL2561 I2C sensor with a 16x2 LCD and onboard LED to provide real-time lux readings and adaptive LED feedback.


# STM32 FreeRTOS Ambient Light Monitoring System

An embedded project built on **STM32** using **FreeRTOS** (CMSIS-RTOS v2) to monitor ambient light intensity with a **TSL2561 I2C sensor** and display results on a 16x2 I2C LCD.  
Additionally, the system provides visual feedback by adjusting the blink rate of the onboard LED depending on brightness levels.

---

## 🚀 Features
- FreeRTOS multitasking with CMSIS-RTOS v2 APIs  
- Real-time lux measurement using TSL2561 sensor  
- LCD updates via I2C driver (16x2 KS0061)  
- Adaptive LED blinking (faster in bright, slower in dark)  
- Modular drivers: `tsl2561.h/c` and `lcd_i2c.h/c`  

---

## 🧩 Setup
1. Install **STM32CubeIDE**  
2. Clone this repository  
3. Import project into CubeIDE  
4. Add the required drivers:  
   - `tsl2561.h/c` (light sensor driver)  
   - `lcd_i2c.h/c` (LCD driver)  
5. Build and flash to STM32 board

---

## ⚙️ How It Works
- **Sensor Task**: Reads lux values every 1 second and sends them via FreeRTOS message queue.  
- **Display Task**: Receives sensor data and updates the LCD display.  
- **LED Task**: Adjusts onboard LED blink rate based on brightness.  

---


## 🛠️ Hardware Requirements
- STM32F446RE NUCLEO (or STM32F103C8 Blue Pill)  
- TSL2561 Ambient Light Sensor  
- 16x2 I2C LCD Display  
- Breadboard + jumper wires  
- Onboard LED (PC13, active low)  



## 🔑 Notes
- Ensure I2C lines (SCL, SDA) have pull-up resistors (if not already on the module).  
- Uses **CMSIS-RTOS v2 APIs** (`osThreadNew`, `osMessageQueueNew`, etc.).  
- Designed to be portable to other STM32 boards with minor pin changes.  

---

## 📚 Skills Demonstrated
- Real-time embedded system design  
- FreeRTOS multitasking & inter-task communication  
- I2C communication with sensors & peripherals  
- STM32 HAL & driver development  

---
