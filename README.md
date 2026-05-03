# Cloud Recognition Models

A comprehensive deep learning repository for **cloud type classification** and **cloud segmentation**, designed for efficient deployment and geoscience applications.

---

## Overview

This repository contains two core components:

- **Cloud Type Classification** – Multi-class classification using transfer learning  
- **Cloud Segmentation** – Pixel-level cloud detection using a lightweight segmentation model  

The models are designed to be **lightweight, efficient, and suitable for mobile deployment (e.g., TensorFlow Lite)**.

---

## Models

### 1. Cloud Type Classification (MobileNetV3Small)

#### Description
A transfer learning-based model built on MobileNetV3Small, designed for accurate and efficient cloud type classification from ground-based images.

#### Features
- **Architecture**: MobileNetV3Small  
- **Training Strategy**: Transfer Learning + Fine-tuning  
- **Input**: RGB cloud images (224 × 224 × 3)  
- **Output**: Multi-class cloud type probabilities (Softmax)  
- **Optimization**: Lightweight for mobile inference  

#### Supported Cloud Types
Aligned with WMO classification:

- Altocumulus (Ac)  
- Altostratus (As)  
- Cumulonimbus (Cb)  
- Cirrocumulus (Cc)  
- Cirrus (Ci)  
- Cirrostratus (Cs)  
- Contrail (Ct)  
- Cumulus (Cu)  
- Nimbostratus (Ns)  
- Stratocumulus (Sc)  
- Stratus (St)  

---

### 2. Cloud Segmentation Model (CloudSegNet)

#### Description
A lightweight encoder–decoder segmentation model based on CloudSegNet, designed to identify cloud regions at the pixel level.

#### Features
- **Architecture**: CloudSegNet (encoder–decoder, no skip connections)  
- **Task**: Binary semantic segmentation  
- **Input**: RGB cloud images (300 × 300 × 3)  
- **Output**: Probability map (300 × 300 × 1)  
- **Post-processing**: Thresholding for binary mask generation  

---

## Performance Summary

| Model | Metric | Score |
|------|--------|------|
| Cloud Type Classification | Accuracy | 0.96 |
| Cloud Segmentation | IoU | 0.83 |

## Dataset

This project utilizes publicly available datasets:

- **CCSN Dataset**  
  Zhang et al., 2018  
  https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/CADDPD  

- **SWIMSEG / SWINSEG Dataset**
  Dev et al., 2017
  https://malea.winkler.site/swinseg.html  

- **TCDD Dataset**
  Zhang et al., 2022
  https://github.com/shuangliutjnu/TJNU-Cloud-Detection-Database  

> ⚠️ Note: Datasets are included for research purposes only. All rights belong to the original authors.


