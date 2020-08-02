# Image Segmantion using U-Net Deep Leaarning Architecture in Tensorflow 2 
TGS Salt Identification Challenge - Segment salt deposits beneath the Earth's surface

Dataset : https://www.kaggle.com/c/tgs-salt-identification-challenge/data

Model :

![unet](https://github.com/sunilpankaj/Image-Segmantion-using-U-Net-Deep-Leaarning-Architecture/blob/master/U-Net.PNG)


U-Net architecture is separated in 3 parts:

1 : The contracting/downsampling path :

    Contracting path is composed of 4 blocks. Each block is composed of
    
    a. 2, 3x3 Convolution Layer + activation function (with batch normalization)
    
    b. 2x2 Max Pooling
    
2 : Bottleneck :

    The bottleneck is built from simply 2, 3x3 convolutional layers (with batch normalization) with dropout.
    
3 : The expanding/upsampling path :

    Expanding path is also composed of 4 blocks. Each of these blocks is composed of
    
    a. Deconvolution layer with stride 2
    
    b. Concatenation with the corresponding cropped feature map from the contracting path
    
    c. 2, 3x3 Convolution layer + activation function (with batch normalization)
    
    
    
I used similar architecture (number of filters are lesser than actual and adding dropout after every contracting and expanding blocks).

    



   
   
