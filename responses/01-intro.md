# Basics of TensorFlow Tutorial Using Fashion MNIST
![clothes dataset images]({{repoUrl}}/raw/master/img/clothes.png)
*Figure 1 [Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist) samples (by Zalando, MIT License).*

## Introduction
Machine learning (ML)/Neural Network (NN) tools have recently made a huge splash with applications in data analysis, image classification, and data generation. Although ML methods have existed for decades, recent advancements in hardware have generated systems powerful enough to run these algorithms.

The typical "hello world" example for ML is a classifier trained over the MNIST dataset; a dataset of the handwritten digits 0-9. This dataset is getting a little stale and is no longer impressive with employers as a proof of capability due to both its seeming simplicity and to the plethora of existing tutorials on the topic. Here we will use a newer dataset to perform our ML "hello world", the Fashion MNIST dataset!

The Zeroth Step of ML (that should be completed before ever putting a hand to mouse, or finger to key) is understanding the format and sizes of your data. This step is often referred to as feature engineering. Feature engineering, typically, includes selecting and preprocessing the particular aspects of training data to give to your algorithm. You and I will start a good habit of examining the data and its format to make decisions concerning the appropriate size and format for our NN.

The Fashion MNIST dataset is comprised of 70,000 grayscale images of articles of clothing. The greyscale values for a pixel range from 0-255 (black to white). Each low-resolution image is 28x28 pixels and is of exactly one clothing item. Alongside each image is a label that places the article within a category; these categories are shown in Figure 2 with an example image belonging to the class.

![detail view of clothing categories]({{repoUrl}}/raw/master/img/clothesDetails.png)
*Figure 2 class numbers are shown next to image labels*

_This is an interactive tutorial where you will be prompted to do something at the end of each step. Sometimes you need to refresh the browser before the bot will respond._

*Enter a comment (TRUE or FALSE) about the following statement:*

_"Before starting a machine learning project, you often need to select and process some of the data"_