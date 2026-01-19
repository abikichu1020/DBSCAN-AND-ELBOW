# DBSCAN Clustering Using Elbow (k-Distance) Method

## Overview
This project demonstrates **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** and the use of the **Elbow (k-distance) method** to determine the optimal value of `eps`.

Unlike K-Means, DBSCAN **does not require you to predefine the number of clusters**, but it *does* require sensible density parameters. Choosing them blindly will break the algorithm—this project avoids that mistake.

---

## What This Project Does
- Loads and preprocesses a dataset
- Computes k-nearest-neighbor distances
- Plots the **k-distance graph**
- Uses the **elbow point** to estimate the optimal `eps`
- Applies DBSCAN clustering
- Identifies clusters and noise points

---

## Why Elbow Method for DBSCAN?
DBSCAN depends mainly on:
- `eps` → neighborhood radius
- `min_samples` → minimum points to form a dense region

The **k-distance elbow method** works by:
1. Calculating the distance to the k-th nearest neighbor
2. Sorting these distances
3. Plotting them
4. Finding the sharp bend (elbow)

That elbow approximates a **good eps value**.  
No elbow → DBSCAN is probably the wrong choice for your data.

---

## Tech Stack
- Python
- NumPy
- Pandas
- Matplotlib / Seaborn
- Scikit-learn
