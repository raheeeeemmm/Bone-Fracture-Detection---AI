# Bone-Fracture-Detection---AI
Introduction
Bone fractures have long posed significant challenges in medical diagnostics, traditionally relying on manual examination of X-ray images by radiologists. These manual methods, though effective, are not devoid of errors. Recent advancements in Machine Learning (ML) and Artificial Intelligence (AI) offer potential solutions for more accurate and efficient fracture detection. This project aims to leverage these technologies, specifically Convolutional Neural Networks (CNNs), to automate the process of identifying and classifying bone fractures in X-ray images.

Objectives
The primary objectives of this project are:
Developing a Classification System: Create a robust machine learning model capable of identifying and classifying fractures in X-ray images of the elbow, hand, and shoulder.
Building a User-Friendly Application: Develop an intuitive GUI for users to upload X-ray images and receive fracture diagnoses.
Evaluating Model Performance: Assess the accuracy and reliability of the developed models and document their performance.

Methodology
The methodology employed in this project involves several stages, from data collection and preprocessing to model training and evaluation.
Data Collection and Preprocessing:
Dataset: The MURA dataset, containing 20,335 musculoskeletal radiographs, was used. The dataset includes images of the elbow, hand, and shoulder, with the following distribution:
Part	       Normal	       Fractured	       Total
Elbow	        3160	       2236                   5396
Hand	        4330	       1673	       6003
Shoulder    4496	       4440	       8936
Data Augmentation: Techniques such as horizontal flipping were applied to enhance the dataset and improve the model's robustness.

Model Architecture:
Bone Type Classification: Utilized a ResNet50 model to classify the type of bone in the image.
Fracture Detection: Developed specific models for each bone type (elbow, hand, and shoulder) to detect the presence of fractures. Each model was trained on data specific to its corresponding bone type.

Training and Evaluation:
Training: The dataset was split into 72% training, 18% validation, and 10% test sets. The models were trained using the Adam optimizer with a learning rate of 0.0001 and evaluated on the validation set.
Early Stopping: Implemented early stopping to prevent overfitting and restore the best model weights.
Evaluation: Model performance was assessed using accuracy metrics on the test set.

Implementation
The implementation involved several scripts and modules:
Data Loading and Preprocessing (training_parts.py and training_fracture.py):
Loaded X-ray images and their labels from the dataset.
Applied data augmentation techniques and split the dataset into training, validation, and test sets.
Model Training (training_parts.py and training_fracture.py):
Trained a ResNet50 model for bone type classification.
Trained specific models for fracture detection in each bone type (elbow, hand, and shoulder).
Prediction (predictions.py):
Loaded trained models and used them to predict the bone type and the presence of fractures in new X-ray images.
GUI Application (GUI.py):
Developed a graphical user interface for users to upload X-ray images and receive predictions.
Evaluation and Reporting (predictions_test.py):
Evaluated the performance of the models and generated detailed accuracy and loss plots.
