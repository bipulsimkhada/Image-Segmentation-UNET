# Image-Segmentation-UNET

## UNET
U-Net is a convolutional neural network (CNN) architecture that is commonly used for image segmentation tasks. It has a U-shaped structure, which consists of a contracting path, a bottleneck, and an expanding path.

The contracting path, also known as the encoder, begins with a series of convolutional layers followed by max pooling layers, which downsample the input image while increasing the number of feature channels. The downsampling allows the network to capture increasingly abstract and high-level features. The bottleneck is formed by a layer that consists of convolutional and pooling layers without any further downsampling. This layer enables the network to capture contextual information from the input image, which is useful for accurately segmenting objects. The expanding path, also known as the decoder, begins with a series of upsampling layers, which increase the size of the feature maps. Each upsampling layer is followed by a concatenation with the corresponding feature map from the contracting path through skip connections. This allows the network to incorporate detailed information from the earlier layers, which helps to improve the accuracy of the segmentation.

The upsampling layers are followed by a series of convolutional layers that reduce the number of feature channels. This step helps reduce the network's complexity and ensure a smooth segmentation map.


## Libraries 
* Keras
* matplotlib
* tqdm
* itertools
* skimage
* numpy
* pandas

## Tool
* Google Colab
* Google Drive

## Dataset
Data Set: https://drive.google.com/drive/folders/1jA2rIBqL8SwvZK6lJdGNXRM1IqESArXG?usp=sharing

## Image Segmentation using UNET 
In this project, we used the dataset containing image with multiple nucleus and UNET archetecture is implemented to segment necleus only. We have original image and masked image and we trained our data to learn how nucleus look and use the model to recognize the location of nucleus in the image.  Here are the steps involved:
* Mount Google Drive and load data. 
* Create Custom Metric - Intersection over Union (IoU)
* * Build U-Net Model
* Compile and train the model
* Predicting masks in training data
* Predicting maks in test data. 

## Original and Masked image for Training
<img src="https://github.com/bipulsimkhada/Image/blob/main/UNET/Training%20and%20masked.png">

## Original, Training Masked, and Predicted Masked images
<img src="https://github.com/bipulsimkhada/Image/blob/main/UNET/predicted%20masked%20for%20training.png">

## Original and Predicted Masked for test image
<img src="https://github.com/bipulsimkhada/Image/blob/main/UNET/predicted%20masked%20for%20test.png">
