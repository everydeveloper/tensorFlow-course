## Import Packages
We will be executing all of our Python code from the Window's Command Line (CMD). Although CMD doesn't afford us syntactic color coding, it provides us with a degree of immediate responsiveness and the ability to see all messages passed during operations instead of just fail or pass state messages. Note that we have provided you syntactic color coding in this tutorial as it, generally, makes the code more readable.
To import packaged into a specific Python environment, you need only use the 'import' command.
```console
C:\>python
Python 3.6.7 (v3.6.7:6ec5cf24b7, Oct 20 2018, 13:35:33) [MSC v.1900 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import numpy
>>>
```
We are also able to give packages nicknames, really useful so we don't have to type out matplotlib or tensorflow thousands of times.  We assign these nicknames by "importing as".
```console
>>> import matplotlib.pyplot as plt
>>>
```
And finally, we import Tensorflow and its Keras interface. Note that we can always call Keras as a Tensorflow object (i.e. tf.keras.command() ), but that takes too much typing. To save us time, we will import Keras from Tensorflow.
```console
>>> import tensorflow as tf
>>> from tensorflow import keras
>>>
```
All of our prerequisite packages are now installed!

*Leave a comment after you have imported the libraries above for the next step.*
