## MLHandDetection Documentation

This repository contains a basic iOS application built with Xamarin.iOS that utilizes CoreML and Vision frameworks for hand detection in images. The application employs a pre-trained CoreML model (`HandDetectionModel.mlmodel`) to classify images and identify the presence of hands.

### Inputs

- **Image data:** The application takes image data as input, either captured from the device's camera or loaded from the photo library.

### Outputs

- **Classification results:** Upon processing the input image, the application provides classification results indicating the presence or absence of hands in the image, along with a confidence score.
- **Alert message:** The results are displayed to the user through an alert message, showing the identified class label (e.g., "HAND") and the confidence level. 

### Usage

The application offers two ways to provide input images:

1. **Real-time camera feed (if ARKit is supported):** If the device supports ARKit, the application displays a live camera feed. Tapping on the screen captures the current frame and performs hand detection.

2. **Image from library (if ARKit is not supported):** On devices without ARKit support, the application provides an interface to choose an image from the photo library. Tapping the screen prompts the user to select an image for hand detection.

Once the input image is processed, an alert message is displayed with the classification results.

### Notes

- The application utilizes a compiled version of the CoreML model (`HandDetectionModel.mlmodelc`) for performance reasons.
- The confidence score ranges from 0 to 1, representing the model's certainty about the classification. A higher score indicates greater confidence.
- This documentation provides a general overview of the code's functionality and usage. Detailed implementation details can be found within the code comments.