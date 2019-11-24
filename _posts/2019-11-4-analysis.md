---
title: "Data Analysis"
bg: '#63BD2F'
color: white
---

## Raw Data

You can download all Raman spectral data from this [zip file](https://github.com/juliachu216/ABE-516X-Project/blob/master/Raw%20Data.zip)

## Pre-processing

1. Combine negative and positive data separately - Columns are wavelength value. Rows are different samples.
  
2. Smooth by moving average method - Define a smooth function
  
3. Baseline Correction by polynomial fitting method - Define a baseline correction function


[Pre-processing python notebook in Jupyter](https://nbviewer.jupyter.org/github/juliachu216/ABE-516X-Project/blob/master/analysis/Pre-process%20data.ipynb)


The final data frame is 520 rows × 1557 columns. The first 280 rows are negative signed as N, and the rest are positive signed as P.

## Classification
1. Principal Component Analysis - Reduce the variable to 10 components.

2. Support Vector Machine - Use GridSearchCV to find the best parameters in suport vector machine.

3. Neural Network - Create a neural network model with 9 hidden layers, and the output layer is 2 classes (binary classification, 0 or 1). 


[Classification python notebook in Jupyter](https://nbviewer.jupyter.org/github/juliachu216/ABE-516X-Project/blob/master/analysis/Classification.ipynb)


