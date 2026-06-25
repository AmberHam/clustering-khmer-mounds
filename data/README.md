# Data

The data files used in this analysis cannot be included in this repository due to 
EFEO licensing restrictions. Two files are required to run the notebooks:

## 1. `isaura_features.gpkg`
The primary input dataset. This file was derived from the `features.gpkg` file 
included in the original Archaeoscape dataset, clipped to the extent of 
`08_isaura_extent_parcels.gpkg` to isolate the Isaura parcel. It contains 
mound, temple, hydrology and void polygons for that parcel.

**Source**: derived from `features.gpkg`, available via https://archaeoscape.ai/data/2024/  

## 2. `08_isaura_extent_parcels.gpkg`
A parcel boundary file derived from the `parcels.gpkg` file included in the 
original Archaeoscape dataset. It defines the spatial extent of the Isaura parcel 
and is used to set figure axes and clip the KDE grid across all notebooks.

**Source**: derived from `parcels.gpkg`, also available via https://archaeoscape.ai/data/2024/  

---

## Attribution

Data attribution: © École française d'Extrême-Orient (EFEO).  
All use must comply with the Archaeoscape/EFEO licence terms.

## Coordinate system

The dataset uses a local metric coordinate system with origin at (0, 0). 
Coordinates are in metres. No reprojection is applied; all spatial operations 
are performed in native coordinates.

## Feature classes used

| Class | Count (Isaura) | Used in analysis |
|---|---|---|
| Mounds | 2,671 | Yes — primary analysis input |
| Temples | 192 | Yes — contextual overlay and TDR evaluation |
| Hydrology | 3,911 | Yes — contextual overlay only |
| Void | 469 | No — excluded
