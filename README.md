# idr-notebooks

A set of Python Notebooks to demonstrate how to access the images and metadata from the Image Data Repository (IDR, https://idr.openmicroscopy.org), including features and all descriptive tags.

Full access to IDR metadata and images is provided through the standard OMERO API, documentation for which can be found [here](https://www.openmicroscopy.org/site/support/omero5.2/developers/), with the Python bindings found specifically [here](https://www.openmicroscopy.org/site/support/omero5.2/developers/Python.html). The notebooks in this repository are meant to exemplify the use of that API in the context of the IDR, and the sort of queries that can be done. In particular, they show how to reproduce Figure 1 and Figure 2 of the paper.<sup>[1](#footnote1)</sup> They also make use of the [scipy](https://www.scipy.org/) ecosystem, including [pandas](pandas.pydata.org).

## Getting started: ##

OAuth logins to Jupyter are controlled by membership in the "[idr-contrib](https://github.com/idr-contrib)" GitHub organization.
Contact idr at openmicroscopy.org to be added.
Once you've accepted the invitation, you will need to set your membership to "public".

![oauth login](/includes/login_1.png?raw=true "OAuth login")

## Basic notebooks:

- **[Getting Started](notebooks/Getting_Started.ipynb)**: How to connect, some simple data access
   ([launch](https://idr.openmicroscopy.org/jupyter/user/x/notebooks/notebooks/Getting_Started.ipynb))
- **[IDR API example script](notebooks/IDR_API_example_script.ipynb)**:
   Shows an example of using the web API to extract metadata from the IDR
   ([launch](https://idr.openmicroscopy.org/jupyter/user/x/notebooks/notebooks/IDR_API_example_script.ipynb))

## Paper-related notebooks:

- **[Figure 1 Sample of Phenotypes](notebooks/Figure_1_Sampling_of_Phenotypes.ipynb)**:
  Reproduces Fig. 1 of the paper: downloads annotations from all screens and computes and plots some statistics
  on phenotypes. Interactive visualization is done using [bokeh](bokeh.pydata.org/)
   ([launch](https://idr.openmicroscopy.org/jupyter/user/x/notebooks/notebooks/Figure_1_Sampling_of_Phenotypes.ipynb))
- **[Gene Network](notebooks/GeneNetwork.ipynb)**: Reproduces Fig. 2 of the paper: downloads annotations from 3 screens
  with a phenotype in common, queries StringDB for interactions and plots the resulting network.
  Uses a conversion table for orthologues and gene identifiers which was built offline using biomart
  (see article for more details.). It uses [bokeh](bokeh.pydata.org/) and py2cytoscape to display networks.
   ([launch](https://idr.openmicroscopy.org/jupyter/user/x/notebooks/notebooks/GeneNetwork.ipynb))

## Study-related notebooks:

- **[Rohn Phenotype Clustering](notebooks/RohnPhenotypeClustering.ipynb)**:
  Downloads annotations from IDR008, and performs some simple phenotypic clustering, building a figure
  similar to Fig. 1 of the corresponding paper. Builds a gallery of thumbnails from images of several phenotypes.
   ([launch](https://idr.openmicroscopy.org/jupyter/user/x/notebooks/notebooks/RohnPhenotypeClustering.ipynb))
- **[PCA analysis of Charm features](notebooks/PCAanalysisOfCharmFeatures.ipynb)**:
  Shows how to access the computed CHARM features using OMERO.tables
  and performs some analysis on them, showing that single cell information can be accessed from generic tile-based features
  without segmentation.
   ([launch](https://idr.openmicroscopy.org/jupyter/user/x/notebooks/notebooks/PCAanalysisOfCharmFeatures.ipynb))

----

<a name="footnote1">1</a>: Available on bioRxiv under https://doi.org/10.1101/089359
