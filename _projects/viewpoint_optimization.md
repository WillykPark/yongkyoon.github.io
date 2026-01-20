---
layout: project
title: 'Active Multiview Target Recognition via POMDP-Guided PPO'
caption: Viewpint optimization for UUVs.
description: >
  This project presents an active multiview recognition framework for underwater targets using POMDP-guided Proximal Policy Optimization (PPO).
  The system optimizes viewpoint selection for UUVs to improve recognition accuracy through adaptive and information-driven exploration.
date: 24 Nov 2025
image: 
  path: /assets/img/projects/viewpoint.png
  srcset: 
    1920w: /assets/img/projects/viewpoint.png
    960w:  /assets/img/projects/viewpoint@0,5x.png
    480w:  /assets/img/projects/viewpoint@0,25x.png
links:
  - title: Link
    url: https://github.com/WillykPark/viewpoint_optimization_UUVs.git
accent_color: '#4fb1ba'
accent_image:
  background: '#193747'
theme_color: '#193747'
sitemap: false
---

### Hybrid Model-Based-and-Model-Free Policy Learning for Forward-Looking Sonar (FLS)

This repository implements a hybrid POMDP-guided PPO framework for active multiview target recognition using Forward-Looking Sonar (FLS) images.
The method integrates:

 - Bayesian belief updates
 - Information-Gain–based reward shaping
 - A learned PPO policy
 - Temperature-calibrated CNN likelihood
 - Radon-transform–based orientation estimation

  #### POMDP-Guided Policy Learning

  During training, the agent uses:

    - CNN likelihoods
    - Bayesian belief updates
    - Expected Information Gain (EIG)
    - to learn an efficient viewpoint-selection strategy using PPO.

   During deployment:

    - No EIG
    - No POMDP tree search
    - No planning
    - Real-time reactive policy
    - Belief update + PPO forward pass

```yml
├── Baseline/
│   ├── auv_ppo_model_free.zip       # Model-free baseline
│   ├── eval_greedy_eig.py           # Evaluate model-based baseline
│   ├── eval_modelfree_ppo.py        # Evaluate model-free baseline
│   ├── training_model_free.py       # Training model-free baseline
│   └── uuv_env_modelfree.py         # Environment information for model free
│
├── CNN/                             # ResNet-18 + temperature scaling CNN training
├── Radon/                           # Radon transfromer based orientaion estimation
│
├── uuv_env_eig_cnn.py               # Model environment definitions
├── training_eig_cnn.py              # Model training
├── auv_ppo_model_eig_cnn_radon.zip  # Training result
├── check_viewpoint.py               # Visited viewpint evaluation
├── cnn_classifier.py                # To use CNN's result
├── dataset_provider.py              # Data input
├── evaluation_eig_cnn.py            # Evaluate a model
├── obs_provider.py                  # Data input
└── viz_trajectory.py                # To visualize the trajectory of agent
│
├── results/                         # Model training results
└── tb_logs/								    	   # Tensorboard logs
```

<!-- The configuration I use to enable the system font on my site. Feel free to copy!
{:.figcaption} -->
