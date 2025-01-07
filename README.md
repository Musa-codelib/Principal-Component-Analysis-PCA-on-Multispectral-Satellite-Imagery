
# Principal Component Analysis (PCA) on Multispectral Satellite Imagery

This repository contains a Python implementation of Principal Component Analysis (PCA) for dimensionality reduction on multispectral satellite imagery. The project demonstrates how to reduce the spectral dimensionality of Landsat 8 data while minimizing information loss, enabling efficient storage and analysis.  The specific area of study for this project is Topi, KPK, Pakistan.

## Table of Contents

* [Introduction](#introduction)
* [Installation](#installation)
* [Data](#data)
* [Methodology](#methodology)
* [Results](#results)
* [Contributing](#contributing)


## Introduction

Multispectral satellite imagery provides valuable information for various remote sensing applications. However, the high dimensionality of this data can pose challenges for processing and analysis. This project addresses this challenge by applying PCA to reduce the spectral dimensionality while preserving essential information content.  The implementation is built from fundamental linear algebra principles using Python and includes a comprehensive error analysis.

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/Musa-codelib/Principal-Component-Analysis-PCA-on-Multispectral-Satellite-Imagery.git
   ```

## Data

This project uses Landsat 8 Level-2 surface reflectance data for a region centered around Topi, KPK, Pakistan. You can download similar data for other regions from the USGS EarthExplorer platform ([https://earthexplorer.usgs.gov/](https://earthexplorer.usgs.gov/)).  Make sure to select the appropriate bands (B1-B7) and your desired region of interest.  Place the downloaded data files (including the MTL.txt metadata file) in the `data` directory (or specify the correct path in your script).  The expected file format is GeoTIFF.


## Methodology

The project follows these steps:

1. **Data Preprocessing:** Scaling (using gain and offset from MTL.txt), cropping to a 5000x5000 ROI, flattening, and standardizing the Landsat 8 bands.
2. **PCA Implementation:** Calculating the covariance matrix, performing eigenvalue decomposition, selecting principal components based on explained variance (using thresholds like 90%, 95%, and 98%), and projecting the data onto the principal components.
3. **Error Analysis:** Quantifying information loss using MSE, RMSE, and PSNR to assess the impact of dimensionality reduction.
4. **Visualization:** Generating grayscale images of the principal components to visualize spatial patterns.


## Results

The project demonstrates that a significant reduction in dimensionality can be achieved while preserving a high percentage of the original data's variance.  For the Topi, KPK region, two principal components captured over 95% of the variance.  The project report (if you have a detailed report, link or mention it here) provides detailed results and discussion, including visualized principal components and reconstruction error metrics.


## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
