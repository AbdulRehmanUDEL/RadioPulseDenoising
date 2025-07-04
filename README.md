# RadioPulseDenoising

This repository contains scripts for the construction and training of convolutional neural networks (CNNs) designed for classifying and denoising radio pulses from cosmic-ray air showers. The CNNs were developed and trained using TensorFlow and Keras, so these libraries are required to run the provided scripts. 

The repository is organized as follows:
- **`models/`**: Contains the pre-trained networks.
- **`data/`**: Contains waveform datasets used for testing and demonstration.
  - **`sample_set/`**: A small sample of waveforms that can be used to see how the data is prepared for training the neural networks. This is not sufficient for actual model training — a larger dataset should be prepared in the same format as demonstrated here.
  - **`validation_data/`**: A validation dataset for evaluating the performance of the provided pre-trained models. This data is intended exclusively for testing the already trained models found in the "**models**" directory.

- **Notebooks**: Provide essential workflows for data preprocessing, network training, and model application.

## Notebooks Overview

### 1. DataReshapingForNetworks
This notebook preprocesses waveform data for network training. It reshapes waveforms from two channels into single samples and supports:
- Preparing datasets for the **Denoiser**, requiring both pure signal traces and signal-plus-noise traces.
- Preparing datasets for the **Classifier**, requiring signal-plus-noise traces and noise-only traces.
- Splitting the data into training and test sets.

### 2. NetworksArchAndTraining
This notebook defines the architecture of the CNNs (both Classifier and Denoiser) and handles their training.

### 3. Apply_Networks
This notebook evaluates the pre-trained networks located in the /models directory using the validation dataset.

## Reference Proceedings:

The following are the proceedings that were written for this work:

1- Application of Machine Learning to Identify Radio Pulses of Air Showers at the South Pole. Link: https://pos.sissa.it/470/034/

2- Search for Cosmic-Ray Events Using Radio Signals and CNNs in Data from the IceTop Enhancement Prototype Station. Link: https://pos.sissa.it/444/291/

3- Deep Learning for the Classification and Recovery of Cosmic-Ray Radio Signals against Background Measured at the South Pole. Link: https://pos.sissa.it/424/012/

4 -Classification and Denoising of Cosmic-Ray Radio Signals using Deep Learning. Link: https://pos.sissa.it/395/417/pdf

## Acknowledgments:

We want to acknowledge the **Tunka-Rex** people, **Kostunin, Dmitriy** (dmitriy.kostunin@desy.de and github [@kostunin](https://github.com/kostunin)) and **Dmitry Shipilov** (justforprince@gmail.com and github @Dofollow), for sharing their CNN code with us, which became the basis for this work, their code can be found here: https://gitlab.iap.kit.edu/tunkarex/denoiser


