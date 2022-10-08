Dependencies:

- Numpy
- Pandas
- Matplotlib

Please check the notebook for a more detailed report.

Question 1:

- The derivation of the update rule is in the pdf attached named "Backprop.df"

- And the update rule for this regression problem is different because:
It uses an identity activation function at the output layer since it is a regression problem, 
while a sigmoid activation function is used for the logloss since it is for classification problems. 
The logloss is used to predict discrete values, meanwhile regression problems require continous value outputs, 
hence the need for mean squared error.

Question 2:

1. I would use an identity/linear activation function at the output since it requires a continous value output and not 
the prediction or probability of occurrence which classification problems usually require for the output.

2. There should be only one neuron at the output layer since we are predicting a single continous value.

3. Please check the notebook for the average loss and accuracy

4. Please check the notebook for these plots

5. 
- The learning rate speeds up the time it takes for the training to converge. 
But if a very large learning rate is used, the model might keep bouncing around the global minima 
and never converge (or takes too much time to converge). And if is too small, it takes too much time to converge. 
In otherwords, its important to select a learning rate that would be just right for the training process.

- As can be seen, the accuracy is best with a low learning rate, and then fluctuates until it starts dropping when 
it approaches 1. This is to say that the model started bouncing around the global minima and found it difficult to 
converge as a result of the large learning rate

6. 
a. The update rule does not need to be recomputed since it does not take into account the number of neurons in each layer, 
just as it does not also take into account the number of inputs and outputs in the network. However, the dimensions need to 
be updated to ensure the matrix multiplications works.

b. The above plots show that increasing the number of neurons could improve the performance of the model as it would 
allow it capture more information in the data. However, it could start to overfit when it goes beyond a certain threshold, 
so care should be taken when selecting the number of neurons to be used in a neural network to avoid running into the 
risk of having an underfitting or overfitting. Also, as can be seen in the accuracy vs number of neurons plot, 
the model's peformance was almost constant when the number of neurons was between 5 and 6, then dropped between 6 and 7, 
before shouting up between 7 and 8.

7. Activation function determines the neurons that would be activated and how the input is transformed into an output. 
Essentially, it can help introduce non-linearity to the network (when a linear or identity activation function is not used).

a. Since the update rule is based on the value of g(Zi) and g'(Zi), a change in the value would require a change in the update rule as well when computing the gradients. However, mathematically, we don't need to alter our equations since g(Zi) and g'(Zi) signify an arbitrary activation function and its derivative.

b. For this experiment, I will be using the Tanh and the ReLu activation functions, and their derivatives need to 
be computed and used in the backpropation algorithm instead of the derivative of the sigmoid function. 
These functions and their derivatives have been implemented at the top of the notebook.

c. From the results above, we can see that there was a decrease in the train loss and train accuracy when the 
Tanh function was used as compared to the sigmoid function. However, the test loss and test accuracy increased for 
the Tanh function from the values for the sigmoid function.

In the case of linear activation function, we experienced an overflow due to its inability to capture the non-linearity in the network.
