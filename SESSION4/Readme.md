# Architectural Basics

##### 1. How many layers
I have used 3 convolution layers followed by transition block which includes Maxpooling and 1x1 convolution. Then further added 4 more convolotion layers before flattening. 

##### 4. 3x3 Convolutions
All convolution layers are using 3x3 convlution as we can reach to any size of receptive field using 3x3.

##### 2. MaxPooling
Since the image size is small and the object utilized the whole image, so Maxpooling at a receptive field of 7x7 in this case is providing us the best accuracy.

##### 5. Receptive Field
Receptive field provides us the idea that at which layer the model could be seeing the gradient, texture, patterns, parts of objects and objects. We are flattening the model at 20x20 receptive field.  

##### 6. SoftMax
Softmax is used because in this case we need to get a better classification and not the most honest results.

##### 3. 1x1 Convolutions
1x1 convoution is used after maxpooling, so that, once maxpooling is applied the feature maps are projecting the patterns/textures more loudly, then 1x1 pools these loud features so that the spatial information is not lost and can be used further.

Secondly it also is used here to reduce the number of channels in a very inexpensive way.
##### 11. Position of MaxPooling
Maxpooling is placed considering the receptive field.

##### 12. Concept of Transition Layers
Maxpooling followed by a 1x1 can be referred as Transition layer. Maxpooling reduces the dimensions of output images while 1x1 is mostly used to reduce the number of channels. Therefore using both combinedly, reduce the overall dimension. 

##### 13. Position of Transition Layer


##### 8. Kernels and how do we decide the number of kernels?
I have use 3x3 kernels. nUmber of kernels have been kept less to reduce the number of parameters.
##### 10. Image Normalization
In this model, we are normalizing the image by dividing pixel by 255 on the input images. Image normalization is not being applied on any output images at any layer. 

##### 9. Batch Normalization
##### 15. DropOut
Added Dropouts at each layer to address overfitting.

##### 7. Learning Rate
I observed that Adding Dropouts have reduced the overfitting issue, but the accuracy was still fluctuating. Learning rate helped to reduce this and attain high accuracy at a very early stage than model without learning rate. 

##### 14. Number of Epochs and when to increase them

##### 16. When do we introduce DropOut, or when do we know we have some overfitting
##### 17. The distance of MaxPooling from Prediction
##### 18. The distance of Batch Normalization from Prediction
##### 19. When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered)
##### 20. How do we know our network is not going well, comparatively, very early
##### 21. Batch Size, and effects of batch size
##### 22. When to add validation checks
##### 23. LR schedule and concept behind it
##### 24. Adam vs SGD


