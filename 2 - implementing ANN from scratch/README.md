## Artificial Neural Network in Python: Multilayer Perception from scratch

This code implements 3-layer artificial neural network with **Sigmoid** activation function based on the follwoing chart:

* **X** - input vector
* **W** - 2x3 Matrix of input weights
* **h** - Sum of weighted inputs, or dot product between x and W: **xW**
* **f(x)** - Activation function, Sigmoid function in this case
* **a** - Ativated net input **h**: **a**=**f(h)**
* **Y** - Final output

![alt text](https://github.com/paabes/AudioSignal-Deep-Learning/blob/main/2%20-%20implementing%20ANN%20from%20scratch/figures/1.png)

* Activated input obtained at the end of the 2nd layer then gets transformed into **h(3)** - a weighted sum of activated inputs. For obtaining the final output , **h(3)** is passed through the activation function:


![alt text](https://github.com/paabes/AudioSignal-Deep-Learning/blob/main/2%20-%20implementing%20ANN%20from%20scratch/figures/2.png)
 
