Dependencies:

- Numpy
- Pandas
- Matplotlib
- Tensorflow
- Sklearn

Please check the notebook for a more detailed report.

Question 1:

1.1 
During the course of this experiment, I tried tuning the model by varying the hyperparameters. The hyperparameters I tried include:

- Epochs = 15, 20, 25, 30
- Batch sizes = 128, 64, 64, 32
- Optimizers = Adam with lr of 0.001, SGD with lr of 0.001, Adam with lr of 0.005, and finally Adam with lr of 0.01

Of these hyperparamters that were tried, the following combinations gave the bet performance with an accuracy of 99.33% 

Optimizer: SGD 
Learning rate: 0.001 
Batch size: 64 
Epochs: 20

We note that the performance was due to the combinations of the different hyperparameters. Here we used a batch size of 64 and learning 
rate of 0.001 which gave a way better performance than using a combination of 0.01 learning rate, epoch of 30, and batch size of 32. 
The latter combination prevented the training from converging before the training ended since the learning rate which controls the 
update made to the weights is large and hence perhaps bounced around global minima and didn't converge before the training ended, 
hence producing a poor performance.

1.2 
During the course of this experiment, I tried tuning the model by varying the hyperparameters. The hyperparameters I tried include:

- Epochs = 15, 20, 25, 30
- Batch sizes = 128, 64, 64, 32
- Optimizers = Adam with lr of 0.001, SGD with lr of 0.001, Adam with lr of 0.005, and finally Adam with lr of 0.01

The performance of this model is also similar to the previous one given that they had similar hyperparameters and number of neurons.

Of these hyperparamters that were tried, the following combinations gave the bet performance with an accuracy of 99.30% 

Optimizer: SGD 
Learning rate: 0.001 
Batch size: 64 
Epochs: 20

Just like in the previous model, we note that the performance was due to the combinations of the different hyperparameters. 
Here we used a batch size of 64 and learning rate of 0.001 which gave a way better performance than using a combination of 0.01 
learning rate, epoch of 30, and batch size of 32. The latter combination prevented the training from converging before the training 
ended since the learning rate which controls the update made to the weights is large and hence perhaps bounced around global minima 
and didn't converge before the training ended, hence producing a poor performance.

1.3
Just like in the previous variants of the model above, I tried tuning the model using varying hyperparameters. 
The hyperparameters I tried include:

- Epochs = 15, 20, 25, 30
- Batch sizes = 128, 64, 64, 32
- Optimizers = Adam with lr of 0.001, SGD with lr of 0.001, Adam with lr of 0.005, and finally Adam with lr of 0.01

The hour-glass shaped CNN also gave some interesting results. We can see that the following hyperparameters gave the best performance 
with an accuracy of 99.27%.

Optimizer: SGD 
Learning rate: 0.001 
Batch size: 64 
Epochs: 20

It can be noted that this performance is due to the combination of the hyperparameters especially the learning rate and the batch size. 
I also observe a consistent poor performance using the last hyperparameter combinations of Adam optimizer, 0.01 learning rate, 
32 batch size, and 30 epochs. It can be noted that this could be due to the learning rate and the batch size.


Question 2:

2.1
As can be seen from the plots in the notebook, the model's performance on the training data was best with an accuracy of approx. 75%. 
However, at this same learning rate on the test data, we can see that the accuracy dropped to 38.32% although it still remained 
the learning rate with the best performance even on the test data. This large difference between the accuracy on the training and 
test data shows that the model might have gotten overfitted to the training data. Therefore, to optimize the model and find the 
right balance, more tuning of the hyperparameters needs to be done.

2.2
As can be seen from the results in the notebook, the number of batch size is directly proportional to the performance of the model, 
however it fluctuated at certain batch sizes (64 and 80). The model trained on a batch size of 128 gave the best performance with an 
accuracy of 32.77%.

2.3 
Below are the details of the lenet hyperparameters that gave the best accuracy of 63.68% on the test data.

Optimizer: SGD
Learning rate: 0.001
Batch size: 64
Epochs: 20

The following is a list of the combinations of hyperparameters with their accuracies on the test data:

Adam optimizer, 0.001 learning rate, 128 batch size, and 15 epochs with an accuracy of 62.9%
Adam optimizer, 0.005 learning rate, 64 batch size, and 25 epochs with an accuracy of 59.6%
Adam optimizer, 0.01 learning rate, 32 batch size, and 30 epochs with an accuracy of 10%

2.4a
The feed forward network model produce an accuracy of 0.1 (10%) and a loss of 2.31, while the leNet model produced an accuracy of 
0.41 (41%) and a loss of 1.69 which is 4x the performance of for the model for the feed forward network.

2.4b
From the result gotten from the summary functions of the two networks, we can see that the feedforward network has 31,604 params and 
the LeNet model has 62,006 params which is clearly bigger. However, CNN architectures show way greater performance compared to regular 
feed forward networks (almost 4 times the performance of the feedforward network) and hence are better for image classification tasks 
and are completely worth it.


Question 3:
Please check the notebook for the detailed answers to this question

3.1
The kernel has 10 parameters

3.2
[[ 16   9  -4 -18]
 [ 17  -5 -10 -12]
 [ 11  -9 -17   2]
 [  9  -1 -15  16]]

3.3
[[17 -4]
 [11 16]]