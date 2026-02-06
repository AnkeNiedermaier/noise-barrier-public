# NoiseBarrierTool
The **NoiseBarrierTool** consist of individual PythonParts and enables the creation of noise barriers based on a 3D surface as terrain and a 3D polyline as route axis
- **DrawPath** a new layer file from an external template
- **RecalculatePath** an existing layer file
- **SavePathPoints** of a layer file modified in Excel
- **CreateWallComponents** a new layer file from an external template
- **DrawWallElevations** an existing layer file
- **DrawWallSection** of a layer file modified in Excel

The Excel file used for this purpose has to follow the provided schema to make sure that the PythonPart can read it when executed.

## Installation
The PythonPart **NoiseBarrierTool** can be installed directly from the Plugin Manager in ALLPLAN. 

Alternatively, the corresponding ***.allep** package can be downloaded from the [release page](https://github.com/AnkeNiedermaier/noise-barrier-public/releases). ***.allep** files are ALLPLAN internal setups that can be installed via drag and drop into the program window.

At least the version 2026 is needed to install the PythonPart.

## Installed PythonPart Scripts
If the installation was successfull, the PythonPart **LayerHandling.pyp** as well as the Ecxel schema template **Schema_LayerHandling.xlsx** can be found
in the ALLPLAN Library:
`Office` → `ALLPLAN GmbH` → `NoiseBarrierTool`
