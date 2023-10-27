# ENSO-Antarctica
Data used for the publication: 

Huguenin, M. F., Holmes, R. M., Spence, P. and England, M. H. (2023). Subsurface warming of the West Antarctic continental shelf linked to El Niño-Southern Oscillation. In review at *Geophysical Research Letters*.

See also [ENSO-Antarctica_scripts](https://github.com/mauricehuguenin/ENSO-Antarctica_scripts) for the analysis scripts.

# A Note on the Model Input for the Perturbation Experiments
The full forcing for the El Niño and La Niña simulations is constructed by adding for each input field the ENSO spatial patterns multiplied by the composite time series to the climatological repeat year forcing. That means, for example for the surface air temperature field during El Niño, we multiply the *tas_10m* spatial map (x,y) in [ENSOAnt_data/FigS5_All_Spatial_Maps_anoms_EN.nc](ENSOAnt_data/FigS5_All_Spatial_Maps_anoms_EN.nc) with composite time series (t), the fifth column in [ENSOAnt_data/Fig1d_Time_Series_Composite_EN.nc](ENSOAnt_data/Fig1d_Time_Series_Composite_EN.nc), and add the resulting field (t, x, y) to the repeat year forcing (t, x, y).

# Full 5 TB Model Output Data on the NCI Supercomputer Gadi
```
| Description of simulation | From where I run the simulation | Input files                      | Output stored on              |
| ------------------------- | ------------------------------- | -------------------------------- | ----------------------------- |
| Control run               | * + 01deg_jra55_ryf_Control/    | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_Control/ |
| El Niño simulation        | * + 01deg_jra55_ryf_ENFull/     | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_ENFull/  |
| "    "    "    "          |                                 | *** + forcing_mean_anoms_ENFull/ |                               |
| La Niña simulation        | * + 01deg_jra55_ryf_LNFull/     | /g/data/ua8/JRA55-do/RYF/v1-3/   | ** + 01deg_jra55_ryf_LNFull/  |
| "    "    "    "          |                                 | *** + forcing_mean_anoms_LNFull/ |                               |
| Location of repeat year climatological forcing: /g/data/ua8/JRA55-do/RYF/v1-3/                                                 |
```
\* `/home/561/mv7494/`
\** `/g/data/e14/mv7494/access-om2/archive/`
\*** `/g/data/e14/mv7494/ENSOAnt_input/`


# To Do:
- clean up scripts
- upon acceptance, check final order of SI figures and update the list including the link to scripts
- upon acceptance, check all data and update metadata in the ENSOAnt_data folder
- rename scripts so they are easier to understand
- when final, push to zenodo and create doi
