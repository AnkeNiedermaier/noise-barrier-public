# NoiseBarrierTool
The **NoiseBarrierTool** consist of individual PythonParts and enables the axis-related creation of noise barrier walls both as 3D objects and 2D drawings. Bais for the creation is a 3D surface (polyhedron) as terrain and a 3D polyline as route axis. Each step of the complete workflow can be executed with an individual PythonPart:
- **DrawPath** to determine the initial path
- **RecalculatePath** to aligne a modified path
- **SavePathPoints** to save the geometry and object parameters
- **CreateWallComponents** to create a 3D model of the noise barrier wall
- **DrawWallElevations** to create 2D longitudinal views of the noise barrier wall
- **DrawWallSection** to create 2D sections of the noise barrier wall piles

<img src = "./docs/NoiseBarrierContent.png" width = 450/>

Altough related to each other, the workflow steps are more or less idependent. Therefor besides creating noise barrier walls, the tool can also be used to calculate **route courses in a terrain** as placement basis for any kind of object. The ALLPLAN function **Copy along path** for example serves this purpose.


Another essential component of the tool is the Excel file **NoiseBarrierParameters.xlsx**. All parameters and key values of the noise barrier wall are saved and (re)calculated here.The file also enables the individual adaption and modification of each segment. In addition it can be used to retrieve coordinates and geometric values for further use, for example as basis for quantity or cost calculation.
Together with the other components, also several ***.rdlc  templates** are installed. They can be used to evaluate the 3D objects both as ALLPLAN reports or Excel tables. 

## Installation
The PythonPart **NoiseBarrierTool** can be installed directly from the Plugin Manager in ALLPLAN. 

Alternatively, the corresponding ***.allep** package can be downloaded from the [release page](https://github.com/AnkeNiedermaier/noise-barrier-public/releases). ***.allep** files are ALLPLAN internal setups that can be installed via drag and drop them into the program window.

At least the version 2026 is needed to install the PythonPart.

## Installed PythonPart Scripts
If the installation was successfull, the individual PythonParts of the **NoiseBarrierTool** as well as the Ecxel file **NoiseBarrierParameters.xlsx** can be found
in the ALLPLAN Library:
`Office` → `ALLPLAN GmbH` → `NoiseBarrierTool`
The ***.rdlc** files are also stored in the office folder:
`Office` → `Reports` → `NoiseBarrierTool`
Besides the library, the tools PythonParts can also be found in the ActionBar in a newly created task area **NoiseBarrierTool** inside the task **Plug-ins**.


## Preparation
As mentioned, the basis for the tool are **3D polylines** and connected close **3D areas** in the form of polyhedrons.

<img src = "./docs/Basic_Surface.png" width = 250/>
<img src = "./docs/Basic_Polyline.png" width = 250/>

Therefor it might be necessary to convert the existing ALLPLAN objects into such types. This is done in using functions from the **Modeling** modul, mainly **Convert Elements** and **Shell**.

<img src = "./docs/Prep_Convert_I.png" width = 150/>
<img src = "./docs/Prep_Convert_II.png" width = 150/>


To union individual areas, the **Boolean operator** of the same name can be used, as it not only serves for 3D bodies. All objects used as basis have to be on drawing files either in active or edit mode, as in reference mode a selection is not possible.




