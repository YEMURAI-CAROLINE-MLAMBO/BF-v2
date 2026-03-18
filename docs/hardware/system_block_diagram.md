# System Block Diagram: BendingForce v2

## Overview
This document outlines the full system architecture for the BendingForce v2 Spatial Light Computing Platform. It integrates the high-performance computing core, the specialized **Holographic Synthesis Unit (HSU)**, the sensor suite, and the **Spatial Light Engine (SLE)**.

## 1. Full Tablet Architecture (System Level)

```mermaid
graph TD
    subgraph "Power Management (PMIC)"
    Battery[100Wh Battery]
    Supercap[Supercapacitor Buffer]
    Solar[Perovskite Solar Film]
    Charging[Charge Controller]
    end

    subgraph "Main Processor (SoC)"
    CPU[Multicore ARM CPU]
    GPU[High-Performance GPU]
    NPU[AI-Accelerated NPU]
    HSU[Holographic Synthesis Unit]
    UnifiedMem[Unified LPDDR5X Memory]
    end

    subgraph "Sensors & Input"
    ToF[Short-Range ToF]
    IR[Gesture Cameras]
    LiDAR[Environmental LiDAR]
    Touch[Capacitive 2D Touch]
    ALS[Ambient Light Sensor]
    IMU[9-axis IMU]
    end

    subgraph "Display Output (SLE)"
    Emitter[Micro-LED Emitter Array]
    Stack[Optical Stack / DHF / MPOL / FAL]
    Switch[2D/3D Mode Switch]
    end

    subgraph "I/O & Connectivity"
    Radio[5G / Wi-Fi 7 / LEO Sat]
    Ports[USB4 / Thunderbolt 4]
    Audio[Spatial Audio Beamforming]
    Haptics[Localized Voice-Coil Haptics]
    end

    Charging --> Battery
    Battery --> PMIC[Power Distribution]
    Solar --> Charging
    Supercap --> PMIC

    ToF --> NPU
    IR --> NPU
    LiDAR --> CPU
    Touch --> CPU
    IMU --> CPU

    GPU --> HSU
    HSU --> Emitter
    Emitter --> Stack
    Stack --> Switch
    CPU --> Switch

    Radio --> CPU
    Ports --> CPU
    Audio --> CPU
    Haptics --> CPU
```

## 2. The Holographic Synthesis Unit (HSU) Data Flow
The HSU is a specialized hardware accelerator within the SoC that transforms 3D coordinate data into phase-modulated light field patterns for the SLE.

```mermaid
sequenceDiagram
    participant Engine as 3D Game/CAD Engine
    participant GPU as Main GPU
    participant HSU as Holographic Synthesis Unit
    participant SLE as Spatial Light Engine (Micro-LED)

    Engine->>GPU: 3D Mesh / Mesh Data
    GPU->>GPU: Real-time Ray Tracing / Depth Map
    GPU->>HSU: Depth Map & Angular Metadata
    HSU->>HSU: Phase Modulation & Interference Calc
    HSU->>SLE: Pixel-level Light Field Pattern (Spatial)
    Note over HSU, SLE: < 10ms Photon-to-Motion Latency
```

## 3. Subsystem Interconnects

| Interconnect | Protocol | Purpose |
| :--- | :--- | :--- |
| **GPU to HSU** | Proprietary High-Speed Bus | Low-latency transfer of raw depth/mesh data. |
| **HSU to SLE** | High-bandwidth DSI/MIPI | High-resolution spatial frame delivery. |
| **PMIC to SLE** | Adaptive Voltage Rail | Manages high-current pulses for the Micro-LED array. |
| **NPU to CPU** | Shared Memory | Fusion of gesture and environmental sensor data. |

---
*Diagram Note: This system block diagram represents the targeted final architecture for BendingForce v2, prioritizing high-performance spatial computing and energy efficiency.*
