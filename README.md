# Computational-Intelligence-ThirdProject

This project focuses on separating epilepsy data from normal data in a dataset using various preprocessing and classification techniques.

## Dataset Preparation

In the initial stage, the dataset is loaded and prepared for classification. You can access the dataset [here](https://physionet.org/content/chbmit/1.0.0/). The primary objectives in this stage are as follows:

1. Sufficient Data Load
2. Balanced Dataset After Load
3. At Least 25% of Normal Data from Records with Seizures

We load and preprocess the data to ensure that it meets these requirements. One of the significant challenges in this phase is balancing the dataset while adhering to the distribution constraints.

In this part, we work with 11 signals, of which 10 contain seizure parts. The dataset is obtained from "physionet.org/content/chbmit/1.0.0," and its summary text file helps identify seizure segments. To increase the number of samples, we employ a 10-second window and overlapping, resulting in ten times more samples. Out of 3000 samples, 600 contain seizure parts, and 2400 are considered normal. Crucially, 25% of the normal data is derived from records that include seizure parts.

We also filter the samples based on the sampling frequency, and the data is prepared for feature extraction. The outcome is a balanced dataset, with samples containing both seizure and normal data. A corresponding label array is created for classification, with values 0 for normals and 1 for seizures.

## Classification

In this phase, the project requires utilizing the dataset to train and test a CNN model. The model should take the selected features, which are derived from the previous phase, as input. The steps include feature normalization and handling the data's two channels.

The most complex part of this project is designing the optimal CNN model to achieve high classification accuracy.

## Results and Evaluation

After training the model, results are evaluated. Key metrics include accuracy, validation accuracy, test loss, and test accuracy. The project uses a categorical cross-entropy classifier and converts it into a binary classifier. Evaluation metrics such as accuracy_score, confusion_matrix, recall_score, precision_score, and ROC graph are calculated.

## Authors

- Mehrnaz Sadeghieh
- Faridreza Momtaz Zandi
