# chart-curvature
A simple proof of concept project that aims to demonstrate price chart data analysis.

<p align="center">
  <img width="600" alt="Sample Result"
  src="https://github.com/pinarmeltem/chart-curvature/blob/master/docs/chart-curvature.png">
  </p>

## Concept
I have started this project with the aim of experimenting with price data and
running an analysis to test a mathematical concept, in that case curvature
calculation.

## Abstract
Why Curvature is important and what does it tells us? The curvature of a spline
is an important indicator the signals change of direction on a curve. In order
to keep this article focused on the actual technical steps that I have followed
I will refrain from going into great detail when it comes to understanding the
maths behind the curvature calculations. However, I would like to provide
a quick reference.

## Background
_Images and notes about what curvature is etc._

## Prerequisites
In order to acquire the data that we are going to run our analysis on, we will
need the following Poloniex API wrapper:
[s4w3d0ff/python-poloniex][link01]

In addition to these, the following Python libraries will be required to run
the example code. These modules are essential for any data analysis tasks so
they are quite popular and the steps required for the installation are well
documented:

* [plotly.py][link02]
* [pymongo (required by python-poloniex)][link03] 
* [NumPy][link04]
* [Pandas][link05]

## Process
We first start by pulling some data from the Poloniex exchange. The part of our
application used to pull the price data from Poloniex is called `get-data.py`.
This small python script is based on one of the examples provided with the
Poloniex API wrapper project.

Once we have generated the `data.csv` we can run the `plot-data.py` component
of our application in order to plot the results. In the next section, I will be
going through the stages in a more detailed approach.

### Generating Source Data
```
./get-data.py
```

Should generate a `data.csv` file located inside project's `data` folder. You
can skip this step and simply use the pre-cached `data.csv` that is currently
available as part of the github repository.

### Source Data
The 

## Conclusion

[link01]: <https://github.com/s4w3d0ff/python-poloniex>
[link02]: <https://plot.ly/d3-js-for-python-and-pandas-charts>
[link03]: <https://api.mongodb.com/python/current>
[link04]: <http://www.numpy.org>
[link05]: <https://pandas.pydata.org>
[link04]: <>
[link06]: <>
[link07]: <>
[link08]: <>
[link09]: <>

