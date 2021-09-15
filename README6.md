# Machine Learning Overview

<H3>softmax function</H3>

- for items with one unique class
- the range will be 0 to 1
- the sum of all probabilities is one
-
<H3>Cost Function</H3>

- C(W,B,S,E) ; W -weight, B - bias ,S - input of single training sample, E - disired output

- minimize a cost function -> which means what value of w results in the minimum of C(W)
- we will use gradient descent
- until it converge to zero - searching for the minimum
- step size is the learning rate
- "Adaptive Gradient Descent" - smaller step size as it approches zero
- Adaptive gradient descent - Adam performs better
- gradient is another way of calling derivative
- cross entropy loss function - for classification problems
- backpropagation is to update weights and biases
- from the last error, we calculate the error, biases and weights accordingly and minimize the cost function 
- that is the gist

- z <sup>L</sup>=w<sup>L</sup>a<sup>L-1</sup> + b<sup>L</sup>
- a<sup>L-1</sup> = sigmoid(z <sup>L</sup>) # sigmoid is gradient I think
- C<sub>0</sub> = (a<sup>L-1</sup> -y)<sup>2</sup>
- error vector
-  delta<sup>L</sup>=Delta<sub>a</sub>C. sigmoid'(Z<sup>L</sup>)

<H3>Keras Syntax</H3>

```
import panda as pd
import numpy as np
import seaborn as sns
df = pd.read_csv('../DATA/fake_reg.csv')
```
- df.head
- sns.pairplot(df)
- from sklearn.model_selection import train_test_split #this will split the data into training set and test set
- X = df[['feature1','feature2']].values
- y = df['price'].values
- train_test_split (tab twice)
- train_test_split .....
- X_train.shape # returns the size of the training set
- X_test.shape # for test set
- should normalize and scale
- from sklearn.preprocesssing import MinMaxScaler
- help (MinMaxScaler)
- we just need to scale the feature
- scaler = MinMaxScaler()
- scaler.fit(X_train)
- X_train = scaler.transfrom(X_train)
- X_test = scaler.transform(X_test)
- Next we will create neurons 
- from tensorflow.keras.models import Sequential
- from tensorflow.keras.layers import Dense
- help(Sequential)
- model = Sequential ([Dense(4,activation='relu'),Dense(2, activation='relu'),Dense(1)])
- the preferred one is as follow
```
 model = Sequential()
 model.add(Dense(4,activation='relu'))
 model.add(Dense(2,activation='relu'))
  model.add(Dense(1))
  model.compile()
    ```
    - I will stop this here and go to CNN
- 
