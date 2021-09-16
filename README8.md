# CNN on CIFAR-10
- CIFAR-10 dataset are 32by32 image of 10 different objects

```
import panda as pd
import numpy as np

import matplotlib.pyplot as plt
%matplotlib inline
from tensorflow.keras.datasets import cifar10
```

- (x_train, y_train),(x_test,y_test) = cifar10.load_data()
- x_train.shape
- x_train[0].shape
- plt.imshow(x_train[12])
- x_train[0].max()
- x_train=x_train/255
- x_test = x_test/255
- x_test.shape
- y_train
- from tensorflow.keras.utils import to_catetegorical
- y_cat_train = to_categorical(y_train, 10)
- y_cat_test = to_categorical(y_test, 10)
- plt.imshow(x_train[0])
- copy and pasting
- 6:31 
