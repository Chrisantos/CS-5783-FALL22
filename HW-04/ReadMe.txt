Dependencies:

- Numpy
- Pandas
- Matplotlib
- Sklearn
- Pillow

Please check the notebook for a more detailed report.

Question 1:

1.1 The answer for this question can be found in Q1_answer.pdf

1.2 The probabilities for the examples in the test data are in the notebook.

Question 2:

2.1a The accuracy on the training set is 1.0
2.1b The accuracy on the test set is 0.4

2.2 Increasing the maximum depth leads to the model overfitting as seen in the plots in the notebook. As can be seen, the two plots start 
to diverge at max depth = 2.

2.3 Decision trees tend to overfit when max depth is high. As seen in the previous plot, the training error is zero from a max depth of 5, 
which means that the variance is high.

2.4 The path is outlined using the red arrows on the image below. And the class is Apartment. To load the image, kindly move the 
Q4_answer.png image to your Drive folder (the usual folder you place the data file). 

Question 3:

The plot in the notebook shows that there is a very high variance at lesser values of k which results to the model overfitting to the 
training data. The variance reduces as the value of k is increased. Predictions on test was constant from k = 2 to k = 8, before it 
dropped and then started increasing at k = 10. The best accuracy gotten on the test data is 60%.