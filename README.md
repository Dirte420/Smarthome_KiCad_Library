# Smarthome KiCad Library

My custom library for KiCad which includes various symbols, footprints and 3D models for devices and modules which are often used for smarthome DIY projects.

## Installation

- Clone this repository to any location on your computer.
- Create an environment variable called `MY_KICAD_LIB` and assign the location where you cloned the repository to this variable.
- Open KiCad > Preferences > Manage Symbol Libraries... and create a new global library entry with Nickname `Smarthome` and Library Path `${MY_KICAD_LIB}/symbols/Smarthome.kicad_sym`.
- Open KiCad > Preferences > Manage Footprint Libraries... and create a new global library entry with Nickname `Smarthome` and Library Path `${MY_KICAD_LIB}/footprints/Smarthome.pretty`.

## Structure

- Symbols are located in subdirectory `/symbols` and at least for now there is only one symbol-library file called `Smarthome.kicad_sym` which includes all symbols.
- Footprints are located in subdirectory `/footprints` where there is already a `Smarthome.pretty` library where all footprint-files (`*.kicad_mod`) are located.
- 3D-Models (step-files) are located in subdirectory `/3dmodels`.

## Creating new symbols / footprints

### Symbol

- If possible try to avoid to create additional symbol-library-files (*.kicad_sym) because it is necessary to add all of the manually in the KiCad Symbol Library Manager.  
- Instead try to use the existing `Smarthome.kicad_sym` symbol library.
- If possible reuse already existing symbols (copy from existing) and don't draw new symbols if not really necessary.
- Make sure all pins are declared correctly (electrical type, pin name, pin number).
- Assign correct Reference (U, PS,...), Value and footprint to the symbol.

### Footprint

- Get exact mechanical dimensions from datasheet.
- It is recommended to use AI as assistant for creating the footprint (to get the exact dimensions, pad-diameter,...)
- Place pads first and make sure the size and drill-diameter is correct.
- Draw outlines of the actul device on F.Fab, line width 0,1mm
- Draw Silkscreen with a distance of xx to F.Fab, line width 0,2mm
- Draw Courtyard with a distance of xx to Silkscreen on F.Silkscreen, line width 0.05mm
- Assign correct Value, Descrioption and Name and also assign the correct 3D model (placed according to the footprint) and only use paths using environment variable ${MY_KICAD_LIB} followed by a relative path.

### 3D Model

Naming convention is `<MANUFACTURER>_<MODEL>`

- A 3D model is not mandatory but highly recommended
- If not possible to download 3D models from manufacturer website it is recommended to search at Mouser or GrabCAD
- It is also possible to AI generate a 3D model
