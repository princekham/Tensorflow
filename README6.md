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
- a<sup>L-1</sup> = sigma(z <sup>L</sup>) # sigma is gradient I think
- C<sub>0</sub> = (a<sup>L-1</sup> -y)<sup>2</sup>
