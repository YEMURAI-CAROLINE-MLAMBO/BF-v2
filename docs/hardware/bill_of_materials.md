# Bill of Materials (BOM) – BendingForce v2

## Overview
This document outlines the estimated component costs for the **BendingForce v2** Spatial Light Computing Platform. The target is to remain competitive with flagship tablets from Samsung and Apple ($999 – $1,499), while incorporating advanced spatial optics and industry-leading performance.

**Volume Assumption:** Initial Pilot Run (1,000 – 5,000 units).
**Strategy:** High R&D investment to drive down component costs for future mass production.

## 1. Bill of Materials (Estimated)

| Component Category | Key Specifications | Pilot Cost (Est.) | Mass Prod. Target |
| :--- | :--- | :--- | :--- |
| **Spatial Light Engine (SLE)** | Micro-LED Array + Optical Stack | $650.00 | $350.00 |
| &nbsp;&nbsp;*- Micro-LED Display* | *1000+ PPI, 12" Panel* | *$450.00* | *$250.00* |
| &nbsp;&nbsp;*- Optical Layers* | *MLA, DOE, Prism Lattice, QD Film* | *$200.00* | *$100.00* |
| **Apex SoC** | 3nm High-Performance Spatial Processor | $280.00 | $220.00 |
| **Memory & Storage** | 16GB LPDDR5X + 512GB UFS 4.0 | $140.00 | $110.00 |
| **Interaction & Sensors** | SISS Suite (LiDAR, ToF, IR) | $110.00 | $70.00 |
| **Housing & Chassis** | CNC Magnesium-Titanium Hybrid | $95.00 | $65.00 |
| **Power System** | 200Wh All-Solid-State (ASSB) + IPDN | $250.00 | $120.00 |
| **Connectivity & Audio** | 5G, Wi-Fi 7, Spatial Audio Array | $50.00 | $35.00 |
| **Assembly & Testing** | Precision alignment & IP69K sealing | $110.00 | $65.00 |
| **Total Estimated BOM** | | **$1,495.00** | **$955.00** |

## 2. Competitive Performance Benchmarks (SoC)

| Processor | Manufacturing Node | NPU Performance | Target Architecture |
| :--- | :--- | :--- | :--- |
| **Apex SoC (BendingForce)** | **3nm (GAA)** | **100 TOPS** | **Spatial Synthesis (HSU)** |
| Apple M4 (iPad Pro) | 3nm (N3E) | 38 TOPS | General Productivity |
| Apple A18 Pro (iPhone 16) | 3nm (N3E) | 35 TOPS | Mobile/Imaging |
| Snapdragon 8 Elite (Gen 4) | 3nm | 80 TOPS (Total) | General Flagship |

## 3. Cost Analysis & Strategy

### 3.1 The "Spatial" Premium
Standard high-end tablets (iPad Pro/Galaxy Tab) have a BOM ranging from **$450 – $650**. The BendingForce v2 carries a significant premium due to the **Spatial Light Engine (SLE)** and the high-capacity **ASSB** battery.
*   **Pilot Phase:** The device will likely be sold at a near-zero or negative margin ($1,495 BOM vs $1,499 MSRP) to seed the market and technical partners.
*   **Scaling Phase:** As Micro-LED yields improve and nano-imprint lithography for the optical films scales, the BOM is projected to drop below **$960**, allowing for healthy "Apple-like" margins at the $1,499 price point.

### 3.2 R&D Amortization
The "High R&D" strategy involves significant up-front investment in:
1.  **Custom Optical Design:** Proprietary designs for the Micro-Prism Lattice.
2.  **Rendering Pipeline:** Custom silicon logic within the Apex SoC (HSU) for real-time holographic synthesis.
3.  **Manufacturing Tooling:** Custom alignment jigs for sub-micron layer stacking (LOS).

---
*BOM Note: The Micro-LED panel remains the single most volatile cost. Prototyping may utilize high-end Mini-LED as a cost-reduction fallback if Micro-LED yields do not meet pilot targets.*
