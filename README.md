# Repository for the AKTIVES Dataset 2022

## Description

This is a supplementary repository for the Emognition AKTIVES Dataset 2022 presented in the article titled "AKTIVES dataset: stress recognition with physiological signals".
Necessary libraries are in [requirements.txt](https://github.com/hiddenslate/aktives-scientific-data/blob/main/requirements.txt).

The AKTIVES dataset is 5.41 GB in size. In the dataset, there are four disease categories in the first index. These categories are Brachial Plexus, Dyslexia, Intellectual Disabilities, and Typically Developed. There are two children in the Brachial Plexus category, five children in the Dyslexia category, eight in the Intellectual Disabilities category, and ten in the Typically Development category. CatchAPet and LeapBall game folders are in the children's folders in each category. Then there are 7 files belonging to the child in both game folders. There are 14 files for a child in total. These files have the following content:

- **Three label files:** Label files annotated by each expert. The files are named "ExpertNumber.csv" and the data is in csv format.
- **Video file:** Contains video footage recorded during the game. It is in mp4 format.
- **Game file:** There are game-related parameters collected during the game. It is stored in json format.
- **E4 file:** It is the file where the physiological data collected from the E4 device during the game is stored. It is stored in txt format.
- **Facial expression files:** These are csv files that include each child's automatically detected facial expressions.
**Note: Video footage can only be used for analysis purposes and must not be shared anywhere.**

The contents of each notebook are given below.
* [Label_Sync.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/Label_Sync.ipynb) compares the three expert labels with each other and selects the label with the majority of votes for use.
* [preprocess.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/preprocess.ipynb) includes converting time values into DateTime, removing unnecessary data parts, separating data as Blood Volume Pulse (BVP), Electrodermal Activity (EDA), and Skin Temperature (ST), and filtering and visualization of the signals.
* [SignaltoNoiseRatio(SNR).ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/SignaltoNoiseRatio(SNR).ipynb) calculates the signal-to-noise ratio (SNR) [3] of the physiological signals and their statistical features.
* [Annotation_Validation.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/Annotation_Validation.ipynb) calculates the agreement percentages of the expert annotations.
* [Aktives-face.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/Aktives-face.ipynb) detects facial expressions with the FER library [1] and detects facial landmarks with DLIB shape predictor [2].

## Project Configuration

* Install Python (at least 3.9 version is recommended),
* Setup your environment (venv, conda, etc.) and install dependencies from requirements.txt

[1] https://pypi.org/project/fer/

[2] http://dlib.net/face_landmark_detection.py.html

[3] https://github.com/psychosensing/popane-2021/blob/main/scripts/snr.py
