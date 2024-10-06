# Spatial-Temporal analysis of urban environmental variables using building height features

This repository contains the code and resources for the paper "Spatial-Temporal analysis of urban environmental variables using building height features" by M. Kakooei and Y. Baleghi.

## Citation
Kakooei M, Baleghi Y. Spatial-Temporal analysis of urban environmental variables using building height features. Urban Climate. 2023 Nov 1;52:101736. https://doi.org/10.1016/j.uclim.2023.101736

## Overview
This project utilized a combination of satellite imagery to generate temporal building height data. A spatiotemporal analysis was then conducted, incorporating urban environmental variables and building height features.

## Installation
Clone this repository and install the required packages:

```bash
git clone https://github.com/Mohammadkakooei/Height_Environment.git
cd Height_Environment
pip install -r requirements.txt
```

## Simulation
This repository demonstrates how the models are trained, how the maps are generated, and how the spatiotemporal analysis is conducted. For more details on building height map generation, please refer to the [Building_Height repository](https://github.com/Mohammadkakooei/Building_Height).

Training a variety of deep models [Jupyter Notebook](https://github.com/Mohammadkakooei/Height_Environment/blob/fe337f5177fb62e79d5505bb3127511390261db5/Simulation/TrainingDeepModel.ipynb)

Five fold cross-validation is used to evaluate the trained deep models [Jupyter Notebook](https://github.com/Mohammadkakooei/Height_Environment/blob/df368d2d095f85a2ae69c5bc94d5568a2652540d/Simulation/FiveFoldCrossValidation.ipynb)

Export satellite data patches for building height estimation [Python Script](https://github.com/Mohammadkakooei/Height_Environment/blob/df368d2d095f85a2ae69c5bc94d5568a2652540d/Simulation/GeoTif_FastDownload.ipynb)

Load the trained model and predict the building height per patch and save it as GeoTif [Jupyter Notebook](https://github.com/Mohammadkakooei/Height_Environment/blob/df368d2d095f85a2ae69c5bc94d5568a2652540d/Simulation/LoadModelTifOutput.ipynb)

Generate a mosaic building height map from predicted GeoTifs [Jupyter Notebook](https://github.com/Mohammadkakooei/Height_Environment/blob/df368d2d095f85a2ae69c5bc94d5568a2652540d/Simulation/GeoTifMosaic.ipynb)

Shallow regression algorithms are applied to explore how different building height feature configurations contribute to environmental variables such as NO, SO2, and CO, as captured by the Sentinel-5 satellite. Various scenarios are compared to identify the most informative features. The following regressors are utilized in this phase: Ridge Regression (RR), Support Vector Regression with a Linear Kernel (SVRL), Multi-Layer Perceptron Neural Networks (NNs), Gradient Boosting (GB), Random Forest (RF) with 100 tree estimators, and Voting (VOT). [Jupyter Notebook](https://github.com/Mohammadkakooei/Height_Environment/blob/fe337f5177fb62e79d5505bb3127511390261db5/Simulation/Regression_Analysis.ipynb)

[GEE app showing the building height map and the relevant enviorenmental variable](https://temporary.users.earthengine.app/view/height2iran)

![image](https://github.com/user-attachments/assets/ecaa6807-1880-4c22-923d-9f2ef1915639)





