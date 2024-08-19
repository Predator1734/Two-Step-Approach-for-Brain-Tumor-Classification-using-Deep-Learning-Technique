# Two Step Approach for Brain Tumor Classification using Deep Learning Technique

This project presents a two-stage deep learning method for detecting and classifying brain tumors using MRI scans. The proposed approach utilizes a Capsule Neural Network (CapsNet) for initial tumor detection and a Convolutional Neural Network (CNN) enhanced with a Swin Transformer for tumor classification.

Stage 1: Tumor Detection

Dataset: The BR35H MRI dataset is employed, containing 1,500 images labeled "Tumor" and 1,500 labeled "No Tumor."
Pre-processing: Images are resized to 224x224 pixels, normalized, and annotated to ensure consistent input for the model.
Model Architecture: A custom CapsNet is developed, featuring convolutional layers for initial feature extraction, followed by primary and digit capsule layers. The network uses routing algorithms to optimize feature aggregation.
Performance: The CapsNet achieved a testing accuracy of 97.83%, effectively identifying the presence of tumors.

Stage 2: Tumor Classification

Dataset: A combination of the BraTs2020 dataset and another commonly available dataset, categorized into 16 distinct brain tumor types, is used for classification.
Pre-processing and Data Augmentation: Images are resized to 224x224 pixels, normalized, and augmented with random flips and rotations to enhance the model's ability to generalize.
Model Architecture: A CNN model, integrated with a Swin Transformer pre-trained on large datasets, is utilized for feature extraction and classification. The architecture includes dense layers with ReLU activation, dropout for regularization, and a final softmax layer for outputting class probabilities.
Performance: The CNN with the Swin Transformer reached an overall accuracy of 92.86%, with the ability to generate confidence scores for each of the 16 tumor classes.

Evaluation Metrics:

Accuracy, Loss, and Confusion Matrix: These metrics are used to evaluate the model's performance, ensuring robustness and reliability.
Precision, Recall, and F1-Score: These metrics assess the model's ability to correctly classify tumor types, with particular attention to handling imbalanced datasets.
Confidence Score: The classification model provides confidence scores, indicating the certainty of the model's predictions, which is critical for clinical decision-making.

Conclusion:

This dual-stage methodology demonstrates significant improvements in brain tumor detection and classification over traditional methods. The integration of CapsNet for detection and a CNN enhanced with a Swin Transformer for classification offers a robust and accurate solution for diagnosing brain tumors. The approach holds potential for early and precise diagnosis, with the confidence scores providing an additional layer of reliability in clinical settings.






