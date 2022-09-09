# aktives-scientific-data

## Description

This is a supplementary repository for the Emognition Wearable Dataset 2020 and article titled
AKTIVES dataset: stress recognition with physiological signals.

Necessary libraries are in [requirements.txt](https://github.com/hiddenslate/aktives-scientific-data/blob/main/requirements.txt).

The AKTIVES dataset is 5.41 GB in size. In the dataset, there are four disease categories in the first index.
These categories are Brachial Plexus, Dyslexia, Mental Retardation, and Normal Development. There are two children in the Brachial Plexus category, five children in the Dyslexia category, 8 children in the Mental Retardation category and 10 children in the Normal Development category.
There are CatchAPet and LeapBall game folders in the folders of the children in each category. Then there are 6 files belonging to the child in both game folders. There are 12 files for a child in total. These files have the following content:

- Three label files: Label files made by each expert. The files are in csv format.
- Video file: It belongs to the client images recorded during the game. It is in mp4 format.
- Game file: There are game-related parameters collected during the game. It is stored in json format.
- E4 file: It is the file where the physiological data collected from the E4 device during the game is stored. It is stored in txt format.

The contents of each notebook are given below.

* [Label_Sync.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/Label_Sync.ipynb), compares the three expert labels with each other and selects the    label with the majority of votes for use.
* [preprocess.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/preprocess.ipynb), contains the necessary edits to be made before using the E4 data for the model.
* [SignaltoNoiseRatio(SNR).ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/SignaltoNoiseRatio(SNR).ipynb),
* [Annotation_Validation.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/Annotation_Validation.ipynb),
* [Aktives-face.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/Aktives-face.ipynb),


## Project Configuration

* Install Python (at least 3.9 version is recommended),
* Setup your environment (venv, conda, etc.) and install dependencies from requirements.txt
