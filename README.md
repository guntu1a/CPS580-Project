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

**Dataset**

The data set used for this project was acquired from Sully Chen’s Github repository(https://github.com/SullyChen/driving-datasets). It was curated by Sully Chen, who is a Researcher at The National Institutes of Health. With a passion for learning and implementing machine learning, he took up a
college project named Tensor Flow Auto Pilot. He did reverse engineering on the signal system for his own car’s CANBUS
interface to collect the labeled driving data and implemented the acquired data to published paper6. Driving data includes a
sequence of images from his car’s front dash camera and the steering angle at each image while driving.
A typical camera captures 30 frames per second. Since we have 45,406 images from the front dash camera images, the data
is captured approximately 25 minutes of video, and it is broken down into each frame image. The data set images, and the
respective steering angle in degrees is maintained in the data.txt file. If we see the file for the first 22 temporal frames, the angle
is 0.0 degrees, which means that the steering is maintained straight. To reduce the big numbers representing the steering angle,
we convert them from degrees to radians.
The whole data, 45,406 images, cut to 3000, is divided into training data, validation data, and test data by considering the
temporal relation in the frames. The first 60 percent of data is split into training data, the next 20 percent is split into validation
data, and the remaining 20 percent is used as test data. The test data will not be used while training the data, and validation data
is used as a signal to tune the hyperparameters and monitor the training.
The data set has each image frame of 256x455 length and width to keep the same aspect ratio; all the input images are
resized to 66 x 200. These images are resized using the scipy library and visualized using the matplotlib library.
