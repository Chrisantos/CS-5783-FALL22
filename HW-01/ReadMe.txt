Dependencies:

- Numpy
- Pandas
- Matplotlib
- Seaborn

Please check the notebook for a more detailed report.

Question 1: 

- Linear Regression was implemented using gradient descent
- Dataset relationship is not linear
- Discovered that the model have a linear relationship to the dataset and does not capture its non-linearity
- Added basis functions such as the 2nd, 3rd, and 4th order polynpmial to capture the non-linearity
- Including basis functions captured the non-linearity and improved performance.


Question 2:

- It was observed that the weight of a feature tells us about the importance of the feature to the model. The farther away the weight is from zero,
the more important it is, while the closer it is to zero, the less important.
- Hence, "Local Price" gave the most importance, while "Age of home" gave the least importance.
- Using only "Local Price" didn't diminish the performance considerably.
- Result of the model improved after the "Age of home" was removed.


Question 3:

- No basis function was required since the model captured the non-linearity of the data.
- The locally weighted linear regression implementation is different from the Iterative Linear Regression in Question 1 in the following ways:
    - To make each label prediction, the weights for each point to be predicted has to be computed.
    - This leads to high computation costs, but removes the overhead of having to use basis functions to engineer a model that would fit the non-linear data.
