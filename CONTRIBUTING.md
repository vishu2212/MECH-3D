# Contributing Guidelines

Welcome to the **Mechanical CAD Portfolio** repository! This document outlines the standards, naming conventions, and best practices required when contributing mechanical designs, assemblies, drawings, or resources to this repository.

These guidelines ensure that all CAD files are clean, parameterized, industry-compliant, and optimized for collaboration.

---

## 📂 Repository & Folder Structure

All projects must follow this rigid directory structure to maintain consistency across the portfolio:

```text
Projects/XX_Project_Name/
├── README.md               # Project-specific documentation & design report
├── Images/                 # Renders, screenshots, exploded views, animations
├── Parts/                  # Individual CAD parts (.SLDPRT, .ipt, etc.)
├── Assembly/               # CAD assembly files (.SLDASM, .iam, etc.)
├── Drawings/               # 2D engineering drawings (.SLDDRW, .dwg, .dxf)
├── BOM/                    # Bill of Materials spreadsheets (.xlsx, .csv)
├── Manufacturing/          # Fabrication files (STEP, STL, IGES, G-code)
└── Resources/              # Vendor datasheets, calculations, references
```

---

## 🏷️ Naming Conventions

Consistency in file naming prevents broken references in assemblies. Please adhere to the following rules:

### 1. Parts (`Parts/`)
- Use **Snake Case** with a numeric prefix denoting assembly hierarchy.
- Format: `[Hierarchy_ID]_[part_name].SLDPRT`
- *Example*: `01_01_flange_a.SLDPRT`, `01_02_tapered_key.SLDPRT`

### 2. Assemblies (`Assembly/`)
- Use **Pascal Case** for assemblies.
- Format: `[Project_Name]_Assembly.SLDASM`
- *Example*: `ProtectedFlangeCoupling_Assembly.SLDASM`

### 3. Drawings (`Drawings/`)
- Match the drawing name exactly to the part or assembly it represents.
- *Example*: `01_01_flange_a.SLDDRW`, `ProtectedFlangeCoupling_Assembly.SLDDRW`

---

## 📐 CAD Modeling Standards (SolidWorks & AutoCAD)

To ensure files can be easily edited and are parameterized:

### 1. Part Modeling Check
- **Fully Defined Sketches**: All sketches *must* be fully defined. Avoid blue under-defined lines.
- **Intentional Design Rules**: Rename key features (e.g., `M12_Tapped_Hole`, `Main_Revolve`, `Keyway_Cut`) to make the design tree easy to navigate.
- **Materials**: Always assign a specific material and density (e.g., *AISI 1020 Steel*, *Alloy 6061-T6*) in the feature tree to ensure correct mass calculations in the BOM.

### 2. Assembly Design
- **First Component Fixed**: Fix the base component at the origin `(0,0,0)` to orient the assembly coordinate system properly.
- **Mate Hierarchy**: Use logical mates. Avoid redundant or over-defining mates. Use Sub-assemblies for complex mechanisms.
- **Interference Detection**: Perform an interference check before submitting. No interferences should exist unless they represent press-fits (clearly documented).

---

## 📝 Technical Drawing & Drafting Standards

All 2D drawings must follow standard ASME or ISO conventions:

1. **Projection Angle**: State the projection system (First Angle or Third Angle) on the title block.
2. **GD&T / Tolerancing**: Apply Geometric Dimensioning & Tolerancing (GD&T) to critical fit surfaces (e.g., shaft-to-bore fits should specify cylindrical tolerances and runout).
3. **Title Block**: Fill in the drawing title, scale, material, weight, sheet size, and drawing number.
4. **BOM & Balloons**: Assemblies must have a Bill of Materials table with parts numbered and matched to callout balloons.

---

## 📤 Manufacturing & Export Formats

In addition to native SolidWorks files, every project must provide the following open-source/neutral formats under the `Manufacturing/` directory:

- **3D Neutral Format**: `.STEP` (preferred standard: **STEP AP214** to retain color/assembly data).
- **3D Printing**: `.STL` or `.3MF` (high resolution, binary format).
- **2D Vector Graphics**: `.DXF` (for sheet metal laser cutting) and `.PDF` (for readable drawing sheets).

---

## 🛠️ Submission Checklist

Before submitting a Pull Request, verify the following:
- [ ] No broken file references in Assemblies.
- [ ] Sketches are fully defined.
- [ ] Interference check reports zero interferences.
- [ ] 2D drawing PDFs are exported and legible.
- [ ] Neutral STEP and DXF files are generated.
- [ ] The README inside the project folder is updated with the latest specifications.
