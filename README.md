# [CS231N Convolutional Neural Networks for Visual Recognition](http://cs231n.github.io/)

## Assignments

This repository provides CS231N assignment and answers (**not official**)

 [Assignment #1: Image Classification, kNN, SVM, Softmax, Neural Network](http://cs231n.github.io/assignments2019/assignment1/)

 [Assignment #2: Fully-Connected Nets, Batch Normalization, Dropout, Convolutional Nets](http://cs231n.github.io/assignments2019/assignment2/)

 [Assignment #3: Image Captioning with Vanilla RNNs, Image Captioning with LSTMs, Network Visualization, Style Transfer, Generative Adversarial Networks](http://cs231n.github.io/assignments2019/assignment3/)



## Docs

- [English version](http://cs231n.github.io/)

- [Chinese version]()

## Problems
You may meet some problems as below:

**1.Import Error: no module named 'past'**

`pip install future`

**2.ImportError: cannot import name 'imread'**

imread is deprecated! imread is deprecated in SciPy 1.0.0, and will be removed in 1.2.0. Use imageio.imread instead.

- *Solvement1:*
degrade scipy to 1.2.0 or less
- *Solvement2:*
use `from imageio import imread` instead.

**3.ImportError: cannot import name 'imresize'**

imresize is deprecated! imresize is deprecated in SciPy 1.0.0, and will be removed in 1.2.0. Use skimage.transform.resize instead.

- *Solvement1:*
degrade scipy to 1.2.0 or less
- *Solvement2:*
use `from skimage.transform import resize as imresize` instead.
  
