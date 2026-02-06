# NoiseBarrierTool
The **NoiseBarrierTool** consist of individual PythonParts and enables the axis-related creation of noise barrier walls both as 3D objects and 2D drawings. Bais for the creation is a 3D surface (polyhedron) as terrain and a 3D polyline as route axis. Each step of the complete workflow can be executed with an individual PythonPart:
- **DrawPath** to determine the initial path
- **RecalculatePath** to aligne a modified path
- **SavePathPoints** to save the geometry and object parameters
- **CreateWallComponents** to create a 3D model of the noise barrier wall
- **DrawWallElevations** to create a 2D longitudinal views of the noise barrier wall
- **DrawWallSection** to create 2D sections of the noise barrier wall piles

<img src = "./docs/NoiseBarrierContent.png" width = 450/>

Another main component of the tool is the Excel file **NoiseBarrierParameters.xlsx**.

## Installation
The PythonPart **NoiseBarrierTool** can be installed directly from the Plugin Manager in ALLPLAN. 

Alternatively, the corresponding ***.allep** package can be downloaded from the [release page](https://github.com/AnkeNiedermaier/noise-barrier-public/releases). ***.allep** files are ALLPLAN internal setups that can be installed via drag and drop into the program window.

At least the version 2026 is needed to install the PythonPart.

## Installed PythonPart Scripts
If the installation was successfull, the individual PythonParts of the **NoiseBarrierTool** as well as the Ecxel file **NoiseBarrierParameters.xlsx** can be found
in the ALLPLAN Library:
`Office` → `ALLPLAN GmbH` → `NoiseBarrierTool`
