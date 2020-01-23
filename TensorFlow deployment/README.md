# TensorFlow Android Camera Demo

This folder contains an example application utilizing TensorFlow for Android
devices.

## Description

The demos in this folder are designed to give straightforward samples of using
TensorFlow in mobile applications.

Inference is done using the [TensorFlow Android Inference
Interface](../../tools/android/inference_interface), which may be built
separately if you want a standalone library to drop into your existing
application. Object tracking and efficient YUV -> RGB conversion are handled by
`libtensorflow_demo.so`.

A device running Android 5.0 (API 21) or higher is required to run the demo due
to the use of the camera2 API, although the native libraries themselves can run
on API >= 14 devices.

![alt text](https://jalammar.github.io/images/android-tensorflow-app-structure_2.png "Logo Title Text 1")

### Installation Steps

If you already have Android Studio, skip to Step 5!

#### Step 1 Download Android studio

https://developer.android.com/studio/index.html

#### Step 2 Download Android SDK

`$ wget https://dl.google.com/android/android-sdk_r24.4.1-linux.tgz
$ tar xvzf android-sdk_r24.4.1-linux.tgz -C ~/tensorflow`

#### Step 3 Download SDK Build Tools

`$ cd ~/tensorflow/android-sdk-linux
$ tools/android update sdk --no-ui`

#### Step 4 Download Android NDK

`$ wget https://dl.google.com/android/repository/android-ndk-r12b-linux-x86_64.zip
$ unzip android-ndk-r12b-linux-x86_64.zip -d ~/tensorflow`

Set correct SDK and NDK versions in your workspace file

#### Step 5 Train Model in Python on your desktop or a server 

#### Step 6  Convert Mask rcnn model to Tensorflow .pb Using Freeze_Session.ipynb

#### Step 7  Navigate to the android\assets directory. Copy and Paste your frozen_inference_graph.pb file from the inference_graph folder in your object_detection API directory.
#### Step 8 File<open android. In left-side navigation panel, open the java<org.tensorflow.demo<DetectorActivity.java file. The file uses the Tensorflow Object Detection API by default. In lines 66–67 replace:


“file:///android_asset/ssd_mobilenet_v1_android_export.pb”; private static final String TF_OD_API_LABELS_FILE = “file:///android_asset/coco_labels_list.txt”; 

with

“file:///android_asset/frozen_inference_graph.pb”; private static final String TF_OD_API_LABELS_FILE = “file:///android_asset/labels.txt”;
#### Step 9 Connect your Android device to the computer and enable USB debugging. Once you build the Android APK, it will install all Tensorflow demo applications. Open the “TF Detect” app and test it out! 


