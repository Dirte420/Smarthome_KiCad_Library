# Smarthome KiCad Library

My custom library for KiCad which includes various symbols, footprints and 3D models for devices and modules which are often used for smarthome DIY projects.

## Installation

- Clone this repository to any location on your computer.
- Create an environment variable called `MY_KICAD_LIB` and assign the location where you cloned the repository to this variable.
- Open KiCad > Preferences > Manage Symbol Libraries... and create a new global library entry with Nickname `Smarthome` and Library Path `${MY_KICAD_LIB}/symbols/Smarthome.kicad_sym`.
- Open KiCad > Preferences > Manage Footprint Libraries... and create a new global library entry with Nickname `Smarthome` and Library Path `${MY_KICAD_LIB}/footprints/Smarthome.pretty`.
