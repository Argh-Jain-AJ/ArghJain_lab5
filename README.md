# ArghJain_lab5
Aim

The aim of this project is to detect human faces in an image using Haar Cascade Classifier and classify the detected faces into clusters using KMeans clustering based on HSV color features.

Methodology

The project is implemented in the following stages:

 Face Detection
- Used OpenCV Haar Cascade (`haarcascade_frontalface_default.xml`)
- Converted input image to grayscale
- Applied `detectMultiScale()` to identify face regions
- Drew bounding boxes around detected faces

Feature Extraction
- Converted detected face regions from BGR to HSV color space
- Extracted:
  - Mean Hue
  - Mean Saturation
- Created feature vectors for clustering

 KMeans Clustering
- Applied KMeans algorithm (k = 2)
- Clustered faces based on HSV features
- Computed centroids of clusters

Template Classification
- Detected face in template image
- Extracted HSV features
- Predicted cluster using trained KMeans model


 Visualizations

 Template Classification Result

![Template Classification](images/template_result.png)



Key Findings

- HSV color features provide meaningful separation between face groups.
- KMeans effectively clusters similar faces based on color similarity.
- The template image was successfully classified into one of the trained clusters.
- Model performance depends on correct face detection and feature extraction.


  Bias-Variance Insight (KNN Context)

- Small K → Low bias, High variance (overfitting)
- Large K → High bias, Low variance (underfitting)
- Optimal K balances both.


 Conclusion

This project demonstrates how computer vision and unsupervised learning can be combined for practical classification tasks. Face detection using Haar cascades works efficiently, and clustering in HSV space enables meaningful grouping of visual patterns. The approach highlights the importance of feature representation in machine learning tasks.



