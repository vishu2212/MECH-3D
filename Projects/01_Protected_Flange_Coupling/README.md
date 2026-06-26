# ⚙️ Protected Flange Coupling Assembly

[![Status - Completed](https://img.shields.io/badge/Status-Completed-success.svg)](#)
[![CAD - SolidWorks](https://img.shields.io/badge/CAD-SolidWorks-blue.svg)](#)
[![Standard - ISO/ASME](https://img.shields.io/badge/Standard-ISO%20%2F%20ASME-orange.svg)](#)

A rigid mechanical coupling designed to connect two rotating shafts for power and torque transmission, featuring a protective outer lip (flange cover) to shield the bolts and nuts, preventing workspace hazards and clothing entanglement.

---

## 📌 Project Overview

This project showcases a fully defined, parameterized 3D assembly of a **Protected Flange Coupling** modeled in SolidWorks. The design connects two inline shafts of \(\varnothing 40 \text{ mm}\) and transmits up to \(450 \text{ N}\cdot\text{m}\) of torque. 2D manufacturing drawings are generated with geometric tolerancing, surface finish marks, and a full Bill of Materials (BOM).

### 🔍 Key Operating Principle
In a protected flange coupling, the bolt heads and nuts are recessed inside a projecting circumferential flange cover. This prevents contact with rotating fasteners, resolving safety issues common to standard unprotected couplings.

---

## 🎯 Design Objectives

1. **Safety Compliance**: Shield rotating bolts according to industrial safety standards.
2. **Torque Transmission**: Model a key-and-shaft system capable of transmitting \(450 \text{ N}\cdot\text{m}\) at \(1500 \text{ RPM}\).
3. **Drafting Excellence**: Produce production-ready 2D drawings using **Third Angle Projection** with ISO-standard tolerances.
4. **Assembly Integrity**: Ensure zero static interferences between mates.

---

## 🛠️ Design Calculations & Sizing
To demonstrate engineering analysis, the coupling is sized using standard machine design equations:

### 1. Shaft Torque (\(T\))
Given power \(P = 70 \text{ kW}\) and speed \(N = 1500 \text{ RPM}\):
\[T = \frac{60 \times P}{2\pi N} = \frac{60 \times 70000}{2 \pi \times 1500} \approx 445.63 \text{ N}\cdot\text{m} \quad (\text{Designed for } 450 \text{ N}\cdot\text{m})\]

### 2. Shaft Shear Stress (\(\tau\))
Using the polar section modulus for a solid shaft of diameter \(d = 40 \text{ mm}\):
\[\tau = \frac{16 T}{\pi d^3} = \frac{16 \times 450 \times 10^3}{\pi \times 40^3} \approx 35.81 \text{ MPa}\]
*With AISI 1045 steel (Yield Strength \(\sigma_y = 310 \text{ MPa}\), Shear Yield Strength \(\tau_y \approx 155 \text{ MPa}\)), this design offers a safety factor of \(FS \approx 4.3\).*

---

## 📋 Component Specifications & BOM

| Item | Component | Qty | Material | Fit Class / Thread | Function |
|:---:|:---|:---:|:---|:---|:---|
| 1 | **Flange A** (Keyway) | 1 | Gray Cast Iron (Grade 25) | H7 (Hub Bore) | Keyed to driving shaft; features projecting protective rim. |
| 2 | **Flange B** (Keyway) | 1 | Gray Cast Iron (Grade 25) | H7 (Hub Bore) | Keyed to driven shaft; aligns with Flange A. |
| 3 | **Shaft** | 2 | Carbon Steel (AISI 1045) | g6 (Shaft OD) | Main rotating members transmitting input/output torque. |
| 4 | **Sunk Key** | 2 | Mild Steel (AISI 1020) | JS9 (Key Width) | Transmits torque between shaft and flange hub. |
| 5 | **Hex Bolt** | 4 | Medium Carbon Steel (Gr 8.8) | M12 × 1.75 | Fastens Flange A and B together. |
| 6 | **Hex Nut** | 4 | Carbon Steel (Gr 8) | M12 × 1.75 | Secures the hex bolts in place. |

---

## 🔄 Modeling & Assembly Workflow

### 1. Part Modeling Step-by-Step
- **Flanges (A & B)**:
  1. Created a 2D cross-sectional sketch of the flange profile, incorporating the protective lip and hub.
  2. Applied a **Revolved Boss/Base** feature around the central axis.
  3. Sketched a keyway profile (\(12 \text{ mm} \times 8 \text{ mm}\)) on the front face of the hub and applied an **Extruded Cut** (Through All).
  4. Created a bolt hole pitch circle diameter (PCD) of \(\varnothing 120 \text{ mm}\). Modeled a single M12 clearance hole using the **Hole Wizard**.
  5. Applied a **Circular Pattern** to generate 4 equally spaced clearance holes.
- **Keys & Shafts**:
  1. Extruded the shaft from a \(\varnothing 40 \text{ mm}\) circular sketch.
  2. Used a **Cut-Extrude** on a sketch plane tangent to the shaft to create a flat-bottomed key seat.
  3. Modeled the sunk key with fillet details (\(R=1 \text{ mm}\)) to minimize stress concentration.

### 2. Assembly Mates Configuration
In the assembly environment (`ProtectedFlangeCoupling.SLDASM`), the parts were mated in the following hierarchy:
1. **Shaft 1 to Origin**: The driving shaft was inserted first and **Fixed** at the assembly origin to set the main coordinate system.
2. **Flange A to Shaft 1**: 
   - **Concentric Mate**: Between the shaft outer diameter and the flange inner bore.
   - **Coincident Mate**: Between the flange hub back face and the shaft shoulder.
   - **Parallel Mate**: Between the shaft keyway side face and the flange keyway side face to align key channels.
3. **Key insertion**: Concentric/Coincident mates aligning the sunk key inside the aligned keyways.
4. **Flange B & Shaft 2**: Mated symmetrically to the driven side.
5. **Flange A to Flange B**:
   - **Coincident Mate**: Joining the two polished mating faces of Flange A and B.
   - **Concentric Mate**: Between the clearance bolt holes to align the pattern.
6. **Fasteners**: Concentric mates for the M12 bolts, with coincident mates securing the bolt heads and nuts inside the protective recesses.

---

## 🎨 Exploded View & Animation
Below is the design explosion sequence showing the assembly order (from center outwards):

```mermaid
graph LR
    Shafts --> Keys
    Keys --> Flanges
    Flanges --> Bolts
    Bolts --> Nuts
```

*The exploded state offsets the bolts axially by \(120 \text{ mm}\), the flanges by \(60 \text{ mm}\), and the keys radially by \(30 \text{ mm}\) for visual clarity in user documentation.*

---

## 📐 Drafting & Tolerancing Details

The technical drawings are designed for standard machine shop fabrication:
- **Projection Standard**: Third Angle Projection.
- **Section View**: A full axial offset sectional view displays internal keyways and mating faces.
- **GD&T Application**:
  - **Runout Tolerance**: \(0.02 \text{ mm}\) radial runout on the flange mating faces relative to the shaft axis to prevent vibration at high RPM.
  - **Perpendicularity**: \(0.03 \text{ mm}\) on the flange mating face relative to the shaft bore.
- **Surface Finish**: \(Ra \, 1.6 \ \mu\text{m}\) on mating faces, \(Ra \, 3.2 \ \mu\text{m}\) on general machined surfaces.

---

## 📁 Repository Deliverables

The deliverables for this project are organized as follows:

*   **Parts**: Contains individual SolidWorks part files ([`Parts/`](file:///c:/Users/VISHAV/OneDrive/Desktop/MECH%20PORTFOLIO/Projects/01_Protected_Flange_Coupling/Parts/))
    *   `01_01_flange_a.SLDPRT`
    *   `01_02_flange_b.SLDPRT`
    *   `01_03_shaft.SLDPRT`
    *   `01_04_key.SLDPRT`
*   **Assembly**: The master assembly file ([`Assembly/`](file:///c:/Users/VISHAV/OneDrive/Desktop/MECH%20PORTFOLIO/Projects/01_Protected_Flange_Coupling/Assembly/))
    *   `ProtectedFlangeCoupling_Assembly.SLDASM`
*   **Drawings**: 2D fabrication drawing sheets ([`Drawings/`](file:///c:/Users/VISHAV/OneDrive/Desktop/MECH%20PORTFOLIO/Projects/01_Protected_Flange_Coupling/Drawings/))
    *   `ProtectedFlangeCoupling_Assembly.SLDDRW`
    *   `ProtectedFlangeCoupling_Assembly.dwg`
*   **Neutral CAD / STEP**: Located in [Manufacturing/](file:///c:/Users/VISHAV/OneDrive/Desktop/MECH%20PORTFOLIO/Projects/01_Protected_Flange_Coupling/Manufacturing/)
    *   `ProtectedFlangeCoupling_Assembly.STEP` (AP214)
    *   `ProtectedFlangeCoupling_Assembly.PDF` (Ready-to-print 2D blueprint)

---

## 🏆 Skills Demonstrated

- **CAD Modeling (SolidWorks)**: Revolved features, circular patterns, hole wizards, advanced mating.
- **Machine Design Calculations**: Shaft torsional shear stress calculations, fastener spacing, material selection.
- **Geometric Dimensioning & Tolerancing (GD&T)**: Applying perpendicularity, runout, and limit fits (H7/g6).
- **Drafting & Documentation**: Structuring comprehensive mechanical Bill of Materials (BOM) and multi-view layouts.
