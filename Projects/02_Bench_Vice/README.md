# Bench Vice Assembly

# Project Overview
This project is a 3D assembly of a mechanical bench vice. A bench vice is a clamping tool mounted to a workbench, designed to hold workpieces securely during operations like filing, sawing, drilling, or assembly. Rotation of the lead screw translates into linear motion of the movable jaw, clamping the workpiece against the fixed jaw on the base.

# Components
The assembly consists of the following components:
* **Base**: The main casting containing the fixed jaw and mounting slots.
* **Movable Jaw**: The sliding body that moves along the guide rails to clamp the workpiece.
* **Movable Jaw Plate**: Plates attached to the jaws to provide a secure grip and protect the jaws from wear.
* **Lead Screw**: The main threaded spindle that drives the movable jaw.
* **Handle**: The shaft inserted through the lead screw head to rotate the screw.
* **Knob**: Caps screwed onto the handle ends to keep the handle in place.
* **Bushing**: The sleeve inserted into the base to support the lead screw.
* **Washer**: A flat spacer situated between the screw spindle collar and the base face.

# Software Used
* SolidWorks

# Project Workflow
* **Part Modeling**: Sketched and extruded the base and movable jaw. Revolved features were used to model the lead screw, handle, knobs, and bushing. The jaw plate features textured grip cuts.
* **Assembly Creation**: Inserted the base first and fixed it at the origin. Mated the movable jaw to the base slots, then aligned the lead screw, washer, handle, and knobs.
* **Applying Mates**: Used concentric mates for the screw spindle, bushing, and handle, coincident mates for the washer and jaw plates, and advanced width/distance limits to constrain the sliding jaw's travel range.
* **Creating Engineering Drawings**: Formatted multi-view layouts of the vice assembly (planned).
* **Exporting Project Files**: Saved the assembly and parts in native SolidWorks formats and exported renders.

# Repository Contents
* `Assembly/` - Contains the master SolidWorks assembly file (`Bench_Vice.SLDASM`).
* `Parts/` - Contains individual SolidWorks part files (`Base.SLDPRT`, `Bushing.SLDPRT`, `Handle.SLDPRT`, `Knob.SLDPRT`, `Movable_Jaw_Plate.SLDPRT`, `Movable_Jaw.SLDPRT`, `Lead_Screw.SLDPRT`, `Washer.SLDPRT`).
* `Images/` - Contains JPEG rendering files showing the vice assembly (`Bench_Vice_Render1.JPG`, `Bench_Vice_Render2.JPG`, `Bench_Vice_Render3.JPG`).
* `Drawings/` - Placeholder for future 2D engineering drawings.
* `BOM/` - Placeholder for the Bill of Materials.
* `Manufacturing/` - Placeholder for future STEP and neutral CAD files.
* `Resources/` - Placeholder for calculations or reference files.

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
* **Creating Parametric Parts**: Practiced assigning sketch constraints so that sliding guides and clearances update dynamically if dimensions are changed.
* **Understanding Assembly Relationships**: Practiced using concentric and limit mates to restrict the movable jaw to single-axis linear motion.
* **Working with Engineering Drawings**: Learned how internal clearances (e.g., between the lead screw, bushing, and base) are represented using section cuts in 2D sheets.
* **Organizing CAD Files**: Maintained a clean folder hierarchy, keeping parts and assemblies separate, which prevented broken reference warnings when opening the model.
* **Learning SolidWorks Workflow**: Gained experience with sliding assemblies, axis alignments, and custom threads.

# Future Improvements
* Additional renders
* Exploded view
* Animation
* Manufacturing drawings
* STEP exports
