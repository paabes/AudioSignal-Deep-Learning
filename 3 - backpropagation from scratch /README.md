## Training ANN: Backpropagation and Gradient Descent From Scratch

**Loss Function E(p,y)** is defined as a deviation of predicted values from actual values, where:
* **p**: Predicted value
* **y**: Actual value

![alt text](https://github.com/paabes/AudioSignal-Deep-Learning/blob/main/3%20-%20backpropagation%20from%20scratch%20/figures/loss.png)

However, Predicted value **p** is itself a function of input vector **x** and input weight matrix **W**, hence, for easiaer differentiability, loss function **E(p,y)** can be expressed as a functional- a function of another function:
 
![alt text](https://github.com/paabes/AudioSignal-Deep-Learning/blob/main/3%20-%20backpropagation%20from%20scratch%20/figures/loss%20functional.png)

By varying input weights one can tune the predicted values to be arbitrarily closer to actual values, this would entail minimizing a gradient of loss function along the input weights, in the opposite direction of the gradient. In calulus terms, this quantity would be expressed as a partial derivative of loss function **E(p,y)** with respect to the input weights **W**:

![alt text](https://github.com/paabes/AudioSignal-Deep-Learning/blob/main/3%20-%20backpropagation%20from%20scratch%20/figures/gradient.png)

By substituting loss function **E(p,y)** with its' extended form **E(f(x,W),y)** and applying chain rule, derived functions with respect to W1 and W2 will be the following:

![alt text](https://github.com/paabes/AudioSignal-Deep-Learning/blob/main/3%20-%20backpropagation%20from%20scratch%20/figures/result.png)

This code is the final, in the 3-part project of re-implemening artificial neural networks from scratch to better understand how they work. This part extends the **MultiLayerPerception**() class implemented in the stage 2 and attempts to:

* save activations and derivatives
* implement backpropagation
* implement gradient descent
* create train method that uses backpropagation and gradient descent
* train network with a dummy dataset
* make test predictions







