# Contributing Guidelines

Welcome to the **Mechanical CAD Portfolio** repository! This document outlines simple guidelines and naming conventions to keep CAD files organized and consistent.

---

## 📂 Folder Structure

Each project folder is organized as follows:

```text
Projects/XX_Project_Name/
├── README.md               # Project description and details
├── Images/                 # Screenshots and renders
├── Parts/                  # SolidWorks part files (.SLDPRT)
├── Assembly/               # SolidWorks assembly files (.SLDASM)
├── Drawings/               # 2D engineering drawings (.SLDDRW, .PDF)
├── BOM/                    # Bill of Materials spreadsheets (.xlsx, .csv)
├── Manufacturing/          # Neutral CAD files (STEP, STL)
└── Resources/              # Calculations or reference worksheets
```

---

## 🏷️ Naming Conventions

To prevent broken references when opening SolidWorks assemblies on different computers, please use descriptive and consistent file names:

### 1. Parts (`Parts/`)
* Use descriptive names with words separated by underscores.
* Capitalize the first letter of each word.
* *Example*: `Flange_A.SLDPRT`, `Key.SLDPRT`, `Shaft.SLDPRT`

### 2. Assemblies (`Assembly/`)
* Use descriptive names with words separated by underscores.
* Capitalize the first letter of each word.
* *Example*: `Protected_Flange_Coupling.SLDASM`, `Bench_Vice.SLDASM`

### 3. Drawings (`Drawings/`)
* Match the drawing name to the part or assembly it represents.
* *Example*: `Protected_Flange_Coupling_Drawing.SLDDRW`

---

## 📐 CAD Design Standards

* **Fully Defined Sketches**: Ensure 2D sketches are fully defined before creating features. Under-defined sketches (blue lines) should be avoided.
* **Feature Tree Organization**: Name important features (e.g., `Main_Revolve`, `Keyway_Cut`) to make the design tree easier to understand.
* **Assembly Mates**: Use logical mates (concentric, coincident, parallel) and ensure the base part of the assembly is fixed.
* **Interference Checks**: Check for static interferences in the assembly before saving.
