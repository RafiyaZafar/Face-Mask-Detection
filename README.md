# Face-Mask-Detection

## Overview
This project focuses on developing a robust Face Mask Detection system using the Faster R-CNN architecture. The model is trained to identify individuals wearing masks, differentiate between various mask-wearing scenarios (with_mask, without_mask, mask_worn_incorrect), and provide precise bounding box annotations.

## Dataset Source
The dataset used for training and validation was obtained from Kaggle. It includes a diverse collection of images capturing individuals in different scenarios, emphasizing various face poses, lighting conditions, and mask-wearing variations.

## Dataset Content
- Images: The dataset consists of images in .png format.
- Annotations: Each image is accompanied by an XML file containing bounding box annotations. These annotations provide information about the presence or absence of masks and the correct or incorrect placement of masks on individuals' faces.

## Dataset Size
The dataset comprises 1232 images for training and 109 images for validation. The classes are distributed as follows:
- "without_mask"
- "with_mask"
- "mask_worn_incorrect"

## Data Preprocessing
Before training, images undergo preprocessing, including resizing and color conversion. XML files are parsed to extract bounding box coordinates and class labels, ensuring compatibility with the Faster R-CNN model.

## Model Training
The face mask detection model is trained using the Faster R-CNN architecture with pre-trained weights. The training process involves iteratively presenting the training dataset to the model, allowing it to learn features and patterns associated with face mask detection.

## Loss Function
The model minimizes a combination of classification and regression losses during each training iteration. The classification loss assesses the accuracy of predicted class labels, while the regression loss evaluates the accuracy of predicted bounding box coordinates.

## GPU Acceleration
To expedite training, the model utilizes GPU acceleration, specifically CUDA if a compatible GPU is available. This accelerates matrix operations, significantly reducing training time and facilitating faster convergence.

## Averaging Losses
An Averager class is employed to track and average both training and validation loss values. This class aids in obtaining a smoothed representation of the model's performance, enabling better monitoring and analysis.

## Evaluation Metrics
- Mean Average Precision (mAP): Achieved an average mAP score of 0.8130, surpassing the threshold of 0.8 for robust object detection.
- Intersection over Union (IOU): Consistently exceeded 0.6, indicating precise localization of detected faces.

## Example Output
In the GUI, the system will showcase images with different mask scenarios, including masked, unmasked, and incorrectly worn masks.
![check](https://github.com/RafiyaZafar/Face-Mask-Detection/assets/90679542/a3726536-cc75-455b-8e37-b36e4b266403)

## Data Flow Diagram
The data flow diagram illustrates the process of the Face Mask Detection system.
![Data Flow Diagram](https://github.com/RafiyaZafar/Face-Mask-Detection/assets/90679542/896161ad-bcdc-49e2-b7d9-2c4c01bf1434)



This Face Mask Detection system serves as a reliable tool in ensuring public health and safety, showcasing a high degree of precision and recall.
