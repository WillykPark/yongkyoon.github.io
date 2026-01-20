---
layout: project
title: 'Multimodal Classifier for Medical Dataset'
caption: Multimodal Disease Prediction Model for Medical Data
description: >
  The model jointly processes medical images and clinical questions through separate encoders followed by feature fusion.
  The fused features are used to perform binary disease prediction.
date: 29 Dec 2025
image: 
  path: /assets/img/projects/multimodal.png
  srcset: 
    1920w: /assets/img/projects/multimodal.png
    960w:  /assets/img/projects/multimodal@0,5x.png
    480w:  /assets/img/projects/multimodal@0,25x.png
links:
  - title: Link
    url: https://github.com/WillykPark/Multimodal_Classifier_for_Medical_Dataset.git
accent_color: '#4fb1ba'
accent_image:
  background: '#193747'
theme_color: '#193747'
sitemap: false
---

Medical Visual Question Answering (Med-VQA) aims to support clinical decision-making by jointly interpreting medical images and natural-language queries. However, existing Med-VQA datasets, such as VQA-RAD, are constrained by limited dataset size, severe label imbalance, and the lack of explicit diagnostic labels, which makes reliable prediction challenging. 

In this project, we first conduct an exploratory analysis of the VQA-RAD dataset and observe that the majority of questions follow a binary yes/no format, while the associated medical images lack direct diagnostic annotations. Based on these findings, we establish uni-modal baselines for the yes/no task: a text-only classifier using PubMedBERT and an image-only classifier using ResNet-18. 

Furthermore, we propose a multimodal architecture that integrates PubMedBERT for textual encoding, a Swin Transformer for visual encoding, and a lightweight Transformer-based fusion module to jointly learn cross-modal representations. Experimental results show that the proposed model achieves improved performance over the uni-modal baselines in the closed (in-distribution) split, demonstrating the benefit of combining complementary modalities. However, performance degrades significantly in the open split, indicating sensitivity to unseen question types and the limitations of simple fusion strategies. 

Overall, our findings highlight the importance of modality-specific encoders, effective data processing strategies, and more robust fusion mechanisms for reliable multimodal medical question answering.

<!-- The configuration I use to enable the system font on my site. Feel free to copy!
{:.figcaption} -->
