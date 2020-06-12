# DCASE CHALLENGE 2020 - Sound Event Localization and Detection - task 3

This work report the system submitted to the DCASE 2020 Challenge Task 3: Sound Event Localization and Detection. The algorithm consists of a CRNN using dense rectangular filters specialized on recognize significant frequency features related to the task. In order to further improve the score and to generalize the system performance to unseen data, the training dataset size has been increased using data augmentation based on channel rotations and reflection on the xy plane in the First Order Ambisonic domain, which allow to improve Direction of Arrival labels keeping the physical relationships between channels. Evaluation results on the cross-validation development dataset show that the proposed system outperforms the baseline results, considerably improving Error Rate and F-score for location-aware detection.

More information about the challenge can be foun at [1].

[1]: http://dcase.community/challenge2020/task-sound-event-localization-and-detection

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

### Prerequisites

The following modules are necessary to run the notebook: numpy, essentia-tensorflow, json, sklearn, matplotlib and seaborn.

All the modules will be directly imported running the notebook.

Essentia will be installed directly running the notebook.

## Open the notebok in Google Colab

The notebook can be directly open from Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RonFrancesca/Analysis_Essentia_models-MTG_Jamendo-dataset/blob/master/LargeScale-Dataset-ClassificationRonchini.ipynb)

Read the Notebook instructions to properly change directories paths and run the notebook correctly.

All the data used in this work have been stored in Goodle Drive, so they can be mount directly from the notebook. 

## Clone or Download the repository 

If the user wants a local copy of the notebook, clone or download the reposiotry.
It contains a Google Colab notebook, please read the Notebook instruction to properly change directories paths and run the notebook correctly.

Command to clone the repository:
```
$ git clone https://github.com/RonFrancesca/AnalysisEssentiamodels-MTGJamendodataset.git
```
Once the notebook is installed, open it from google colab and follow the instruction to configure it correctly. 

## MTG jamendo annotator 

More information about MTG jamendo annotator, how to configure it and run it can be found at the following link: https://github.com/MTG/mtg-jamendo-annotator. 

## DCASE Challenge 2020 - Sound Event Localization and Detection

The dataset can be found at the following links: https://github.com/MTG/mtg-jamendo-dataset

More information about the MTG jamendo dataset can be found in the following paper. 

> Bogdanov, D., Won M., Tovstogan P., Porter A., & Serra X. (2019).  [The MTG-Jamendo Dataset for Automatic Music Tagging](http://mtg.upf.edu/node/3957). Machine Learning for Music Discovery Workshop, International Conference on Machine Learning (ICML 2019).

## Tenworflow models for Essentia 

The models used for this work can be downlaoded at the following link: https://mtg.github.io/essentia-labs/news/2020/01/16/tensorflow-models-released/. 
For this work, two tasks have been examinated (mood and miscellanous). 
The following models have been considered: 
- Mood task: MusiCNN_MSD and VGGish_AudioSet
- Miscellanous task: MusiCNN_MSD and VGGish_AudioSet

Download and save them the inside a folder in Google Drive which will be mounted from the notebook in Google Colab


## Author 
- Francesca Ronchini


