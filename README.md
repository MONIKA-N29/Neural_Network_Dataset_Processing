Introduction:
Images from the Intel Image Dataset are classified into six categories—buildings, forest, glacier, mountain, sea, and street—using Convolutional Neural Networks (CNNs).
The goal is to compare different CNN architectures, evaluate their performance, and visualize results with accuracy/loss curves and sample predictions.

Dataset:
Source: Kaggle – Intel Image Classification
Structure:
- seg_train/seg_train → training images
- seg_test/seg_test → validation images
- Each folder contains subfolders for each class
Number of classes: 6
Preprocessing:
Resized images to 150×150 pixels
Normalized pixel values to [0,1]
Converted labels to one-hot encoding

CNN Architectures

Architecture 1 – Basic CNN
3 Conv2D layers (32 → 64 → 128) with MaxPooling
Flatten → Dense(128) → Dropout(0.5) → Output
Optimizer: Adam
Loss: categorical_crossentropy
Results:
Training epochs: 10
Validation Accuracy: XX% (replace with your result)

Architecture 2 – Deeper CNN
4 Conv2D layers (32 → 64 → 128 → 256)
BatchNormalization after each Conv layer
GlobalAveragePooling instead of Flatten
Dense(256) → Dropout(0.5) → Output
Optimizer: Adam
Loss: categorical_crossentropy
Results:
Training epochs: 20
Validation Accuracy: YY% (replace with your result)

Training Curves:
Accuracy and loss plots

![Architecture1 Accuracy and Loss] https://github.com/MONIKA-N29/Neural_Network_Dataset_Processing/blob/main/Screenshot%202025-09-05%20180046.png

![Architecture2 Accuracy and Loss] https://github.com/MONIKA-N29/Neural_Network_Dataset_Processing/blob/main/Screenshot%202025-09-05%20180435.png

Sample Predictions:
Sample images showing True vs Predicted labels

![Sample Predictions Architecture 1]-
https://github.com/MONIKA-N29/Neural_Network_Dataset_Processing/blob/main/Screenshot%202025-09-05%20181153.png

![Sample Predictions Architecture 2]-
https://github.com/MONIKA-N29/Neural_Network_Dataset_Processing/blob/main/Screenshot%202025-09-05%20181602.png


Conclusion:

In this project, we successfully built and trained Convolutional Neural Networks (CNNs) to classify images from the Intel Image Dataset into six categories: buildings, forest, glacier, mountain, sea, and street. Two different architectures were implemented and evaluated.

Observations from Architecture 1 (Basic CNN):
The model achieved reasonable accuracy with fewer layers.Training was faster but the network struggled with complex patterns in some classes.It provided a good baseline for comparison with deeper architectures.

Observations from Architecture 2 (Deeper CNN with BatchNormalization):
Adding more convolutional layers and batch normalization improved feature extraction and generalization.GlobalAveragePooling reduced overfitting compared to Flatten, and Dropout further helped in regularization.Validation accuracy was higher than Architecture 1, indicating better performance on unseen images.

Overall, the project demonstrates that increasing network depth and using regularization techniques like BatchNormalization and Dropout can significantly improve CNN performance on multi-class image classification tasks. Visualizing predictions and training curves helped us understand how the models learned and where they could improve.

Future Work:
Implementing Transfer Learning with pre-trained models such as VGG16 or ResNet50 to further improve accuracy.
Experimenting with data augmentation to expand the dataset and make the models more robust.
Fine-tuning hyperparameters like learning rate, batch size, and optimizer choice to optimize performance.

This work shows the practical workflow of building, evaluating, and comparing CNN models for image classification and highlights the importance of architecture choices, training strategies, and model evaluation in deep learning projects.
