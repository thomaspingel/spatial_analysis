# programming_in_gis

These notebooks with require an installation of [ArcGIS Pro](https://apps.itpals.vt.edu/arcgis/ArcGIS_Pro_Installation_Instructions.pdf) and Anaconda with a class environment.

#### Anaconda installation instructions
* [Download and install the software](https://www.anaconda.com/products/individual).  It's free, and can install on Windows, Linux, and Mac.
* The default installation of Anaconda comes with numpy, Pandas, matplotlib, and many other useful packages.  However, it does not come with many geospatial packages.  
* Install instructions after opening an Anaconda command window (paste these three lines in, one-at-a-time).
~~~
conda create --name gis --file https://nearearthimaginglab.org/python/neil.20220730.txt
conda activate gis
pip install opencv-python 
# pip install pypdf2==2 pyppeteer==0.2.2  (deprecated?)
pip install nbconvert[webpdf]
# To convert your first notebook using webpdf, you'll need to run on the python/gis environment commandline:
# jupyter nbconvert --to webpdf --allow-chromium-download path/to/any_notebook.ipynb
# After this, you can do it in the browser as normal.
~~~
From here, you should be able to close the window, and use normally except that: when you open the Anaconda command window, in addition to changing directory to your working directory you'll need to type
~~~
conda activate gis
~~~ 
# Manual Install (for mac?)
~~~
conda create --name gis -c conda-forge python=3.10 spyder jupyter jupyterlab numpy pandas matplotlib
conda activate gis
pip install nbconvert[webpdf]
# To convert your first notebook using webpdf, you'll need to run on the python/gis environment commandline:
# jupyter nbconvert --to webpdf --allow-chromium-download path/to/any_notebook.ipynb
# After this, you can do it in the browser as normal.
~~~

# Exporting to PDF
* To install the package needed for conversion:
~~~
pip install nbconvert[webpdf]
~~~
* To create the PDF from the commandline.  Useful for first conversion as it will downloaded the needed Chromium component.
~~~
jupyter nbconvert --to webpdf --allow-chromium-download "01. Variables and If-Else.ipynb"
~~~
* But then these can be created in Notebooks directly
~~~
!jupyter nbconvert --to webpdf "01. Variables and If-Else.ipynb"
~~~
