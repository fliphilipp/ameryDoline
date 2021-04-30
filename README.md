# Rapid formation of an ice doline on Amery Ice Shelf, East Antarctica

## Key Points:
- Satellite images showed an 11 km$^2$ depression on Amery Ice Shelf as an ice-covered lake drained abruptly in winter 2019 forming an ice doline
- ICESat-2 and WorldView data show elevation fell as much as 80 m in the depression, amidst 60 km$^2$ of hydrostatic rebound and uplift over 36 m
- ICESat-2 photon data profiled a new meltwater channel, incised when a lake formed by the flexural uplift overflowed into the doline in 2020


## Plain Language Summary:

Surface melting over Antarctica’s floating ice shelves is predicted to increase significantly during coming decades, but the implications for their stability are unknown. The Antarctic Peninsula has already seen meltwater driven ice shelf collapses. We are still learning how meltwater forms, flows and alters the surface, and that rapid water-driven changes are not limited to summer. We present high-resolution satellite data (imagery and altimetry) showing an abrupt change on East Antarctica’s Amery Ice Shelf in June 2019 (midwinter). Meltwater stored in a deep, ice-covered lake drained through to the ocean below, leaving a deep, uneven 11 km2 depression of fractured ice (a “doline”) in the ice shelf surface. The reduced load on the floating ice shelf resulted in flexure, with uplift of up to 36 m centered on the former lake. Simple flexure modeling showed that this corresponds to about 0.75 km$^3$ of water being lost to the ocean. ICESat-2 observations in summer 2020 profiled a new narrow channel inside the doline as meltwater started refilling it from a new lake created by the flexure. ICESat-2’s capacity to observe surface processes at small spatial scales greatly improves our ability to model them, ultimately improving the accuracy of our projections.

## Contents:
1. **Main Scripts**
    - [Fig1_formation_of_doline_on_Amery_Ice_Shelf.ipynb](/Fig1_formation_of_doline_on_Amery_Ice_Shelf.ipynb): Jupyter notebook that outputs Fig. 1 in the paper. 
    - [Fig2_height_change_profiles.ipynb](/Fig2_height_change_profiles.ipynb): Jupyter notebook that outputs elevation profile comparisons for Fig. 2 in the paper.
    - [Fig3_first_melt_season_after_doline_formation.ipynb](/Fig3_first_melt_season_after_doline_formation.ipynb): Jupyter notebook that outputs Fig. 3 in the paper. 
2. **Directories**
    - [data/IS2/](/data/IS2/): Contains pickle files with all the relevant ICESat-2 data. Data can also be read in from the corresponding .h5 files, which are available from NSIDC.
    - [data/L8/](/data/L8/): Contains the Landsat 8 data used for Figs 1 and 3. The mosaic for Fig 1 is in the main folder, the pan-sharpened and windowed images for Figures 1 and 3 are in the [pansharpened](/data/L8/pansharpened/) subdirectory.
    - [data/siogz/](/data/siogz/): Contains grounding line data for plotting maps in Fig 1.
    - [figs/](/figs/): Contains the figures / output from the main scripts.
    - [readers/](/readers/): Contains helper functions to read ICESat-2 data from .h5 files to Python dictionaries. 
3. **Helper functions / code**
    - [0_process_L8_pansharpening.ipynb](/0_process_L8_pansharpening.ipynb): Jupyter notebook that reads the required Landsat 8 image files directly from S3, pan-sharpens and windows them, and writes them to files. This was used to produce the files in *data/L8/pansharpened*
    - [mosaic_windowing_downsampling.ipynb](/mosaic_windowing_downsampling.ipynb): Contains code to create smaller Landsat-8 mosaic files from a massive image that is too large and inconvenient to put on github.
    - [curve_intersect.py](/curve_intersect.py): A helper function that is needed to label the graticule on the maps produced.

![Fig1_formation_of_doline_on_Amery_Ice_Shelf](figs/Fig1_formation_of_doline_on_Amery_Ice_Shelf_revised.jpg)

![Fig2_DEM differencing and elevation profile comparison](figs/figure_2.png)

![Fig3_first_melt_season_after_doline_formation](figs/Fig3_first_melt_season_after_doline_formation_revised.jpg) 
