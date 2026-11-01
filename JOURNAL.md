---
title: "Projet Forge - Smart LED Lamp"
author: "tedythebee"
description: "A custom dimmable RGB lamp powered by ESP32-C3-MINI-1 with a rotary encoder and USB-C"
created_at: "2026-28-10"
---

# October 28: Designed the power supply & USB-C interface

Started the schematic in KiCad for the custom lamp PCB. Added the USB-C 16-pin connector with 5.1k pull-down resistors on CC lines, a 100uF bulk capacitor, a PPTC polyfuse for overcurrent protection, and an AP2112K-3.3 LDO regulator for stable 3.3V logic supply.


**Total time spent: 2 hours**

# October 28: Integrated ESP32-C3 MCU and 74AHCT1G125 Level Shifter

Wired the ESP32-C3-MINI-1 microcontroller with its reset/boot circuit and decoupling capacitors. Added a 74AHCT1G125 level shifter to boost the 3.3V GPIO data output to 5V logic for reliable WS2812B LED data transmission. Also connected an EC11 rotary encoder for physical brightness and mode control.



**Total time spent: 2.5 hours**

# october 30: Placed 32 WS2812B RGB LEDs & Decoupling Array

Completed the schematic by routing a 4x8 matrix of 32 WS2812B addressable RGB LEDs. Added individual 100nF decoupling capacitors (`C9` to `C40`) on each LED power pin to prevent voltage dips during full brightness operation.


**Total time spent: 1.8 hours**
