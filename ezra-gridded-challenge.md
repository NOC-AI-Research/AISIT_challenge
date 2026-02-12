## Challenge
We want you to produce a gridded dataset of O18 isotope abundance in the Arctic ocean using machine learning. 

### Dataset requirements 

The grid bounds are as follows (EPSG:3995):

xmin:  -4,500,000
xmax:   4,500,000
ymin:  -4,500,000
ymax:   4,500,000

Your grid should have a 10 km resolution. 

Your grid should cover three depths (0-100m, 100-500m, >500 m).

Your gridded dataset should cover 540 months of data (January 1980 - December 2025)

The gridded dataset should be saved in a netCDF file with dimensions (540 months * 3 depth slices * 900 x * 900 y).

### Model requirements
Your model should be a machine learning model trained on the training data. The output grids should be produced directly by your model entirely within the submitted code. We will verify that the grids you submit for assessment are created by your model code. 

### Assessment

We will compare the O18 values in the gridded datasets your model produces with a private held-out gridded dataset of observed O18 values. We will assess the model performance based on Root Mean Square Error for these comparison points.

### Relevant studies

* [Global gridded data set of the oxygen isotopic composition in seawater](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2006gl026011) [AGU Oceans 2006]  - (360 x * 180 y * 33 depths). Authors used salinity and O18 data from [Schmidt et al. 1999](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2006gl026011#grl21439-bib-0016) to produced a single 3D dataset based on the average of 50 years of data.

* [A Dynamical Reconstruction of the Global Monthly Mean Oxygen Isotopic Composition of Seawater](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2006gl026011) - (360 x , 180 y, 15 depth, 12 months). 

### Notes for WP3 discussion 
* The expected dimensions of the gridded dataset (540 months * 3 depth slices * 900 x * 900 y) should be adjusted based on reasonable expectations.

* I think for this challenge to work we'd need to convert Charles' database into an equivalent (540 * 3 * 900 * 900) gridded training dataset which would require a bit of work, for example averaging depths/months and projecting points onto a grid. I don't know whether we could make this compatible with croissant format. (JC: I don't think netCDF (or any other common gridded data format) is within the realms of croissant)

* Here we would be evaluating the resulting grids they produce rather than the model directly. I think this just makes life easier.

* I think we'd also want to give them access to other gridded products - for example ERA5 temperaure/precipitation/atmospheric pressure data, or Arctic Ocean Reanalysis temperature/salinity. One question is whether we have to specify exactly what training data participants can use, or whether any gridded data participants can get their hands on is fair game. This could cause problems if they were to use an existing O18 gridded product to train their model. 

* This is similar to what Archie Cable has been working on. So Archie's input would be very helpful in drafting this type of challenge. 



