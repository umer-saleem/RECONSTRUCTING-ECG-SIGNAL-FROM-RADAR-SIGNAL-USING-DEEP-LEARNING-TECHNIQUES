# Reconstructing-ECG-From-RADAR-Signal-using-Deep-Learning-Techniques
Radar-to-ECG Signal Reconstruction using Deep Learning for Heart Rate Estimation

## Abstract

The human heart, a vital organ responsible for circulating blood throughout the body, plays a critical role in delivering oxygen and essential nutrients to tissues and organs, thereby sustaining their proper function and overall health. Unlike contact-based methods such as electrocardiography (ECG), photoplethysmography (PPG), phonocardiography (PCG), and ballistocardiography (BCG) for monitoring vital signs like heart rate, contactless methods offer advantages including reduced risk of infectious disease transmission, increased subject comfort and convenience, and facilitation of remote health monitoring. Consequently, recent years have witnessed significant research in accurately measuring vital signs using contactless heart signal detection to assess cardiovascular health. Various radar systems have been employed in studies to capture heart signals from subjects under challenging conditions.

This thesis investigates the effectiveness of implementing CNN and UNet architectures, combined with different hyperparameter settings, to reconstruct heart signals from input radar data. To enhance neural network performance in learning heart signal features, two transformation techniques are applied to reference ECG signals before feeding them into the convolutional neural networks. The study evaluates the performance of these deep learning approaches using two datasets: a publicly available guardian vital sign dataset and another dataset acquired using FMCW radar systems. A comprehensive training pipeline conducts extensive experiments with different combinations of deep learning methods, ECG signal transformations, datasets, and evaluation metrics.

The performance of these methods is assessed using metrics such as average inter-beat interval (IBI) error and root mean square error (RMSE) on test data. The results provide insights into the effectiveness of deep learning techniques in accurately measuring heart rate through reconstructed heart signals. The study also presents a detailed analysis of relevant parameters and evaluation metrics to guide future research in contactless heart rate measurement.

## Scope of the Thesis

This thesis explores the integration of CNN and UNet architectures into a signal processing framework for reconstructing ECG signals from radar data, facilitating precise heart rate estimation. The study utilizes two datasets: a publicly accessible vital signs dataset [5] and an in-house FMCW radar dataset from VTT Technical Research Centre, Finland. Evaluation of the study's outcomes is conducted using metrics such as average interbeat interval (IBI) and root mean square error (RMSE). Furthermore, the results are benchmarked against previous state-of-the-art deep learning models and associated performance metrics.

## Objective of the Thesis

The objective of this thesis is to assess the possibility of effectively translating radar signals to closely resemble reference ECG signals, achieved through an exploration of the intrinsic physiological connection between these signal types. This study employs deep learning techniques such as convolutional neural networks (CNN) and UNet architectures to establish a mapping between radar and ECG signals, facilitating precise estimation of heart rate.
