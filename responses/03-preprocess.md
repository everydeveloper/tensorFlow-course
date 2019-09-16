## Preprocessing the dataset
The greyscale assigned to each pixel within an image has a value range of 0-255. We will want to flatten (smoosh… scale…) this range to 0-1. To achieve this flattening, we will exploit the data structure that our images are stored in, arrays.  You see, each image is stored as a 2-dimensional array where each numerical value in the array is the greyscale code of particular pixel. Conveniently, if we divide an entire array by a scalar we generate a new array whose elements are the original elements divided by the scalar.

```console
>>> train_images = train_images / 255.0
>>> test_images = test_images / 255.0
>>>
```

Two vital notes about the above.
 
1. Use the value "255.0". This value is a floating point number (float), and will always return a float during algebraic operations. In Python, the division operator always returns a float to avoid rounding; but, that is not true for all programming languages, so it's a good habit to include that decimal because it automatically sets that number to be a float. 
2. Do not rescale the train_labels or test_labels arrays, these values are already in the range 0-9, as they should be!

*Enter a comment (TRUE or FALSE) about the following statement:*

_We need to rescale both the images and labels, so they are on the same scale._