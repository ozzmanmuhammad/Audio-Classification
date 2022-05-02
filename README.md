# Audio-Classification
Audio classification using Tensorflow for "Z by HP Unlocked Challenge 3 - Signal Processing" Competition. 

## Overview
I did this project to enter the competition by [Z by HP Unlocked Challenge 3](https://www.hp.com/us-en/workstations/industries/data-science/unlocked-challenge.html). This project aim was to Classify Capuchinbird birds calling (AUDIO) and to get Density of Capuchinbird Birds though those audios.
I was able to get the model to predict the class of the food from 101 classes with 100% accuracy, recall, and precision.

## Code and Resources Used
- Python Version: 3.10
- Tensorflow Version: 2.8.0
- Packages: pandas, numpy, sklearn, matplotlib, seaborn
- GPU Configuration: Using Google Colab == T4 GPU

## Dataset and EDA
The datasets was downloaded from [Kaggle](https://www.kaggle.com/datasets/kenjee/z-by-hp-unlocked-challenge-3-signal-processing?resource=download). As we can see the data is skewed, to improve results we have to fix the datasets in future.

|               | Properties  |
| ------------- |:-------------------:|
| Dataset source| Preprocessed download from Kaggle|
| POS data| 217 images|
| NEG data | 593 images|
| Data loading|tf Data API|

These audio files were converted into wav then into visual spectrums so that we can use CNN for the classification.
<img src="https://raw.githubusercontent.com/ozzmanmuhammad/Audio-Classification/main/Images/spectrum.png" alt="Confusion Matrix"  width="500"/>


## Model Building

The Model I trained was very shallow and was trained on only 6 epochs to avoid overfitting as the data was very small.

|               | Properties | 
| ------------- |:-------------------:|
| Models | CNN|
| Layers| Cov2D, MaxPool, Conv2D, Flatten, Dense, Dense|
| Depth | 16, 16, 128, 1 |
| Epochs| 6 |
| Total params |189,954,737|

<br/><br/>

## Results:

### Confusion Matrix:
<img src="https://raw.githubusercontent.com/ozzmanmuhammad/Audio-Classification/main/Images/confusionMatrix.png" alt="Confusion Matrix"/>

### Recal:
<img src="https://raw.githubusercontent.com/ozzmanmuhammad/Audio-Classification/main/Images/recall.png" alt="Confusion Matrix"/>

### Precision:
<img src="https://raw.githubusercontent.com/ozzmanmuhammad/Audio-Classification/main/Images/precision.png" alt="Confusion Matrix"/>
