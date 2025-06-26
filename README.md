<!-- --------------------------------------------------------------------- -->
<!--         TFM-S4ACyL-Classification-Results – Official README           -->
<!-- --------------------------------------------------------------------- -->
<p align="center">
  <img src="https://img.shields.io/github/last-commit/RodrigoPascual/TFM-S4ACyL-Classification-Results?style=flat-square">
  <img src="https://img.shields.io/badge/Type-Research%20Results-blue.svg?style=flat-square">
  <a href="https://github.com/RodrigoPascual/S4A-CyL"><img src="https://img.shields.io/badge/Dataset%20Repo-S4A--CyL-green?style=flat-square"></a>
  <a href="https://github.com/Orion-AI-Lab/S4A-Models"><img src="https://img.shields.io/badge/Framework%20Repo-S4A--Models-green?style=flat-square"></a>
  <a href="https://hdl.handle.net/10259/10551"><img src="https://img.shields.io/badge/dataset-Riubu-orange?style=flat-square"></a>
</p>

<h1 align="center">S4A-CyL Crop Classification Results</h1>
<p align="center"><em>A visual annex for the Master's Thesis: "Creation of a Dataset for Crop Classification using Deep Learning"</em></p>

---

### Why this repository?

This repository serves as a digital supplement to the official Master's Thesis document. Due to strict page limitations, it was not possible to include all the generated figures and visual artifacts in the main paper. This space provides a comprehensive and detailed view of the model performance, including confusion matrices and prediction visualizations.

> **TL;DR**
> This repo contains all the cool visuals that didn't fit in the paper. Browse the results below to see how the models performed.

---

### Table of Contents
- [Quick Links](#quick-links)
- [OAD-BiLSTM Model Results](#oad-bilstm-model-results)
- [OAD-Transformer Model Results](#oad-transformer-model-results)
- [How to Cite](#how-to-cite)

---

### Quick Links

* **[S4A-CyL Dataset (Creation Code)](https://github.com/RodrigoPascual/S4A-CyL)**: Repository with the source code for the S4A-CyL dataset generation.
* **[S4A-Models (Experiment Framework)](https://github.com/Orion-AI-Lab/S4A-Models)**: The base framework used for all Deep Learning experiments.
* **[S4A-CyL Dataset (Download)](https://hdl.handle.net/10259/10551)**: Official link to the final dataset hosted in the RIUBU institutional repository.

---

## OAD-BiLSTM Model Results

The OAD-BiLSTM (Bidirectional Long Short-Term Memory) model demonstrated outstanding performance, achieving over 99% accuracy on the test set. It proved to be exceptionally robust in distinguishing between different crop types, even those with similar phenological cycles.

### Confusion Matrices (OAD-BiLSTM)

The normalized confusion matrices show a near-perfect diagonal, indicating a very high true positive rate and minimal confusion between classes at both the pixel and parcel levels.

| Pixel-Level Confusion Matrix                               | Parcel-Level Confusion Matrix                              |
| ---------------------------------------------------------- | ---------------------------------------------------------- |
| ![LSTM Pixel-level Confusion Matrix](assets/lstm/confusion_matrices/lstm_pixel_confusion_epoch0.png) | ![LSTM Parcel-level Confusion Matrix](assets/lstm/confusion_matrices/lstm_parcel_confusion_epoch0.png) |

### Visualization Examples (OAD-BiLSTM)

The following images compare the ground truth labels with the predictions from the LSTM model on specific patches. The visual alignment between the prediction and the ground truth is remarkably high.

**Patch Prediction: `2024_30TUM_patch_00_16`**
![LSTM Visualization on Patch 1](assets/lstm/visualizations/oad_visualization_single_lstm_2024_30TUM_patch_00_16.nc.png)

**Patch Prediction: `2023_30TUM_patch_05_10`**
![LSTM Visualization on Patch 2](assets/lstm/visualizations/oad_visualization_single_lstm_2023_30TUM_patch_05_10.nc.png)

---

## OAD-Transformer Model Results

The OAD-Transformer model, while competent, showed a lower performance compared to the LSTM. Its main challenge was a noticeable confusion between winter cereal classes, such as Wheat, Barley, and Rye.

### Confusion Matrices (OAD-Transformer)

The confusion matrices below highlight the model's tendency to misclassify certain crops, as seen by the values outside the main diagonal.

| Pixel-Level Confusion Matrix                                      | Parcel-Level Confusion Matrix                                     |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| ![Transformer Pixel-level Confusion Matrix](assets/transformer/confusion_matrices/transformer_pixel_confusion_epoch0.png) | ![Transformer Parcel-level Confusion Matrix](assets/transformer/confusion_matrices/transformer_parcel_confusion_epoch0.png) |

### Visualization Examples (OAD-Transformer)

These visualizations showcase specific areas where the Transformer model struggles, particularly in differentiating crops with similar temporal signatures.

**Patch Prediction: `2024_30TUM_patch_00_16`**
![Transformer Visualization on Patch 1](assets/transformer/visualizations/oad_visualization_single_transformer_2024_30TUM_patch_00_16.nc.png)

**Patch Prediction: `2023_30TUM_patch_05_10`**
![Transformer Visualization on Patch 2](assets/transformer/visualizations/oad_visualization_single_transformer_2023_30TUM_patch_05_10.nc.png)

---
