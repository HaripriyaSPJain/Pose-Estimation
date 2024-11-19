# TensorFlow Lite Pose Estimation Android Demo

### Overview
This is an app that continuously detects the body parts in the frames seen by
your device's camera. These instructions walk you through building and running
the demo on an Android device. Camera captures are discarded immediately after
use, nothing is stored or saved.

The app demonstrates how to use 3 models:

* Single pose models: The model can estimate the pose of only one person in the
input image. If the input image contains multiple persons, the detection result
can be largely incorrect.
   * PoseNet
   * MoveNet Lightning
   * MoveNet Thunder
     
![WhatsApp Image 2024-11-19 at 19 01 37_5a8b1a26](https://github.com/user-attachments/assets/ac3466da-0b17-4e9a-9b70-9df030a3d6a2)
![WhatsApp Image 2024-11-19 at 19 01 37_d21bdf86](https://github.com/user-attachments/assets/1bb829fa-bc3e-4be1-95a1-8d9532858e30)



## Build the demo using Android Studio

### Prerequisites

* If you don't have it already, install **[Android Studio](
 https://developer.android.com/studio/index.html)** 4.2 or
 above, following the instructions on the website.

* Android device and Android development environment with minimum API 21.

### Building
* Open Android Studio, and from the `Welcome` screen, select
`Open an existing Android Studio project`.

* From the `Open File or Project` window that appears, navigate to and select
 the `lite/examples/pose_estimation/android` directory from wherever you
 cloned the `tensorflow/examples` GitHub repo. Click `OK`.

* If it asks you to do a `Gradle Sync`, click `OK`.

* You may also need to install various platforms and tools, if you get errors
 like `Failed to find target with hash string 'android-21'` and similar. Click
 the `Run` button (the green arrow) or select `Run` > `Run 'android'` from the
 top menu. You may need to rebuild the project using `Build` > `Rebuild Project`.

* If it asks you to use `Instant Run`, click `Proceed Without Instant Run`.

* Also, you need to have an Android device plugged in with developer options
 enabled at this point. See **[here](
 https://developer.android.com/studio/run/device)** for more details
 on setting up developer devices.


### Model used
Downloading, extraction and placement in assets folder has been managed
 automatically by `download.gradle`.

If you explicitly want to download the model, you can download it from here:

* [Posenet](https://storage.googleapis.com/download.tensorflow.org/models/tflite/posenet_mobilenet_v1_100_257x257_multi_kpt_stripped.tflite)
* [Movenet Lightning](https://kaggle.com/models/google/movenet/frameworks/tfLite/variations/singlepose-lightning)
* [Movenet Thunder](https://www.kaggle.com/models/google/movenet/frameworks/tfLite/variations/singlepose-thunder)
* [Movenet MultiPose](https://www.kaggle.com/models/google/movenet/frameworks/tfLite/variations/multipose-lightning-tflite-float16)

