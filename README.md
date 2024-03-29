# DAPNN

This is the source code for the paper Detection of Anomal Process Behavior through Neural Networks that is currently under review for the ML4PM 2022 THIRD INTERNATIONAL WORKSHOP ON LEVERAGING MACHINE LEARNING IN PROCESS MINING.

This repository contains the following notebooks:

- 01_log_conversion.ipynb: Converts the event logs into CSV format to make it easier to load them.
- 02_data_processing.ipynb: Handles the processing, including encoding of attributes, creation of sliding windows, adding of start and end events, and generation of data loaders.
- 03_anomaly.ipynb: Includes the anomaly detection algorithm, i.e., the prediction model, the loss functions, and the anomaly score calculation and classification, as well - as the metric computation.
- 04_training.ipynb: Includes the training phase of the neural networks for all datasets.
- 05_heuristics.ipynb: Includes the implementation of the heuristics.
- 06_performance_control_flow.ipynb: Covers the performance analysis for the first experiment. Additionally, the performance is evaluated for the second experiment when looking at only the control flow
- 07_performance_multi_attributes.ipynb: Covers the performance analysis for the second experiment for multi-attribute anomaly detection
- 08_hyper_parameter_analysis.ipynb: Includes some hyper-parameter analysis such as window size, threshold, and model parameters.
- 09_performance_with_fixed_th.ipynb: Includes the performance analysis with a fixed threshold only [depricated].
- 10_dataset_statistics.ipynb: Covers latex exports of the dataset stats.

In order to run the notebooks, it is required to install fastai and pm4py. The easiest way to get everything running is with anaconda:

```
  git clone https://github.com/joLahann/dapnn/blob/main/README.md
  conda create -n dapnn 
  conda activate dapnn
  conda install -c pytorch -c fastai fastai=1.0.61
  pip install pm4py
  cd dapnn
  pip install -e . 
```


