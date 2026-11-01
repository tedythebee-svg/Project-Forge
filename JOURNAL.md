---
title: "Projet Forge - Smart LED Lamp"
author: "tedythebee"
description: "A custom dimmable RGB lamp powered by ESP32-C3-MINI-1 with a rotary encoder and USB-C"
created_at: "2026-28-10"
---

I used more time to do this because i'm a beginner
# October 28: Designed the power supply & USB-C interface

Started the schematic in KiCad for the custom lamp PCB. Added the USB-C 16-pin connector with 5.1k pull-down resistors on CC lines, a 100uF bulk capacitor, a PPTC polyfuse for overcurrent protection, and an AP2112K-3.3 LDO regulator for stable 3.3V logic supply.
<img width="2048" height="1220" alt="{EE882EB8-D708-4EC3-B372-DB437C1F3A0E}" src="https://github.com/user-attachments/assets/26e5d7f7-f988-4c83-a151-cbb066f4d32a" />



**Total time spent: 2.5 hours**

# October 29: Integrated ESP32-C3 MCU and 74AHCT1G125 Level Shifter

Wired the ESP32-C3-MINI-1 microcontroller with its reset/boot circuit and decoupling capacitors. Added a 74AHCT1G125 level shifter to boost the 3.3V GPIO data output to 5V logic for reliable WS2812B LED data transmission. Also connected an EC11 rotary encoder for physical brightness and mode control.
<img width="2048" height="1220" alt="{B5F15330-CE4D-4F82-A2D8-8D76E0AEA5FC}" src="https://github.com/user-attachments/assets/c3c16418-9f85-4649-ac1f-817fdcba569d" />




**Total time spent: 3 hours**

# october 30: Placed 32 WS2812B RGB LEDs & Decoupling Array

Completed the schematic by routing a 4x8 matrix of 32 WS2812B addressable RGB LEDs. Added individual 100nF decoupling capacitors (`C9` to `C40`) on each LED power pin to prevent voltage dips during full brightness operation. ANd verified a few times for errors
<img width="2048" height="1220" alt="{58A5C11F-3ABE-41C7-99F1-E84B952A4A70}" src="https://github.com/user-attachments/assets/3daa4bbf-c40a-4f02-8a63-6950353b40e0" />



**Total time spent: 3.5 hours**
