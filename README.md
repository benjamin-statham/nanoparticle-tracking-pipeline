\# Nanoparticle Tracking Pipeline



A machine learning pipeline for detecting and tracking fluorescent nanoparticles in microscopy video data of ciliated tissue. Combines YOLOv8 for detection and DeepSORT for multi-object tracking.



Developed as part of a BEng Engineering Project at Durham University (2025–2026).



\## Requirements



Install dependencies via pip:



```bash

pip install ultralytics==8.4.6 deep-sort-realtime opencv-python tifffile pandas numpy scipy matplotlib

```



Both notebooks are designed to run in Google Colab with GPU runtime enabled.



\## Pretrained Model



A trained YOLOv8m model is provided in this repository (`nanoparticle\_detector\_best.pt`). Set `MODEL\_PATH` in the inference pipeline configuration cell to point to this file.



\## Usage



\### 1. Training Pipeline

`nanoparticle\_detection\_training\_pipeline.ipynb`



Prepares annotated microscopy data and fine-tunes a YOLOv8m model. Edit the configuration cell at the top to set your data paths before running.



\### 2. Inference \& Analysis Pipeline

`nanoparticle\_tracking\_analysis\_pipeline.ipynb`



Runs detection, tracking, and flow analysis on preprocessed TIF video stacks. Edit the configuration cell at the top to set your video path, model path, and analysis parameters before running.



Raw `.nd2` videos must be preprocessed in Fiji/ImageJ before use — see the preprocessing steps in the notebook header.



\## Output



Results are saved to the directory specified in `OUTPUT\_DIR`, including tracking CSVs, verification videos, and flow analysis plots.

