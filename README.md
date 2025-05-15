# Hackathon
## May 12 Introduction
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
  * Tell it zoom level and time interval
* Zarr works with xarray
  * stores data in chunks
  * knows where to get the data you want (in space and time)
* loading data through catalogs
  * select parameters you want
* GitHub issue for discussions
* Can make pull requests to contribute analysis code
## SCREAMv1 simulations
* dx=3.25 km
* L28 40km top
* NH SE-Dycore
* SHOC is like a simplified version of CLUBB
* No deep convection scheme
* Literature generally says weaker cloud feedbacks at higher res.
* tune TOA imbalance
* Biases in tropical convection
 * lots of popcorn convection (doesn't organize)
* Cloud feedbacks have resolution sensitivity (mainly shortwave)
* Are there shared biases in storm-resolving models
## UXarray and HEALPix
* You have a tree structure (you know parent face and child face)
* hp.ang2pix (angle to pixel)
## May 12 Presentations
* track on HEALPix grid (bryce harrop)
## Zhe Feng
* MCS frequency and total precipitation does not need to be calculated at high zoom level (6 would be okay)
## NVIDIA
* foundation model <==> GCM
* interactivity?
* autoregression (time-stepping)
 * e.g. graphcast, ACE2
## MCS Breakout
* MCSMIP examples for standard output
* Wei-Ming Tsai
* adding IMERG tracking to catalog
* Add what variables are output at what zoom levels and temporal resolutions
  * large-scale environment variables
  * Trying to extract additional info. surrounding tracks
  * def extract_mcs_var(ds_tracks, ds_enviro_vars, var_name='TCWV')
* 2D variables centering each track
* compute gradients on HEALPix grid
## May 13 Presentations
* Bulk microphysics schemes
* SCREAM. Compare to IMERG.
* Are the models still 'dreary'
Satoh:
* Large TC group
* pyNICAM
* May 14 9:40 JST Chunks in HEALPix
Julia:
* MCS hours
* Cloud ice in MCSs
* TempestExtreme for TC tracking
## May 14 Presentations
* divergence and vorticity on healpix grid
* DYAMOND organized convection paper
* radius around MCS centroid and select environment variables (healpy function)
* TempestExtremes: TC, AR, and ETC (should try)
* John Mejia power, period plots
## May 15 Presentations
* Models underestimate convective organization
* Alex Loijko energy transfer jupyter notebook
## Tips
* virtual environment
* venv, conda, docker
* git status
* look at branch prefix
* if prefix is master/upstream you are not on your local fork
* kernel supports multiple softwares
