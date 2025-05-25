# Asymmetrics
Python Script using Open3D to calculate an asymmetry map for the human torso and parametric evaluations

As package manager Anaconda was used and the code was implemented in a Jupyter Notebook using VisualStudioCode
as CodeEditor. The script is based on Python 3.9 utilizing Open3d and the following libraries:

import open3d as o3d
import numpy as np
import matplotlib.pyplot as plt
import copy
import math
import os
import sys
import array

The implementation uses a human torso 3D (360deg) scan as input (.PLY) resulting from any scanning source (3D sensor,
fotogrammetric, 3D scanner, smart phone app) and calculates an asymmetry map between left and right torso side together
with a visualization of areas (red) showing larger asymmetries (>9mm).

The script calculates several surface topography parameters for predicting the risk of having a Scoliosis and finally
predicts the maximum spine curve angle (Cobb angle). As output the script delivers all asymmetry values in each data
point of the torso, 4 parameters describing the affinity towards Scoliosis and an ROI matrix at the torso backside
(5 * 5 data points) with calculated mean asymmetry distances in each matrix square. The matrix values can be used
as input for a convolutional neural network together with a predictor variable in oder to classify or predict an
outcome variable.
