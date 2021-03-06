# CLIMATE MODELLING USING ORACLE BIG DATA APPLIANCE

### Introduction

A parameteric approach makes assumptions about the distribution of the underlying population and its parameters from which the sample was taken. A main feature for this modelling approach is that if the data deviates strongly from the assumptions, using a parameteric approach using results in improper conclusions. I have used kstest (Koglomorov-Smirnoff Goodness of fit test) in order to make a decision on the distribution chosen for modelling the data.

The demo exploits two of the most popular parametric methods on top of Oracle Big Data Appliance to model historic Rainfall Data for Nashville, TN.

* Maximum Likelihood Estimation
* Method Of Moments

### Architecture

### Prerequisites

* Oracle Big Data Appliance
* Anaconda Parcels for Cloudera Manager installed
* Plotly needs to be installed accross all cell nodes
* Cufflinks to work with Plotly and Pandas

### Interesting Results

#### Koglomorov Test Statistics

I had chosen 4 distributions (details below) but gamma distribution showed the best distance statistic and hence was chosen as the best choice to model the distribution.

KstestResult(statistic=0.77216731986892584, pvalue=0.0)

KstestResult(statistic=0.87857142857142856, pvalue=0.0)

KstestResult(statistic=0.78699163553602158, pvalue=0.0)

KstestResult(statistic=0.79827003150003439, pvalue=0.0)

#### Histogram of the rainfall data

[plotly link](https://plot.ly/~kpadmana/838/jan-feb-mar-apr-may-jun-jul-aug-sep-oct-nov-dec)
[![ScreenShot](https://rawgit.com/KartikPadmanabhan/Parametric-Estimation/master/html/climate-histogram.png)](https://rawgit.com/KartikPadmanabhan/Parametric-Estimation/master/html/climate-histogram.htm)

#### Method of Moments Based Modelling Results

[plotly link](https://plot.ly/~kpadmana/856/-line0-line1-line0-line1-line0-line1-line0-line1-line0-line1-line0-line1-line0-l)
[![ScreenShot](https://rawgit.com/KartikPadmanabhan/Parametric-Estimation/master/html/climate-mom.png)](https://rawgit.com/KartikPadmanabhan/Parametric-Estimation/master/html/climate-mom.htm)

#### Maximum Likelihood Based Modelling Results

[plotly link](https://plot.ly/~kpadmana/858/-line0-line0-line0-line0-line0-line0-line0-line0-line0-line0-line0-line0)
[![ScreenShot](https://rawgit.com/KartikPadmanabhan/Parametric-Estimation/master/html/climate-mle.png)](https://rawgit.com/KartikPadmanabhan/Parametric-Estimation/master/html/climate-mle.htm)

### Note

If you are using the plotly data for presenting the results to the audience, please download the code and the dataset from the plotly link provided. The charts shown in plotly are modified from the images that are exported from matplotlib onto plotly.
