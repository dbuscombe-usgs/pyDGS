### About

![alt tag](http://dbuscombe-usgs.github.io/figs/2013-02-24-dgs/nicegrains1.jpg)

pyDGS - a Python framework for wavelet-based digital grain size analysis

pyDGS is an open-source project dedicated to provide a Python framework to compute estimates of grain size distribution  using the continuous wavelet transform method of Buscombe (2013) from an image of sediment where grains are clearly resolved. DOES NOT REQUIRE CALIBRATION

This program implements the algorithm of:

Buscombe, D. (2013) Transferable Wavelet Method for Grain-Size Distribution from Images of Sediment Surfaces and Thin Sections, and Other Natural Granular Patterns. Sedimentology 60, 1709-1732

http://dbuscombe-usgs.github.io/docs/Buscombe2013_Sedimentology_sed12049.pdf

### install:
    python setup.py install
    sudo python setup.py install
    pip install pyDGS
    
### test:
    python -c "import DGS; DGS.test.dotest()"

### processing example:
    python
    import DGS
    density = 10 # process every 10 lines
    res = 0.01 # mm/pixel
    doplot = 0 # don't make plots
    image_folder = '/home/sed_images'
    DGS.dgs(image_folder,density,doplot,res)

 REQUIRED INPUTS:
 folder e.g. '/home/my_sediment_images'
 if 'pwd', then the present directory is analysed

 OPTIONAL INPUTS [default values]
 density = process every density lines of image [10]
 doplot = 0=no, 1=yes [0]
 resolution = spatial resolution of image in mm/pixel [1]

Note that the larger the density parameter, the longer the execution time. 

### license:
    GNU Lesser General Public License, Version 3
    (http://www.gnu.org/copyleft/lesser.html)
    
    This software is in the public domain because it contains materials that
    originally came from the United States Geological Survey, an agency of the
    United States Department of Interior. For more information, 
    see the official USGS copyright policy at
    http://www.usgs.gov/visual-id/credit_usgs.html#copyright
    Any use of trade, product, or firm names is for descriptive purposes only 
    and does not imply endorsement by the U.S. government.
    
### Note for Windows Users

I recommend the Anaconda python distribution for Windows which includes all of the library dependencies required to run this program. Anaconda comes with a variety of IDEs and is pretty easy to use. To run the test images, launch the Anaconda command terminal and type:

```
pip install pyDGS
python -c "import DGS; DGS.test.dotest()"
```

### Contributing & Credits

This program implements the algorithm of 
Buscombe, D. (2013) Transferable Wavelet Method for Grain-Size Distribution from Images of Sediment Surfaces and Thin Sections, and Other Natural Granular Patterns, Sedimentology 60, 1709 - 1732

 Author:  Daniel Buscombe
           Grand Canyon Monitoring and Research Center
           United States Geological Survey
           Flagstaff, AZ 86001
           dbuscombe@usgs.gov
 First Revision January 18 2013

For more information visit https://github.com/dbuscombe-usgs/pyDGS

Please contact:
dbuscombe@usgs.gov

to report bugs and discuss the code, algorithm, collaborations

For the latest code version please visit:
https://github.com/dbuscombe-usgs

See also the project blog: 
http://dbuscombe-usgs.github.com/

Please download, try, report bugs, fork, modify, evaluate, discuss. Thanks for stopping by!
