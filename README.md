# GrabChallenge
The Grab_v3 files can be divide into two parts:
  - Model building
  - Prediction
This two parts can be executed independently. A series of models files pre-trained are also uploaded in this repository.
Please unzip it before start the prediction. There is another .pkl file uploaded, which is for the purpose of storing number of inputs used for pre-trained model. For each unique geohash in the training dataset, there are a correspond model, and a dictionary stored in .pkl file is used to stored the relevant parameters that used during the training. 
