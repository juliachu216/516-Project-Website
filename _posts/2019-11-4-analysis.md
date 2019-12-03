---
title: "Data Analysis"
bg: red
color: black
fa-icon: laptop
---

# Raw Data

You can download all Raman spectral data from this [zip file](https://github.com/juliachu216/516-Project-Analysis/blob/master/Raw%20Data.zip).

There are 26 samples, and each samples has 20 data files. In each data file, the 1st columne is the wavelength from 99 to 3000 cm^-1, and the 2nd columne is the intensity. The values of wavelength in each file are the same. Positive samples are named with '+'. 

# Pre-processing

1. Combine negative and positive data separately - Columns are wavelength value. Rows are different samples.
  
2. Smooth by moving average method - Define a smooth function
  
  Moving average is the simplest smoothing algorithm. It simply replaces each point in the signal with the average of m adjacent points, where m is a positive integer called the smooth width. You can change the smooth width in the function.
  
3. Baseline Correction by polynomial fitting method - Define a baseline correction function

  Baseline correction aims to eliminate the interference of fluorescence spectra. The traditional baseline correction algorithm based on polynomial fitting is simple and easy to implement, but its flexibility is poor due to the uncertain fitting order. In the code, degree of the polynomial is 3, which is default.


[Pre-processing python notebook in Jupyter](https://nbviewer.jupyter.org/github/juliachu216/ABE-516X-Project/blob/master/analysis/Pre-process%20data.ipynb)


### The final data frame is 520 rows × 1557 columns. The first 280 rows are negative signed as N, and the rest are positive signed as P.

# Classification
1. Principal Component Analysis - Reduce the variable to 10 components.

2. Support Vector Machine - Use GridSearchCV to find the best parameters in suport vector machine.

3. Neural Network - Create a neural network model with 9 hidden layers, and the output layer is 2 classes (binary classification, 0 or 1). When trainning the model, it iterats on the data in batches of 8 samples and 100 of epochs.


[Classification python notebook in Jupyter](https://nbviewer.jupyter.org/github/juliachu216/516-Project-Analysis/blob/master/analysis/Classification.ipynb)


