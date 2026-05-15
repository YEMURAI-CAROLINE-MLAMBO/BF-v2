# Energy Flow and Spatial Rendering Diagrams: BendingForce v2

## 1. AI-Managed Intelligent Power Distribution Network (IPDN)
The IPDN utilizes the Snapdragon NPU to predict rendering loads and dynamically shunt power between the SoC and the Spatial Light Engine (SLE). This ensures maximum efficiency and protects the solid-state battery from high-current stress.

```mermaid
graph TD
    subgraph "Energy Sources"
    ASSB[200Wh Main Battery]
    ForcePack[150Wh Apex Force-Pack]
    Supercap[Supercapacitor Array]
    end

    subgraph "Intelligent Control (IPDN)"
    NPU[Snapdragon NPU] -->|Load Prediction| Control[IPDN Controller]
    end

    subgraph "Load Distribution"
    Control -->|Steady State Power| SoC[Snapdragon 8 Elite SoC]
    Control -->|High-Current Pulses| SLE[Spatial Light Engine]
    Control -->|Active Thermal Control| Piezo[Piezoelectric Cooling]
    end

    ASSB --> Control
    ForcePack --> Control
    Control --> Supercap
    Supercap -->|Burst Power| SLE
```

## 2. Spatial Rendering Data Flow (Zero-Copy Architecture)
To achieve sub-10ms "photon-to-motion" latency, BendingForce v2 utilizes a Unified Spatial Memory architecture and a Predictive Rendering Engine.

```mermaid
sequenceDiagram
    participant SISS as Spatial Interaction Sensor Suite
    participant PRE as Predictive Rendering Engine (NPU)
    participant Memory as Unified Spatial Memory (Zero-Copy)
    participant HSU as Holographic Synthesis Unit
    participant SLE as Spatial Light Engine

    SISS->>Memory: Raw Head/Eye Tracking Data
    PRE->>Memory: Fetch Tracking Data
    PRE->>PRE: Predict User Position (+10ms)
    Memory->>HSU: 3D Assets & Predicted Coordinate Map
    HSU->>HSU: Interference Pattern Synthesis
    HSU->>SLE: Uncompressed Spatial Frame
    Note over SISS, SLE: Total Latency < 10ms
```

## 3. Power State Matrix (Adaptive Shunting)

| Device State | NPU Load Prediction | IPDN Action | SLE Mode |
| :--- | :--- | :--- | :--- |
| **Idle / 2D** | Minimal | Power save; Charging ASSB | 2D (LC Diffuse) |
| **Active 3D (Gaming)** | High (Sustained) | Direct shunt from ASSB + Force-Pack | 3D (Spatial) |
| **High-Brightness SOOS** | Extreme (Burst) | Supercap Discharge to SLE | 3D (Boost) |
| **Thermal Limit** | NPU Throttle Detected | Divert power to Piezo-Cooling | Power-Limited 3D |

## 4. Unified Spatial Memory (Zero-Copy) Diagram
Traditional architectures copy data between CPU, GPU, and Display buffers. BendingForce v2 eliminates this overhead.

```mermaid
graph LR
    subgraph "Unified Memory Pool"
    Data[3D Geometry / Voxel Data]
    end

    subgraph "Processing Nodes"
    CPU[8-core Oryon CPU]
    GPU[Adreno GPU]
    HSU[Holographic Synthesis Unit]
    NPU[Hexagon NPU]
    end

    CPU <-->|Pointer Access| Data
    GPU <-->|Pointer Access| Data
    HSU <-->|Pointer Access| Data
    NPU <-->|Pointer Access| Data

    HSU -->|Direct Drive| SLE[Spatial Light Engine]
```

---
*Diagram Note: These flows are optimized for the Snapdragon 8 Elite platform and the custom HSU co-processor.*
