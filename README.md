# Medical Image Segmentation

Segmentation is the process of dividing an image into regions with similar properties such as gray level, color, texture, brightness, and contrast. Segmentation divides or partitions the image into various parts called segments. Since it’s not a great idea to process the entire image at the same time as there will be regions in the image which do not contain any information, by dividing the image into segments, we can make use of the important segments for processing the image. For our project, we have currently used and further planned to use the results of segmentation for the following:
* Identify Region of Interest i.e. locate tumour, lesion and other abnormalities
* Measure tissue volume to measure growth of tumour (also decrease in size of tumour with treatment)
* Help in treatment planning prior to radiation therapy; in radiation dose calculation
* Predict the spread of the tumour

## K - Means
K-means is one of the simplest and conventional method in cluster analysis which can be applied for segmentation purpose. This algorithm divides the given dataset into two or more clusters, where clusters are basically group of data points which are similar to each other, having similar properties. A distance metric is used for segregating the dataset, so in the context of lung cancer images the pixels will be assigned to an individual cluster based on the chosen distance metric. Euclidean distance is the general measure used as the distance metric in K-means.

## K - Median
K-median is also a clustering algorithm but it is slightly modified from the k-means algorithm. It is a variation of the k-means algorithm in which for centroid calculation instead of calculating the mean value like we do in k-means, we consider the median value. The basic steps followed in k-median clustering are as follows:

## Unseeded region growing algorithm
The seeded region growing (SRG) algorithm is one of the simplest region-based segmentation methods. It performs a segmentation of an image with examine the neighbouring pixels of a set of points, known as seed points, and determine whether the pixels could be classified to the cluster of seed point or not. The unseeded region growing (URG) algorithm is a derivative of seeded region. Their distinction is that no explicit seed selection is necessary. In the segmentation procedure, the seeds could be generated automatically. So this method can perform fully automatic segmentation with the added benefit of robustness from being a region-based segmentation.

## Watershed algorithm
The primary goal of the watershed segmentation algorithm is to find the “Watershed lines” in an image in order to separate the distinct regions. To imagine the pixel values of an image is a 3D topographic chart, where x and y denote the coordinate of plane, and z denotes the pixel value. The algorithm starts to pour water in the topographic chart from the lowest basin to the highest peak. In the process, we may detect some peaks disjoined the catchment basins, called as “dam”.

## Segmentation by thresholding
Thresholding simply involves the comparison of each pixel value of the image i.e. pixel intensity to some specified threshold. Based on this comparison the image is divided into two segments where one segment contains the pixels having intensity value lower than or equal to the specified threshold and the other segment contains the pixels having intensity value greater than or equal to the specified threshold.
