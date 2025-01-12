# IMUNet: Efficient Regression Architecture for IMU Navigation and Positioning

This is the Python implementation for the Paper: [IMUNet](https://arxiv.org/abs/2208.00068)

A new Architecture called IMUNet which is appropriate for edge-device implementation has been proposed for processing IMU measurements and performing inertial navigation. 

In this repository, the data-driven method for inertial navigation proposed in [here](https://github.com/Sachini/ronin) for the ResNet18 model has been modified.
Other than ResNet18, four state-of-the-art CNN models that have been designed for IoT device implementation have been reimplemented for inertial navigation and IMU sensor processing. 

# Architectures
Other than IMUNet, MobileNet, MobileNetV2, MnasNet, and EfficientNetB0 models have been re-implemented to work with one-dimensional IMU mesurements. 

# Dataset
Five datasets have been used in the paper.
* A new method for collecting a dataset using Android cellphones that uses [ARCore API](https://developers.google.com/ar/reference) for collecting the ground truth trajectory has been proposed and a dataset using this method along with the method proposed in [RIDI](https://github.com/higerra/ridi_imu) using a Lenovo Tango device for collecting the ground truth trajectory has been collected. A preprocessing step has been added to read and prepare the data. The collected dataset can be downloaded from [IMUNet_dataset](https://www.dropbox.com/s/lm5fbym7azjn5ws/IMUNet_dataset.zip?dl=0).

Other datasets are:

1- RONIN which is available at [here](https://ronin.cs.sfu.ca/) 

2- RIDI which is available at [DropBox](https://www.dropbox.com/s/9zzaj3h3u4bta23/ridi_data_publish_v2.zip?dl=0)  

3- OxIOD: The Dataset for Deep Inertial Odometry which is available at [OxIOD](http://deepio.cs.ox.ac.uk/ )   

4- Px4 which can be downloaded from [px4](https://px4.io/)  and the scripts provided [here](https://github.com/majuid/DeepNav) has been used to download the data and pre-process it. 

# Keras Implementation
The data-driven method for inertial navigation proposed in [RONIN](https://github.com/Sachini/ronin) for the ResNet18 model with all the new architectures and datasets as well as the proposed architecture have been implemented in Tensorflow-Keras. 

# Android
The Android Application is available at [Android](https://github.com/BehnamZeinali/IMUNet_Android). 
It contains three sections: 

1- The application for collecting a new dataset.

2- The test part of the [RONIN](https://github.com/Sachini/ronin) for ResNet18 model using all the proposed models and some samples of the collected dataset.

3- A comparison has been implemented to show the efficiency and accuracy of the proposed model. The result can be seen in the video below:  


https://user-images.githubusercontent.com/29498989/181649816-e1adcb44-e899-445e-b1a0-f2467a0030dc.MP4


