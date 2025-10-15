## Real-Time Hand Gesture and Indian Sign Language Recognition using CVZone

### Overview

This Python project utilizes the CVZone library for real-time hand gesture and Indian Sign Language (ISL) recognition. The code detects hand gestures captured through a webcam and classifies them into predefined categories. The system supports directional gestures ("Down", "Up", "Right", "Back", "Left", "Front"), alphabet letters (A-Z), and specifically Indian Sign Language alphabet gestures. The hand gestures are detected using computer vision techniques and classified using a pre-trained model from Google's Teachable Machine. 

![Real Time Detection](real-time-detection(cvzone).jpg)

### Requirements

- Python 3.x
- OpenCV (cv2)
- CVZone
- NumPy
- Math module

### Setup

1. Ensure you have Python installed on your system.
2. Install the required libraries using pip:

   ```bash
   pip install opencv-python cvzone numpy
   ```

3. Download the pre-trained model and labels file (keras_model.h5 and labels.txt) from the Google Teachable Machine platform or another suitable source.
4. Place the downloaded files in the same directory as the Python script.

### Usage

#### For Indian Sign Language (ISL) Detection:
1. Run `indian_sign_language_detection.py` or `simple_isl_detection.py` for ISL recognition.
2. Ensure that your webcam is connected and functioning properly.
3. A window will open displaying the live webcam feed with ISL recognition overlay.
4. Show Indian Sign Language gestures for letters A-Z in front of the webcam.
5. The recognized letter will be displayed on the screen along with gesture descriptions.
6. Hold each letter gesture for a few seconds to add it to the current word.
7. Press 'h' to toggle help screen with gesture descriptions.
8. Press 'c' to clear the current word, 'q' to quit.

#### For General Alphabet Detection:
1. Run `simple_alphabet_detection.py` or `alphabet_detection.py` for general alphabet recognition.
2. Ensure that your webcam is connected and functioning properly.
3. A window will open displaying the live webcam feed with alphabet recognition overlay.
4. Show hand gestures for letters A-Z in front of the webcam.
5. The recognized letter will be displayed on the screen along with a bounding box around the detected hand.
6. Hold each letter gesture for a few seconds to add it to the current word.
7. Press 'c' to clear the current word, 'q' to quit.

#### For Original Gesture Detection:
1. Run `cvzone_real_time_detection.py` for directional gesture recognition.
2. Ensure that your webcam is connected and functioning properly.
3. A window will open displaying the live webcam feed with hand gesture recognition overlay.
4. Perform hand gestures in front of the webcam.
5. The recognized gesture will be displayed on the screen along with a bounding box around the detected hand.

### Scripts Description

#### `indian_sign_language_detection.py`
An advanced ISL detection script with:
- Object-oriented design for better organization
- ISL-specific gesture descriptions and help system
- Smooth prediction with confidence thresholds
- Automatic word building with timing controls
- Enhanced UI with cultural context and gesture guidance
- Help screen with detailed ISL gesture descriptions

#### `simple_isl_detection.py`
A straightforward ISL detection script that:
- Detects Indian Sign Language gestures for letters A-Z
- Builds words by holding letter gestures
- Shows confidence levels and prediction counts
- Includes ISL gesture descriptions
- Help screen toggle functionality
- Word clearing functionality

#### `simple_alphabet_detection.py`
A straightforward alphabet detection script that:
- Detects hand gestures for letters A-Z
- Builds words by holding letter gestures
- Shows confidence levels and prediction counts
- Includes word clearing functionality

#### `alphabet_detection.py`
An advanced alphabet detection script with:
- Object-oriented design for better organization
- Smooth prediction with confidence thresholds
- Automatic word building with timing controls
- Enhanced UI with multiple information displays

#### `cvzone_real_time_detection.py`
The original gesture detection script for directional movements.

### Technical Details

The scripts use CVZone, an open-source computer vision library, for hand detection and classification. They capture video input from the webcam and process it frame by frame. The HandDetector class from CVZone is used to detect hands in the video stream, while the pre-trained model loaded using the Classifier class is employed to classify the hand gestures.

#### Important Components:

- **Hand Detection**: The HandDetector class is used to find hands in each frame of the video stream. It returns the bounding box coordinates of the detected hands.
- **Gesture Classification**: The pre-trained model loaded from 'keras_model.h5' and 'labels.txt' is used to classify the hand gestures. The model predicts the label corresponding to each detected hand gesture.
- **Image Preprocessing**: The captured hand region is resized and aligned to a standard size before being fed into the classification model.
- **Visualization**: The recognized gesture label and a bounding box around the detected hand are overlaid onto the video feed for visualization purposes.
- **Word Building**: For alphabet detection, the system tracks consecutive predictions to build words from individual letter gestures.
- **ISL Support**: Specialized support for Indian Sign Language with cultural context and gesture descriptions.
- **Help System**: Interactive help screens with detailed gesture descriptions and usage tips.

### Indian Sign Language (ISL) Features

- **Cultural Context**: Gestures designed specifically for Indian Sign Language standards
- **Gesture Descriptions**: Built-in descriptions for each ISL alphabet gesture
- **Help System**: Press 'h' to toggle detailed gesture reference guide
- **Accessibility**: Designed to be inclusive and accessible for the deaf community
- **Reference Guide**: Comprehensive `ISL_Gesture_Reference_Guide.md` with detailed instructions

### Dataset

The dataset used to train the hand gesture recognition model can be found on Kaggle at the following link: [Hand Gesture Recognition Dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet).

For Indian Sign Language specific datasets, consider:
- **ISLTranslate**: A dataset for translating Indian Sign Language
- **IIITA-ROBITA ISL Gesture Database**: Contains 23 different ISL gestures
- **Static Gestures of ISL**: Includes static hand gestures for English alphabets

### Credits

- CVZone: [GitHub Repository](https://github.com/cvzone/cvzone)
- Google Teachable Machine: [Platform](https://teachablemachine.withgoogle.com/)

For any questions or feedback, please contact [sousannahabdalla@gmail.com].
