# Oldham Coupling

# Project Overview
This project is a 3D assembly of an Oldham coupling in SolidWorks. An Oldham coupling is a mechanical coupling designed to connect two parallel shafts that have lateral (radial) misalignment. It transmits torque between the shafts using a three-piece design: two flanges keyed to the shafts and a floating center disc with perpendicular tongue-and-groove slots that slide to accommodate the offset.

# Components
The assembly consists of the following components:
* **Flange**: Two matching flanges (driving and driven) with slots to receive the center disc.
* **Disc**: The floating center disc with perpendicular grooves on its opposite faces.
* **Shaft**: Cylindrical rotating power shafts.
* **Key**: Sunk keys to link the shafts to the flanges and prevent slip.

# Software Used
* SolidWorks

# Project Workflow
* **Part Modeling**: Modeled the cylindrical flanges and cut slots at 90-degree offsets. Sketched and extruded the shafts, keys, and center disc.
* **Assembly Creation**: Inserted the shafts with a lateral offset to simulate misalignment. Fixed the input shaft at the origin, then aligned the flanges, keys, and sliding center disc.
* **Applying Mates**: Used concentric mates for the shafts and flange hubs, coincident mates to seat the keys, and mechanical sliding constraints to allow the center disc to slide inside the flange slots.
* **Creating Engineering Drawings**: Generated 2D drawings for the individual parts (flange, disc) and the overall assembly layout.
* **Exporting Project Files**: Saved native SolidWorks files (`.SLDPRT`, `.SLDASM`, `.SLDDRW`) and standard sheet formats (`.slddrt`).

# Repository Contents
* `Assembly/` - Contains the master assembly (`Oldham_Coupling.SLDASM`), subassembly (`Flange_Subassembly.SLDASM`), and secondary assembly (`Oldham_Coupling_Assem1.SLDASM`).
* `Parts/` - Contains individual part files (`Disc.SLDPRT`, `Flange.SLDPRT`, `Key.SLDPRT`, `Shaft.SLDPRT`).
* `Drawings/` - Contains detailed 2D engineering drawings (`Oldham_Coupling_Drawing.SLDDRW`, `Disc_Drawing.SLDDRW`, `Flange_Drawing.SLDDRW`, `Oldham_Drawing.SLDDRW`) and custom sheet formats (`Oldham_Sheet_Format.slddrt`).
* `Images/` - Placeholder for future renderings and screenshots.
* `BOM/` - Placeholder for the Bill of Materials.
* `Manufacturing/` - Placeholder for future STEP and neutral CAD files.
* `Resources/` - Placeholder for design references.

# Skills Demonstrated
* 3D Part Modeling
* Assembly Design
* Engineering Drawings
* Parametric Modeling
* Dimensioning
* Mechanical Components
* Technical Documentation
* SolidWorks

# Key Learnings
* **Creating Parametric Parts**: Practiced designing perpendicular mating slots and keys that align relative to the central axes.
* **Understanding Assembly Relationships**: Learned how to define sliding constraints that allow a component to move relative to two perpendicular mating guides simultaneously.
* **Working with Engineering Drawings**: Gained experience setting up custom drawing sheet templates (`.slddrt`) and detailing multi-part assembly sheets.
* **Organizing CAD Files**: Organized subassemblies (`Flange_Subassembly.SLDASM`) and nested parts to prevent broken reference links.
* **Learning SolidWorks Workflow**: Explored the use of mechanical mates for sliding components.

# Future Improvements
* Additional renders
* Exploded view
* Animation
* Manufacturing drawings
* STEP exports
