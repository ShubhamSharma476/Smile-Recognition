# Smile-Recognition:
 This repository contains the code for a deep learning model for classifying smiles as positive, negative, or not smiling using transfer learning on 
ResNet50 architecture. The model was trained and tested on a custom dataset of facial images.

Dataset:

 The dataset used for this project contains images of faces labeled as positive smile, negative smile, and not smile. The dataset was split into training
and testing sets and saved as CSV files.

Data Preprocessing:

 The input images were resized to a fixed size of (224, 224) to comply with the input size required by ResNet50 architecture.
Data augmentation was applied using the ImageDataGenerator from Keras library. The training and validation data were generated using this data generator 
with categorical class mode and a batch size of 32. The test data was generated with a batch size of 1.

Model:

 The model was based on ResNet50 architecture, and transfer learning was used with weights pre-trained on the ImageNet dataset. 
The last layer of the model was replaced with a dense layer with softmax activation function to output the predicted class probabilities. 
The model was compiled with the Adam optimizer, categorical crossentropy loss function, and accuracy as a metric. The model was trained for 20 epochs.

Results:

 The final model achieved an accuracy of 85% on the validation set and 82% on the test set. The model could be further improved by increasing the number 
of epochs or making the model trainable, but this would increase training time and the number of parameters. The final model's parameters were 24+ million,
with trainable parameters around 1 million and the rest being non-trainable.
