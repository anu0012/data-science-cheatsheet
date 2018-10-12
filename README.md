# Data Science CheatSheet

* [A](#a)

# A

## Accuracy - 
Accuracy is the measure of a classification model. It is a ratio of correctly predicted observations to the total observations.

## Activation Function -
Activation functions are used to provide non-linear properties to the neural network. It is applied to the weighted sum of the inputs of a neuron in a neural network.

### What is the need of non-linearity - 
Neural-Networks are considered Universal Function Approximators. That's why we need an activation function which allows our model to approximate any function.

The main terminologies needed to understand for nonlinear functions are:
###Derivative or Differential: 
Change in y-axis w.r.t. change in x-axis.It is also known as slope.
###Monotonic function: 
A function which is either entirely non-increasing or non-decreasing.

###Why derivative/differentiation is used ? -
When updating the curve, to know in which direction and how much to change or update the curve depending upon the slope.That is why we use differentiation in almost every part of Machine Learning and Deep Learning.

## Some Activation Functions:
###Sigmoid or Logistic Activation Function
The Sigmoid Function curve looks like a S-shape. The main reason why we use sigmoid function is because it exists between (0 to 1). Therefore, it is especially used for models where we have to predict the probability as an output.Since probability of anything exists only between the range of 0 and 1, sigmoid is the right choice.The function is differentiable.That means, we can find the slope of the sigmoid curve at any two points.

The function is monotonic but function’s derivative is not.

The logistic sigmoid function can cause a neural network to get stuck at the training time.

###Tanh or hyperbolic tangent Activation Function
tanh is also like logistic sigmoid but better. The range of the tanh function is from (-1 to 1). tanh is also sigmoidal (s - shaped).The advantage is that the negative inputs will be mapped strongly negative and the zero inputs will be mapped near zero in the tanh graph.

The function is differentiable.

The function is monotonic while its derivative is not monotonic.

The tanh function is mainly used classification between two classes.

###ReLU (Rectified Linear Unit) Activation Function
The ReLU is the most used activation function in the world right now. It is used in almost all the convolutional neural networks or deep learning.

###f(z) = max(0, z)

The ReLU is half rectified (from bottom). f(z) is zero when z is less than zero and f(z) is equal to z when z is above or equal to zero.

Range: [ 0 to infinity)

The function and its derivative both are monotonic.

But the issue is that all the negative values become zero immediately which decreases the ability of the model to fit or train from the data properly. That means any negative input given to the ReLU activation function turns the value into zero immediately in the graph, which in turns affects the resulting graph by not mapping the negative values appropriately.

### Leaky ReLU
It is an attempt to solve the dying ReLU problem.

f(z) = az, z<0

f(z) = z,  z>0

The leak helps to increase the range of the ReLU function. Usually, the value of a is 0.01 or so.
