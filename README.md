# Foreground-segmentation-using-kmeans-AND-Face-recognization-using-KNN

## Interactive Foreground Segmentation and Face Recognition
This repository contains two main ASSIGNMENTS:

- Interactive Foreground Segmentation Using K-Means Clustering
- Face Recognition Using K-Nearest Neighbors (K-NN)
Each ASSIGNMENT involves detailed data preprocessing, algorithm implementation, and result analysis. Below are the instructions and descriptions for each project.

## Assignment 1: Interactive Foreground Segmentation Using K-Means Clustering
## Objective
Implement a basic version of the interactive image cut-out/segmentation approach called Lazy Snapping. The program uses K-Means Clustering to segment images into foreground and background based on user-provided seed pixels.

## Libraries Used
time: To measure the processing time for segmentation.
PIL (Image): For opening and manipulating images.
matplotlib.pyplot (plt): To display the segmentation results.
numpy: For numerical operations.
cv2 (OpenCV): For image processing tasks like reading images, converting color spaces, and displaying images.
## Solution
- Segmentation Mask Processing:

Create three versions of the input image:
One with background pixels set to black.
One with foreground pixels set to black.
The original image.
- Lazy Snapping:

Utilize human annotations (foreground and background seed pixels) to compute a precise figure-ground segmentation.
- Optimization:

K-Means Optimization: Use Mini-batch K-Means for efficiency.
Reduce Color Space Dimensionality.
Parallelize K-Means computation for foreground and background classes.
Results and Observations
- N Values:

Increasing N results in more refined segmentation but increases computational complexity.
Lower N values provide coarse segmentation but reduce computation time.
- Comparison:

Varying N values and strokes impact segmentation consistency and robustness.
Running the Scripts

## Assignment 2: Face Recognition Using K-Nearest Neighbors (K-NN)
## Objective
Implement a K-Nearest Neighbors classifier from scratch for face recognition using the CMU Pose, Illumination, and Expression (PIE) Dataset.

## Libraries Used
- numpy: For numerical operations.
- matplotlib: For visualization.
## Tasks
- Pre-process the Dataset:

Normalize each face image vector to unit length.
Split the dataset into training and testing sets.
- Implement K-NN Classifier:

Use Euclidean and cosine similarity distance measures.
Evaluate performance for different k-values (2, 5, 7, 11).
- Apply SVM and GaussianNB:

Compare accuracy with K-NN.
Perform Dimensionality Reduction:

Visualize datasets in 3-D using PCA.
Preprocessing Steps
- Normalization:

Divide each vector by its magnitude.
- Splitting Dataset:

Randomly select 150 images for training and 20 for testing for each subject.
Results and Observations
- Accuracy Comparison:

               - SVM: Highest accuracy (~97.65%).
               - K-NN: Competitive accuracy (~96.08%).
GaussianNB: Lower accuracy (~75.69%).
- Distance Metrics:

            - Euclidean Distance: Effective for face recognition.
            - Cosine Distance: Less effective for this dataset.
