# Steering Angle Prediction Project in Autonomous Vehicles using C-LSTM Neural Network

**Abstract**

Deep Learning has been a trending topic, and its evolution has had a significant impact on the automotive industry. Driving a
car through traffic is a challenging task, and automating that involves very complex models built, as the decision of steering
and human life’s are dependent on it. Different Deep Learning architectures are applied to predict the steering angle in
the Autonomous Vehicle (AVs). A survey was conducted on the researches that have been implemented in the steering
angle prediction. It is found that most researches depends on Convolution Neural Network (CNN) over other Deep Learning
architectures in predicting the steering angle of autonomous driving vehicles1. This project uses Convolution Long Short-term
memory Neural Network (ConvLSTM)to train the machine learning model to predict the accurate steering angle and increase
the performance by considering the temporal relation between the input images.
The project involves securing the data from the front cameras (Left, Centre, and Right) of the car as input and processing the
steering angle prediction. The traditional approach of Convolution Neural Network involves matrix multiplication. This approach
only considers the Visual camera frames as input and thus ignoring the temporal relationship between the images2. This
relationship between the images will improve the efficiency of predicting the steering angle. The ConvLSTM Neural Network
combines a CNN (Convolutional Layers) and an LSTM, replacing matrix multiplication with convolution operations at each gate
in the LSTM cell3, which will give more accurate results over the traditional CNN prediction of steering angle.
The regression problem solved with Convolutional Long Short Term Memory approach is an improved version of the traditional
Convolutional Neural Networks approach and improves the steering angle prediction accuracy when the data contains noise
and less useful information. As the Long Short Term Memory architecture stores the past information and uses that information
along with current to predict the steering angle it has improved control accuracy of the steering.
