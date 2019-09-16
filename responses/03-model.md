*Nailed it!* 

Remember, the label arrays are only used to associate images with their lables.

## Model Generation
Every NN is constructed from a series of connected layers that are full of connection nodes. Simple mathematical operations are undertaken at each node in each layer, yet through the volume of connections and operations, these ML models can perform impressive and complex tasks. 

Our model will be constructed from 3 layers. The first layer – often referred to as the Input Layer – will intake an image and format the data structure in a method acceptable for the subsequent layers.  In our case, this first layer will be a Flatten layer that intakes a multi-dimensional array and produces an array of a single dimension, this places all the pixel data on an equal depth during input. Both of the next layers will be simple fully connected layers, referred to as Dense layers, with 128 and 10 nodes respectively. These fully connected layers are the simplest layer in the sense of understanding, yet allow for the greatest number of layer-to-layer connections and relationships.

The final bit of hyper-technical knowledge you'll need to learn is that each layer can have its own particular mathematical operation. These activation functions determine the form and relationship between the information provided by the layer. The first dense layer will feature a Rectified Linear Unit (ReLU) Activation Function that outputs values between zero and 1; mathematically, the activation function behaves like f(x)=max(0,x). The final layer uses the softmax activation function. This function also produces values in the 0-1 range, BUT generates these values such that the sum of the outputs will be 1!  This makes the softmax a layer that is excellent at outputting probabilities.

```console
>>> model = keras.Sequential([ keras.layers.Flatten(input_shape=(28,28)), keras.layers.Dense(128, activation=tf.nn.relu), keras.layers.Dense(10, activation=tf.nn.softmax)])

WARNING: Logging before flag parsing goes to stderr.
W0824 22:50:02.551490  8392 deprecation.py:506] From C:\Users\ross.hoehn\AppData\Local\Programs\Python\Python36\lib\site-packages\tensorflow\python\ops\init_ops.py:1251: calling VarianceScaling.__init__ (from tensorflow.python.ops.init_ops) with dtype is deprecated and will be removed in a future version.
Instructions for updating:
Call initializer instance with the dtype argument instead of passing it to the constructor
>>>
```

*Enter a comment (TRUE or FALSE) about the following statement:*

_The softmax activation function will generate values which will add up to 1_