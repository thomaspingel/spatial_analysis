These notebooks with require an installation of [ArcGIS Pro](https://apps.itpals.vt.edu/arcgis/ArcGIS_Pro_Installation_Instructions.pdf) and Anaconda with a class environment.

#### Anaconda installation instructions
* [Download and install the software](https://www.anaconda.com/products/individual).  It's free, and can install on Windows, Linux, and Mac.
* The default installation of Anaconda comes with numpy, Pandas, matplotlib, and many other useful packages.  However, it does not come with many geospatial packages.  
* Install instructions after opening an Anaconda command window:
~~~
conda create --name gis conda-forge python=3.11 spyder jupyter scipy seaborn geopandas scikit-image rasterio statsmodels openpyxl
~~~

From here, you should be able to close the window, and use normally except that: when you open the Anaconda command window, in addition to changing directory to your working directory you'll need to type
~~~
conda activate gis
~~~ 

#### Shortcut installation
It's generally good to see how environments get created from scratch (as above).  But you can also run (only for Windows!):
~~~
conda create --name gis --file https://nearearthimaginglab.org/python/gis.20260126.txt
conda activate gis
~~~
