# Detailed Optical Path Diagrams: BendingForce v2

## Overview
The BendingForce v2 optical path is a sequence of light manipulations that transforms two-dimensional light into a three-dimensional volumetric field. This document visualizes the journey of a photon from its generation in the emitter array to its reconstruction as part of the "Crystal Lattice."

## 1. The Light Path Journey (Cross-Sectional)
This diagram illustrates the progression of light rays through the BendingForce v2 optical stack.

```mermaid
graph TD
    A[Micro-LED Emitter Array] -->|Isotropic Blue/UV Photons| B[Micro-Lens Array]
    B -->|Collimated Light Channels| C[Diffractive Holographic Film]
    C -->|Phase-Modulated Wavefronts| D[Micro-Prism Optical Lattice]
    D -->|Angularly Redirected Rays| E[Fluorescent Amplification Layer]
    E -->|RGB Visible Light Field| F[Floating Crystal Lattice Point]

    subgraph "Spatial Reconstruction Engine"
    B
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

## 3. The Fluorescent Conversion Light Path
In this stage, invisible or blue light is converted into high-intensity visible RGB, minimizing energy loss and maximizing clarity.

```mermaid
sequenceDiagram
    participant Emitter as Micro-LED Emitter
    participant FAL as Fluorescent Amplification Layer
    participant Space as Spatial Volume (Crystal Lattice)

    Emitter->>FAL: 450nm (Blue/UV) Photons
    FAL->>FAL: Phosphor / Quantum Dot Excitation
    FAL->>Space: 620nm (Red), 530nm (Green), 460nm (Blue) Visible Photons
    Note over FAL, Space: High-Brightness 3D Reconstruction
```

## 4. Multi-Layer Optical Specification Table

| Layer | Optical Function | Tolerance | Material Class |
| :--- | :--- | :--- | :--- |
| **Micro-LED Array** | Photon Generation | Sub-Micron | GaN-on-Si |
| **MLA** | Beam Shaping/Collimation | < 10nm RA | Nano-Imprinted Polymer |
| **DHF** | Phase/Depth Encoding | < 5nm SRG | Diffractive Film |
| **MPOL** | Angular Parallax | < 0.05° Facet Angle | Precision-Etched Polymer |
| **FAL** | Photon Conversion | Layer Thickness < 5µm | Quantum Dot / Phosphor |

---
*Diagram Note: These visualizations represent the conceptual optical flow and are subject to refinement during physical prototyping (Phase 1 & 2).*
