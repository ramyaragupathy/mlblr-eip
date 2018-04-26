
# Ramya Ragupathy | Batch 1


## Convolution
Convolution is the bedrock of CNNs. Extending the dictionary definition of the term, Convolution is a mathematical technique to roll together different streams of information. To understand `information` we need to understand the practical applications of CNNs. CNNs are largely used in computer vision problems where the algorithms try to replicate how human eyes work. An image for machine processing purposes is represented as a matrix of pixel values. For eg: a 3 x 3 image is represented as a 3 x 3 matrix with each value in the matrix correpsonding to a single pixel in the image. These values are between 0-255.

  ![image as matrix](https://user-images.githubusercontent.com/12103383/39181741-3a33716c-47d8-11e8-8668-a9629fb6d580.gif)

_Source: [setosa.io](http://setosa.io/)_

So at a very basic level  `information` for CNN algorithms is a matrix. This information/data from the image is mixed/merged/rolled with another data matrix called kernels/features to extract or alter specific pixel information from the input image matrix. In the context of CNNs, this merging is a simple elementwise matrix multiplication.

In any CNNs, a series of convolutions will be performed in different layers that are sequentially connected.


## 3 x 3 convolution

A 3x3 convolution is named by the shape of the kernel/feature that is merged with the input image.

| ![3 x 3 kernel](https://user-images.githubusercontent.com/12103383/39184623-b523f686-47e1-11e8-8e10-fb7fc848b2dd.png) | 
|:--:| 
| *3 x 3 kernel* |
  

- Kernel/feature matrix is slided over the input image matrix starting from the top left
- 3 x 3 feature matrix is matched with the 3 x 3 pixel grid. 
- Each value in the current pixel grid is multiplied with the corresponding element in the feature.
- Result of the elementwise multiplication is summed up and the result is stored in a `feature map`.
- Kernel/feature matrix is slided/convolved one step at a time to move to the next element. This slide is usually towards the right and when the feature matrix reaches the end of the input matrix, slide is downwards. Process is repeated after each slide till the feature matrix covers/reaches the bottom right 3 x 3 pixel grid.
- In this methd the resulting `feature map` is smaller in size when compared to the input

![3 x 3 convolution](https://user-images.githubusercontent.com/12103383/39185071-817e77be-47e3-11e8-8e15-2b03745eff90.gif)

_Source: [setosa.io](http://setosa.io/)_

So far convolution has been explained on just a 2D image (grayscale image). While doing the operation on 3D images there are three different color channels (RGB) in the input. Hence the kernel/feature will also have the same number of channels i.e A 3 x 3 kernel/feature will become a 3 x 3 x 3 matrix. Extra layer has been added to match the depth of the input image.

On a given input image, multiple convolutions will be applied with different kernels/features. Each of these kernels will give a separate feature map. Different feature map values are combined together to arrive at image classification results.

## Filters/Kernels
 It is a simple matrix with values that are called weights/parameters. Kernels are `convolved` over an input image to transform the information present as pixels. As each pixel is processed with the filter matrix, a new pixel value emerges thereby resulting in a new image. Pixel value change depends upon the weights/parameters present in the filter matrix. There are specific filters used for  different image processing techniques like sharpening, embossing, horizontal/vertical edge detection, blurring. A few examples are present here: http://matlabtricks.com/post-5/3x3-convolution-kernels-with-online-demo

## Epochs

An epoch is a single pass of the entire training dataset by the training algorithm. Training dataset is the input based on which the neural network/learning algorithm learns about a dataset. Just one glance at the entire dataset is not sufficient for the algorithm to learn and make predictions. It has to repeat the process several times, each time improving the learning compared to the earlier pass. Depending on the problem to be solved number of epochs might vary and the cycle effectively stops at a point when the predictions for the training dataset are quite close to the already labelled values.

## Receptive Field
A receptive field in a CNN is a part of the input image, i.e pixel grid that is visible to a feature/kernel during the sliding/convolution operation.