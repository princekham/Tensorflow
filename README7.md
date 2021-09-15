# Convolutional Neuro Network

<H3>Image Filter </H3>
``` 
import panda as pd
import numpy as np

import matplotlib.pyplot as plt
%matplotlib inline
```
to get the MNIST data set,
- from tensorflow.keras.datasets import mnist
- (x_train,y_train),(x_test,y_test)=mnist.load_data()
- single_image = x_train[0]
- single_image.shape
- plt.imshow(single_image) #for showing 2D 
- y_train # but still we need to tell tensorflow that this is classification problem
- from tensorflow.keras.utils import to_categorical
- y_example = to_categorial(y_train)
- we will transform test and to categorical
- y_cat_test= to_categorical(y_test, num_classes=10)
- y_cat_train = to_categorical(y_train,10)
- time to normalize the training data
- to keep value between 0 and 1
- x_train = x_train/255
- x_test = x_test/255
- scaled_image= x_train[0]
- scaled_image.max()
- plt.imshow(scaled_image)
- x_train.shape
- we still add to one more dimension - black and white
- x_train=x_train.reshape (60000,28,28,1) #batch_size, width, height, color_channels
- x_test = x_test.reshape(10000, 28,28,1)
<H3>Training and Creating a model </H3>

- from tensorflow.keras.models import Sequential
- from tensorflow.keras.layers import Dense,Conv2D,MaxPool2D, Flatten
- model = Sequential()
- model.add(Con2D(filters= 32,kernel_size=(4,4), input_shape=(28,28,1),activation='relu'))
- model.add(MaxPool2D(pool_size=(2,2)))
-  
