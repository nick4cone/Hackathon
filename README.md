# Hackathon
## May 12
* at least 9 modeling groups provided data
* regional and global models
* Front-end: Jupyter hub and Python
* Year long runs
* NVIDIA AI climate model
* dx < 10km
* DYAMOND-3 protocol
* E3SM-SCREAM
* EarthWorks (CAM-MPAS)
* 1 timestep of 2D output for SCREAM (3.5 km, 25 million columns) = 10 GB
* Most on equal-area, unstructured grids
* Organize the data better tg=han file paths
  * Intake
* Zarr file format
* re-gridded to hierarchical format (HEALPix)
  * what scale do you actually need
  * Do you need to convert to lat-lon?
  * 12 cells for zoom level 0
  * zoom level 10 ~6k , 12.5 M columns
  * Going higher than zoom level 7 for display on screen may not make sense
* Zarr works with xarray
  * stores data in chunks
  * knows where to get the data you want (in space and time)
* loading data through catalogs
  * select parameters you want
* GitHub issue for discussions
* Can make pull requests to contribute analysis code
