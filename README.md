# Classification-of-images-using-cifar10-dataset

Cifar10 is a collection of images of 10 classes. Here i have 50000 training images and 10000 test images each of size (32, 32, 3). I had used keras library because it is very useful in the tasks of image classification as there are many built in function which i require. Also the cifar 10 dataset is present in the keras library.

First i had downloaded the images and loaded them in to the tain and test sets.
As there were 10 categorical classes we convert them in to binary class matrices.

# Building the model

Here we use sequential API for building the model so each layer is stacked with the previous layer.
layer1: convolution layer with filter size (3, 3) and 32 feature maps. i had used padding =same so the output of feature maps width and height is same as input.
layer 2: I had used the activation function 'relu'.
layer 3: Batch Normalization
and the layers will repeat including dropout layers to resist the model from over fitting and max pooling layers to reduce the size of feature maps.
At the end the output is fed to flatten layer so it converts the input to a one dimensional vector and feeds to the neural network layer with 512 neurons.
At the end i used softmax activation function so the output would be probabilities of predicted classes.

# Normalizing the input 

Here i had converted the images in to float 32 as the normalization would be easier when it is in floating point
Normalization would be done when we divide image vector matrix with 255 so each the values in it would be ranging between 0 to 1.0

# Compiling the model

Here i fixed the batch size to 32 and epochs to 50
Loss function is categorical cross entropy and optimizer is sgd.

# Fitting the model
we use model.fit so the compiler fits the training data to the model and tests on the testing data in each epoch and it runs for 50 epochs and the validation accuracy increases in each and every epoch


