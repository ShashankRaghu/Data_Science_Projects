# Gesture Recognition Project
## This project deals with developing a model which takes a video(30 frames) of a hand gesture as input and classify it into one of 5 gestures.

* ### The dataset can be downloaded from this [drive](https://drive.google.com/uc?id=1ehyrYBQ5rbQQe6yL4XbLWe3FMvuVUGiL).
* ### We have build a generator to set up the data ingestion pipeline, we have perpormed image pre-processing techniques.
* ### We have build several 3D CNN models, and tuned the hyper parameters; learning rate, optimizer used etc.
* ### We have tried Batch Normalization, Dropout and some other techniques to arrive at the best model.
* ### The best model is a 5 layer CNN model with relu activation function, Batch Normalization, Dropout, optimizer: RMSProp and learning rate: 0.005.
