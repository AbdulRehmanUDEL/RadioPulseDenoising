This folder contains waveform datasets for testing and demonstrating the trained networks. It consists of the following subdirectories:

- **`sample_set/`**: Contains individual-channel waveform files such as `ch0_NoiseOnly.npz`, `ch1_Signals.npz`, etc.  
  Each file stores a NumPy array of shape **(N, 1000)**, where:
  - **N** is the number of waveforms  
  - **1000** is the number of time samples per waveform  

  The two channels represent the two polarizations of the antenna.

  The provided notebook **`DataReshapingForNetworks.ipynb`** can be used to combine corresponding channel files into a single two-channel input suitable for training the classifier and denoiser networks.

- **`validation_data/`**: Contains already combined, two-channel waveform data stored as NumPy arrays of shape **(N, 1000, 2)**, where:
  - **N** denotes the total number of samples  
  - **1000** represents the length of each channel's waveform  
  - **2** corresponds to the two polarization channels  

  These are used to evaluate the performance of the pre-trained models directly, without additional preprocessing.

All waveforms have been bandpass-filtered to the **[70 – 350] MHz** range and are stored in compressed NumPy `.npz` format.

