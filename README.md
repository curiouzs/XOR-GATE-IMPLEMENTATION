### EX NO : 08
### DATE  : 16.05.22
# <p align="center"> XOR GATE IMPLEMENTATION </p>
## Aim:
To implement multi layer artificial neural network using back propagation algorithm.
## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## Related Theory Concept:
Logic gates using neural networks help understand the mathematical computation by which a neural network processes its inputs to arrive at a certain output. This neural network will deal with the XOR logic problem. An XOR (exclusive OR gate) is a digital logic gate that gives a true output only when both its inputs differ from each other.

The information of a neural network is stored in the interconnections between the neurons i.e. the weights. A neural network learns by updating its weights according to a learning algorithm that helps it converge to the expected output. The learning algorithm is a principled way of changing the weights and biases based on the loss function.


## Algorithm
1. Import the required libraries.
2. Create the training dataset.
3. Create the neural network model with one hidden layer.
4. Train the model with training data.
5. Now test the model with testing data.
<br />
<br />
<br />

## Program:
```python
/*
Program to implement XOR Logic Gate.
Developed by   : Lokesh Krishnaa M
RegisterNumber :  212220230030
*/
import numpy as np
from keras.models import Sequential
from keras.layers.core import Dense


training_data=np.array([[0,0],[0,1],[1,0],[1,1]],"float32")
target_data=np.array([[0],[1],[1],[0]],"float32")
model=Sequential()
model.add(Dense(16,input_dim=2,activation='relu'))
model.add(Dense(1,activation='sigmoid'))
model.compile(loss='mean_squared_error',optimizer='adam',metrics=['binary_accuracy'])
model.fit(training_data,target_data,epochs=1000)
scores=model.evaluate(training_data,target_data)
print("\n%s: %.2f%%" % (model.metrics_names[1],scores[1]*100))
print(model.predict(training_data).round())

```

<br />
<br />
<br />
<br />
<br />

<br />
<br />
<br />
<br />
<br />

<br />
<br />

<br />
<br />
<br />
<br />
<br />


## Output:
![Screenshot (15)](https://user-images.githubusercontent.com/75234646/168518291-ffea8d92-0644-4301-8c38-a74c6302cd53.png)
![xor](https://user-images.githubusercontent.com/75234646/169733551-60f42181-76b8-4d06-b89e-06ada7b525b3.jpg)

## Result:
Thus the python program successully implemented XOR logic gate.
