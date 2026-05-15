# Detailed Optical Path Diagrams: BendingForce v2

## Overview
The BendingForce v2 optical path is a sequence of light manipulations that transforms two-dimensional light into a three-dimensional volumetric field. This document visualizes the journey of a photon from its generation in the emitter array to its reconstruction as part of the "Crystal Lattice."

## 1. The Enhanced Optical Stack (Laminated Optical Sandwich)
This diagram illustrates the progression of light rays through the BendingForce v2 optical stack, including the mode-switching and ambient feedback loops.

```mermaid
graph TD
    ALS[Ambient Light Sensor] -->|Spectral Data| NPU[Snapdragon NPU]
    NPU -->|Excitation Control| A[Micro-LED Emitter Array]

    A -->|Coherent Blue/UV Photons| B[Micro-Lens Array]
    B -->|Collimated Light Channels| LCS[Liquid Crystal Switch]

    LCS -->|3D Mode: Transparent| C[Diffractive Holographic Film]
    LCS -->|2D Mode: Diffuse| DIFF[2D Image Plane]

    C -->|Phase-Modulated Wavefronts| D[Micro-Prism Optical Lattice]
    D -->|Angularly Redirected Rays| E[Fluorescent Amplification Layer]
    E -->|RGB Visible Light Field| F[Floating Crystal Lattice Point]

    subgraph "The Spatial Light Engine (SLE)"
    B
    LCS
    C
    D
    E
    end
```

## 2. The 3D Parallax Generation (View Angle Detail)
The **Micro-Prism Optical Lattice (MPOL)** ensures that different viewing angles receive unique light rays, creating the parallax effect for the naked eye.

```mermaid
graph LR
    subgraph "Optical Stack Detail"
    MPOL[Micro-Prism Lattice]
    end

    MPOL -->|Ray Alpha| LA[Left Angle / Left Eye]
    MPOL -->|Ray Beta| RA[Right Angle / Right Eye]
    MPOL -->|Ray Gamma| CA[Center Angle / Dual-Eye]

    LA -->|Depth Cue A| Brain[User Brain]
    RA -->|Depth Cue B| Brain
    Brain -->|Result| Volumetric[Volumetric 3D Perception]
```

## 3. The Photon's Journey: Adaptive Spectral Conversion
This sequence illustrates how the system adapts to ambient light while converting high-energy blue/UV photons into the visible RGB spatial field.

```mermaid
sequenceDiagram
    participant ALS as Ambient Light Sensor
    participant NPU as Snapdragon NPU (Apex)
    participant Emitter as Micro-LED Emitter
    participant FAL as Fluorescent Amplification Layer
    participant Space as Spatial Volume (Crystal Lattice)

    ALS->>NPU: Detects 5000K Sunlight (100,000 lux)
    NPU->>Emitter: Boost Radiance / Shift Spectral Bias
    Emitter->>FAL: 395nm/450nm High-Intensity Photons
    FAL->>FAL: Quantum Dot Excitation (Spectral Matching)
    FAL->>Space: 7,500 Nit RGB Volumetric Reconstruction
    Note over ALS, Space: Sunlight-Critical Mode Active
```

## 4. Multi-Layer Optical Specification Table

| Layer | Optical Function | Tolerance | Material Class |
| :--- | :--- | :--- | :--- |
| **Micro-LED Array** | Photon Generation | Sub-Micron | GaN-on-Si |
| **MLA** | Beam Shaping/Collimation | < 10nm RA | Nano-Imprinted Polymer |
| **LC Switch** | 2D/3D Mode Toggling | < 1ms Switching | Liquid Crystal / ITO |
| **DHF** | Phase/Depth Encoding | < 5nm SRG | Diffractive Film (NIL) |
| **MPOL** | Angular Parallax | < 0.05° Facet Angle | High-Index Polymer ($n=1.78$) |
| **FAL** | Photon Conversion | Layer Thickness < 5µm | Quantum Dot / Phosphor |

---
*Diagram Note: These visualizations represent the conceptual optical flow and are subject to refinement during physical prototyping (Phase 1 & 2).*
