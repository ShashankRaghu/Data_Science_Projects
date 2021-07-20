# Dow Jones Stock Price Prediction using Reddit News Headlines
## This is project looks to build a model which reads news headlines of a certain day, and predicts the movement dow jones industrial average.

- ### The dataset used in this project can be downloaded from this [Kaggle link](https://www.kaggle.com/aaron7sun/stocknews).
- ### The DowJones dataset contains the dow jones price values of a particular day, for this project we will be only looking at the open price. We will subtract the dow jones of next day from current day, to get the price change.
- ### The various headlines is the input, the price difference is the output. We have normalized the output.
- ### We have decontracted the words, and removed unwanted characters from the headlines.
- ### We have used Glove embeddings to intialize the weights, we have changed the rare words which are not available in Glove to <UNK> token. We have also, fixed the limit of day's news to 200 words, and length of any headline to 16 words.
- ### We have used a CNN-RNN model, with 1 embedding layer, 2 CNN layer, 1 RNN layer. The optimzer is Adam, loss is mean_squared_error. The final model has 0.0073 validation loss.
