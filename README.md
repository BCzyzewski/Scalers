# Visualizing different Scalers available in Scikit-Learn and their effect on input data

### Why should you be using scalers in Machine Learning problems?

Scaling is one of the most crucial steps in Machine Learning. Most of the algorithms used in ML see highest ranging feature as more significant. Those features can dominate the whole model and influence it more than they should. So if a dataset contains a variety of features with different ranges scaling them to similar range is crucial.

Some of the algorithms like Neural Network Gradient Decent can work much faster with scaling than without it.

## What methods should you be using?

This question was an inspiration to create this project. In the visualization below which is a result of the project we can see different scaling methods visualized on the same input data.

<center>
<img src="Scaling Visualization - Result.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" /> </center>

The input data was:

<ol>
<li>Poisson distribution of 1000 samples with lambda of: 1</li>
<li>Normal distribution of 1000 sample with mean of 1.22 and standard deviation of 1</li>
</ol>

### Different methods explained

All of the methods used in visualization will be biefly explained below.

##### Standard Scaler

$xscaled=(x-y)/c$