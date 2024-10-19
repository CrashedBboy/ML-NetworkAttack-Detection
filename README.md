# Machine Learning-Based Attack Detection For Electric Vehicle Charging Infrastructure Security

## Contributors

* **Cheng-Lin Wu** ([@CrashedBboy](https://github.com/CrashedBboy))
  - MEng, School of Engineering Science, Simon Fraser University
  - Student No.: 301606107
  - Email: cheng-lin_wu@sfu.ca / crashedbboy@gmail.com
* **Daegil Kang**
  - MEng, School of Engineering Science, Simon Fraser University
  - Student No.: 301626179
  - Email: dka160@sfu.ca
* **Shiyu Zhang**
  - MEng, School of Engineering Science, Simon Fraser University
  - Student No.: 301588601
  - Email: sza212@sfu.ca

## Introduction
The increasing reliance on Electric Vehicle Supply Equipment (EVSE) for electric vehicle charging has made these systems a critical infrastructure component, yet vulnerable to a variety of cyberattacks. This project aims to identify network and host-based attack scenarios on EV chargers from three distinct perspectives: network traffic, host events, and power consumption.  
The EV charging systems are susceptible to threats like Reconnaissance and Denial-of-Service attacks from the network side, as well as host-based threats, including backdoor vulnerabilities and cryptojacking. As the adoption of electric vehicles grows, securing EVSE from these attacks is imperative to ensure both the stability of the charging infrastructure and the broader network. This proposal briefly outlines the experiments, methods, and datasets to evaluate the effectiveness of machine learning for the security of EV charging stations.

## Dataset Description
The CIC EV Charger Attack Dataset 2024 (CICEVSE2024)[1] serves as the primary dataset for this project. It offers a comprehensive view of both benign and attack scenarios involving EV chargers. This dataset captures key metrics such as power consumption, network traffic, and host-based events like Hardware Performance Counter (HPC) and Kernel Events. The structure of the dataset consists of three main subdirectories [2]:
* Network Traffic, which includes pcap files and extracted CSV files for two types of chargers, EVSE-A and EVSE-B.
* Host Events, which contain CSV files detailing HPC and Kernel Events for EVSE-B under both normal and attack conditions.
* Power Consumption, which includes data showing power consumption patterns for EVSE-B in both benign and compromised environments.

This dataset is essential for tasks such as behavioural profiling, anomaly detection, and system performance analysis. It supports both statistical and machine learning-based analysis and is a vital resource for identifying security vulnerabilities in EVSE systems.

## Methodologies
To analyze the data and build an anomaly detection system, we plan to implement a transformer model[3] for multiclass classification tasks. Unlike traditional Recurrent Neural Networks (RNNs)[4], transformers use an attention mechanism that enables them to process long-term dependencies more efficiently. This makes transformers particularly well-suited for large temporal datasets like the ones found in the EVSE 2024 dataset. The project will also include comparisons with baseline models like RNNs to evaluate performance differences across various metrics.

## Experiment Design and Analysis
In the experimental phase, the focus will be on evaluating the model’s prediction accuracy, precision, and F-score. The following experiments are planned:  
### Experiment 1: Comparison of Prediction Accuracy
Objective: Compare the classification accuracy of the transformer model against a baseline RNN model.  
In this experiment, we aim to detect anomalies in a mixed dataset containing both normal and abnormal traffic. This will help assess the model's generalization ability across different traffic patterns.
### Experiment 2: Performance on Skewed Datasets  
Objective: Evaluate the model’s ability to detect anomalies when only a small portion of the data contains attack scenarios, as is common in real-world settings and how well the model performs in detecting outliers in a skewed dataset.

## Timeline
The project will be executed in the following phases:  
* Literature Survey: Oct.7 - Oct.13
* Data Cleaning and Preprocessing: Oct.14 - Oct.21
* Model Training and Tuning: Oct. 22 - Nov.3
* Experiments, Analysis, and Report Writing: Nov.3 - Nov.24

## Reference
1. Buedi, Emmanuel Dana, et al. "Enhancing EV Charging Station Security Using a Multi-Dimensional Dataset: CICEVSE2024." IFIP Annual Conference on Data and Applications Security and Privacy. Cham: Springer Nature Switzerland, 2024.
2. “EVSE Dataset 2024 | Datasets | Research | Canadian Institute for Cybersecurity.” University of New Brunswick, https://www.unb.ca/cic/datasets/evse-dataset-2024.html. Accessed 5 October 2024.
3. Vaswani, A. "Attention is All You Need." Advances in Neural Information Processing Systems (2017).
4. Hochreiter, S., & Schmidhuber, J. "Long Short-Term Memory." Neural Computation, 9(8), 1735–1780. https://doi.org/10.1162/neco.1997.9.8.1735
5. Wang, Haomin, and Wei Li. "DDosTC: A transformer-based network attack detection hybrid mechanism in SDN." Sensors 21.15 (2021): 5047.
6. Long, Zhenyue, et al. "A Transformer-based network intrusion detection approach for cloud security." Journal of Cloud Computing 13.1 (2024): 5.
