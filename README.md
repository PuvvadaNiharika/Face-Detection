# Face-Detection
Certainly! Here’s a `README.md` file tailored for your `FaceRecognitionVideo` Java application. This file provides an overview of the project, installation instructions, and usage details.

---

# FaceRecognitionVideo

## Overview

The `FaceRecognitionVideo` Java application is a simple tool for capturing video frames from a webcam, detecting faces in those frames using OpenCV, and displaying the results in a JavaFX application. It also provides functionality to save the processed images to disk.

## Requirements

1. **Java Development Kit (JDK):** Make sure you have JDK 8 or later installed on your machine.
2. **JavaFX SDK:** Ensure that the JavaFX SDK is properly set up in your project.
3. **OpenCV Library:** The application uses the OpenCV library for face detection. You need to have the OpenCV native libraries available and correctly configured.
4. **OpenCV Cascade Classifier XML:** The application requires a pre-trained face detection model (cascade classifier) in XML format. The path to this file should be correctly specified.

## Setup

### 1. Install Dependencies

- Download and install OpenCV. Follow the OpenCV installation guide for your operating system:
  - [OpenCV Installation Guide](https://docs.opencv.org/4.x/d7/d9f/tutorial_linux_install.html)

- Download the JavaFX SDK if not already installed:
  - [JavaFX SDK Download](https://gluonhq.com/products/javafx/)

### 2. Configure Your Project

- **Add OpenCV and JavaFX libraries to your project.** Ensure that the native OpenCV libraries are available in your system's library path.

- **Set up the OpenCV and JavaFX libraries:**
  - In your IDE or build tool (e.g., Maven, Gradle), include dependencies for JavaFX and OpenCV.

### 3. Set Up the Cascade Classifier

- Download or create a pre-trained face detection model (XML file) using OpenCV. Place this file in an accessible location and update the path in the `FaceRecognitionVideo` class.

## Running the Application

1. **Compile the Application:**

   ```bash
   javac -cp "path/to/opencv.jar;path/to/javafx-sdk/lib/*" myproject/FaceRecognitionVideo.java
   ```

2. **Run the Application:**

   ```bash
   java -cp "path/to/opencv.jar;path/to/javafx-sdk/lib/*;." -Djava.library.path="path/to/opencv/native/libs" myproject.FaceRecognitionVideo
   ```

   Make sure to replace `path/to/opencv.jar`, `path/to/javafx-sdk/lib/*`, and `path/to/opencv/native/libs` with the actual paths on your system.

## Code Description

- **`FaceRecognitionVideo` class**: Contains the main functionality of the application.
  - **`start(Stage stage)`**: Initializes and displays the JavaFX application window with the captured and processed image.
  - **`captureFrame()`**: Captures a video frame from the webcam, detects faces using OpenCV, draws rectangles around detected faces, and converts the frame to a `WritableImage`.
  - **`saveImage()`**: Saves the processed image to a specified location.
  - **`main(String args[])`**: Entry point of the application, which launches the JavaFX application.

## Troubleshooting

- **Camera not detected:** Ensure that the camera is properly connected and accessible by other applications.
- **Library issues:** Verify that all library paths and dependencies are correctly configured.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [OpenCV](https://opencv.org/) for face detection capabilities.
- [JavaFX](https://openjfx.io/) for creating the graphical user interface.

