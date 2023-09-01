Relu 
ReLU (Rectified Linear Unit) is an regression activation function commonly used in neural networks to add non linearity properities in our network. 

<img src="https://github.com/k17hawk/deep-Learning-beginner/blob/main/Screenshot%20from%202023-08-31%2019-21-05.png"/>

It addresses some of the issues associated with sigmoid and tanh activation functions.
The problem associated with sigmoid was, it was not zero centric, due to which it fluctuates during deviation, and takes long time in convergence which could consume high resources.


<img src="https://github.com/k17hawk/deep-Learning-beginner/blob/main/vanish.drawio%20(1).png"/>



Another  problem was because of derivative of sigmoid which ranges from (0, 0.25).During backpropagation the updated weight will be quite similar to new weight evantually leading to vanishing gradient problem.


<img src="https://github.com/k17hawk/deep-Learning-beginner/blob/main/Picture1.png"/>





Tanh is zero centric but face same problem as sigmoid which is vanishing gradient problem.


<img src="https://github.com/k17hawk/deep-Learning-beginner/blob/main/tanh.png"/>






Relu is zero centric (0,y). It’s derivative lies between (0,1) because any negative values are changed to 0 and non negative value to 1, solving the problem of  vanishing gradient.

<img src="https://github.com/k17hawk/deep-Learning-beginner/blob/main/ReLU-activation-function-and-its-derivative.png"/>



But relu comes with the problem of dead neuron. There could be scenario when Relu(z) = 0. 
This happens, if the input to a Relu neuron is always negative, leading to zero gradients during backpropagation, preventing weight updates.
To solve this issue we have varient of Relu called Leaky relu which has a small, non-zero slope for negative inputs </br>
if x > 0: </br>
     relu = x </br>
else: </br>
    relu = alpha*x </br>
alpha is a small positive constant (typically very close to zero, e.g., 0.01)

