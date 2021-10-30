# Cryptocurrencies. Project 18 of the UofT.
## `-Contents-`	
	
- [Overview of the Cryptocurrencies Analysis](#Overview-of-the-Cryptocurrencies-Analysis)	
- [Resources](#resources)	
- [The Cryptocurrencies Analysis Summary](#The-Cryptocurrencies-Analysis-Summary)
## `Overview of the Cryptocurrencies Analysis`

The purpose for the project is to prepare an analysis for the clients who are preparing to get into the cryptocurrency market. For the purpose, and as there is no known output it needs to process data, to cluster it, to reduce the dimensions, and the principal components by using unsupervised learning. Unsupervised learning doesn't have a clear outcome or target variable and it is used to find patterns.

The analysis consists of four technical analysis deliverables as the following: 

- Preprocessing the Data for PCA;
- Reducing Data Dimensions Using PCA;
- Clustering Cryptocurrencies Using K-means;
- Visualizing Cryptocurrencies Results.

## `Resources`	
The analysis was created using next software: Jupyter-notebook 6.3.0, Python 3.8.8, Pandas 1.2.4, Visual Studio Code 1.58.0, Python machine learning library scikit-learn  0.24.1 , Python visualization library hvplot 0.7.3, graphing library plotly 5.1.0.

The dataset of the analysis can be found here [Crypto_data](./crypto_data.csv).

## `The Cryptocurrencies Analysis Summary`

The result of the Cryptocurrencies Analysis can be found in the [Crypto_clustering](./crypto_clustering.ipynb) file.

Firstly the data should be properly prepared to can select features that help us find patterns.

During data processing, the focus was on making sure the data is set up for the following:
•	Null values are handled.
•	Only numerical data is used.
•	Values are scaled. In other words, data has been manipulated to ensure that the variance between the numbers won't skew results.

After data processing the Principal Component Analysis algorithm (PCA - a statistical technique to speed up machine learning algorithms when the number of input features (or dimensions) is too high) was applied and, the dimensions of the X DataFrame were reduced to three principal components.

![image](https://user-images.githubusercontent.com/68247343/139560401-ab087180-1f14-4e51-8db2-a367c87f1a6e.png)

Additionally, the data points should be grouped together in other word clustering data. To identify and solve clustering issues it was used K-means. The K-means algorithm groups the data into K clusters, where belonging to a cluster is based on some similarity or distance measure to a centroid (the arithmetic mean position of all the points on a cluster).

An easy method for determining the best number for K is the elbow curve. So the elbow curve was created and the angle at point 4 looks like an elbow on the graph below:

![image](https://user-images.githubusercontent.com/68247343/139560407-6caf8cb4-e48b-49c9-8bca-2897508a7461.png)

Finally, the clusters (results) were visualizated by using hvPlot python library. 

The 3D scatter plot can be rotated using the mouse to click and drag and panned using the scroll wheel.
There are now four distinct groups that correspond to the four clusters that is expectable.

![image](https://user-images.githubusercontent.com/68247343/139560410-38b23733-7db0-4abf-993a-44e9747b4ba0.png)

In the results, 3D plot looks like more informative than 2D but last is easier to analyze with only two features. See bolow grath:

![image](https://user-images.githubusercontent.com/68247343/139560415-d1495396-88ca-4b23-a346-47821be60ad3.png)

So, on the last plot it appears two clusters are overlapping and not quite forming the distincts groups. They look not okay because of some data points mixed in the middle a lot.
