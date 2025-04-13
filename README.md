# Image Classification - Computer Vision with Convolutional Neural Networks and PyTorch
Image classification with a CNN

In this project, we'll have a look at a typical workflow for an image classification problem with a convolutional neural network and PyTorch.

## Contents

### Data Preparation
In this project, we'll have a look at a typical workflow for an image classification problem with a convolutional neural network and PyTorch.
We're going to use the EuroSAT dataset. It's one of many datasets meant for image classification available in torchvision.datsets.

Here's the original description of the dataset:

*In this study, we address the challenge of land use and land cover classification using Sentinel-2 satellite images. The Sentinel-2 satellite images are 
openly and freely accessible provided in the Earth observation program Copernicus. We present a novel dataset based on Sentinel-2 satellite images covering 
13 spectral bands and consisting out of 10 classes with in total 27,000 labeled and geo-referenced images.*

![image](https://github.com/user-attachments/assets/02787806-e2bf-4b5f-9402-a5c726a2153d)

### Baseline Model
It's always good practice to start with a baseline model other models will be compared to. This way, we'll be able to see how our next models perform - better 
or worse than the baseline model.

![image](https://github.com/user-attachments/assets/969f2bd1-2ddb-47dd-8fb9-6f7698874023)

### Model with Nonlinearities
Let's create another model, very much like the baseline model, but this time with some nonlinear activation functions between the layers.

![image](https://github.com/user-attachments/assets/a18fd627-3026-4cbe-a77c-96806c64c565)

### Convolutional Neural Network (CNN)
Convolutional neural networks are good at finding patterns in visual data. Between the input and output layers they contain blocks with, possibly repeated, convolutional 
layers, activation layers and pooling layers. And possibly also other types of layers.

![image](https://github.com/user-attachments/assets/61ef681c-234d-4f16-a15a-8c67805d097e)

### Model Comparison
Let's compare all three models.

![image](https://github.com/user-attachments/assets/1859845d-e94e-4585-abf4-2e8e2004f956)


### Optimizing the CNN Model
The first thing we could do is add some nn.Dropout layers to the two blocks. We can further optimize the model by adding another nn.Conv2s layer to each block.Let's add one more 
improvement. This time, we'll modify the classifier by adding a 50%-nn.Dropout layer, an nn.ReLU layer and another linear layer.

![image](https://github.com/user-attachments/assets/2b82bd57-01bb-4853-8b7f-ba8ec494fc04)

### Predictions
Let's use the best model to make some predictions.

![image](https://github.com/user-attachments/assets/c56da5a2-c09b-400d-affd-12a270a45b02)

