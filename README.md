# PCR-GLOBWB

PCR-GLOBWB (PCRaster Global Water Balance) is a large-scale hydrological model intended for global to regional studies and developed at the Department of Physical Geography, Utrecht University (Netherlands). This repository holds the model scripts of PCR-GLOBWB. 

contact: Edwin H. Sutanudjaja (E.H.Sutanudjaja@uu.nl).

Please also see the file README.txt.

Main reference/paper: Sutanudjaja, E. H., van Beek, R., Wanders, N., Wada, Y., Bosmans, J. H. C., Drost, N., van der Ent, R. J., de Graaf, I. E. M., Hoch, J. M., de Jong, K., Karssenberg, D., López López, P., Peßenteiner, S., Schmitz, O., Straatsma, M. W., Vannametee, E., Wisser, D., and Bierkens, M. F. P.: PCR-GLOBWB 2: a 5 arcmin global hydrological and water resources model, Geosci. Model Dev., 11, 2429-2453, https://doi.org/10.5194/gmd-11-2429-2018, 2018.

## Input and output files (including OPeNDAP-based access)

PCR-GLOBWB input and output files for the runs made in Sutanudjaja et al. (2018, https://doi.org/10.5194/gmd-11-2429-2018) are available on https://geo.data.uu.nl/research-pcrglobwb/pcr-globwb_gmd_paper_sutanudjaja_et_al_2018/. For requesting access, please send an e-mail to E.H.Sutanudjaja@uu.nl.

The input files (and some output files) are also available on the OPeNDAP server: https://opendap.4tu.nl/thredds/catalog/data2/pcrglobwb/catalog.html. The OPeNDAP protocol (https://www.opendap.org) allow users to access PCR-GLOBWB input files from the remote server and perform PCR-GLOBWB runs **without** the need to download the input files (with total size ~250 GB for the global extent).

## How to install

Please follow the following steps required to install PCR-GLOBWB:

 1. You will need a working Python environment, we recommend to install Miniconda, particularly for Python 3. Follow their instructions given at https://docs.conda.io/en/latest/miniconda.html. The user guide and short reference on conda can be found [here](https://docs.conda.io/projects/conda/en/latest/user-guide/cheatsheet.html).

 2. Get the requirement or environment file from this repository [conda_env/pcrglobwb_py3.yml](conda_env/pcrglobwb_py3.yml) and use it to install all modules required (e.g. PCRaster, netCDF4) to run PCR-GLOBWB:

    `conda env create --name pcrglobwb_python3 -f pcrglobwb_py3.yml`

    The requirements file will create a environment named *pcrglobwb_python3*.

 3. Activate the environment in a command prompt:

    `conda activate pcrglobwb_python3`

 4. Clone or download this repository. We suggest to use the latest version of the model, which should also be in the default branch. 

    `git clone https://github.com/UU-Hydro/PCR-GLOBWB.git`

    This will clone PCR-GLOBWB into the current working directory.


## How to run

Please make sure that the correct sourenvironment in a command prompt:

`conda activate pcrglobwb_python3`

Change to the PCR-GLOBWB *model* directory.

You can start a PCR-GLOBWB run the command prompt using the following 

`python deterministic_runner.py <ini_configuration_file>`

where <ini_configuration_file> is the configuration file of PCR-GLOBWB. 

Some configuration files examples are given in the *config* directory. To be able to run using these examples, there are two things that you have to edit. 

First, please make sure that you edit or set the *outputDir* (output directory) to the directory that you have access. 


Moreover, please also make sure that the *cloneMap* file is stored locally in your computing machine. The *cloneMap* file defines the spatial resolution and extent of your study area and must be in the pcraster format. Some examples are given in the folder


, 
# - Please make sure that the file 

that will use PCR-GLOBWB input files from the 4TU.ResearchData server, as set in their *inputDir* (input directory).

`inputDir = https://opendap.4tu.nl/thredds/dodsC/data2/pcrglobwb/version_2019_11_beta/pcrglobwb2_input/'


First, 


cloneMap    = /quanta1/home/hydrowld/data/hydroworld/pcrglobwb2_input_release/version_2019_11_beta/pcrglobwb2_input/global_05min/cloneMaps/RhineMeuse05min.clone.map
#~ cloneMap = /quanta1/home/hydrowld/data/hydroworld/pcrglobwb2_input_release/version_2019

You can also open individual notebooks directly by specifying the filename, e.g. the intervention planning with:

`jupyter-notebook intervent_parameter.ipynb`


## Make your own study areas (clone and landmask areas)



## PCR-GLOBWB website is under development

Currently under development. 
We will include some exercises. 


