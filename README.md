# NoiseBarrierTool
The **NoiseBarrierTool** consist of individual PythonParts and enables the axis-related creation of noise barriers both as 3D objects and 2D drawings. Bais for the creation is a 3D surface (polyhedron) as terrain and a 3D polyline as route axis. Each step of the complete workflow can be executed with an individual PythonPart:
- **DrawPath** to determine the initial path
- **RecalculatePath** to aligne a modified path
- **SavePathPoints** to save the geometry and object parameters
- **CreateWallComponents** to create a 3D model of the noise barrier
- **DrawWallElevations** to create 2D longitudinal views of the noise barrier
- **DrawWallSection** to create 2D sections of the noise barrier piles

<img src = "./docs/NoiseBarrierContent.png" width = 450/>

Altough related to each other, the workflow steps are more or less idependent. Therefor besides creating noise barrierss, the tool can also be used to calculate **route courses in a terrain** as placement basis for any kind of object. The ALLPLAN function **Copy along path** for example serves this purpose.


Another essential component of the tool is the Excel file **NoiseBarrierParameters.xlsx**. All parameters and key values of the noise barrier are saved and (re)calculated here.The file also enables the individual adaption and modification of each segment. In addition it can be used to retrieve coordinates and geometric values for further use, for example as basis for quantity or cost calculation.
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
As mentioned, the basis for the tool are **3D polylines** and connected close **3D areas** in the form of surfaces/polyhedrons.

<img src = "./docs/Basic_Surface.png" width = 350/>          <img src = "./docs/Basic_Polyline.png" width = 350/>

Therefor it might be necessary to convert the existing ALLPLAN objects into such types. This is done in using functions from the **Modeling** modul, mainly **Convert Elements** and **Shell**.

<img src = "./docs/Prep_Convert_I.png" width = 150/>           <img src = "./docs/Prep_Convert_II.png" width = 150/>


To union individual areas, the **Boolean operator** of the same name can be used, as it not only serves for 3D bodies. All objects intended as basis have to be on drawing files either in **active** or **edit mode**, as in reference mode a selection is not possible.

## Workflow

The complete workflow with all the options the tool offers, from drawing the inital path up to the evaluation of the wall components, contains several steps. Most of them are also represented by one of the individual PythonParts:
- defining the inital noise barrier path
- modifying it to fit the local conditions
- recalculating the the modified path
- saving coordinates and object parameters
- adjusting individual wall segments
- creating 3D models of the noise barrier
- drawing views and sections
- evaluating the 3D objects

Altgough they are executed separte and not necessarily sequently, initial definition and saving in the excel file are mandatory to create objects or drawings in ALLPLAN. Therefor it is recommended to follow the described order and skip not beeded steps inbetween the workflow.

In general, all installed PythonParts can be found in the **Library palette**, no matter if an additional ActionBar entry is created or not. They are started either with a **double-click** on the icon or per **Drag and Drop** into the viewport. This shows the corresponding Properties palette and executes the underlying skripts.
##
### Step I: PythonPart DrawPath
Calculation of the inital noise barrier path concurrent to the existing route course polyline
- selection of the terrain (3D surface) and the route axis (3D polyline) in the given order
- input of the desired values for path distance from axis and lenght of the single segments
- definition of the axis part to take over, either complete or in entering a start and end point number
- definition of the direction (ascending/descending) of the calculation
- setting of the path and numbering format (pen, stoke, color layer)

Once terrain and route are selected, a preview  is shown and can be adapted in changing the palette values. With the create button the inital path is drawn as element group of a 3D polyline and 2D text in the current active drawing file.<br>
>**HINT**: as the palette stays open, it is possible to draw several paths at once with different distance and segmentation and also new sources for route and terrain can be choosen<br>
##
### Step II: Path modification
Calculation of the inital noise


