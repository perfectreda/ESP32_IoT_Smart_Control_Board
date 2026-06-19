# ⚡ ESP32 IoT Smart Control Board

A compact, 2-layer **ESP32-based IoT development PCB** designed for real-world embedded systems, USB connectivity, and modular expansion. Built for learning, prototyping, and portfolio-level hardware design.

---

## 🚀 Overview

This project implements a fully-featured IoT control board based on the ESP32-WROOM-32. It integrates USB communication, regulated power, expansion headers, protection circuitry, and proper RF/layout practices for production-grade design.

Target: **clean schematic + manufacturable PCB + professional documentation**

---

## 🧠 System Architecture

```mermaid
graph LR
    PWR[5V Input USB] --> LDO[3.3V Regulator]
    LDO --> ESP[ESP32-WROOM-32]

    USB[USB-C Connector] --> UART[USB-UART Bridge]
    UART --> ESP

    ESP --> I2C[I2C Header]
    ESP --> SPI[SPI Header]
    ESP --> GPIO[GPIO Expansion]
    ESP --> BTN[Boot / Reset Buttons]
    ESP --> LED[Status LEDs]
    ESP --> SENSOR[Optional Sensor Header]
