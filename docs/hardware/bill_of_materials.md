# Bill of Materials (BOM) – BendingForce v2

## Overview
This document outlines the estimated component costs for the **BendingForce v2** Spatial Light Computing Platform. The target is to remain competitive with flagship tablets from Samsung and Apple ($999 – $1,499), while incorporating advanced spatial optics and industry-leading performance.

**Volume Assumption:** Initial Pilot Run (1,000 – 5,000 units).
**Strategy:** High R&D investment to drive down component costs for future mass production.

## 1. Bill of Materials: Optimization Tiers

| Component Category | "Standard" Tier (Est.) | "Pro/Field" Tier (Est.) | Mass Prod. Target (Scale) |
| :--- | :--- | :--- | :--- |
| **Spatial Light Engine (SLE)** | $450.00 (Mini-LED Hybrid) | $650.00 (Pure Micro-LED) | $320.00 |
| &nbsp;&nbsp;*- Display Backplane* | *$300.00 (1000 PPI)* | *$450.00 (2000+ PPI)* | *$220.00* |
| &nbsp;&nbsp;*- Optical Layers* | *$150.00 (MLA/DHF)* | *$200.00 (Full LOS)* | *$100.00* |
| **Apex SoC (SD 8 Elite)** | $240.00 (Standard) | $280.00 (Extreme) | $210.00 |
| **Memory & Storage** | 16GB LPDDR5X + 512GB UFS 4.0 | $140.00 | $110.00 |
| **Interaction & Sensors** | SISS Suite (LiDAR, ToF, IR) | $110.00 | $70.00 |
| **Housing & Chassis** | CNC Magnesium-Titanium Hybrid | $95.00 | $65.00 |
| **Power System** | 200Wh All-Solid-State (ASSB) + IPDN | $250.00 | $120.00 |
| **Connectivity & Audio** | 5G, Wi-Fi 7, Spatial Audio Array | $50.00 | $35.00 |
| **Assembly & Testing** | Precision alignment & IP69K sealing | $110.00 | $65.00 |
| **Total Estimated BOM** | **$1,225.00** | **$1,495.00** | **$910.00** |

## 2. Cost Optimization Roadmap

### 2.1 The "Standard" Hybrid Strategy
To achieve the **$1,199 MSRP** for the Standard edition, BendingForce v2 utilizes a **Mini-LED / Micro-LED Hybrid** approach for the pilot phase. This allows for high-quality spatial imagery at a significantly lower cost while the custom pure-Micro-LED yields mature.

### 2.2 Yield-Driven Reduction
The primary cost driver is the **Laminated Optical Sandwich (LOS)**. Optimization focuses on:
*   **Monolithic Integration:** Moving from seven laminated sheets to a three-layer integrated module using Step-and-Repeat Nano-imprint Lithography (NIL).
*   **Scale Amortization:** Leveraging Motorola/Lenovo’s existing supply chain for the Snapdragon 8 Elite and memory modules to achieve immediate volume discounts.

## 3. Competitive Performance Benchmarks (SoC)

| Processor | Manufacturing Node | NPU Performance | Target Architecture |
| :--- | :--- | :--- | :--- |
| **Snapdragon 8 Elite + HSU** | **3nm** | **80 TOPS + HSU Logic**| **Spatial Computing** |
| Apple M4 (iPad Pro) | 3nm (N3E) | 38 TOPS | General Productivity |
| Apple A18 Pro (iPhone 16) | 3nm (N3E) | 35 TOPS | Mobile/Imaging |

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
