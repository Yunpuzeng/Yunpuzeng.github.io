---
layout: default
title: Research
permalink: /research/
---

<nav class="site-nav">
  <a href="/">About</a>
  <a href="/research/">Research</a>
  <a href="/education/">Education</a>
  <a href="/publications/">Publications</a>
  <a href="/CV_Yunpu_Zeng_7_7.pdf">CV</a>
</nav>

## Research Interests

- Healthcare Operations
- Disease Modeling & Microsimulation
- State-Transition Modeling
- Cost-Effectiveness & Intervention Evaluation
- Public Health Analytics
- Data Analytics & Simulation

---

## Research

### Long COVID Progression Modeling

I develop population-level and state-transition models to characterize Long COVID progression and estimate disease burden over time.

My work links acute COVID-19 dynamics with post-acute symptom trajectories and individual-level simulation to study incidence, prevalence, symptom trajectories, and persistent disease burden.

### Alcohol-Related Disease Microsimulation

I develop individual-level microsimulation models to study alcohol consumption, disease progression, mortality, and healthcare interventions.

Current applications include cirrhosis progression, alcohol-attributable mortality, esophageal cancer, and intervention evaluation.

### Flu Hospitalization Forecasting

I worked on probabilistic forecasting of seasonal influenza hospitalizations using epidemiological models, Google search trends, and real-time data assimilation.

### Respiratory Motion Modeling

I developed computational approaches for modeling respiratory motion using 4D CT imaging, deformable vector fields, image registration, and optimization methods.

### Airway Tree Segmentation Using U²-Net
<p class="research-tags">
  Deep Learning · Medical Imaging · CT · U²-Net · PyTorch
</p>

This project focused on automatic **airway tree segmentation from chest CT scans**, with the goal of accurately extracting both the main trachea and smaller peripheral bronchi from three-dimensional medical images.

We developed a deep-learning segmentation pipeline based on **U²-Net**, a nested U-shaped convolutional neural network architecture. The model was trained using multi-site CT scans from the **ATM'22 Airway Tree Modeling Challenge**, which provided 299 annotated CT scans for training and 50 additional scans for validation.

A major challenge in airway segmentation is the strong **class imbalance** between airway and non-airway voxels, since airway structures occupy only a small portion of a chest CT scan. To address this, we trained the U²-Net using the **Dice loss function** rather than conventional binary cross-entropy, allowing the model to place greater emphasis on accurately identifying small airway structures.

The workflow included:

- CT intensity normalization and preprocessing to improve training efficiency and feature extraction
- A two-level nested **U²-Net architecture** with Residual U-blocks (RSUs) for multi-scale feature learning
- Multiple side-output saliency probability maps combined into a final airway probability map
- Dice-loss-based end-to-end optimization to address airway/non-airway class imbalance
- Thresholding and connected-region post-processing to remove spurious non-airway regions and refine the final airway tree

The resulting model demonstrated good segmentation of the **trachea and major bronchial branches**, with generally strong connectivity and anatomical accuracy on the validation CT scans, while also highlighting the greater difficulty of preserving connectivity in smaller peripheral bronchi.

[📄 Read the paper on arXiv](https://arxiv.org/abs/2209.10796)
