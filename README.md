# Project: Image Analysis and Clustering

## Overview

Welcome to an exciting project where we bring images to life through data analysis and clustering! In this journey, we’ll take a vibrant image of a rainbow, transform it into a dataset full of colorful pixel information, and explore the beauty of data by grouping these pixels into clusters. Whether it’s using scikit-learn’s trusty KMeans or diving into custom clustering magic with PyTorch, each task is a step deeper into the art and science of image processing. Let’s paint a picture with pixels, break it down into data, and watch the patterns unfold!

## Tasks

### Task 1: Creating the Dataset

**Objective**: Extract valuable data from the `rainbow` image. We will transform each pixel into a row of data containing its (x, y) coordinates and RGB color values, creating a comprehensive dataset ready for analysis and visualization.

**Steps**:
1. **Load the Image**: Use the `PIL` (Pillow) library to open and read the image file.
2. **Convert to a NumPy Array**: Transform the image into a NumPy array for easy access to pixel data.
3. **Extract Coordinates and RGB Values**: Create arrays for x and y coordinates and extract the RGB values for each pixel.
4. **Create a Pandas DataFrame**: Combine the (x, y) coordinates and RGB values into a structured DataFrame.
5. **Inspect the DataFrame**: Print the first ten rows to ensure successful data extraction.

### Task 2: Visualizing and Cleaning the Image Data

**Objective**: Visualize the `rainbow1.jpg` image and address any noise it may contain. The goal is to identify noise and use the dataset to remove or reduce it for a cleaner representation.

**Steps**:
1. **Visualize the Original Image**: Use `matplotlib` to display the image and observe any visible noise.
2. **Analyze Noise**: Look for patterns or outliers in the pixel data that indicate noise.
3. **Filter the Dataset**: Use conditions to filter out unwanted noise based on RGB values.
4. **Reconstruct and Display the Cleaned Image**: Reconstruct the image using the filtered DataFrame and visualize it to confirm noise reduction.

### Task 3: Clustering with Scikit-Learn

**Objective**: Apply the KMeans clustering algorithm from the `scikit-learn` library to group the pixels of the cleaned rainbow image into distinct clusters. This task will help us understand the underlying color patterns in the image.

**Steps**:
1. **Prepare the Data**: Select the relevant features (x, y, R, G, B) from the cleaned DataFrame.
2. **Apply KMeans**: Use `scikit-learn`'s `KMeans` to fit the data and group the pixels into nine clusters.
3. **Visualize the Clustered Image**: Reconstruct the image using the cluster assignments to visualize the segmented colors.

### Task 4: Custom Clustering with PyTorch

**Objective**: Implement a custom KMeans clustering algorithm from scratch using `PyTorch`. This will provide a deeper understanding of how clustering algorithms work under the hood.

**Steps**:
1. **Convert Data to Tensors**: Transform the data into PyTorch tensors for GPU-accelerated computation.
2. **Initialize Centroids**: Randomly select initial cluster centers from the data.
3. **Assign Clusters**: Assign each data point to the nearest centroid.
4. **Update Centroids**: Recalculate the centroids based on the mean of the data points in each cluster.
5. **Visualize the Result**: Reconstruct the image with the custom cluster assignments and display the result.

### Task 5: Comparative Analysis

**Objective**: Compare the results of the `scikit-learn` KMeans and the custom `PyTorch` implementation to evaluate their performance and differences.

**Analysis**:
- **Performance**: Compare the execution time and efficiency of both methods.
- **Segmentation Quality**: Visually inspect the segmented images to assess the quality of the clustering.
- **Implementation Differences**: Discuss the differences in implementation, such as floating-point precision and convergence criteria, and how they affect the results.

## Methodology

- **Data Extraction**: `PIL`, `NumPy`, `Pandas`
- **Data Cleaning**: Filtering based on RGB values
- **Clustering**: `scikit-learn KMeans`, custom `PyTorch` implementation
- **Visualization**: `matplotlib`
