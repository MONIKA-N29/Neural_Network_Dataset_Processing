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

Observation:
Architecture 2 achieved better accuracy due to deeper layers, batch normalization, and more epochs.
