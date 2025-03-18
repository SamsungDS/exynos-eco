# Pose Estimation In Android
This document describes a method to operate Android sample application using the [Posenet mobilenet](https://prd.ai-studio-farm.com/kr/solution/ai/models/detail/f40473cb-a6e6-42a3-a50a-daf428273eab) model that is optimized for Exynos hardware.

## Functionality
This application detects key points in images that are either from stored image files or those captured through the camera and automatically measures joint positions.
Additionally, the inference time is displayed at the bottom of the application interface.

## Getting Started
Perform the following steps to utilize the sample application:
1.	Download or clone the sample application from this repository.
2.  If there is no device available to run the application, you can use the actual devices provided in the Device Farm.
    For more information on connecting a device to Android Studio, refer to ADB Client Proxy.
3.  Use adb push command to push a sample image to the following path for testing.
4.  Select Tools → Device Manager in Android Studio. Please verify whether the physical device is properly connected.
5.  Run the depth estimation project from the sample applications obtained through git clone in Android Studio.
6.  Upload the image data for inference and execute the application.

Perform the following steps to modify the model used in the sample application:
1.	Copy the desired model file to the `assets` directory within the project.
2.	Modify the parameters in the ModelConstants.kt file to reflect the specifications of the new model.
3.	If the inputs and outputs of the model differ from the pre-designed sample application, modify the `preProcess()`, `postProcess()` and `convertBitmapToFloatArray()` functions.

## Compatible AI Models
Currently there are no supported models.
Later, if any new models are registered and are expected to be compatible with the sample application, we will update them here.