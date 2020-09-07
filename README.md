# ACM Research Coding Challenge (Fall 2020)

## No Collaboration Policy

**You may not collaborate with anyone on this challenge.** You _are_ allowed to use Internet documentation. If you _do_ use existing code (either from Github, Stack Overflow, or other sources), **please cite your sources in the README**.

## Submission Procedure

Please follow the below instructions on how to submit your answers.

1. Create a **public** fork of this repo and name it `ACM-Research-Coding-Challenge`. To fork this repo, click the button on the top right and click the "Fork" button.
2. Clone the fork of the repo to your computer using . `git clone [the URL of your clone]`. You may need to install Git for this (Google it).
3. Complete the Challenge based on the instructions below.
4. Email the link of your repo to research@acmutd.co with the same email you used to submit your application. Be sure to include your name in the email.

## Question One

![Image of Cluster Plot](ClusterPlot.png)
<br/>
Given the following dataset in `ClusterPlot.csv`, determine the number of clusters by using any clustering algorithm. **You're allowed to use any Python library you want to implement this**, just document which ones you used in this README file. Try to complete this as soon as possible.

Regardless if you can or cannot answer the question, provide a short explanation of how you got your solution or how you think it can be solved in your README.md file.


# My Explanation

I used the k-means clustering method to determine that the dataset has 8 clusters. I figured this out by following the tutorial listed here: https://medium.com/code-to-express/k-means-clustering-for-beginners-using-python-from-scratch-f20e79c8ad00. First, my code reads in the .csv file and plots the values on a scatterplot. Then I scaled the data so the values have equal weights when clustering. I concluded 8 clusters when I implemented the elbow method. The elbow method clusters the dataset from 1 to the total amount of numbers (in this case, 150). In each cluster, the distance between each data point and its centroid (the center of gravity from cluster) is squared and added. Then, all of the sum of squared errors are added. This will produce a downward slope in a shape of an elbow. The best number of clusters is where the 'elbow' would be located. In this case, it was 8. 

## Libraries

1. import numpy as np
2. import pandas as pd
3. import matplotlib.pyplot as plt
4. import seaborn as sns
5. from sklearn.cluster import KMeans
6. from sklearn import preprocessing
