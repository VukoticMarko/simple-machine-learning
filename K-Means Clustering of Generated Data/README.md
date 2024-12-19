# KMeans Clustering with Synthetic Dataset

## Overview

This project generates a synthetic dataset of points belonging to three distinct clusters (zones) and performs KMeans clustering on this dataset. The dataset consists of points generated from multivariate normal distributions with different means. It uses `KMeans` clustering from `sklearn` to identify clusters in the data and visualize the results.

## Key Features
- **Synthetic Data Generation**: The dataset is created by generating points from three distinct clusters, each represented by a random mean and a diagonal covariance matrix.
- **KMeans Clustering**: The `KMeans` algorithm is applied to the generated data to group the points into clusters and identify their centroids.
- **Data Persistence**: If the dataset already exists, it is loaded from a CSV file to avoid re-generating the data.
- **Visualization**: The data points and cluster centroids are visualized using `matplotlib` for better understanding.

## Requirements

Ensure you have the following Python libraries installed:

- `numpy`: For numerical operations and data generation.
- `pandas`: For handling and saving data in a DataFrame format.
- `matplotlib`: For visualizing the data and clusters.
- `scikit-learn`: For applying the KMeans clustering algorithm.

## How It Works

1. **Data Generation**:
   - Three clusters (zones) are created by sampling points from three different multivariate normal distributions. Each cluster has its own random mean and covariance matrix.
   - The points for each cluster are generated independently, and the `x` and `y` coordinates are combined into a dataset.

2. **Saving and Loading Data**:
   - The dataset is saved to a CSV file named `dataset.csv` inside the `datasets` folder. If the dataset already exists, it will be loaded to avoid regeneration.
   
3. **KMeans Clustering**:
   - The KMeans algorithm from `scikit-learn` is used to fit the data and identify three clusters. It also calculates the centroids of these clusters.
   
4. **Visualization**:
   - A scatter plot is generated to visualize the data points, color-coded by their assigned cluster.
   - The centroids of the clusters are displayed as red "X" markers on the plot.
   
## Data Structure

The generated dataset has the following columns:

- **x**: The `x` coordinate of each data point.
- **y**: The `y` coordinate of each data point.
- **label**: The label indicating the zone/cluster the point belongs to (e.g., "Zone 1", "Zone 2", "Zone 3").

## Usage

1. **Run the Script**:
   - The script will first check if the `datasets` folder and `dataset.csv` file already exist.
   - If the file exists, it will load the data from it and perform clustering.
   - If the file does not exist, the script will generate new data, save it to `dataset.csv`, and then apply KMeans clustering.

2. **View the Results**:
   - After the script runs, a plot will be displayed showing the clusters and their centroids.
   - The console will print the centroids of the clusters and the means used to generate the data.

### Sample Output:
Dataset saved at: datasets/dataset.csv [[123.45 67.89] [135.67 78.90] [145.23 67.12]] [50, 50] [30, 45] [75, 75]

## Notes
- If you want to regenerate the data with new random means, simply delete the `dataset.csv` file in the `datasets` folder.
- The dataset is synthetic and may not represent real-world data; it is meant for demonstration and learning purposes.
