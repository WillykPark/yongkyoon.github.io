---
layout: project
title: 'Handwritten Digit Recognition'
caption: Handwritten Digit Recognition.
description: >
  This project implements a YOLOv8-based handwritten digit detection system trained on an augmented dataset of rotated images.
  Transfer learning is applied to improve detection accuracy and performance across diverse digit variations.
date: 14 Dec 2024
image: 
  path: /assets/img/projects/handwritten.jpg
  srcset: 
    1920w: /assets/img/projects/handwritten.jpg
    960w:  /assets/img/projects/handwritten0,5x.jpg
    480w:  /assets/img/projects/handwritten0,25x.jpg
links:
  - title: Link
    url: https://github.com/WillykPark/Handwritten_Recognition_Project.git
accent_color: '#4fb1ba'
accent_image:
  background: '#193747'
theme_color: '#193747'
sitemap: false
---

This project focuses on detecting handwritten (one or more) digit(s). To start with, we had 4190 images and the corrosponding labels. Image augmentation was done and every image was rotated by 90, 180, and 270 degrees to get 3 copies, and the total training set contained close to 14000 images and labels. The YOLOv8 model was fine tuned and trained on these images and labels, carrying out transfer learning.

```yml
Handwritten_Recognition_Project/
├── Report/                                              # Final Report
│   ├── Handwritten Digit Classifier Report_SSS.pdf      # Final Report
│
├── Results/                                             # Training Results
│   ├── F1_curve.png                                     # performance result
│   ├── PR_curve.png                                     # performance result
│   ├── confusion_matrix.png                             # performance result_confusion matrix for model
│   ├── ...                                              # etc
│
├── weifhts/                                             # model's parameter
│   ├── best.pt                                          # Has to be loaded for running the predictions on the test data.
│   ├── lsst.pt 
│
├── data.yaml/                                           # info
├── test.ipynb/                                          # Test code for model
├── train.ipynb/                                         # Training code for model
├── yolov8n.pt                                           # The YOLO model from the Ultralytics library
```

To use the 'torchmetrics' package for evaluating preformance metrices, we need to install 'torchmetrics'.
!pip install torchmetrics should do the job.

<!-- The configuration I use to enable the system font on my site. Feel free to copy!
{:.figcaption} -->
