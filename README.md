# DCASE CHALLENGE 2020 - Sound Event Localization and Detection - task 3

This work reports the system submitted to the DCASE 2020 Challenge Task 3: Sound Event Localization and Detection. The algorithm consists of a CRNN using dense rectangular filters specialized on recognize significant frequency features related to the task. In order to further improve the score and to generalize the system performance to unseen data, the training dataset size has been increased using data augmentation based on channel rotations and reflection on the xy plane in the First Order Ambisonic domain, which allow to improve Direction of Arrival labels keeping the physical relationships between channels. Evaluation results on the cross-validation development dataset show that the proposed system outperforms the baseline results, considerably improving Error Rate and F-score for location-aware detection.

More information about the DCASE 2020 Challenge can be found at [1].

The methodology proposed in this report is based on Adavanne et. al SELDNet [2], including some of the adopted additions in the baseline algorithm of the DCASE 2020 Task 3, such as the use of log-mel spectral coefficients and acoustic intensity vector for the FOA format. However, the system proposed in this report differs from the baseline in different points such as (i) data augmentation, (ii) network architecture and (iii) training loss functions. With respect to (i), -90◦, 90◦ and 180◦ channel rotations and reflection on the xy plane are used as data augmentation technique, implementing the 16 patterns spatial augmentation as proposed by Mazzon et al. for the same task of last year’s challenge [3]. The 16 patterns technique allows to augment DOA labels maintaining the physical relationships between channels. Regarding (ii), the network has been increased, adding 2 convolutional layers. Furthermore the receptive field has been expanded using dense rectangular filters (instead of squared ones) in order to make the network able to recognize fre- quency features relevant for the task. With regard to (iii), we used the same loss functions proposed in [2]. Binary cross-entropy loss is used for SED prediction task while mean square error (MSE) loss is used for DOA estimation.
Results on developments dataset are evaluated considering the evaluation metrics proposed by Mesaros et. al in [4], considering the joint nature of localization-and-detection. The same are used as evaluation metrics for the challenge.

[1]: http://dcase.community/challenge2020/task-sound-event-localization-and-detection 
[2]: Adavanne, Sharath, et al. "Sound event localization and detection of overlapping sources using convolutional recurrent neural networks." IEEE Journal of Selected Topics in Signal Processing 13.1 (2018): 34-48.

[3]: Mazzon, L., et al. "Sound event localization and detection using FOA domain spatial augmentation." Proc. of the 4th Workshop on Detection and Classification of Acoustic Scenes and Events (DCASE). 2019.

[4]: Mesaros, Annamaria, et al. "Joint Measurement of Localization and Detection of Sound Events." 2019 IEEE Workshop on Applications of Signal Processing to Audio and Acoustics (WASPAA). IEEE, 2019.

More informations regarding the system implementation and evaluation can be found on the technical report at: https://github.com/RonFrancesca/dcase2020-task3-fp/blob/master/Ronchini_UPF_task3.technical_report.pdf

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 


### Prerequisites
This repository consists of two Jupyter Notebooks which need to be run separately. 
The first notebook to run is *Feature_Extraction.ipynb*, allowing the features extraction. 
Afterwards, the notebook *TFr_5CNN_1X48.ipynb* should be run in order to train the network, make predictions and evaluate the system.  

The following modules are necessary to run the notebook: numpy, tensorflow, json, sklearn, matplotlib, librosa, scipy.

All the modules will be directly imported running the notebook.


## Open the notebok in Google Colab

The two notebooks can be directly open from Google Colab:

Feature_Extraction: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/RonFrancesca/dcase2020-task3-fp/blob/master/Feature_Extraction.ipynb)

TFr_5CNN_1x48: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/RonFrancesca/dcase2020-task3-fp/blob/master/TFr_5CNN_1x48.ipynb)

Read the Notebook instructions to properly change directories paths and run the notebook correctly.

The system implemented in this jupyter notebook uses rectangular filters of shape 1x48. 
The user can change and test different shapes changing the filter dimension in the funcion *get_model* in the TFr_5CNN_1X48. 

All the data used in this work have been stored in Goodle Drive, so they can be mount directly from the notebook. 

## Clone or Download the repository 

If the user wants a local copy of the notebook, clone or download the reposiotry.
It contains a Google Colab notebook, please read the Notebook instruction to properly change directories paths and run the notebook correctly.

Command to clone the repository:
```
$ git clone https://github.com/RonFrancesca/dcase2020-task3-fp.git
```
Once the notebook is installed, open it from google colab and follow the instruction to configure it correctly. 

 

## Dataset

TAU-NIGENS Spatial Sound Events 2020 dataset has been used to evaluate the model. 
Two formats of TAU-NIGENS Spatial Sound Events 2020 are provided for DCASE 2020 task 3:  First Order Ambisonic (FOA) and 4 channels from a Microphone Array (MIC). This system only use Ambisonic format.



The dataset can be found at the following links: https://zenodo.org/record/3870859#.XuOtWWozadY. 

More information about the TAU-NIGENS Spatial Sound Events 2020 dataset can be found in the following paper. 

> Politis, Archontis, Sharath Adavanne, and Tuomas Virtanen. "A Dataset of Reverberant Spatial Sound Scenes with Moving Sources for Sound Event Localization and Detection." arXiv preprint arXiv:2006.01919 (2020).


## Author 
- Francesca Ronchini
- Andrés Pérez López
- Daniel Arteaga


