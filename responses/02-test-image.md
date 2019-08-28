## Import MNIST
Now we are ready to roll! First, we must admit that it takes a lot of data to train a NN, and 70,000 examples is an anemic dataset. So instead of doing a more traditional 70/20/10 or 80/10/10 percent split between training/validating/testing, we will do a simple 6:1 ratio of training:testing (note that this is not best practices, but when there is limited data it may be your only recourse).

We first load in the dataset from the Keras package:
```console
>>> fashion_mnist = keras.datasets.fashion_mnist
>>> (train_images, train_labels), (test_images, test_labels) = fashion_mnist.load_data()
Downloading data from https://storage.googleapis.com/tensorflow/tf-keras-datasets/train-labels-idx1-ubyte.gz
32768/29515 [=================================] - 0s 1us/step
Downloading data from https://storage.googleapis.com/tensorflow/tf-keras-datasets/train-images-idx3-ubyte.gz
26427392/26421880 [==============================] - 2s 0us/step
Downloading data from https://storage.googleapis.com/tensorflow/tf-keras-datasets/t10k-labels-idx1-ubyte.gz
8192/5148 [===============================================] - 0s 0us/step
Downloading data from https://storage.googleapis.com/tensorflow/tf-keras-datasets/t10k-images-idx3-ubyte.gz
4423680/4422102 [==============================] - 0s 0us/step
>>>
```
The first line merely assigns the name fashion_mnist to a particular dataset located within Keras' dataset library. The second line defines four arrays containing the training and testing data, cleaved again into separate structures for images and labels, and then loads all of that data into our standup of Python. The training data arrays will be used to (duh) train the model, and the testing arrays will allow us to evaluate the performance of our model.

### Look at data
It's always nice to be able to show that we've actually done something; ever since kindergarten there has been no better way than with a picture!  You'll note that we pip installed and imported MatPlotLib, a library for plots and graphs.  Here we'll use it to visualize an example of the Fashion MNIST dataset.
```console
>>> plt.figure()
<Figure size 640x480 with 0 Axes>
>>> plt.imshow(train_images[0])
<matplotlib.image.AxesImage object at 0x00000133F2152518>
>>> plt.colorbar()
<matplotlib.colorbar.Colorbar object at 0x00000133F2184A90>
>>> plt.grid(False)
>>> plt.show()
```
The first command basically generates a figure object that will be manipulated by commands 2 through 4. Command 2 specifies what it is that we shall be plotting: the first element from the train_images array. *NOTE*: Recall that python is an inclusive counting language, meaning that it numbers/indexes things starting from zero, not one!  And the final command, "show()", tells Python to generate this figure in an external (from CMD) window.
Your window should contain a plot that looks similar to Figure 3. Also, be aware that after plt.show(), Python will not return you to a command line until the newly generated window (containing our super nice picture) is closed. Upon closing the window, you will be able to continue entering Python commands.

![image of boot]({{repoUrl}}/raw/master/img/boot.png)
*Figure 3 The graphical output of the above code snip. Note that this is a pixelated ankle boot image in greyscale that has been false-colored.*

*When you have generated a graph of a boot image, close this issue*