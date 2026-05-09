DLM: Universal Neural Signature Classifier 
Universal P300 Event-Related Potential Detection via EEGNetv4

This repository contains a high-performance Deep Learning Model (DLM) designed for the real-time classification of human recognition signals (P300 Event-Related Potentials). Built on the EEGNetv4 architecture, this model is "Universal," meaning it is trained to work across multiple subjects without requiring individual calibration.

Overview
In high-stakes industrial environments, verifying human "recognition" of critical events is essential for safety. This DLM analyzes 16-channel EEG data to determine if a user has consciously registered a visual stimulus.

Model: EEGNetv4 (Convolutional Neural Network)

Accuracy: ~84% (Cross-Subject)

Sensitivity (Recall): 86% (Optimized to never miss a "Target" signal)

Data Source: BNCI 2014-009 (10 Subjects, 17,280 epochs)

Repository Contents
DLM_Classifier.ipynb: The complete Python pipeline (Data loading, Preprocessing, Training, and Evaluation).

eegnet_p300_universal.pth: The pre-trained weights for the DLM.

DLM_Research_Report.pdf: A formal technical report detailing the performance and spatial feature maps.

Results/: Visualizations including the Spatial Importance Map and Consistency Gallery.

Future Industrial Application (Safety Case)
The primary future application of this framework is in Industrial Cognitive Safety Systems.

Passive Monitoring: The DLM monitors a pilot's or operator's brainwaves.

Recognition Verification: When a warning light flashes, the DLM looks for a P300 spike.

Emergency Intervention: If the light flashes but the DLM detects a "Non-Target" (Miss), the system triggers an immediate intervention to prevent human-error-related accidents.

Scientific Validation
The model was validated using Spatial Feature Mapping, which confirmed that the DLM prioritizes the Parietal and Occipital lobes (Channels 11-12) for decision-making—matching established neurophysiological expectations for visual recognition tasks.

Requirements
Python 3.x
PyTorch
Braindecode
MOABB (Mother of All BCI Benchmarks)
