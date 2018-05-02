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