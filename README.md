# Pneumonia Multiclass Classification

## Project Overview
This project aims to classify chest X-ray images into different pneumonia types: **Bacterial Pneumonia, Viral Pneumonia, and Normal (Healthy)** using **deep learning (CNNs)** in **TensorFlow/Keras**. The model is trained on labeled pneumonia X-ray images and can predict pneumonia type from new images.

## Dataset
The dataset consists of chest X-ray images classified into:
- **Bacterial Pneumonia**
- **Viral Pneumonia**
- **Normal (Healthy Lungs)**

The dataset is preprocessed and augmented to improve model performance.

## Steps Involved
1. **Data Preprocessing**
   - Organizing images into labeled folders.
   - Splitting data into training (80%) and validation (20%).
   - Image augmentation: rotation, scaling, flipping.

2. **Model Training Pipeline**

- 1. Transfer Learning with DenseNet121
  - Used **DenseNet121** as the base model (pretrained on ImageNet).
  - Removed the top layers and added **custom convolutional layers**.
  - Used **Dropout and Batch Normalization** for regularization.
  - Trained the model on **pneumonia X-ray images**.

- 2. Fine-tuning the Model
  - Performed **data augmentation** (rotation, zoom, flipping, brightness).
  - Trained additional layers while **freezing lower layers** of DenseNet121.
  - Unfroze some base model layers and fine-tuned the full model.
  - **Final training stage**: 15 epochs for optimized results.

3. **Evaluation & Testing**
   - Model performance metrics: Accuracy, AUC.
   - Confusion matrix and classification report.
   - Predicts on unseen X-ray images.

## Results
- **Evaluation metrics**:
  - **Accuracy:** *86*
  - **AUC Score:** *95*


