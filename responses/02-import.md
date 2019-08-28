## Pip Installing Packages

To complete this project we will need a few packages; these are add-ons available to Python but not included in the base install. Very luckily, we installed the latest Python 3, which includes the Pip Installation module of Python. Pip is a fast and easy way to install packages and their dependencies. As we are doing an NN-based project, we will need to use TensorFlow. For those who only recognize TensorFlow by its association with NNs, it may be shocking to learn that TensorFlow is a more general tool for the manipulation of mathematical entities called tensors.  NNs are just a single use of tenor mechanics, and therefore TensorFlow. 

As tensors and TensorFlow can be fairly complex to manage, there exists another package named Keras that acts as a high-level API (Application Programming Interface), allowing users to easily generation, define and manipulate the structures within TensorFlow.
Finally, as we wish to visualize aspects of our dataset and generate some informational plots, we will want Python's Mathematical Plotting Library, MatPlotLib. Additionally, MatPlotLib facilitates the generation of graphical plots in new windows, even when executed from the Command Line. And finally, to handle numerical computations and array-based operations we will import Numpy.

Starting from the c-prompt (where we left off above), you will need to tell the easy Python package manager (a program that helps you install, uninstall, update and upgrade ancillary features to a larger application) that we want to install Numpy, MatPlotLib, and Tensorflow.
```console
C:\>pip install Numpy
C:\>pip install MatPlotLib
C:\>pip install Tensorflow
```
After each of these actions, pip will display that it is downloading and installing the package. If you have an existing (but not up-to-date) version, pip will first uninstall the old version before installing the new.  If you have previously installed the current version of any package, pip will inform you that the 'requirement already exists'.
Now we can test if Python has installed our Tensorflow correctly (this being the testier of the three packages), by returning to the Python Environment and printing the version of our Tensorflow:
```console
C:\>python
Python 3.6.7 (v3.6.7:6ec5cf24b7, Oct 20 2018, 13:35:33) [MSC v.1900 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import tensorflow as tf
>>> print(tf.__version__)
1.14.0
>>> exit()
```
We can see that I have Tensorflow version 1.14.0 installed!  Unless you have specified an earlier version (and dialing in the version that you need for any particular existing project can be a hassle with Tensorflow) you will have automatically installed the newest stable release, which at the time of this writing was version 2.0.0.
And yes, I have intentionally had to enter and exit the Python environment from the CMD several times. This is called Reinforcement Learning; you've been subjected to the human equivalent of another machine learning technique you will learn about later.

*Leave a comment with the letter (A, B, C, or D) that is false about TensorFlow*

A. TensorFlow can be installed using pip
B. TensorFlow is only used for Neural Networks
C. TensorFlow is used to manipulate tensors
D. The Keras package can make using TensorFlow more easy