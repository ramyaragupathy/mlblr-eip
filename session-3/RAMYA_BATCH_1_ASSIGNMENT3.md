# Ramya Ragupathy | Batch 1 | Assignment 3
Also available in [Github](https://github.com/ramyaragupathy/mlblr-eip/blob/master/session-3/RAMYA_BATCH_1_ASSIGNMENT3.md)

## Data Augmentation:
Going by the dictionary definition, augmentation refers to increasing the input data points. This is a technique used to increase the amount of data we have using our existing dataset.

This is achieved using operations like flipping/rotating images. A CNN is expected to detect objects even when it is in different orientations - like in different size, position, lighting, colours. A neural network that's robust enough to detect objects in any different condition is said to be invariant. Data augmentation helps in achieving `invariance` by providing more examples using the existing dataset.

Inspite of whether the available dataset is small/huge, this technique is valuable. Either ways, having diverse data will help avoiding the problem of overfitting and result in good generalisation.

![rose is a rose](https://media.giphy.com/media/kkFmE8jN0Ygco/giphy.gif)

There are different ways to do image augmentation - like rotation, flipping, altering light conditions, changing orientation, modifying the scale/size, adding noise. For example, in [Imagenet classification](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf), 2 forms of data augmentation is applied:
 1. Cropping the image
 2. Altering the intensities of RGB images

Each deep learning engine has different classes to implement Data Augmentation. eg: keras uses `ImageDataGenerator()`.

![cat image](https://user-images.githubusercontent.com/12103383/39521104-c50c2718-4e2a-11e8-996c-9a369d11631f.png)

_[Random images generated from an input using keras](https://blog.keras.io/)_

Before data augmentation, all images are pre-processed and brought to a fixed size. In general data augmentation is done in a per epoch basis. In each epoch, data is fed in batches of fixed size and data augmentation is carried out for each batch input. In this method, network gets to see different images during each epoch. Data augmentation can also be done all at once for the entire training dataset even before the actual training begins. By adopting this practice we increase the size of the entire dataset and create a copy of image translations on hard disk. However while implementing data augmentation during batch training, we reduce the memory overhead and also increase the diversity of the dataset that the network gets to train on!

## Initialisation

Initialisation refers to initialising the network with right weights. Initial weights play a vital role in how quick we reach at global minimum/convergence and the accuracy. Suppose we initialise all the weights to `0`, then the network does not learn anything. When we train a network for a dataset, it implies choosing the right weights, that would keep the cost/loss as low as possible.

### Random weight initialisation

In tensor flow random weight initialisation can happen from a normal/gaussian distirbution or uniform distribution.


## Activation Functions

Activation functions are similar to the cell body of a neuron, that processes information. In a CNN, an activation unit takes the inputs, multiplies by a corresponding weights, sums up all the values from the input into one and then decides whether to send it past further(activate) or not. Activation is also called a transfer function as it decided the flow/transfer of information from one layer to another.

![image](https://user-images.githubusercontent.com/12103383/39525095-ac7d045c-4e38-11e8-8409-283979937fd8.png)

_[Source](http://shodhganga.inflibnet.ac.in/bitstream/10603/48/6/chaper%204_c%20b%20bangal.pdf)_

