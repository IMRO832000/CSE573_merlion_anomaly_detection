# CSE 573: Semantic Web Mining, Group - 30
PROJECT: Evaluating Anomaly Detection Methods for Multivariative Time Series

### Team 
Mary McCready, Pranavi Addagatla, Rohith Krishna Papani, Rahulrajan Karthikeyan, Shawn Mian, Nikhil Bodela

## Project Intent
We aim to investigate multiple ML related approaches to anomaly detection and  use our finding to develop anomaly detection techniques using a variety of tested approaches

## Problem Definition
Rising data volume across the computing world calls for a greater need for reliable anomaly detection systems and anomalous data may signal critical incidents or highlight data errors and accurately identifying these issues can lead prevent critical errors and improved data set representations.

## Dataset
Univariate data sets: 2 NAB datasets
Ec2_request_latency_system_failure.csv - 4033 entries
Machine_temperature_system_failure.csv -  22696 entries

Multivariate datasets: two real-world public datasets expert-labeled by NASA
Soil Moisture Active Passive (SMAP) satellite data - 132045 entries
Mars Science Laboratory (MSL) rover data -  562799 entries

## Algorithms and Parameters
Isolation Forest:  max _n_ samples , n_estimators , max_score , Threshold.
Random cut forest: n_estimators , seed , max_n_samples , Thread_pool_size , max_score , Threshold.
Variational Autoencoder: encoder hidden sizes , decoder hidden sizes , sequence len , drop out rate , num_eval_samples , num_epochs , max_score , Threshold.
Autoencoder: hidden size , layer_sizes , sequence len , batch size ,num_epochs , max_score , Threshold.
ZMS: train_data , anomaly labels , train_config.

## Evaluations: Preliminary, Experiments & Findings Metrics
- Most models exhibit high precision, recall and F1 scores across various datasets.
- Deep Point Anomaly Detection consistently demonstrates high precision, recall and F1 scores but its Mean Time to Detection (MTTD) varies significantly among datasets.
- AutoEncoder and VAE models generally perform well with high precision though their recall and F1 scores are slightly lower in some instances.
- The "MSL" dataset poses challenges with lower recall scores for all models particularly with Isolation Forest and AutoEncoder models.
- Choosing an anomaly detection model should consider task-specific requirements, balancing precision, recall, computational efficiency and dataset characteristics.
