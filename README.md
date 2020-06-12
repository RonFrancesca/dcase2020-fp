# DCASE CHALLENGE 2020 - Sound Event Localization and Detection - task 3

This work report the system submitted to the DCASE 2020 Challenge Task 3: Sound Event Localization and Detection. The algorithm consists of a CRNN using dense rectangular filters specialized on recognize significant frequency features related to the task. In order to further improve the score and to generalize the system performance to unseen data, the training dataset size has been increased using data augmentation based on channel rotations and reflection on the xy plane in the First Order Ambisonic domain, which allow to improve Direction of Arrival labels keeping the physical relationships between channels. Evaluation results on the cross-validation development dataset show that the proposed system outperforms the baseline results, considerably improving Error Rate and F-score for location-aware detection.

More information about the challenge can be found at [1].

[1]: http://dcase.community/challenge2020/task-sound-event-localization-and-detection

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

### Prerequisites

The following modules are necessary to run the notebook: numpy, tensorflow, json, sklearn, matplotlib, librosa, scipy.

All the modules will be directly imported running the notebook.


## Open the notebok in Google Colab

The notebook can be directly open from Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RonFrancesca/Analysis_Essentia_models-MTG_Jamendo-dataset/blob/master/LargeScale-Dataset-ClassificationRonchini.ipynb)

Read the Notebook instructions to properly change directories paths and run the notebook correctly.

All the data used in this work have been stored in Goodle Drive, so they can be mount directly from the notebook. 

## Clone or Download the repository 

If the user wants a local copy of the notebook, clone or download the reposiotry.
It contains a Google Colab notebook, please read the Notebook instruction to properly change directories paths and run the notebook correctly.

Command to clone the repository:
```
$ git clone https://github.com/RonFrancesca/dcase2020-task3-fp.git
```
Once the notebook is installed, open it from google colab and follow the instruction to configure it correctly. 

 

## DATASET 

TAU-NIGENS Spatial Sound Events 2020 dataset has been used to evaluate the model. 
Two formats of TAU-NIGENS Spatial Sound Events 2020 are provided for DCASE 2020 task 3:  First Order Ambisonic (FOA) and 4 channels from a Microphone Array (MIC). This system only use Ambisonic format.


The dataset can be found at the following links: https://zenodo.org/record/3870859#.XuOtWWozadY. 

More information about the TAU-NIGENS Spatial Sound Events 2020 dataset can be found in the following paper. 

> Politis, Archontis, Sharath Adavanne, and Tuomas Virtanen. "A Dataset of Reverberant Spatial Sound Scenes with Moving Sources for Sound Event Localization and Detection." arXiv preprint arXiv:2006.01919 (2020).


## Author 
- Francesca Ronchini
- Andrés Pérez López
- Daniel Arteaga


