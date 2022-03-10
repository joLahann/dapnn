# DAPNN

This is the source code for the paper _Detection of Anomal Process Behavior through Neural Networks_ that is currently under review for the BPM 2022. 

This repository contains the following Notebooks:
- 01_log_conversion.ipynb: Converts the event logs into csv format to make it easier to load them.
- 02_data_processing.ipynb: Handles the processing, including encoding of attributes, creation of sliding windows, adding of start and end events, generation of data loaders.
- 03_anomaly.ipynb: Includes the anomaly detection algorithm, i.e. the prediction model, the loss functions and the anomaly score calculation and classification, as well as the metric computation.
- 04_training.ipynb: Includes the training phase of the neural networks for all datasets.
- 05_pdc20.ipynb: Includes the analysis for the PDC 2020 event logs.
- 06_pdc21.ipynb: Includes the analysis for the PDC 2021 event logs.
- 07_binet.ipynb: Includes the analysis for the Binet event logs, including the synthetic data sets and the BPIC datasets
- 08_latex_exp.ipynb: Covers some additional latex exports.

In order to run the notebooks, it is required to install fastai and pm4py. The easiest way to get everything running is with anaconda.
- conda create -n dapnn 
- conda activate dapnn
- conda install -c pytorch -c fastai fastai=1.0.61
- pip install pm4py

