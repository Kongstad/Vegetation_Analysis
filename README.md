# Using multi spectral satellite imagery for vegetation health analysis via QGIS, SNAP and Python.

![Screenshot](/ext_img/fyn_1_classed.PNG)


This repository takes you through the use of multi spectral satellite data for analysis of vegetation health, the effects of a summer drought and investigates the use of machine learning in order to detect land usage and boundaries in the various spectral bands. 

You will find various jupyter notebooks and instructional text in how to accomplish this.

1) [Retrieve satellite data from Sentinel-2 - Jupyter notebook](https://github.com/Kongstad/Vegetation_Analysis/blob/main/Jupyter_Notebook/Download_S2_data.ipynb)
2) [Sentinel-2 Tools](https://github.com/Kongstad/Vegetation_Analysis/tree/main/Sentinel2_tools)
3) [Load data, visualize it and conduct analysis - Jupyter notebook](https://github.com/Kongstad/Vegetation_Analysis/blob/main/Jupyter_Notebook/imagery_analysis.ipynb)
4) [Unsupervised machinelearning - Jupyter notebook](https://github.com/Kongstad/Vegetation_Analysis/blob/main/Jupyter_Notebook/Machine_Learning_Unsupervised.ipynb)
5) [(Unfinished) Supervised machinelearning - Jupyter notebook](https://github.com/Kongstad/Vegetation_Analysis/blob/main/Jupyter_Notebook/Machine_Learning_Supervised.ipynb)

### Further explained:
1) This notebook contains scripts to log in to the Sentinel-2 database, which will download any data that fits the script parameters. Cloud cover, date, geojson input etc. Make sure to narrow your search parameters and set the download destination folder as it will begin downloading large files right away. I can recommend locating the tiles you need first through the EO browser found at [External link - www.sentinel-hub.com/eo-browser](https://apps.sentinel-hub.com/eo-browser).

2) This subpage of this repository contains a little more information on how I preprocssed the images after downloading them and on how the geojson is obtained. Furthermore a youtube video is provided on how to subset and resample the spatial resolution of the various Sentinel-2 bands so all bands can be utilized in the same spatial resolution framework.

3) This notebook loads the data in and visualizes all the bands and genereates histograms. It furthermore takes you through several of the commonly used metrics involved in establishing vegetation health. Furthermore I have included local weather information to compare the actual ground truth with what we can derive from the satellite to put it all in context. You will find a 'class' estimation example based loosely on NDVI parameters and evaluation of false colour images as well.

4) The Unsupervised machine learning notebook looks at classifying objects based on a K-means clustering model. As there are no ground truth available for classification of objects on this particular dataset, K-means ability to discern different types of vegetation, fields, cities etc. is evaluated.

5) The supervised machine learning notebook looks at the performance of machine learning models for the dataset provided classified data to train on. This notebook is not quite finished yet and will be uploaded soon.

