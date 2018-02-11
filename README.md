# chart-curvature
A simple proof of concept project aiming to demonstrate practical application of price-chart data analysis.

<p align="center">
  <img width="600" alt="Sample Result"
  src="https://github.com/pinarmeltem/chart-curvature/blob/master/docs/chart-curvature.png">
</p>

## Concept
This project was started as an experiment with the focus of analysing financial price data and as an attempt to  understand the relation between the price trend as a curve and the curvature of that curve.

## Abstract
The initial question that I have asked at the beginning of my research was: _What are the benefits of representing price data as a curve?_ 

Later, it became a bit more clear that by focusing on a specific quality of the price curve has the potential to provide a greater use value. So I came up with a slightly more specific question: _What is the relation between the curvature of a price curve and the underlying price movement of a security?_

The first question is easier to answer. Representing price with curves is
nothing new.

<p align="center">
  <img width="400" height="400" alt="Example Line Chart"
  src="https://github.com/pinarmeltem/chart-curvature/blob/master/docs/line_chart.png">
</p>

Simply put, curvature is an important indicator that signals change of direction on a curve. In order to keep this article focused on the actual technical aspects that I have followed and reflect my findings as clear as possible, I will refrain from going into details when it comes to explaining the maths behind curvature calculations. However, I would like to provide a quick background on the process.

## Background
 _Curvature_ is a topic widely covered in the realm of Mathematics. There is a wikipedia page dedicated to this topic which can be accessed [here][link09]. Another good resource is the _Curvature_ section under the [_Derivatives of Multivariable Functions_][link11] collection at [khanacademy.org][link12]. There, you can find a set of video tutorials explaining the maths and formulas behind the process used in this case-study.

<p align="center">
  <img width="400" alt="Osculating Circle"
  src="https://github.com/pinarmeltem/chart-curvature/blob/master/docs/osculating_circle.svg">
</p>

The implementation of the curvature calculations used in this project are pretty much based on [this stackoverflow question][link10].

## Prerequisites
This project is compatible with [Python 2.7][link08]. In order to acquire the data that we are going to run our analysis on, we will be needing the following Poloniex API wrapper project: [s4w3d0ff/python-poloniex][link01]

In addition to these, the following Python libraries will be required to run the example code. These modules are essential for any data analysis related tasks so they are quite popular and the steps required for their installation are well documented:

* [plotly.py][link02]
* [pymongo (required by python-poloniex)][link03] 
* [NumPy][link04]
* [Pandas][link05]
* [Scikit][link06]

## Process
We start by caching some data from Poloniex. Poloniex is one of the most popular crypto-currency exchanges with a good API service. The part of our application used to pull the price data from Poloniex is called `get-data.py`. This small python script is based on one of the examples provided with the Poloniex API wrapper project mentioned above.

Once we have generated the required data, we should be able to plot the results and evaluate our findings. In the next section, I will be going through each stage in a more detailed fashion.

### Source Data
By default, the sample data used in this example is the chart data for the BTC/STRAT (Bitcoin/Stratis) pair on Poloniex. More details on how price data is pulled and stored from the exchange is available [here][link07].

Please run the following script to generate our raw data.

```
./get-data.py
```

If everything goes well and you have completed the required steps, running the command above should generate a CSV file named `data.csv` and store this inside project's `data` folder. You can skip this step and simply use the pre-cached `data.csv` that is currently located inside the data folder.

### Analysing and Plotting
The second component of our application is the plotter. 

Please run the following script to plot the resulting analysis.

```
./plot-data.py
```

Running the above command should plot the results of our research. The result should look like the image provided at the top of this page.

## Conclusion

[link01]: <https://github.com/s4w3d0ff/python-poloniex>
[link02]: <https://plot.ly/d3-js-for-python-and-pandas-charts>
[link03]: <https://api.mongodb.com/python/current>
[link04]: <http://www.numpy.org>
[link05]: <https://pandas.pydata.org>
[link06]: <http://scikit-learn.org/stable>
[link07]: <https://github.com/s4w3d0ff/python-poloniex>
[link08]: <https://www.python.org/download/releases/2.7/>
[link09]: <https://en.wikipedia.org/wiki/Curvature>
[link10]: <https://stackoverflow.com/questions/28269379/curve-curvature-in-numpy>
[link11]: <https://www.khanacademy.org/math/multivariable-calculus/multivariable-derivatives#curvature>
[link12]: <https://www.khanacademy.org>
