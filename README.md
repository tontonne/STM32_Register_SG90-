# STM32_Register_SG90-
Bare-metal PWM Servo Motor (SG90) Control on STM32F103C8T6 using direct register access

## Overview
This project demonstrates direct register-level (bare-metal) programming on the **STM32F103C8T6** microcontroller to generate a 50Hz PWM signal for controlling an SG90 servo motor.

## Key Features
- **No HAL/LL Dependencies:** Configured RCC, GPIO, and General-Purpose Timer (TIM2/TIM3) directly via registers based on the STM32F1 Reference Manual (RM0008).
- **PWM Configuration:** 72MHz system clock, Prescaler (PSC) = 71, Auto-Reload Register (ARR) = 19999 (20ms period / 50Hz).
- **Angle Control:** Dynamic update of the Capture/Compare Register (CCR) from 500 to 2500 (0.5ms - 2.5ms pulse width) for 0° to 180° rotation.

## Hardware Setup
- **MCU:** STM32F103C8T6 (Blue Pill)
- **Actuator:** SG90 Micro Servo
- **Connections:** Signal pin connected to Timer PWM output pin, external 5V power supply with common GND.
