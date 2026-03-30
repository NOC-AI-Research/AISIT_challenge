## Overview

The Arctic Ocean is one of the regions most strongly affected by climate change; it may be ice free in summer by the middle of the century. As the region warms, erosion of surrounding coasts is accelerating, changing the composition of material released into the ocean from rivers and glaciers,  and impacting the fragile Arctic ecosystems. Understanding how freshwater and riverborne nutrients enter the Arctic Ocean and where they go is vital to predict and plan for the consequences. Nature has provided us with a tool to do this. All water ($H_{2}O$) is composed of hydrogen (H) and oxygen (O). However, there is a variety (isotope) of oxygen (referred to as $^{18}O$) that is more common in seawater and sea ice (frozen seawater) than in rivers and glaciers. By mapping the relative abundance of $^{18}O$ (referred to as $\delta^{18}O$), we can see how freshwater, and the nutrients it may carry, move around and out of the Arctic.

Our measurements of this valuable tracer are unevenly and sparsely scattered over the Arctic Ocean -- measuring $^{18}O$ requires physically drawing water samples in hostile, often frozen Arctic conditions. To even begin understanding the fate of freshwater in the Arctic, we must stitch these data points together to see the bigger picture. The challenge is to creatively leverage machine learning techniques to generate complete maps of $\delta^{18}O$ in the Arctic Ocean. 

The [British Antarctic Survey](https://www.bas.ac.uk/), [National Oceanography Centre](https://noc.ac.uk/), and [UK Centre for Ecology and Hydrology](https://www.ceh.ac.uk/) have compiled an extensive dataset of existing $\delta^{18}O$ measurements with coincident metadata (e.g. location, date, pressure) that may be of use in reconstructing its distribution. For example, the salinity of seawater has been observed to correlate with $\delta^{18}O$. We encourage participants to use outside data and pretrained models as they see fit. Teams should plan on specifying additional data sources and/or pretrained models when uploading results. 

### Description

We challenge you to generate a gridded dataset of $\delta^{18}O$ values from the sparse observations we have collected. We will then subsample your submitted data set at held-back grid points where we have additional observations that weren't in the supplied data. The requirements for your submitted data set are below. You can see a baseline example, using a simple linear model, in the supplied example `case_study.ipynb` Jupyter notebook.

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

Your gridded data set should cover 540 months of data (January 1980 - December 2025)

The gridded data set should be saved in a netCDF file with dimensions (540 months * 3 depth slices * 900 x * 900 y). 

#### Model requirements
Your model should be a machine learning model trained on the training data. The output grids should be produced directly by your model entirely within the submitted code. We will verify that the grids you submit for assessment are created by your model code. 

### Evaluation

We will compare the $\delta^{18}O$ values in the gridded datasets your model produces with a private held-out gridded dataset of observed $\delta^{18}O$ values. We will assess your trained model performance based on Root Mean Square Error (RMSE) for these comparison points.
You should submit your submission as a netCDF file with the dimensions above. We will subsample your gridded output at our selected observation points and use the RMSE to score your submission.

For $n$ observations points, where $y_i$ is the truth and $\hat{y_i}$ is the ML model prediction at the $i$ th observation point,

$$
RMSE =  \sqrt{\frac{1}{n} \sum_{i=1}^n(y_i - \hat{y_i})^2}
$$

### Prizes

The winners will receive a goody bag of merchandise from the hosts.

### About the hosts

This challenge has been created as part of the [Artificial Intelligence for Stable Isotope Tracers (AISIT)](https://aisit.ac.uk/) project, funded by the UK's [NERC](https://www.ukri.org/councils/nerc/) and [EPSRC](https://www.ukri.org/councils/epsrc/) research councils. AISIT is a collaboration between the British Antarctic Survey (BAS), the National Oceanography Centre (NOC) and the UK Centre for Ecology and Hydrology (UKCEH).

[BAS](https://www.bas.ac.uk/) delivers and enables world-leading interdisciplinary research in the Polar Regions. Its skilled science and support staff based in Cambridge, Antarctica and the Arctic, work together to deliver research that uses the Polar Regions to advance our understanding of Earth and our impact on it. 

[NOC](https://www.noc.ac.uk/) is an ocean research institution. NOC’s scientists work around the globe, uncovering links between the ocean, climate change and biodiversity loss, to help every living thing on our planet flourish.

[UKCEH](https://www.ceh.ac.uk/) is a leading independent research institute dedicated to understanding and transforming how we interact with the natural world. With over 600 researchers, they tackle the urgent environmental challenges of our time, such as climate change, pollution, and biodiversity loss.


### Citation
```
@online{aisit_competition,
author="AISIT team",
title="AISIT machine learning comeptition",
year="2026",
url={https://github.com/NOC-AI-Research/AISIT_challenge}
}
```
