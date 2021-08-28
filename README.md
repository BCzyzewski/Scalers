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

#### Standard Scaler

The most popular method of scaling implemented in scikit-learn. It assumes that the data is normally distributied within each feature. Standarization comes by <b>subtracting the mean </b> and then <b>dividing by standard diviation </b> of every feature in a datset.

This results in a dataset where every featre has a mean of 0 and standard deviation/variance of 1. About 68% of the values will lie between -1 and 1.

#### MinMax Scaler

This scaler transforms the data to a given range. For each value in a column, MinMax <b>subtracs the minimum value</b> in the feature and then <b>divides by the range between the original maximum and original minimum.</b> Those operations preserve the shape of the original distribution.

It is important to note that MinMax works well with data that is <b>not Gaussian</b>, but it is very sensitive to outliers.

#### Robust Scaler

Robust Scaler should be used with data that <b>contains many outliers</b> as this one is "robust" to values that differ greatly from to the median. This scalers transforms the features by subtracting the median and then dividing by the interquertile range (75% value - 25% value). By doing this that way, the outliers do not influence the scaling process.

This method should be used instead of MinMax Scaler when we know that outliers are present in the data. The range of values after applying this scaler will be much greater then after using MinMax.

#### Max Abs Scaler

Each feature is scaled by its maximum absolute value. <b>Maximum value of each featureis set to 1</b>, after appying this scaler. Similar to MinMax this scaler can suffer the the data has outliers.

Using this scaler does not seft the data, and thus does not destroy any sparsity.

#### Power Transformer Scaler

Power Transformer is applied to make data more <b>"Gaussian"</b>. This is very usefull in situations when normality is requiered. The power transform finds the optimal scaling factor in stabilizing variance and minimizing skewness through maximum likelihood estimation. Currently, Sklearn implementation of PowerTransformer supports the Box-Cox transform and the Yeo-Johnson transform.





