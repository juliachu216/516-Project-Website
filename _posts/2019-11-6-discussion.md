---
title: "Discussion"
bg: turquoise
color: black
fa-icon: comments
---

# Discussion

The best accuracy of neural network is a little bit higher than that of support vector machine. But the ideal accuracy we assumed is over 85%, which is far away from the current result. We need to imporve the Raman spectral data of samples. For example, we can extend the exposure time or use 20x microscope objective when collecting samples. We can also add some nano enhancement to improve the Raman spectra. We expect to detect more peaks after adding enhancement so that negative and positive samples can be separated better.

The class provides very useful resource and technology. Module I and II introduce basic information of Python such as merging data and plotting data. The notebooks of plot 3D Raman spectra and pre-processing data are based on the knowledge of module I and II. Module III is text scraping. Module IV introduces machine learning supervised including linear regression, naive bayes classification, support vector machine, and decision trees. In this project, the classification method mainly uses support vector machine, because we purpose to split data into two groups, negative and positive. Neural network was used also to compare the accuracy. Before the classification, I used principal components analysis to reduce variables.

The analysis can be used for any other spectral data after checking inputs. If the raw data is similar to this, you can load data directly. You also need to make sure that the values of wavelength in each data file are the same. Usually, the spectral data exported from the same Raman spectroscopy device has the same wavelength. If the raw data is different, you need to combine all into one file and denoise data by functions. After getting denoised data, you can load them into classification and get the accuracy of fitted model. 
