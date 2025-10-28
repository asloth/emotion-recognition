# NN-EmotionDetection

This repository contains a Jupyter/Colab notebook implementing a neural network for emotion detection from facial images:
drive/MyDrive/Universidad/Tesis/NN-EmotionDetection.ipynb

## Overview

The NN-EmotionDetection notebook demonstrates an end-to-end workflow for building, training, evaluating, and exporting a neural network that detects emotions from images. Typical steps included in the notebook:

- Data loading and inspection
- Data preprocessing (resizing, normalization, augmentation)
- Model definition (neural network / CNN)
- Training and validation
- Evaluation (metrics, confusion matrix, sample predictions)
- Saving the trained model and artifacts

This notebook was created for thesis work (Universidad) and is intended to be run in Google Colab or locally.

## Contents

- NN-EmotionDetection.ipynb — main notebook with code, plots and results
- (Optional) model checkpoints and exported model files if produced by the notebook
- This README.md — usage and reproduction instructions

## Requirements

To run the notebook, you should have:

- Python 3.8+ (Colab provides a suitable runtime)
- TensorFlow (or Keras) — the notebook uses a neural-network library (e.g., tensorflow>=2.x)
- numpy, pandas, matplotlib, scikit-learn
- OpenCV or PIL for image handling (if used in notebook)
- (Optional) Google Drive mounted in Colab if the notebook reads/writes files there

A sample pip install command (adjust versions as needed):
```
pip install -U numpy pandas matplotlib scikit-learn tensorflow opencv-python pillow
```

## How to run (Google Colab)

1. Open the notebook in Colab by clicking the link above or using:
   - File > Open notebook > GitHub and paste the repository URL
2. Mount Google Drive if the notebook reads data from your Drive:
   - from google.colab import drive
   - drive.mount('/content/drive')
3. Ensure dataset files are present at the paths expected by the notebook (often under drive/MyDrive/Universidad/Tesis or a specified data directory)
4. Run the cells sequentially. Use a GPU runtime for faster training:
   - Runtime > Change runtime type > Hardware accelerator: GPU

## Reproducibility

- Seed random number generators if you need reproducible training runs.
- Save model weights and training history (the notebook should already include saving code — check relevant cells).
- Note dataset splits and augmentation parameters to reproduce results.

## Expected outputs

- Trained model file(s) (e.g., .h5, SavedModel directory)
- Training/validation loss and accuracy plots
- Confusion matrix and per-class metrics
- Example image predictions with ground truth vs. predicted labels

## Suggested improvements / next steps

- Add a requirements.txt or environment.yml for exact reproducibility.
- Export a small inference script (predict.py) or a REST API wrapper for deployment.
- Add unit tests for preprocessing and inference pipeline.
- Store and version trained model artifacts (e.g., Git LFS, Hugging Face Hub, or cloud storage).
- Add a brief LICENSE file and CONTRIBUTING guidelines if you plan to share or accept contributions.

## Attribution / Contact

Created by: asloth  
Notebook location: NN-EmotionDetection.ipynb
