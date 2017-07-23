# Behavioral Cloning


The goals / steps of this project are the following:

Use the simulator to collect data of good driving behavior
Build, a convolution neural network in Keras that predicts steering angles from images
Train and validate the model with a training and validation set
Test that the model successfully drives around track one without leaving the road

My project includes the following files:

model.ipynb containing the script to create and train the model
drive.py for driving the car in autonomous mode
model.h5 containing a trained convolution neural network
writeup_report.md  summarizing the results

##### Submission includes functional code Using the Udacity provided simulator and my drive.py file, the car can be driven autonomously around the track by executing

python drive.py model.h5
####3. Submission code is usable and readable

The model.ipynb file contains the code for training and saving the convolution neural network. The file shows the pipeline I used for training and validating the model, and it contains comments to explain how the code works.

### Model Architecture and Training Strategy

##### Architecture
My model consists of a convolution neural network with 3x3 filter sizes and depths between 24 and 64 (model.ipynb ln 5)

The model includes RELU layers to introduce nonlinearity, and the data is normalized in the model using a Keras lambda layer.

##### Attempts to reduce overfitting in the model

The model was trained and validated on different data sets to ensure that the model was not overfitting. The model was tested by running it through the simulator and ensuring that the vehicle could stay on the track.

##### Model parameter tuning

The model used an adam optimizer, so the learning rate was not tuned manually.

##### Appropriate training data

Training data was chosen to keep the vehicle driving on the road. I used a combination of center lane driving, recovering from the left and right sides of the road, usin the left and right camera data. 


####1. Solution Design Approach

My first step was to use a convolution neural network model similar to the Nvidia model. I thought this model might be appropriate because ...

In order to gauge how well the model was working, I split my image and steering angle data into a training and validation set. I found that my first model had a low mean squared error on the training set but a high mean squared error on the validation set. This implied that the model was overfitting.

To combat the overfitting, I modified the model by using the images available from both left and right camera. I also normalized the data before trainign. Furthermore, I collected more data from both driving paths available in the simulator 


At the end of the process, the vehicle is able to drive autonomously around the track without leaving the road.



