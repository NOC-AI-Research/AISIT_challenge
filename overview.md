## Overview

We want you to produce a gridded dataset of oxygen-18 (O18) isotope abundance in the Arctic ocean using machine learning. That is the isotope of oxygen with atomic mass of 18.

### Description

#### Dataset requirements 

The grid bounds are as follows (EPSG:3995):

```
xmin:  -4,500,000
xmax:   4,500,000
ymin:  -4,500,000
ymax:   4,500,000
```

Your grid should have a 10 km resolution. 

Your grid should cover three depths (0-100m, 100-500m, >500 m).

Your gridded dataset should cover 540 months of data (January 1980 - December 2025)

The gridded dataset should be saved in a netCDF file with dimensions (540 months * 3 depth slices * 900 x * 900 y).

#### Model requirements
Your model should be a machine learning model trained on the training data. The output grids should be produced directly by your model entirely within the submitted code. We will verify that the grids you submit for assessment are created by your model code. 

### Evaluation

We will compare the O18 values in the gridded datasets your model produces with a private held-out gridded dataset of observed O18 values. We will assess the model performance based on Root Mean Square Error for these comparison points.

### Prizes

What do points make?

### About the hosts

This challenge has been created as part of the [Artificial Intelligence for Stable Isotope Tracers (AISIT)](https://www.bas.ac.uk/project/aisit) project, funded by the UK's [NERC](https://www.ukri.org/councils/nerc/) and [EPSRC](https://www.ukri.org/councils/epsrc/) research councils. AISIT is a collaboration between the British Antarctic Survey (BAS), the National Oceanography Centre (NOC) and the UK Centre for Ecology and Hydrology (UKCEH).

[BAS](https://www.bas.ac.uk/) is ...

[NOC](https://www.noc.ac.uk/) is an ocean research institution. NOC’s scientists work around the globe, uncovering links between the ocean, climate change and biodiversity loss, to help every living thing on our planet flourish.

[UKCEH](https://www.ceh.ac.uk/) is ...


### Citation

