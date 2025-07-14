# Parking-Lot-Image-Classification

This project classifies images of parking spots as either empty or not_empty using a Support Vector Machine (SVM). The images are pre-labeled, and the model learns pixel-level patterns from the dataset to predict whether a spot is vacant or occupied.

     Note: This project does not detect cars in real-time video feeds or do object detection. It learns from labeled static images.

# Dataset 

    The dataset contains two folders:

        empty/: Images of empty parking spaces

        not_empty/: Images of occupied parking spaces

    Images are pre-labeled and stored in a zip file named clf-data.zip.

# Project Overview

# Step	                        Description
Data Extraction	            Unzipped from Google Drive
Preprocessing	              Resized to 15x15 pixels, flattened
Model Selection	            SVM (Support Vector Classifier)
Hyperparameter Tuning	      GridSearchCV on C and gamma
Model Evaluation	          Accuracy score + Visual validation
Model Persistence	          Saved model using pickle

# Tech Methods 

Python

scikit-learn

NumPy

matplotlib

skimage

Google Colab for training

pickle for model saving


# Preprocessing 

Resize Images: All images resized to 15x15 pixels to reduce dimensionality

Flattening: 3D image array flattened into a 1D vector

Labels:

    empty → 0

    not_empty → 1


# Model Training 

Performed Grid Search over gamma and C values

Used train_test_split with stratify to preserve class balance

# Key Takeaways 

SVMs are effective for small image datasets with clear binary classification

Downscaling images speeds up training without major accuracy loss

Reshaping and flattening image data is essential for feeding into traditional ML models

Grid search helps fine-tune hyperparameters (C and gamma)

Even without deep learning, solid results are achievable with classical ML techniques


