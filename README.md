# Stock-Prediction-
 This ML model demonstrates the stock prediction of  Google between 2013 to 2023. 

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
