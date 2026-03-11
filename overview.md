## Overview

The Arctic Ocean is one of the regions most strongly affected by climate change; it may be ice free in summer by the middle of the century. As the region warms, erosion of surrounding coasts is accelerating, changing the composition of material released into the ocean from rivers and glaciers,  and impacting the fragile Arctic ecosystems. Understanding how freshwater and riverborne nutrients enter the Arctic Ocean and where they go is vital to predict and plan for the consequences. Nature has provided us with a tool to do this. All water ($H_{2}O$) is composed of hydrogen (H) and oxygen (O). However, there is a variety (isotope) of oxygen (referred to as $^{18}O$) that is more common in seawater and sea ice (frozen seawater) than in rivers and glaciers. By mapping the relative abundance of 18O (referred to as $\delta^{18}O$), we can see how freshwater, and the nutrients it may carry, move around and out of the Arctic.

Our measurements of this valuable tracer are unevenly and sparsely scattered over the Arctic Ocean—measuring $^{18}O$ requires physically drawing water samples in hostile, often frozen Arctic conditions. To even begin understanding the fate of freshwater in the Arctic, we must stitch these data points together to see the bigger picture. The challenge is to creatively leverage machine learning techniques to generate complete maps of $\delta^{18}O$ in the Arctic Ocean. 

The British Antarctic Survey, National Oceanography Centre, and UK Centre for Ecology and Hydrology have compiled an extensive dataset of existing $\delta^{18}O$ measurements with coincident metadata (e.g. location, date, pressure) that may be of use in reconstructing its distribution. For example, the salinity of seawater has been observed to correlate with $\delta^{18}O$. We encourage participants to use outside dates and pretrained models as they see fit. Teams should plan on specifying additional data sources and/or pretrained models when uploading results. 

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

