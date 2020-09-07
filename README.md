# My Explanation

I used the k-means clustering method to determine that the dataset has 8 clusters. I figured this out by following the tutorial listed here: https://medium.com/code-to-express/k-means-clustering-for-beginners-using-python-from-scratch-f20e79c8ad00. First, my code reads in the .csv file and plots the values on a scatterplot. Then I scaled the data so the values have equal weights when clustering. I concluded 8 clusters when I implemented the elbow method. The elbow method clusters the dataset from 1 to the total amount of numbers (in this case, 150). In each cluster, the distance between each data point and its centroid (the center of gravity from cluster) is squared and added. Then, all of the sum of squared errors are added. This will produce a downward slope in a shape of an elbow. The best number of clusters is where the 'elbow' would be located. In this case, it was 8. 

## Libraries

1. import numpy as np
2. import pandas as pd
3. import matplotlib.pyplot as plt
4. import seaborn as sns
5. from sklearn.cluster import KMeans
6. from sklearn import preprocessing
