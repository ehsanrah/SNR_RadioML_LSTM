This repository implements a CLDNN using recurrent neural network to classify the modulation of time-series data as one of ten possible
modulation types. The given code file imports the high SNR data, which is already split into
a training and testing set. Ensure that the data files accompanying this project (X_train.npy,
Y_train.npy, X_test.npy, and Y_test.npy) are in the same directory as your Python script. 
Model architecture is as follows:

• Input layer: a 2x128x1 signal
• First hidden layer: a 2-dimensional convolutional layer with 256 feature maps and a 1x3
filter size with a 20% dropout rate
• Second hidden layer: a 2-dimensional convolutional layer with 256 feature maps and a
2x3 filter size
• Third hidden layer: a 2-dimensional convolutional layer with 80 feature maps and a 1x3
filter size with a 20% dropout rate
• Fourth hidden layer: a 2-dimensional convolutional layerwith 80 feature maps and a 1x3
filter size
• Reshape the data to be two-dimensional instead of three-dimensional
• Fifth hidden layer: An LSTM layer with 50 cells
• Sixth hidden layer: a dense (fully-connected) layer consisting of 128 perceptrons
• Output layer (classification probabilites): 10 perceptrons
• Train your model using 200 epochs