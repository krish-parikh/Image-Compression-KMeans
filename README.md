# Image Compression with KMeans
This Python script compresses an image by reducing the number of unique colors used in the image, using KMeans clustering.

## What the Script Does
Given an image and the maximum number of clusters to test, the script performs the following steps:

1. For each number of clusters from 1 to the maximum, it applies the KMeans clustering algorithm to the colors in the image.
2. It maps each color in the image to the centroid of its nearest cluster.
3. It calculates the cost (the sum of squared distances from each color to its cluster centroid) and the compression ratio.
4. It displays the compressed image and prints the number of unique colors and the compression ratio.
5. It plots the cost and the compression ratio against the number of clusters.

The cost typically decreases with the number of clusters. The point where the cost starts to decrease more slowly (the "elbow" of the curve) may be a good choice for the number of clusters, balancing image quality against storage size.

The compression ratio indicates the percentage reduction in the number of unique colors in the image. A higher compression ratio means that the image data takes less space, but it may also reduce image quality.

## How to Run the Script
1. Ensure that you have Python installed, along with the '**cv2**', '**numpy**', '**sklearn**', and '**matplotlib**' libraries.
2. Run the script with python image_compression.py.
3. When prompted, enter the path to the image file and the maximum number of clusters to test.
4. The script will display the compressed images and the graphs of cost and compression ratio against the number of clusters.
