# Cyber Threat Detection
In today's digital age, system security is of paramount importance. With increasingly sophisticated cyber threats, organisations face significant challenges in safeguarding their networks and preventing data breaches. Our algorithm provides real-time detection and analysis of cyber threats to enhance protective techniques used within the system.

Network flow analysis emerges as a powerful technique for detecting cyber threats by examining patterns and behaviors within network traffic. Network flows, often captured in NetFlow data, encapsulate key information about communication between network devices, including the source and destination IP addresses, port numbers, protocols used, and timestamps of communication.

The aim of this project is to leverage machine learning methods to develop a mechanism for cyber attack detection through network flow analysis. By harnessing the wealth of information present in NetFlow datasets, we seek to identify anomalous activities indicative of cyber attacks, such as intrusion attempts, malware propagation, and denial-of-service attacks.

## Data Collection
The dataset used can be found at this link : https://www.stratosphereips.org/datasets-ctu13, and it provides detailed information about Network flows within the system.

A strong data analysis is performed resulting in 22 extracted features from the initial Netflow datasets. All these features are then compared with one another through a feature selection process.Standard cleaning and normalisation techniques were used to prevent feature bias towards larger magnitudes. We also used feature selection to increase the contribution relevant features had towards the output and reduce computational complexity. Variance based comparisions and principal component analysis were used for dimensionality reduction.

## Data Visualisation
Heat maps and plots were constructed for providing a comprehensive understanding of the dataset. They have been included in the file to promote easier viewrship.

## File Description
`preprocessing1.py and preprocessing2.py` are the files used to extract meaningful data from the raw netflow files.

`feature_extraction.py` and `pca_tsne.py` try to decrease the number of features using embedded methods or dimensionality reduction techniques.

`predict_random_forest_bootstrap.py` and `predict_svm.py` implement a classifier to detect malware with Random Forest and with Support Vector Machine.

`predict_gradient_boosting_stat_analysis.py`, p`redict_logistic_reg_stat_analysis.py`, `predict_neural_network_stat_analysis.py` and `predict_statistic_analysis_bootstrap.py` carry out statistical analysis of different classifiers: Gradient Boosting, Logistic Regression, Neural Network and Random Forest with bootstrap respectively.

## Algorithm Selection
- **Random Forest Classification** : Multiple decision trees are constructed and the result is an average of the different outputs attained from each decision tree
- **Bootstrapping** : Bootstrapping is a resampling technique used in statistics to estimate the sampling distribution of a statistic by repeatedly sampling with replacement from the observed data
- **Support Vector Machine**: Support Vector Machines (SVMs) are powerful supervised learning models used for classification and regression tasks. SVMs are particularly effective in high-dimensional spaces and are widely used in various fields, including pattern recognition, image classification, and bioinformatics.

## Results
The experiments show that Random Forest can detect more than 95% of botnets for 8 out of 13 scenarios. Moreover, the accuracy on the 5 most difficult scenarios can be increased thanks to a bootstrap method. 
