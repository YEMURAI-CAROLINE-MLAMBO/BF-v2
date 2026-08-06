# BendingForce: Technical Stack Overview

## 1. Overview: The Screen-Centric Paradigm
The BendingForce technical stack is organized around a single, pivotal innovation: the **Spatial Light Engine (SLE)** screen. Rather than building a locked, luxury device, the hardware and software layers are structured to support the physics and processing requirements of this revolutionary optical stack, making it adaptable to both low-cost humanitarian tablets and standard modular compute architectures.

---

## 2. Core Screen Architecture: The Spatial Light Engine (SLE)
The primary engineering achievement of the platform is the six-layer **Laminated Optical Sandwich** which converts 2D emitter data into a coherent 3D light field.

| Layer | Component | Optical & Physics Specifications | Primary Role |
| :--- | :--- | :--- | :--- |
| **1. Photon Source** | **Monolithic Micro-LED Array** | GaN-on-Si, >1000 PPI, narrow-band Blue (450nm) & Near-UV (395nm), >1,000,000 cd/m² peak. | High-intensity emission to overcome passive layer attenuation. |
| **2. Collimation** | **Micro-Lens Array (MLA)** | Aspheric nano-imprinted high-index polymer ($n = 1.62$), aligned 1:1 with pixels. | Collimates light rays to $\pm 1^\circ$ normal to prevent cross-talk. |
| **3. Mode Toggling** | **Liquid Crystal Switch** | High-speed liquid crystal layer, sub-millisecond response. | Alternates the display between a standard diffuse 2D mode and transparent 3D mode. |
| **4. Wavefront Shaping**| **Diffractive Holographic Film (DHF)**| Surface Relief Gratings (SRG), sub-wavelength pitch (400nm-700nm). | Encodes physical depth and wavefront phase patterns. |
| **5. Parallax Redirect** | **Micro-Prism Optical Lattice (MPOL)**| Hexagonal micro-faceted refractive lattice ($n = 1.78$), angles $15^\circ - 45^\circ$. | Directs unique light-field slices to discrete viewing angles for parallax. |
| **6. Color & Gain** | **Fluorescent Amplification Layer (FAL)**| Quantum Dot (QD) / rare-earth phosphor high-clarity resin film. | Absorbs Blue/UV and emits saturated RGB, eliminating ghosting & boosting gain. |

---

## 3. Modular Computing and Software Integration

### 3.1 Standard Host Integration
The BendingForce screen is designed to interface with standard computing architectures, avoiding dependency on expensive custom processors:
*   **Holographic Synthesis Unit (HSU):** A highly portable, dedicated co-processing silicon block (or GPU-accelerated software shader core) that translates standard 3D depth-mesh data into phase-modulated interference patterns.
*   **Unified Memory Architecture:** Operates on standard system-on-chip architectures (such as ARM-based platforms) using standard zero-copy spatial memory pipelines to achieve sub-10ms "photon-to-motion" latency.

### 3.2 Operating Environment & SDK
*   **ApexOS (Hardened AOSP):** Built on the Android Open Source Project (AOSP) base, providing native compatibility with existing 2D productivity, healthcare, and educational applications.
*   **SpatialCore SDK Plugins:** Open-source developer plugins for Unity and Unreal Engine, allowing rapid conversion of standard 3D teaching tools and medical assets into holographic format.

---

## 4. Open Power and Structural Specifications

### 4.1 Intelligent Power Distribution Network (IPDN)
*   **Dynamic Shunting:** Manages high-current pulses to the high-brightness screen during 3D bursts while maintaining stable current to standard computing sub-systems.
*   **Battery Modularity:** Compatible with standard lithium-polymer battery packs for low-cost humanitarian builds, and supports advanced All-Solid-State Batteries (ASSB) for high-stakes, off-grid disaster response scenarios.

### 4.2 Structural Assembly & Durability
*   **Laminated Stack Alignment:** Utilizes Step-and-Repeat Nano-imprint Lithography (NIL) and vacuum lamination to align optical films with sub-500nm precision.
*   **Chassis Modularity:** The screen can be housed in either a low-cost, impact-resistant composite shell (for educational deployment) or a CNC-machined Magnesium-Titanium alloy housing (for extreme-environment emergency response).

---

## 5. Prototyping and Scaling Pathway
To rapidly lower the cost of the screen for global humanitarian deployment, the development pathway transitions from off-the-shelf development rigs to a fully integrated laminate.

| Feature | Phase 1 (Proof-of-Concept) | Phase 2 (Development Stack) | Phase 3 (Humanitarian Scaling) |
| :--- | :--- | :--- | :--- |
| **Core Light Source** | High-PPI OLED Development Panel | High-PPI Monolithic Mini-LED | Low-cost Custom Micro-LED |
| **Laminated Optics** | Manual Film Alignment Jigs | Machine-aligned Nano-imprinted Film | High-volume Vacuum Laminated Stack |
| **Compute Core** | RTX 4090 / Ubuntu 22.04 | Jetson Orin AGX / Linux | Off-the-shelf Tablet SoC + HSU |
| **Enclosure** | 3D Printed / Acrylic Rig | Standard Aluminum Casing | Impact-resistant Recycled Composites |

---
*Technical Stack Document - Focus: Spatial Light Engine Innovation - Version 1.5*
