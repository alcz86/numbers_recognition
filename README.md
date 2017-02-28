
# Tensorflow numbers recognition

This project implements convolutional neural network in TensorFlow. The classification task is to recognize sequence of digits on images.
The images were generated randomly. Each digit in the sequence was randomly shifted, padded and twisted in order to get some variation.

The project contains scritps for generaing big volume of random images with sequence of digits. 
You can set the sqeunce length and number of images.

## Neural Net architecture
There are two scripts, both implements 3 layer convolutional network
* conv_net_many_digits.py - for classification long digit sequences
    * layer1 - 3x3conv->max pool->dropout
    * layer2 - 3x3conv->max pool->dropout
    * layer3 - Fully connected 1024
    * output - depends on the sequence length
* conv_net_one_digit.py -  script for classification only one digit
    * layer1 - 3x3conv->max pool
    * layer2 - 3x3conv->max pool
    * layer3 - Fully connected 1024
    * output - 10

## How to run

* First run script generate_digits.py in order to generate some data, 
    * Adjust script parameters to your need: set how many images, how many digits and image size.
    * Parameters:
        * font_size = 26 
        * folder='shared/Digits_2f1'
        * random_digits  - how many digits to generate
        * img_size=(32,32) - image resolution:width, height (good for one digit)
        * number_of_images=10 - how many images with one type of font, final dataset has size number_of_images*number_of_fonts
* Run the classification script with particular implementation of neural net.



## Libraries

* Pillow (3.03) - for generating images
* Numpy
* TensorFlow 1.0 - for convolutional neural network implementation


# Code

* download code from Github - https://github.com/ksopyla/numbers_recognition
* run python code online in PLON - https://plon.io/explore/tensorflow-numbers-recognit/UJqSN82nBK3dRC1jE