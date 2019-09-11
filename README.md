# ObjectDetectorAndroidJava

One of the exciting feature announced by Android is TensorFlow. TensorFlow is an end-to-end open source platform for machine learning.

App gets the current frames from the camera and it uses this frame to get predictions using the SSD-Mobilenet model trained using the Tensorflow Object Detection API.


A device running Android 5.0 (API 21) or higher is required to run the demo due to the use of the camera2 API.


Requirement
- NDK (if you have not installed you can download it from here : https://developer.android.com/ndk/downloads)
- Tensorflow (if you have not installed you can download it from here : https://www.tensorflow.org/install)

Here how to use it
- OverlayView callback is used when object is tracked, which returns Canvas. So draw that canvas in camera preview.
```
trackingOverlay.addCallback(
        new OverlayView.DrawCallback() {
          @Override
          public void drawCallback(final Canvas canvas) {
            tracker.draw(canvas);
          }
        });
```

Output:

![alt text](https://github.com/1986webdeveloper/ObjectDetectorAndroidKotlin/blob/master/ezgif-4-0c8fe35564d4.gif)
