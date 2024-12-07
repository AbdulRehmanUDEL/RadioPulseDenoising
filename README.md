# RadioPulseDenoising

This repository contains scripts for the construction and training of convolutional neural networks (CNNs) designed for classifying and denoising radio pulses from cosmic-ray air showers. The CNNs were developed and trained using TensorFlow and Keras, so these libraries are required to run the provided scripts. 

The repository is organized as follows:
- **`model/`**: Contains the pre-trained networks.
- **`data/`**: Includes waveforms that can be used to test the pre-trained models.
- **Notebooks**: Provide essential workflows for data preprocessing, network training, and model application.

## Notebooks Overview

### 1. DataReshapingForNetworks
This notebook preprocesses waveform data for network training. It reshapes waveforms from two channels into single samples and supports:
- Preparing datasets for the **Denoiser**, requiring both pure signal traces and signal-plus-noise traces.
- Preparing datasets for the **Classifier**, requiring signal-plus-noise traces and noise-only traces.
- Splitting the data into training and test sets.

### 2. NetworksArchAndTraining
This notebook defines the architecture of the CNNs and handles their training.

### 3. Apply_Networks
This notebook tests the pre-trained models on the sample dataset.
