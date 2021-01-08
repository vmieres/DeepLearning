# DeepLearning
![](https://thumbor.forbes.com/thumbor/fit-in/1200x0/filters%3Aformat%28jpg%29/https%3A%2F%2Fblogs-images.forbes.com%2Fbernardmarr%2Ffiles%2F2018%2F10%2FAdobeStock_179912599-1-1200x797.jpeg)

# **Deep Learning**
 In this repo I am using deep learning recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the closing price while the second model will use a window of closing prices to predict the nth closing price.

 ### **Preparing the data for training and testing**
 - For the closing price model, I used previous closing prices to try and predict the next closing price.
 - For the Fear and Greed model, I used the FNG values to try and predict the closing price.
 - For each model used 70% of the data for training and 30% of the data for testing.
 - Applied a MinMaxScaler to the X and Y values to scale the data for the model.
 Lastly, reshaped the X_train and X_test values to fit the model's requirement of samples, time steps, and features. 
  (example: X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1)))
 
 ### **Building and Training custom LSTM RNNs**
 In each Notebook, I created the same custom LSTM RNN architecture. In one notebook, I fitted the data using the FNG values. In the other notebook, I fitted the data using only closing prices.

 
 ### **Evaluating the performance of each model**
Finally, use the testing data to evaluate each model and compare the performance.

Use the above to answer the following:

- Which model has a lower loss? - RNN CLosing Prices 
- Which model tracks the actual values better over time? - RNN Closing Prices 
- Which window size works best for the model? - window size = 5