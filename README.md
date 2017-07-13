# SelfDrivingCar_CNN
## Introduction
This is an application of [Convolution Neural Network](https://en.wikipedia.org/wiki/Convolutional_neural_network) which is trained to drive a car. The very first problem in having to build such a model is to have a dataset to train the model, this in itself was a very tedious task which was not so practical until recently when the games were used to collect the artificial data. This project uses one such [simulator](https://github.com/udacity/self-driving-car-sim) by [Udacity](https://www.udacity.com) for their **Self-Driving Car Nanodegree** (cheers to **Udacity** for opening thier simulator and the wrapper programs to set up the simulator for everyone to use).

The model to train the *CNN* is built using [Keras](https://keras.io) with [Tensorflow](https://www.tensorflow.org) at the back-end, hence it's a no brainer that we need these two librarires for the project, other than these some of the other librarires include **opencv3** (for image transformations), **PIL** (for loading, saving and basic manipulation). Also one cool aspect (which was done by udacity by default) is the [Client-Server model](https://en.wikipedia.org/wiki/Client–server_model) between the simulator and my python scripts, so that one can control the car in the simulator with the ouput genrated by the python scripts. An exhaustive list of all the dependencies can be found in the *yml* files in the **src**.

The model implemented for the self driving car in **src** is the model proposed by **NVIDIA** in thier research work [End-to-End Deep Learning for Self-Driving Cars](https://devblogs.nvidia.com/parallelforall/deep-learning-self-driving-cars/) It consists of **9 layers** the first being the layer performing normalisation, the next **5** being the *convolutional layers* and **3** *fully connected layers* there is also an intermediate layer to flaateen out the state matrix after all the convolutional layes and there is a final fully connected layer, which gives just one output (the steering angle).

## Some Analysis
Certain subtle issues and analysis of the data is discussed in this [blog post](https://udionblog.wordpress.com)(coming soon) by me.
