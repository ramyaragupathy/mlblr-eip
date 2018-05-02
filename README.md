Deep Learning has revolutionised computer vision and it is the core technology behind capabilities like self-driving car. We use tensorflow and tensorflow implementation of Keras.

## Keras & TensorFlow:
TensorFlow is the most popular tool of deep learning and Keras is the popular API/interface for specifying DL models. Keras started as a standalone library for specifying deep learning models, which could then be run in TensorFlow as well as in other DL computation engines.

Standalone Keras library still exists but TensorFlow has become the dominant engine for DL, os the creator of Keras implemented a version of Keras, that's built into TensorFlow. This allows you to specify models with the elegant of Keras while taking greater advantage of some powerful TensorFlow features.

## How images are stored for ML?
Image is composed of pixels and pixels are present in rows and columns. So it is natural to store them in a matrix. For a black and white/grayscale image, each value represents darkness of pixel in a image. 

Colour images have an extra dimension. There are each matrices, with pixel in each matrix value showing how red/green/blue the pixel is. 

Tensor is the word for something like a matix but with which can have any number of dimensions. So these matrices could be called tensors.


## Convolution

Today's deep learning models apply something called convolutions to image tensors. A convolution is a small tensor that can be multiplied over little sections of a main image.

Depending on values in the convolution array, it can pick out specific patterns from the image.
eg: Horizontal line detector:

|1.5|1.5|
----|----
|-1.5|-1.5|

When multiplied on an image section with horizontal line, it results in a large value. When applied over a section without horizontal line, it gives a value close to zero.

Numerical value in the convolutin tensor decides what pattern it detects in a section of the image.