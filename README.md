# AUTOMATED-DIAGNOSTIC-CLASSIFICATION-OF-CHEST-XRAYS
## Introduction
In the field of medical imaging, the rapid and accurate diagnosis of thoracic diseases is critical for effective patient treatment and management. However, manual interpretation of chest X-rays, which are among the most commonly performed radiological procedures, can be time-consuming and subject to variability based on the radiologist’s experience and number of cases to be reviewed. With the incident COVID-19 pandemic and the high prevalence of respiratory diseases such as pneumonia and tuberculosis, healthcare systems are under immense pressure, necessitating tools that can assist in quick and reliable diagnosis.
This project seeks to address the challenge of automating the classification of chest X-rays into four categories which includes COVID-19, pneumonia, tuberculosis and in normal study using a Convolutional Neural Network (CNN) model. The solution aims to aid radiologists in screening processes by providing preliminary diagnostic suggestions, thus reducing the time to diagnosis and helping prioritize urgent cases. By leveraging deep learning algorithms and a substantial dataset of labeled X-ray images, the model endeavors to match the diagnostic ability of an experienced radiologist in identifying and distinguishing between these critical respiratory conditions.
## Methodology
This involved choosing the appropriate architecture, including the number of layers, types of layers (e.g., dense, convolutional, recurrent), activation functions, and output layer configuration. A sequential CNN model was constructed using Keras, consisting of multiple convolutional layers followed by max-pooling layers, a flattening step, a fully connected layers and finally a softmax layer for multiclass classification.
## Model Architecture
The CNN model was defined using the sequential API and it comprises:
Four convolutional layers with increasing filter sizes (32, 64, 128, 128) and ReLU activation functions, each followed by a max-pooling layer to extract feature from images.
A flattening layer transitions to fully connected layers.
A dropout layer (50% rate) is used for regularization to prevent overfitting.
The final dense layer with a softmax activation function outputs the probability distribution over the four classes.
## Training
Training was performed using the fit method, specifying the number of epochs and utilizing both training and validation data generators. The model was trained for five epochs using the Adam optimizer and categorical cross-entropy loss function. Precision, recall, and F1-score are included as metrics alongside accuracy. 
## Result
The model achieved an accuracy of approximately 81.6% on the test set. Training and validation metrics indicate an overall satisfactory performance. The model demonstrates proficiency in recognizing patterns specific to each class. However, misclassifications are noted, particularly between normal and pneumonia classes, as evident from the confusion matrix.
## Conclusion
This CNN model represents a promising step in automated diagnosis through chest X-rays. Further optimization, possibly through hyperparameter tuning, an expanded dataset, or more sophisticated architectures, could enhance its diagnostic capabilities.
The model seems to perform well for pneumonia detection but shows room for improvement in correctly classifying normal cases and tuberculosis. The model's tendency to confuse COVID-19 with pneumonia and normal cases likely indicates that data representation might need to be reviewed. Increase in dataset could potentially improve distinction across classes. Further analysis using precision-recall curves, ROC curves, or other advanced metrics could provide more insight into the model's classification behavior as well.

