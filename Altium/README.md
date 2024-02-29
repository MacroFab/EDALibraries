### Altium
***
**Altium Libraries and documentation.**

This directory contains the files needed to generate manufacturing data from Altium 21 and up for MacroFab, INC.

Please see the altium documentation at the [knowledge base](https://help.macrofab.com/knowledge/how-do-i-use-altium-with-macrofab) on MacroFab, INC. for more information. 

***
**License Information**

This project is under the [Creative Commons Attribution 4.0 International License](LICENSE.md). These files are provided with no warranty and should be used at your own risk. 

***
| Directory | Description |
|---|---|
| BOM | BOM Template |
| DRC | Design Rules | 
| IntLib | Integrated Libraries compiled from Source |
| Outjob | Output template for Macrofab |
| Source | LibPkg, PcbLib, and SchLib files for components |
| Stackup | PCB Layer Stackup |

***
### Mecanical Layer Definitions

The layers used in the footprints are defined as `Layer Typed Component Layer Pairs` and so if your PCB already has a corresponding named `Layer Type`, the mechanical layer number should automatically be changed to match the PCB. If you don't use named `Layer Types` here are the definitions.

| Top | Bottom | Layer |  Description |
| --- | --- | --- | --- |
| M13 | M14 | 3D Body | 3D Model, step, x_t, or extruded |
| M5 | M6 | Assembly | Compoent outline and assembly notes|
| M15 | M16 | Courtyard | Bounding box for component placement |
| M11 | M12 | THT Solder | Marks through hole pads that need to be soldered but should not on be the solder stencil |


***
### How to use the IntLibs

To install libraries to a single project:
 1. Click the hamburger at the top of the `Components` panel
 1. Click `File-based Libraries Preferences...`
 1. Click on the `Project` tab
 1. Click `Add Library...`
 1. Navigate to `[Path]/Macrofab_EDALibraries/Altium/Intlib`
 1. Change the filetype from `*.DBLIB` to `*.INTLIB`
 1. Select all of the libraries and click Open

To install libraries globally:
 1. Click the hamburger at the top of the `Components` panel
 1. Click `File-based Libraries Preferences...`
 1. Click on the `Installed` tab
 1. Click `Install...`
 1. Navigate to `[Path]/Macrofab_EDALibraries/Altium/Intlib`
 1. Change the filetype from `*.DBLIB` to `*.INTLIB`
 1. Select all of the libraries and click Open

***
### Upload libriares to Altium365

In order to upload the parts to your Altium365 Component Database:
 1. Open the `*.LibPkg` from the `Source` folder
 1. Right-click on the `*.SchLib` and click `Migrate Library`
 1. Open the Adanced Menu
 1. Right-click on the `_Template` parts and `Exclude from Migration`
 1. Select the correct `Component Type` and `Folder` 

