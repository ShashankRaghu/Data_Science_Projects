# Parts of Speech Tagger
## To build a model which can predict the parts of speech of a sentence

- ### The dataset used is from the NLTK corpora, which contains sentences, and POS of each word.
- ### The sentences are converted to intergers using Tokenizer() function of Keras.
![POSTagger](https://user-images.githubusercontent.com/77088516/126310867-b375f2e7-fc8c-4618-a350-e2bd3e29dc8e.PNG)
- ### We have further padded the sentences to 100 words, by using pre padding and post truncating.
- ### We have also, used word embeddings from word2vec to transform the training sentences, and we have used one hot encoding for the 13 unique POS output.
- ### The word embedding created is of size 300, and we have build models with and without embedding to check their effectiveness.
- ### We have build 3 vanilla RNN models(10 epochs), with 'adam' optimizer, 'categorical_crossentropy' loss, and 'accuracy' metric:
  - ### Without fixed embeddings: validation accuracy of 0.9587, validation loss of 0.1229.
  - ### With uninitialized embeddings: validation accuracy of 0.9893, validation loss of 0.0359.
  - ### With pre-trained word2vec embeddings: validation accuracy of 0.9907, validation loss of 0.0301.
- ### We further build 3 more models with word2vec embedding(10 epochs): LSTM, GRU and Bi directional LSTM. The accuracy of all for models on test data can be se below:
![POSTagger2](https://user-images.githubusercontent.com/77088516/126312413-1683f5bc-132a-408a-98c2-58c2834c5514.PNG)
