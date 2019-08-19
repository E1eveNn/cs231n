# [CS231N Convolutional Neural Networks for Visual Recognition](http://cs231n.github.io/)

## Assignments

This repository provides CS231N assignment and answers (**not official**)

 [Assignment #1: Image Classification, kNN, SVM, Softmax, Neural Network](http://cs231n.github.io/assignments2019/assignment1/)

 [Assignment #2: Fully-Connected Nets, Batch Normalization, Dropout, Convolutional Nets](http://cs231n.github.io/assignments2019/assignment2/)

 [Assignment #3: Image Captioning with Vanilla RNNs, Image Captioning with LSTMs, Network Visualization, Style Transfer, Generative Adversarial Networks](http://cs231n.github.io/assignments2019/assignment3/)



## Docs

- [English version](http://cs231n.github.io/)

- [中文文档]()



## Enviroments

-system os: Windows 10

-tensorflow: 2.0-beta1

-pytorch: 1.2.0


## Tips

For the dataset needed in assignment, run `.sh` files to get dataset if you are Linux user, otherwise for Windows user, here are two tips:

1. For examples, open `get_datasets.sh` file, you shall see these codes:
```
# Get CIFAR10
wget http://www.cs.toronto.edu/~kriz/cifar-10-python.tar.gz
tar -xzvf cifar-10-python.tar.gz
rm cifar-10-python.tar.gz 
```
Manually copy the url `http://www.cs.toronto.edu/~kriz/cifar-10-python.tar.gz` to browser, and the browser will automatically start downloading.

2. For those urls can not open in the browser, copy the link, and open Xunlei(迅雷) to create a new task, fill in this url, and Xunlei will start downloading.


## Problems
You may meet some problems as below :

**1. Import Error: no module named 'past'**

`pip install future`

**2. ImportError: cannot import name 'imread'**

imread is deprecated! imread is deprecated in SciPy 1.0.0, and will be removed in 1.2.0. Use imageio.imread instead.

- *Solvement1:* 
degrade scipy to 1.2.0 or less
- *Solvement2:* 
use `from imageio import imread` instead.

**3. ImportError: cannot import name 'imresize'**

imresize is deprecated! imresize is deprecated in SciPy 1.0.0, and will be removed in 1.2.0. Use skimage.transform.resize instead.

- *Solvement1:* 
degrade scipy to 1.2.0 or less
- *Solvement2:* 
use `from skimage.transform import resize as imresize` instead.

**4. Object arrays cannot be loaded when allow_pickle=False** 

open file cs231n/data_utils.py, revise `f = np.load(imagenet_fn)` to `f = np.load(imagenet_fn,allow_pickle=True)` in function load_imagenet_val(num=None) , line 256.

**5. TypeError: 'numpy.float64' object is not iterable**

which may occur in `assignment3/StyleTransfer.ipynb`, open cs231n/image_utils.py, revise `img = imresize(img, scale_factor)` to `img = imresize(img, new_shape)` in function load_image(filename, size=None), line 90.
  
**6. AssertionError:** 

you may encounter it in `assignment3/Generative_Adversarial_Networks_PyTorch.ipynb`, block \[7], replace `assert np.any(np_z < 0.0) and np.any(np_z > 0.0)` with `assert not np.any(np_z < 0.0) and np.any(np_z > 0.0)`
