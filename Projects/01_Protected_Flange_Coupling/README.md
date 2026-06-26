# Protected Flange Coupling

# Project Overview
This project is a 3D assembly of a protected flange coupling. A flange coupling is a mechanical device used to connect two rotating shafts to transmit power from one to the other. The "protected" design uses a flange with a raised outer rim that covers the bolt heads and nuts. This rim shields the rotating fasteners, helping to prevent accidents or clothing entanglement in a workshop environment.

# Components
The assembly consists of the following components:
* **Flange A**: The driving flange containing a central bore and keyway.
* **Flange B**: The driven flange which mates directly with Flange A.
* **Shaft**: The cylindrical transmission shaft (modeled for both input and output sides).
* **Key**: A rectangular sunk key used to lock the shaft to the flange hub and prevent relative rotation.
* **Nut**: Hexagonal nuts to secure the fastening bolts.

# Software Used
* SolidWorks

# Project Workflow
* **Part Modeling**: Sketched and extruded the shafts, keys, nuts, and flanges. Revolved profiles were used for the flanges to create the concentric hubs and protective outer rims.
* **Assembly Creation**: Inserted the parts into the SolidWorks assembly environment.
* **Applying Mates**: Used concentric mates to align the shafts with the flange bores, coincident mates to seat the key in the keyways and align the flanges, and parallel mates to align the keyways.
* **Creating Engineering Drawings**: Generated orthogonal view layouts of the final assembly (planned).
* **Exporting Project Files**: Saved the assembly and parts in native SolidWorks formats and exported renders.

# Repository Contents
* `Assembly/` - Contains the master SolidWorks assembly file (`Protected_Flange_Coupling.SLDASM`).
* `Parts/` - Contains the individual SolidWorks part files (`Flange_A.SLDPRT`, `Flange_B.SLDPRT`, `Shaft.SLDPRT`, `Key.SLDPRT`, `Nut.SLDPRT`).
* `Images/` - Contains JPEG rendering files showing the assembled coupling (`Protected_Flange_Coupling_Render1.JPG`, `Protected_Flange_Coupling_Render2.JPG`).
* `Drawings/` - Placeholder for future 2D engineering drawings.
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
* **Creating Parametric Parts**: Learned how to define geometric relations and dimensions in 2D sketches to ensure parts can be easily resized or modified.
* **Understanding Assembly Relationships**: Practiced using concentric, coincident, and parallel mates to assemble individual components with appropriate degrees of freedom.
* **Working with Engineering Drawings**: Understood how 3D models translate into standard 2D views for technical documentation.
* **Organizing CAD Files**: Learned the importance of structured folder hierarchies and clean file names to avoid broken references when working with SolidWorks assemblies.
* **Learning SolidWorks Workflow**: Gained experience navigating SolidWorks tools, from initial sketches to revolving profiles and mating complex assemblies.

# Future Improvements
* Additional renders
* Exploded view
* Animation
* Manufacturing drawings
* STEP exports
