# HurricaneCNN

## Rapid Hurricane Damage Assessment from Satellite Imagery with CNNs for Efficient Resource Allocation

This repository contains the code, presentation slides, and  paper for a class project on hurricane damage classification using Convolutional Neural Networks (CNNs). We addressed the problem of rapidly assessing hurricane damage from satellite imagery using the dataset provided by Quoc Dung Cao and Youngjun Choe [(2018)](https://arxiv.org/abs/1807.01688). Our project involved designing, implementing, and evaluating our own CNN model for classifying images as either "damage" or "no damage" with quantifiable level of accuracy.

This project is created by Deborah Ugaldes & George Whittington.

## Repository Contents

*   `Hurricane_CNN.ipynb`: The main Jupyter Notebook containing the Python code for data preprocessing, model definition, training, and evaluation.
*   `presentation/`: A directory containing the presentation slidesused for our project presentation.
*   `paper/`: A directory containing the paper written for this project.
*   `README.md`: This file, providing an overview of the project and instructions for using the repository.
*   `trained_model.pth`: A file containing the trained model for the CNN with the best metrics for the test sets we used
  
## Data

This project utilizes a dataset of satellite images from the Greater Houston area after Hurricane Harvey in 2017 [(IEEE DataPort)](https://ieee-dataport.org/open-access/detecting-damaged-buildings-post-hurricane-satellite-imagery-based-customized). The dataset contains images labeled as either "Flooded/Damaged" or "Undamaged," representing the state of buildings and infrastructure following the hurricane. These images serve as the input for training and evaluating the CNN model. The dataset is divided into the following subsets:

*   `train`: 5,000 images per class (training data)
*   `validation`: 1,000 images per class (validation data)
*   `test_another`: 8,000 "Flooded/Damaged" and 1,000 "Undamaged" (unbalanced test set)
*   `test`: 1,000 images per class (balanced test set)

All images are 128x128 pixels.

## Model Architecture

The CNN architecture consists of 4 convolutional layers, each followed by a max pooling layer and ReLU activation function, then 2 fully connected layers to help the model learn. The network was implemented using PyTorch.
