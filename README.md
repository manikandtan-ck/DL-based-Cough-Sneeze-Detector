# DL-based-Cough-Sneeze-Detector
Keras implementation of NLP based cough and sneeze detector based on GRU.

This model has been designed to detect coughing and sneezing sounds by listening to ambient audio on an embedded/mobile hardware using any microphone connected to it. This can run in the background as an app on mobile users given appropriate permissions or as listening pods in public areas where large number of people congregate. Considering the COVID-19 pandemic and future scenarios, this can be used to detect any anomalies in the cough/sneeze baseline count of the general public and raise location and time specific alerts. The system can be designed to maintain user anonymity while capturing data and can run a completely on-device processing without cloud/network audio upload. The application will communicate the statistics to the central server following a pre-configured interval.

<br>
<p align="center">
  <img alt="cough detection" width="60%" height="60%" src="https://github.com/cobaltKite/DL-based-Cough-Sneeze-Detector/blob/master/imgs/displayImage1.jpg?raw=true"> <br><br> 
  <img alt="location alerts" width="100%" height="100%" src="https://github.com/cobaltKite/DL-based-Cough-Sneeze-Detector/blob/master/imgs/map3.jpg?raw=true">
</p>


The model is implemented using Keras with Tensorflow backend. The implementation uses the Gated Recurrent Unit to detect cough/sneeze sounds. 

<br>
<p align="center">
  <img alt="gated recurrent unit" width="65%" height="65%" src="https://upload.wikimedia.org/wikipedia/commons/3/37/Gated_Recurrent_Unit%2C_base_type.svg?raw=true">
</p>

The model is trained on Sick Sounds Dataset (https://osf.io/tmkud/). The model can be trained with more data to reject background noise better, and have higher sensitivity and specificity to cough and sneeze sounds occuring under different background noise conditions.

## Proposed Solution

<p align="center">
  <img alt="proposed solution" width="100%" height="100%" src="https://github.com/cobaltKite/DL-based-Cough-Sneeze-Detector/blob/master/imgs/flowChart_Idea.png?raw=true">
</p>
The proposed solution consists of:
i. Data injection platform

ii. central server

iii. analytics insights/hotspot generation

## Pre-requisites:
Keras==2.3.1
matplotlib==3.2.1
numpy==1.18.4
pydub==0.23.1
scikit-learn==0.22.2
tensorflow==2.2.0

For the complete list of requirements install requirements using pip install -r requirements.txt

## Instructions to run
Run python3 cough_sneeze_inference.py to run the sample input. Detection output is displayed in the terminal.


