## Training the Model
Models must be both compiled and trained prior to use.  When compiling we must define a few more parameters that control how models are updated during training (optimizer), how the model's accuracy is measured during training (loss function), and what is to be measured to determine the model's accuracy (metrics). These values were selected for this project, yet are generally dependent on the model's intent and expected input and output.
```console
>>> model.compile( optimizer = 'adam', loss = 'sparse_categorical_crossentropy', metrics = ['accuracy'])
>>>
```
Now we can begin training our model! Now, with already having generated and compiled the model, the code required to train the model is a single line.
```console
>>> model.fit(train_images, train_labels, epochs=5)

2019-08-24 22:56:32.884249: I tensorflow/core/platform/cpu_feature_guard.cc:142] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2
Epoch 1/5
60000/60000 [==============================] - 2s 40us/sample - loss: 0.4985 - acc: 0.8264
Epoch 2/5
60000/60000 [==============================] - 2s 36us/sample - loss: 0.3787 - acc: 0.8632
Epoch 3/5
60000/60000 [==============================] - 2s 36us/sample - loss: 0.3368 - acc: 0.8766
Epoch 4/5
60000/60000 [==============================] - 2s 35us/sample - loss: 0.3122 - acc: 0.8863
Epoch 5/5
60000/60000 [==============================] - 2s 35us/sample - loss: 0.2962 - acc: 0.8901
<tensorflow.python.keras.callbacks.History object at 0x00000133F219C470>
>>>
```
This single line completes the entire job of training our model, but let's take a brief look at the arguments provided to the model.fit command. The first argument is input data, and recall that our input Flatten layer takes a (28,28) array, conforming to the dimensionality of our images. Now we train the system by providing the correct classification for all the training examples, this is the second argument of the model.fit command. The final argument is the number of epochs undertaken during training; each epoch is a training cycle over all the training data.  Our setting the epoch value to 5 means that the model will be trained overall 60,000 training examples 5 times. After each epoch, we get both the value of the loss function and the model's accuracy (88.97% after epoch 5) at this epoch.

*Leave a comment with the answer to this question:*

_Which argument in the model.fit method is used to classify our data into categories?(1,2, or 3)?_