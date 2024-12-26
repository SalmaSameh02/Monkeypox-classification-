# Monkeypox-classification-
CAD project... 
<h1>Introduction</h1>
This project focuses on building a machine learning model to classify cases of monkeypox using a binary dataset. The goal is to support healthcare professionals by providing a tool for early detection and diagnosis, which could help combat the spread of the disease. By applying advanced techniques in data processing, feature extraction, and model evaluation, this project achieves impressive classification performance.
<h1>
  Dataset Overview
</h1>

The dataset for this project is available on Kaggle and can be accessed here (https://www.kaggle.com/datasets/nafin59/monkeypox-skin-lesion-dataset). It contains images categorized into two classes: "Monkeypox" and "Others." These images form the foundation of the analysis and model development.

<h1>Steps</h1>
<h2>1. Image Enhancement </h2>
To improve the quality of the images, we applied the CLAHE technique (Contrast Limited Adaptive Histogram Equalization). This step enhances the contrast in the images, making them more suitable for analysis. Additionally, the images were converted to greyscale to simplify processing.

<h2>2. Feature Extraction </h2>
We used several powerful techniques to extract meaningful information from the images:

GLCM (Gray-Level Co-occurrence Matrix): For texture analysis.
Fourier Transform: To capture frequency domain features.
Wavelet Transform: For analyzing localized changes in the image.
Discrete Cosine Transform: To focus on spatial frequency information.
<h2>3. Feature Selection </h2>

To choose the most relevant features, we experimented with various selection methods:

Filter Methods: These include Information Gain, Fisher's Score, Chi-Square, and Pearson Correlation.
Wrapper Methods: Sequential Forward Selection, Sequential Backward Selection, and Recursive Feature Elimination (RFE).
Hybrid Method: A combination of Pearson Correlation and RFE that provided the best results.
<h2>4. Exhaustive Search </h2>
We included code for an exhaustive search feature selection method in the notebook, but it wasn’t executed due to high computational demands.
<h1>Modeling </h1>

For the classification task, we used a Random Forest Classifier. Each feature selection method produced its own dataset, which was used to train the model.
<h1>
  Results
</h1>

The best accuracy was achieved using the hybrid method, with a score of 80.4%.
The best ROC curve came from the sequential backward selection method, with an AUC of 0.914.
How to Use This Project
