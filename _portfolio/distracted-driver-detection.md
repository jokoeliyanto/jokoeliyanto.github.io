---
title: "Distracted Driver Detection with MobileNet"
category: certification
order: 3
issuer: "Bangkit 2020 - Google, Gojek, Tokopedia, Traveloka"
date: 2020-09-09
description: "Bangkit 2020 Top 4 final project: real-time distraction detection from dashboard camera using MobileNet transfer learning. 98.2% validation accuracy on 10 activities. Featured by Google Indonesia."
gif: /images/portfolio/distracted-driver-detection.gif
tech: [Python, TensorFlow, Keras, MobileNet, TensorFlow Lite, TensorFlow.js, Django, CNN, Transfer Learning]
repo: https://github.com/jokoeliyanto/bfp-driver-disctracted-cnn
demo: 
credential: https://www.coursera.org/account/accomplishments/specialization/E32DMWHAY3PL
collection: portfolio
---

## Problem

Road crashes kill approximately **1.19 million people annually** (WHO, 2023). Distraction is a leading cause, responsible for **3,275 deaths in the US alone in 2023** (8% of all road deaths). The challenge was building an **Android app that runs in real-time, offline, and on mid-range phones** to detect when drivers are distracted and trigger an alert.

| Stakeholder | Value |
|---|---|
| Ride-hailing & delivery platforms | Fewer crashes and claims across large driver fleets at minimal cost per driver |
| Logistics and bus fleets | Leading indicator of risky behaviour for coaching |
| Insurers (usage-based) | Distraction events per km as a behaviour-based risk signal |

## Approach

1. **Dataset**: State Farm Distracted Driver Detection (Kaggle): **22,424 labelled photos** of **26 drivers** in **10 classes** (safe driving + 9 distraction types). Random 80/20 train/validation split (17,943 / 4,481 images).

2. **Baseline Model**: 4 Conv2D + MaxPooling blocks (512-256-128-64 filters), Dense 512, softmax 10, Adam 1e-4, early stopping → **99.13% validation accuracy**.

3. **Transfer Learning**: ImageNet MobileNet v1 (frozen weights) + Conv2D 1024 + Dropout 0.2 + global average pooling + softmax 10. MobileNet's depthwise-separable convolutions were designed for phones.

4. **Deployment**: Exported to TensorFlow Lite (Android) and TensorFlow.js (web), integrated into Django app with confusion matrix evaluation and per-driver metrics.

5. **Audit of Original 2020 Notebook**: Found 4 issues including preprocessing mismatch (raw 0–255 pixels vs. rescale=1/255) and class order confusion. Corrected in deployed version.

## Result

**Key Metrics Achieved:**

| Metric | Baseline CNN | MobileNet Transfer Learning |
|---|---|---|
| **Validation Accuracy** | 99.13% (epoch 4) | **98.15%** (epoch 20) |
| **Training Time per Epoch** | 647 s | **112 s** (~6× faster) |
| **Model Size** | – | 50.7 MB |
| **CPU Latency** | – | **~72 ms per frame** |
| **Trainable Parameters** | 6.29M | 9.45M |

**Key Findings:**
- ✅ Deployed model reaches **98.2% validation accuracy** on 10 activities
- ⚡ MobileNet trains **~6× faster per epoch** while maintaining high accuracy
- 🎯 Frozen ImageNet features prevent memorisation of 26 drivers (unlike baseline)
- ⚠️ **98% is an upper bound**: validation split is random; same drivers appear in training and validation. Driver-level split is the honest test before deployment.

**Distraction Detection:**
- **c0 (Safe driving)** = "Focused" → No alert
- **c1–c9 (Texting, phone calls, eating, etc.)** = "Distracted" → Alert triggered
- False-alarm rate and distraction recall optimised for real-world deployment

![Demo](/images/portfolio/distracted-driver-detection.gif)

**Recognition:** Featured by **Google Indonesia Blog** (9 September 2020) among the **four best projects** of the Bangkit 2020 cohort.



