# Make-Effective-Data-Visualization
Udacity Data Analyst(Advanced) Nanodegree Project 4

[Final Visulization](http://bl.ocks.org/yuanfresa/2f0b44d6ce963fa65b9fc3386852cf3d)

# Data Introduction

The dataset is from mass cytometry which contain immune system signatures of thousands of cells.

Each data point is consist of its 32 markers' expression and its belonged cluster.

# Summary

Instead of visualise every data point, I use the heatmap to visualize the statistical info, the mean and variance of different markers for different clusters.

# Design

The reason why I chose the heatmap is  that it is simple and direct to present high dimensional data. 

For the first version of heatmap,  each row is a cluster and each column is a marker, and I only use the color to show the mean value of  marker for the cluster. Meanwhile, the detail value can be viewed by hovering the mouse over the demand cell.

![version1](https://ws1.sinaimg.cn/large/006tKfTcgy1fs3bg9k15cj30p60eydh7.jpg)

After I received the feedbacks. I made the following changes.

1) I use the size of each cell to visualize the variance.

The variance of the expressions of a marker within a cluster is related with homogeneity, the higher variance means for same cluster their specific expression have large differences among samples. So here I use the smaller size to represent high variance. Visually, small size is less important.

By doing so, the boundaries unclear and variance missing visualization are solved. Moreover, it can somewhat explain why both mean and variant values are needed to visualize.

![](https://ws1.sinaimg.cn/large/006tKfTcgy1fs3bp0pu5vj30oy0eogn8.jpg)

2) I add one highlight function.

By clicking on specific cluster or marker, the whole row or column cells are highlighted, which can be easier to compare among the cells.

![highlight1](https://ws1.sinaimg.cn/large/006tKfTcgy1fs3bpm0fubj30oz0f5q4n.jpg)

![highlight2](https://ws3.sinaimg.cn/large/006tKfTcgy1fs3bq9rspgj30ow0fdq4n.jpg)

For the final version, I can say that this visualization can be used to find outthe homological relationship within clusters and  which markers have greater influence to differentiate clusters by exploring using the hover or highlight functions. 

#Feedback

### Feedback1

The figure is clear and good looking but it's not clear to me why you only display mean in color and have both mean and variance in detail information.

### Feedback 2

It's not clear to see the boundaries among the cells. And I don't understand what is the point to display mean and variance.

### Feedback 3

It's hard for me to find the boundaries among the cells of similar color. But the general image looks nice and the hover function works well. I noticed that for some markers, it has very low value for most clusters, does it say anything?

## Resources

Fernandez N F, Gundersen G W, Rahman A, et al. Clustergrammer, a web-based heatmap visualization and analysis tool for high-dimensional biological data[J]. Scientific data, 2017, 4: 170151.

