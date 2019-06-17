# GrabChallenge
The Grab_v3 files can be divide into three parts:
  - Import data
  - Model training
  - Prediction

# Import data
  The input file are as per stated in following link: https://s3-ap-southeast-1.amazonaws.com/grab-aiforsea-dataset/traffic-management.zip
The input file path can be changed by alter the variable TRAINING_FILE_PATH in the main execution block. 

# Training
  The model pre-trained is using LinearRegression. There are also other algorithms been tried during the development, such as LSTM, RandomForecastRegressor, GradientBoostingRegressor, and ARIMA. However, linear regression is chosen in this case due to its is faster, leser memory consumption while at the same time provide similar or better results compared to other algorithms.

# Prediction
  Prediction can be executed seperately. A series of pre-trained models files are also uploaded in this repository. There is another .pkl file uploaded, which stores number of inputs used for pre-trained model. For each unique geohash in the training dataset, there are a correspond model, and a dictionary with key-values pair of geohash - number of inputs are stored in .pkl file. This will be used to extract and transform the testing data for prediction.

To start the prediction, please download all the required files, and ensure all of them are in the same directory as per the .ipynb file.
Prediction can be executed by calling the predict method, by providing the TESTING_FILE_PATH & MODEL_FILE_PATH. Please adjust the TESTING_FILE_PATH & MODEL_FILE_PATH accordingly. The predict method will return a dictionary of geohash - predicted values of 5 time steps. 


