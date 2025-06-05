---
# Test Data

This folder contains data for testing the trained networks.  

* **PureSignals**: These are simulated waveforms generated using the CoREAS software, with no added noise.
* **SigPlusNoise**: These waveforms are a combination of CoREAS simulations and measured radio noise from the IceTop enhancement prototype station's antenna.

Both waveform sets have been processed and filtered within the **[70 - 350] MHz** band. 
The data is stored in **NumPy files** as arrays with a shape of $(N, 1000, 2)$. In this structure:

* **$N$** denotes the total number of samples.
* **$1000$** represents the length of each channel's waveform.
* **$2$** corresponds to the two polarization channels.
