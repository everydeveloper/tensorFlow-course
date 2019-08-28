## Evaluating Our Model
Now we are working with a functional and trained NN model. Following our logic from the top, we have built a NN that intakes a (28,28) array, flattens the data into a (784) array, compiled and trained 2 dense layers, and the softmax activation function of the final output layer will provide a probability that the image belongs to each of the 10 label categories.
Our model can be evaluated by using the model.evaluate command, that takes in the images and labels so that it can compare its predictions to the ground truth provided by the labels. Model.evaluate provides two outputs, the value of the loss function over the testing examples, and the accuracy of the model over this testing population. The important output for us is the model's accuracy.
```console
>>> test_loss, test_acc = model.evaluate(test_images, test_labels)
10000/10000 [==============================] - 0s 27us/sample - loss: 0.3543 - acc: 0.8721
>>> print(test_acc)
0.8721
>>>
```
This is great! Our model performs at an accuracy of 87.21%. As good as that is, it is lower than the model accuracy promised above (89.01%). This lower performance is due to the model overfitting on the training data. Overfitting occurs when there are too many parameters within the model when compared to the number of training instances; this allows the model to over learn on those limited examples. Overfitting leads to better model performance over non-training data.

That said, 87.21% is a decent number!  Let's finally learn how you can feed our model the series of test examples from the test_images array, and have it provide its predictions. 
```console
>>> predictions = model.predict(test_images)
>>> predictions[0]
array([5.1039719e-04, 1.4324225e-07, 6.3209918e-06, 1.4587535e-07,
       7.1591121e-06, 3.9024312e-02, 3.2491367e-05, 9.4579764e-02,
       1.8918892e-05, 8.6582035e-01], dtype=float32)
```
As we can see, most of the entries in our prediction array are very close to 0. The entry that stands out is predictions[0][9]  at .8658, or 86.58%, certainty that this image should be classified as a boot! This happens to be true and can be check by you if you repeat the code above to visualize test_images[0].

If you prefer to not look through a list to determine the class label, we can simplify the output by:
```console
>>> numpy.argmax(predictions[0])
9
>>>
```
Finally, we can verify this prediction by looking at the label ourselves:
```console
>>> test_labels[0]
9
>>>
```

*To complete this course, leave a comment with the letter (A,B,C,D) that best answers the following question:*

In the prediction array generated by our model:
```
>>> predictions = model.predict(test_images)
>>> predictions[0]
array([5.1039719e-04, 1.4324225e-07, 6.3209918e-06, 1.4587535e-07,
       7.1591121e-06, 3.9024312e-02, 3.2491367e-05, 9.4579764e-02,
       1.8918892e-05, 8.6582035e-01], dtype=float32)
```
_each number_ represents: 

A. The probability that the image is a boot
B. Average pixle values (between 0 and 1)
C. The probability that the image matches the corresponding label in our set of labels
D. The accuracy of our model