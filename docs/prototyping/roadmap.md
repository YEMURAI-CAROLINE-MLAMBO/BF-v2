# Prototyping Roadmap and Pathways

## Overview
Moving from the BendingForce v2 conceptual architecture to a physical prototype requires a phased approach. Early phases focus on validating the Spatial Light Engine (SLE) layers using high-quality off-the-shelf (OTS) components.

## Phase 1: Optical Validation (Bench-top)
**Goal:** Verify the light manipulation capabilities of individual SLE layers.

### Recommended Components
*   **Light Source:**
    *   *Option A:* High-density Micro-OLED or Micro-LED microdisplays (e.g., **TCL CSOT 0.28" 5131 PPI** prototype or similar modules from **Kopin** or **eMagin**).
    *   *Option B (Low Cost):* 4K Smartphone display (e.g., Sony Xperia 1 series) for initial large-scale proof of concept.
*   **Micro-Lens Array (MLA):**
    *   **Edmund Optics** Square Microlens Arrays (Fused Silica, 300µm - 500µm pitch).
    *   **Thorlabs** Microlens Arrays (Fused Silica).
*   **Diffractive Optical Elements (DOE):**
    *   Custom DOEs from **AGC** or **Holo/Or** for wavefront shaping experiments.
    *   Commercial holographic diffraction gratings (e.g., **Rainbow Symphony** films) for early interference tests.
*   **Fluorescent Layer:**
    *   Quantum Dot (QD) films from **Nanosys** or **Lumina**.
    *   Fluorescent acrylic/polymer sheets for basic photon conversion tests.

## Phase 2: Integrated Light Engine Prototype
**Goal:** Build a functional "Step-Out-of-Screen" engine with a real-time rendering pipeline.

### Compute Platform
*   **NVIDIA Jetson Orin AGX:** Ideal for Phase 2. It provides high-end GPU/NPU performance for light-field synthesis and supports multiple camera inputs for gesture tracking.
*   **PC-Based System:** For initial software development, an **NVIDIA RTX 4090** equipped workstation is recommended to handle unoptimized spatial rendering calculations.

### Interaction Sensors
*   **Depth Sensing:** **Intel RealSense D435i** (Stereo-IR) or **Azure Kinect** (ToF) for high-fidelity hand and environment tracking.
*   **Short-Range Interaction:** **Ultraleap Leap Motion Controller 2** for best-in-class skeletal hand tracking in the spatial volume.

## Phase 3: Tablet Prototype (Integrated)
**Goal:** Integrate the SLE and electronics into a tablet form factor.

### Custom Components
*   **Custom MLA/Prism Lattice:** Collaboration with nano-fabrication partners (e.g., **EV Group** for Nano-imprint Lithography).
*   **Custom SoC:** Evaluation of high-end mobile SoCs (Qualcomm Snapdragon 8 Gen series or MediaTek Dimensity) with custom firmware for SLE control.

## Prototyping Roadmap
| Phase | Focus | Key Deliverable |
| :--- | :--- | :--- |
| **1.1** | MLA & Alignment | Collimated light field from high-PPI source. |
| **1.2** | Diffractive Coding | Validated holographic interference patterns. |
| **1.3** | Phosphor Efficiency | High-brightness RGB conversion from Blue/UV source. |
| **2.1** | Rendering Engine | Real-time 3D model to light-field synthesis. |
| **2.2** | Gesture Integration | Interactive rotation/scaling of floating objects. |
| **3.1** | Mechanical Assembly | First ruggedized "Spatial Tablet" housing. |

## Strategic Technical Partners
*   **Optics:** Edmund Optics, Thorlabs, AGC (Asahi Glass).
*   **Display:** TCL CSOT, Kopin, Samsung Display (Micro-LED division).
*   **Compute:** NVIDIA, Qualcomm.
*   **Fabrication:** EV Group (NIL), TSMC (SoC/Micro-LED).

---
*Prototyping Note: Initial experiments can be performed at a 10x scale using standard LEDs and large-format MLA to simplify alignment before shrinking to the target sub-micron tolerances.*
