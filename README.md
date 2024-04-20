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

## Conclusion

This thesis investigated the utilization of CNN and UNet architectures for converting radar signals into ECG signals to accurately estimate heart rates. The principal findings indicate that the CNN architecture yielded superior results with the least average IBI error and root mean square error (RMSE) values when estimating heart rates from radar signals using the guardian vital signs dataset. Specifically, the CNN approach demonstrated substantial performance enhancements compared to the UNet architecture, assessed through MSE training evaluation metric and representation of reference ECG signals in triangular waveform.

The significance of this study lies in advancing an effective deep learning-based technique for signal translation, applicable to analogous signal processing challenges. Additionally, the proposed method offers a non-contact alternative to ECG sensors for heart rate estimation, beneficial for remote monitoring and healthcare applications, even in noisy and distorted signal environments.

Nonetheless, certain limitations should be addressed in future research. Firstly, the study's datasets were confined to a small number of participants. Secondly, the efficacy of the proposed method may be influenced by radar signal quality, affected by factors like breathing-induced Doppler shifts and noise.

In conclusion, this thesis underscores the potential of deep learning approaches for signal translation and their practical use. The proposed method holds promise for real-world applications, such as remote health monitoring, facilitating early detection and treatment of cardiovascular conditions. It advocates for broader datasets, advanced signal processing, and improved radar systems to refine performance and reduce interference for future investigations. This research offers valuable insights for signal translation and its healthcare applications, poised to make a substantial impact on remote monitoring systems and cardiovascular care.
