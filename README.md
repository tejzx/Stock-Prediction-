# Stock-Prediction-
This ML model demonstrates the stock prediction of  Google between 2013 to 2023. 
 Outputs:
![Screenshot (235)](https://github.com/user-attachments/assets/73102222-d3d3-4202-ab7b-a584b99cd9c7)
![Screenshot (231)](https://github.com/user-attachments/assets/2a45d61a-261b-4267-ace0-84edc4eb73ac)
![Screenshot (237)](https://github.com/user-attachments/assets/e1afe4e4-ccd5-4a4e-8fba-f562767396b1)
![Screenshot (236)](https://github.com/user-attachments/assets/1d764d1d-0854-4e9c-bba9-74aecdd5e3a5)
![Screenshot (234)](https://github.com/user-attachments/assets/cc4567b2-3d27-47b2-b36d-80dd1470da80)
![Screenshot (233)](https://github.com/user-attachments/assets/8f98460a-f778-4200-a254-1d2cb13f37fd)
![Screenshot (232)](https://github.com/user-attachments/assets/b301aee4-997e-489f-8b07-148fffd65f63)
![Screenshot (230)](https://github.com/user-attachments/assets/56639d7c-c567-4a05-931b-e6c9de5ed69d)
![Screenshot (229)](https://github.com/user-attachments/assets/49360f77-8e3f-48e0-9d96-343f7015e068)
![Screenshot (228)](https://github.com/user-attachments/assets/a6582c7e-76e6-4467-ac89-5b7c36bbb715)

 Libraries like numpy, pandas, matplotlib, and yfinance are imported for data processing, visualization, and  costing stock 
 data. 
 The scikit- learn library is used for data scaling(  latterly in the script). 
 Stock Data Retrieval 
 
 Stock data for the ticker" GOOG"( Google) is downloaded using yfinance for the date range from January 1, 2013, to December 
 21, 2023. 
 Data Preprocessing 
 
 The stock data is reset to include the date as a standard column. 
 Missing values are dropped to  insure clean data for analysis. 
 Visualization of Moving Averages 
 
 100- day and 200- day moving  pars are calculated for the stock's  ending price. 
 These moving  pars are colluded along with the  factual  ending prices for trend visualization. 
 Data unyoking 
 
 The dataset is  resolve into training( 80 of the data) and testing( 20 of the data) sets grounded on the  ending prices. 
 Data spanning 
 
 The  ending prices are gauged  using MinMaxScaler to  homogenize the data for machine  literacy models( not completely 
 visible in the  grain). 
 Data spanning 
 
 The training data is gauged  between 0 and 1 using MinMaxScaler to  regularize the input for the LSTM model. 
 Sequence Preparation 
 
 Input sequences( x) of 100 time  way and corresponding target values( y) are created from the gauged  training data. 
 This sliding window approach ensures the model can learn temporal patterns. 
 Deep Learning Framework 
 
 TensorFlow and Keras libraries are used to design and train the prophetic  model. 
 LSTM Model Architecture 
 
 The LSTM model is constructed as follows:
 Input Subcaste Accepts sequences of 100 time  way with one  point each. 
 retired Layers 
 Four LSTM layers with  adding  units( 50, 60, 80, 120) and ReLU activation. Each subcaste except the last has 
 return_sequences =  True to pass the sequences to the coming subcaste. 
 Powerhouse layers are added after each LSTM subcaste to reduce overfitting, with powerhouse rates ranging from 20 to 50. 
 Affair Subcaste A thick subcaste with a single neuron to  prognosticate the  ending price for the coming time step. 
 The model is  collected using the Adam optimizer and mean squared error( MSE) loss. 
 Training 
 
 The model is trained on the  set sequences( x and y) for 50 ages with a batch size( not visible yet, likely 32 or 64). 
