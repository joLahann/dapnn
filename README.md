# DAPNN

This is the source code for the paper _Detection of Anomal Process Behavior through LSTM Neural Networks_ that is currently under review for the BPM 2022. 

## Content
This repository contains the following notebooks:
- 01_log_conversion.ipynb: Converts the event logs into csv format to make it easier to load them.
- 02_data_processing.ipynb: Handles the processing, including encoding of attributes, creation of sliding windows, adding of start and end events, generation of data loaders.
- 03_anomaly.ipynb: Includes the anomaly detection algorithm, i.e. the prediction model, the loss functions and the anomaly score calculation and classification, as well as the metric computation.
- 04_training.ipynb: Includes the training phase of the neural networks for all datasets.
- 05_permormance.ipynb: Includes the global performance anlysis for the three datasets. Also analyses how the prediction accuracy affect the F1-Score.
- 06_hyper_params.ipynb: Covers the analysis of the hyper params including detection threshold, window size, number of layers and hidden state.
- 07_dataset_statistics.ipynb: Includes general statistics of the three datasets, that are exported into latex.
- training.py. A helper script that can be used to run the training from terminal (Can take ~20 h).
- prediction_params.py. A helper script that can be used to train multiple prediction models with different hyer parameter configurations (Can take ~10 h). 


## Installation
In order to run the notebooks, it is required to install fastai and pm4py. The easiest way to get everything running is with anaconda.
```
conda create -n dapnn python=3.9.
conda activate dapnn
conda install -c pytorch -c fastai fastai=1.0.61
pip install pm4py
pip install -e .

```
To run the jupyter notebooks you also have to create a jupyter kernel:
```
python -m ipykernel install --user --name dapnn
```

The repository is build with the nbdev package -> https://nbdev.fast.ai/.

