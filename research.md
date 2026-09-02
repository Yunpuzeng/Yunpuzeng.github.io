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

### Intra-Subject Respiratory Motion Modeling Using a Diffeomorphic Approach

<p class="research-tags">
  Medical Imaging · 4D CT · Image Registration · Diffeomorphic Modeling · Optimization
</p>

Respiratory motion creates an important challenge for image-guided lung interventions. A conventional static CT scan captures the anatomy at only one moment in the respiratory cycle, while lung tissue, vessels, and potential biopsy targets continuously move as a patient breathes.

In this project, we developed a computational framework for modeling **patient-specific respiratory motion from 4D CT images**. The goal was to reconstruct the dynamic motion of lung regions across respiratory phases and provide more informative motion estimates for applications such as image-guided lung biopsy.

The modeling pipeline included:

- Extracting anatomical information from **4D CT images** across different respiratory phases
- Constructing point-cloud representations of lung structures and identifying anatomical landmarks for motion correspondence
- Using **affine transformations** to characterize global respiratory motion between image phases
- Fitting correspondence models using both **linear and nonlinear least-squares optimization**
- Representing local tissue deformation using **deformable vector fields (DVFs)**
- Applying a **diffeomorphic modeling framework** to preserve smooth and anatomically meaningful transformations
- Comparing the derived motion fields with reference vector fields to evaluate motion-model accuracy

A key part of the project was developing and validating DVFs that describe how individual regions of the lung move during respiration. These motion fields provide a continuous representation of tissue displacement and can potentially help estimate the location of anatomical targets when direct imaging information is limited.

The project began as my undergraduate senior project at **Sichuan University–Pittsburgh Institute** and later developed into a peer-reviewed conference publication.

<a class="paper-button"
   href="https://link.springer.com/chapter/10.1007/978-3-031-84460-7_19"
   target="_blank">
   📄 Springer Publication
</a>

<div class="research-poster">

  <div class="poster-heading">
    <span>Project Poster</span>
    <span class="poster-hint">Click to view full size ↗</span>
  </div>

  <a href="/poster.png" target="_blank">
    <img
      src="/poster.png"
      alt="Intra-Subject Respiratory Motion Modeling project poster">
  </a>

</div>

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
