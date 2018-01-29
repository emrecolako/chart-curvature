# chart-curvature
A simple proof of concept project that aims to demonstrate price chart data analysis.

<p align="center">
  <img width="600" alt="Sample Result"
  src="https://github.com/pinarmeltem/chart-curvature/blob/master/docs/chart-curvature.png">
</p>

## Concept
I have started this project as an experiment focusing on financial price data and with the aim of understanding the relation between the price trend as a curve and the curvature of that curve.

## Abstract
This was the question that I have asked at the beginning of my research: _Why curvature is important and what does it tell us about the trend of a financial asset?_ 

Simply put, curvature is an important indicator that signals change of direction on a curve. In order to keep this article focused on the actual technical stages that I have followed and reflect my findings as clear as possible, I will refrain from going into details when it comes to explaining the actual maths behind the curvature calculations. However, I would like to provide a quick reference.

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
We first start with caching some data from the Poloniex exchange. The part of our
application used to pull the price data from Poloniex is called `get-data.py`.
This small python script is based on one of the examples provided with the
Poloniex API wrapper project.

Once we have generated the `data.csv` we can run the `plot-data.py` component
of our application in order to plot the results. In the next section, I will be
going through the stages in a more detailed approach.

### Source Data
By default, the sample data used in this example is the BTC/STRAT (Bitcoin/Stratis) pair on Poloniex. More details on how price data is pulled from the exchange and stored for processing is available at [s4w3d0ff/python-poloniex][link01].

```
./get-data.py
```

If everything goes well and you have completed the required stages, running the command above should generate a CSV file named `data.csv` and store this inside project's `data` folder. You can skip this step and simply use the pre-cached `data.csv` that is currently located inside the data folder.

### Analysing and Plotting
The second component of our application is the plotter. 

```
./plot-data.py
```

Running the above command should plot the results of our research. The result
should look like the image provided above.

## Conclusion

[link01]: <https://github.com/s4w3d0ff/python-poloniex>
[link02]: <https://plot.ly/d3-js-for-python-and-pandas-charts>
[link03]: <https://api.mongodb.com/python/current>
[link04]: <http://www.numpy.org>
[link05]: <https://pandas.pydata.org>
