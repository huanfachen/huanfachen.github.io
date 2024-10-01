---
title: 'Example of clustering on latitude and longitude'
date: 2024-05-30
permalink: /posts/2024/05/Clustering_latitude_and_longitude/
tags:
  - Clustering
  - GIS
  - KMeans
  - NA
---

Updates 2025/05/30

This note is a list of DOs and DON'Ts for conducting (spatial) clustering analysis. The examples are reproductions of student submissions.

# DON'Ts

## Clustering on longitude and latitude of points (without using other features & no justification)

![image-20240530111903273](https://github.com/huanfachen/huanfachen.github.io/raw/master/images/clustering_long_lat.png)

What it is: This is the k-means clustering of crime incidents based on longitude and latitude, which leads to the selection of 10 boroughs for further analysis.

Comments: The student justify using these 10 boroughs by clustering latitude and longitude coordinates, which is obviously going to cluster neighbouring boroughs and is not valid evidence for high-crime regions. If the objective is to identify high-crime boroughs, using the crime density (number of crimes per square km or per 1000 residents) would be more appropriate than clustering.
