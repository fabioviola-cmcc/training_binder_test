# Guidelines/requirements for the creation of the notebooks
MOi manage a scientific environment for the attendees to allow them an access through a simple web link. 
No virtual machine will be needed, just a web browser. 

MOi will put in place a space to upload the notebooks produced by the Lot 1 partner or order to others entities. 
The directory of this space will be given at least 2 months before the session. 
Thanks to start the updload at least 4 weeks before the training workshop (even notebooks are not finished). 

## Requirements

1. Notebooks must tell a story that addresses a local issue (about the seas surrounding the country where the training is delivered) with the help of copernicus products.
1. Notebooks must be written to be runned in Jupyter Ecosystem. 
1. Notebooks must be written in Python3.
1. As both Python and R kernels will be available in the environment set up by MOi, notebooks written in Python3 (see REQ 3) may have their equivalent written in R and should be runnable in either RStudio or Python Notebook written in Python3 (using either "reticulate" or "rpy2"). 
1. Notebooks must call cutting-edge version of Python3 libraries/packages. 
1. Notebooks must be self-explanatory by using markdown cells/images/media to explain each code cell. 
1. Notebooks may be completed by instructions given in a separate PDF and/or PPTX documents to introduce the session (better to do it) 
1. Notebooks must give priority to the use of Python 3 libraries that hide to EndUsers the complexity of API sub-layers (= using the simplest lines of code as possible = avoiding direct call to netCDF4 library for example) 
1. Notebooks may be inspired by the following old notebook examples (=> https://atlas.mercator-ocean.fr/s/RyBG2W8iWyFktoE) but must NOT be the sole source of inspiration/insight to fulfill requirement 1 (= tell a story).
1. Use https://tiny.cc/ if you have to generate shorter URLs
1. Notebooks must apply the following tree directory: 
````
        training-<REGION> 
        |__ data/ 
        |__ img/ 
        |__ _solved/ 
        |__ docs/ 
        |                     |__ QUalityInformationDocument 
        |                     |__ ProductUserManual 
        |                     |__ TrainingGuidelines 
        |                     |__ Posters 
        |                     |__ References 
        |__ <XX>-01-ipynotebook.ipynb 
        |__ <XX>-02-ipynotebook.ipynb 
        |__ <XX>-<YY>-ipynotebook.ipynb 
````
Where: 
* ``REGION`` is the focus of the training (example: MED) 
* `data/` is a directory which must hold netCDF files covered by notebooks.
  * These files must be in file format NetCDF4. 
  * These files must be downloadable by HTTP(s) protocols (when offered thanks to MOTU, WMS, OPENDAP etc) from the CMEMS database. 
  * These files must have been downloaded by FTP protocol ONLY IF FileTransferProtocol is the ONLY download protocol offered by CMEMS database (example: at the moment, some IN SITU netCDF files). 
* ``img/`` is a directory which must hold any images used in notebook to illustrate "something" 
* ``_solved/`` is a directory which must hold .py files answering questions raised in notebook 
* ``docs/`` is a directory which must hold any useful media, helping EndUsers to answer questions or to go deeper into subject not covered by the notebook at 100% 
* ``<XX>-<YY>-ipynotebook.ipynb`` is a python notebook file: 
  * There must be as many notebook files as necessary to cover the variety of Copernicus products offered on the <REGION> where the training is held. 
  * ``<XX>`` must refer to the two digits used to reference the Production Center covered by the notebook (example: ARCTIC-MFC = 02, GLOBAL-MFC = 01, BLK-MFC = 07, INSITU-TAC = 13 etc...). A mix is possible. 
  * ``<YY>`` must refer to the two digits to increment assignments, lessons. It must reflect the order and number of notebooks.

Any question, please servicedesk.cmems@mercator-ocean.eu
