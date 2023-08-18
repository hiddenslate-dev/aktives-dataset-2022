# Repository for the AKTIVES Dataset 2022

## Description

This is a supplementary repository for the AKTIVES Dataset 2022 presented in the article titled "AKTIVES: A physiological signal database of children with neurodevelopmental disorders for stress recognition".
Necessary libraries are in [requirements.txt](https://github.com/hiddenslate/aktives-scientific-data/blob/main/requirements.txt).

The contents of each notebook are given below.
* [Label_Sync.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/Label_Sync.ipynb) compares the three expert labels with each other and selects the label with the majority of votes for use.
* [preprocess.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/preprocess.ipynb) includes converting time values into DateTime, removing unnecessary data parts, separating data as Blood Volume Pulse (BVP), Electrodermal Activity (EDA), and Skin Temperature (ST), and filtering and visualization of the signals.
* [SignaltoNoiseRatio(SNR).ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/SignaltoNoiseRatio(SNR).ipynb) calculates the signal-to-noise ratio (SNR) [1] of the physiological signals nd their statistical features.
* [Annotation_Validation.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/Annotation_Validation.ipynb) calculates the agreement percentages of the expert annotations.
* [Aktives-face.ipynb](https://github.com/hiddenslate/aktives-scientific-data/blob/main/Aktives-face.ipynb) detects facial expressions with the FER library [2] and detects facial landmarks with DLIB shape predictor [3].

[1] https://github.com/psychosensing/popane-2021/blob/main/scripts/snr.py

[2] https://pypi.org/project/fer/

[3] http://dlib.net/face_landmark_detection.py.html

## Dataset Access

The use of the AKTIVES dataset is limited to academic research purposes only. The data will be made available after completing the End User License Agreement (EULA). The EULA is located in the [AKTIVES dataset repository](https://doi.org/10.7303/syn43685982.1) in EULA_AKTIVES.pdf. It should be signed and emailed to aktives.project@gmail.com.

## Project Configuration

* Install Python (at least 3.9 version is recommended),
* Setup your environment (venv, conda, etc.) and install dependencies from requirements.txt

## Reference

If you use the AKTIVES Dataset 2022, please cite the article below:

Coskun, B., Ay, S., Erol Barkana, D., Bostanci, H., Uzun, I., Oktay, A. B., Tuncel, B., & Tarakci, D. (2022). AKTIVES: A physiological signal database of children with neurodevelopmental disorders for stress recognition 
