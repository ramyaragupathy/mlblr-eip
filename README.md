Deep Learning has revolutionised computer vision and it is the core technology behind capabilities like self-driving car. We use tensorflow and tensorflow implementation of Keras.

## Keras & TensorFlow:
TensorFlow is the most popular tool of deep learning and Keras is the popular API/interface for specifying DL models. Keras started as a standalone library for specifying deep learning models, which could then be run in TensorFlow as well as in other DL computation engines.

Standalone Keras library still exists but TensorFlow has become the dominant engine for DL, os the creator of Keras implemented a version of Keras, that's built into TensorFlow. This allows you to specify models with the elegant of Keras while taking greater advantage of some powerful TensorFlow features.

## How images are stored for ML?
Image is composed of pixels and pixels are present in rows and columns. So it is natural to store them in a matrix. For a black and white/grayscale image, each value represents darkness of pixel in a image. 

Colour images have an extra dimension. There are each matrices, with pixel in each matrix value showing how red/green/blue the pixel is. 

Tensor is the word for something like a matix but with which can have any number of dimensions. So these matrices could be called tensors.