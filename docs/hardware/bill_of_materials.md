# Bill of Materials (BOM) – BendingForce v2

## Overview
This document outlines the estimated component costs for the **BendingForce v2** Spatial Light Computing Platform. The target is to remain competitive with flagship tablets from Samsung and Apple ($999 – $1,499), while incorporating advanced spatial optics.

**Volume Assumption:** Initial Pilot Run (1,000 – 5,000 units).
**Strategy:** High R&D investment to drive down component costs for future mass production.

## 1. Bill of Materials (Estimated)

| Component Category | Key Specifications | Pilot Cost (Est.) | Mass Prod. Target |
| :--- | :--- | :--- | :--- |
| **Spatial Light Engine (SLE)** | Micro-LED Array + Optical Stack | $650.00 | $350.00 |
| &nbsp;&nbsp;*- Micro-LED Display* | *1000+ PPI, 12" Panel* | *$450.00* | *$250.00* |
| &nbsp;&nbsp;*- Optical Layers* | *MLA, DOE, Prism Lattice, QD Film* | *$200.00* | *$100.00* |
| **Processing (SoC)** | High-end ARM (e.g., SD 8 Elite / Custom) | $280.00 | $220.00 |
| **Memory & Storage** | 16GB LPDDR5X + 512GB UFS 4.0 | $140.00 | $110.00 |
| **Interaction & Sensors** | LiDAR, ToF, Gesture Cameras | $110.00 | $70.00 |
| **Housing & Chassis** | CNC Magnesium Alloy, Ruggedized | $90.00 | $60.00 |
| **Power System** | 100Wh Battery + Solar Backplane | $60.00 | $40.00 |
| **Connectivity & Audio** | 5G, Wi-Fi 7, Spatial Audio Array | $50.00 | $35.00 |
| **Assembly & Testing** | Precision alignment & IP68 sealing | $100.00 | $60.00 |
| **Total Estimated BOM** | | **$1,480.00** | **$945.00** |

## 2. Cost Analysis & Strategy

### 2.1 The "Spatial" Premium
Standard high-end tablets (iPad Pro/Galaxy Tab) have a BOM ranging from **$450 – $600**. The BendingForce v2 carries a significant premium due to the **Spatial Light Engine (SLE)**.
*   **Pilot Phase:** The device will likely be sold at a near-zero or negative margin ($1,480 BOM vs $1,499 MSRP) to seed the market and technical partners.
*   **Scaling Phase:** As Micro-LED yields improve and nano-imprint lithography for the optical films scales, the BOM is projected to drop below **$950**, allowing for healthy "Apple-like" margins at the $1,499 price point.

### 2.2 R&D Amortization
The "High R&D" strategy involves significant up-front investment in:
1.  **Custom Optical Design:** Proprietary designs for the Micro-Prism Lattice.
2.  **Rendering Pipeline:** Custom silicon or specialized FPGA logic for real-time holographic synthesis.
3.  **Manufacturing Tooling:** Custom alignment jigs for sub-micron layer stacking.

## 3. Competitive Comparison (Retail MSRP)

| Feature | BendingForce v2 | Samsung Tab S10 Ultra | iPad Pro 13" (M4) |
| :--- | :--- | :--- | :--- |
| **Display** | Spatial Light Engine (3D) | Dynamic AMOLED 2X (2D) | Ultra Retina XDR (2D) |
| **Holographic** | Yes (2cm - 30cm) | No | No |
| **Ruggedization** | IP68 / MIL-STD-810H | IP68 | None |
| **Processor** | Flagship ARM + AI | MediaTek Dimensity 9300+ | Apple M4 |
| **Base Price** | **$1,299 - $1,499** | **$1,199** | **$1,299** |

---
*BOM Note: The Micro-LED panel remains the single most volatile cost. Prototyping may utilize high-end Mini-LED as a cost-reduction fallback if Micro-LED yields do not meet pilot targets.*
