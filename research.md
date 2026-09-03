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

### Population-Level Modeling of Long COVID Burden

<p class="research-tags">
  Long COVID · Epidemiological Modeling · State-Transition Modeling · Population Health · Wastewater Surveillance
</p>

**Ongoing Research · 2025–Present**

Long COVID has created a substantial and persistent public health burden, but estimating its population-level impact remains challenging because reported COVID-19 cases do not fully capture the true scale of acute infections.

My current research develops a **population-level modeling framework for Long COVID** that connects acute COVID-19 infection dynamics with post-acute disease progression and longer-term symptom burden.

A major focus of this work is integrating **wastewater-informed estimates of SARS-CoV-2 transmission** with a state-transition framework for Long COVID. By combining population-level infection estimates with heterogeneous post-acute symptom trajectories, the model is designed to better characterize how Long COVID burden accumulates and evolves over time.

The framework incorporates longitudinal symptom patterns informed by clinical evidence and follows individuals through different trajectories of persistent symptoms, improvement, recovery, or continued disease burden. These individual-level trajectories are then aggregated to estimate population-level outcomes such as Long COVID prevalence and active disease burden over calendar time.

Ultimately, this work aims to provide a more comprehensive understanding of the long-term consequences of COVID-19 and to support future evaluation of healthcare needs and public health interventions.


<div class="research-highlight">

  <p><strong>📄 Manuscript</strong></p>

  <p>
    <strong>“Population-Level Burden of Long COVID in the United States:
    A Wastewater-Informed Modeling Study”</strong>
  </p>

  <p>
    Manuscript submitted to <strong><em>Nature Communications</em></strong>.
  </p>

</div>

<div class="research-highlight">

  <p><strong>🎤 Upcoming Presentation — 2026 INFORMS Annual Meeting</strong></p>

  <p>
    <strong>Session:</strong> Epidemic Modeling and Public Health Response<br>
    <strong>Date:</strong> Wednesday, November 4, 2026<br>
    <strong>Time:</strong> 9:30–10:45 AM<br>
    <strong>Location:</strong> Moscone South 105, San Francisco
  </p>

</div>

### Drinking-Behavior-Driven Microsimulation for Alcohol-Related Disease Progression

<p class="research-tags">
  Microsimulation · Alcohol Use · Disease Progression · Population Health · Intervention Evaluation
</p>

**Ongoing Research Program · 2024–Present**

This is an ongoing research program centered on an individual-level microsimulation framework that links **drinking behavior, chronic disease progression, mortality, and healthcare interventions**.

Rather than treating alcohol-related diseases as isolated outcomes, the framework follows individuals across heterogeneous drinking-risk states and disease trajectories over time. It is designed to study how changes in alcohol consumption influence long-term health outcomes across U.S. birth cohorts and to evaluate interventions aimed at reducing alcohol-related disease burden.

The framework has continued to evolve as new disease pathways, mortality risks, and intervention strategies are incorporated.

<div class="research-program">

  <div class="research-stage" markdown="1">

  <div class="research-stage-number">01 · Natural History</div>

  #### Cirrhosis Progression & Alcohol-Related Mortality

  <div class="research-stage-date">2025–2026</div>

  I developed a natural-history state-transition model for **alcohol-related cirrhosis**, linking drinking-risk states with progressive liver disease pathways.

  The model was subsequently extended beyond liver-specific outcomes to incorporate a broader set of **alcohol-attributable causes of death**, including:

  - Cancer
  - Cardiovascular disease
  - Unintentional injuries
  - Other competing mortality risks

  By integrating drinking behavior, liver disease progression, and competing alcohol-related mortality pathways within the same microsimulation framework, this extension provides a more comprehensive representation of the long-term population health burden associated with alcohol use.

  The model is used to examine how heterogeneous drinking patterns and disease trajectories contribute to mortality over time and across different U.S. birth cohorts.

  <div class="research-poster">

    <div class="poster-heading">
      <span>Project Poster</span>
      <span class="poster-hint">Click to view full size ↗</span>
    </div>

    <a href="/poster1.png" target="_blank">
      <img
        src="/poster1.png"
        alt="Alcohol-Related Mortality research poster">
    </a>

  </div>

  </div>


  <div class="research-stage" markdown="1">

  <div class="research-stage-number">02 · Disease Extension</div>

  #### Esophageal Cancer Progression

  <div class="research-stage-date">2025</div>

  The drinking-behavior-driven microsimulation framework was extended to study **alcohol-related esophageal squamous cell carcinoma**.

  I modeled disease progression across a sequence of health states, including:

  - Normal tissue
  - Dysplasia
  - Early-stage esophageal cancer
  - Late-stage esophageal cancer
  - Mortality

  The model was used to evaluate long-term cancer incidence and mortality across U.S. birth cohorts while preserving heterogeneous drinking behaviors within the underlying simulation framework.

  This extension demonstrated how the same drinking-behavior structure could be adapted to different alcohol-related disease pathways rather than being limited to liver disease alone.

  </div>


  <div class="research-stage" markdown="1">

  <div class="research-stage-number">03 · Intervention Evaluation</div>

  #### Alcohol-Use Reduction Interventions

  <div class="research-stage-date">2026–Present</div>

  The current phase of the research program focuses on evaluating interventions designed to reduce alcohol consumption and its downstream health consequences.

  Rather than modifying disease progression directly, the intervention framework acts on **transitions across drinking-risk states**, allowing treatment effects to propagate through subsequent disease and mortality pathways over time.

  Current applications include:

  - Mindfulness-based interventions
  - Pharmacologic interventions for alcohol use disorder
  - Semaglutide-based alcohol-use reduction
  - Alternative treatment-duration strategies
  - Long-term effects on alcohol-related disease burden and mortality

  A major focus of this work is understanding how the **timing, duration, and effectiveness of an intervention** influence population-level outcomes.

  The framework also provides a foundation for future evaluation of intervention value through **cost-effectiveness analysis**.

  </div>

</div>


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

### Flu Hospitalization Forecasting

<p class="research-tags">
  Epidemiological Modeling · Forecasting · SIRS · Extended Kalman Filter · Time Series
</p>

This project focused on probabilistic forecasting of **seasonal influenza hospitalizations** by combining epidemiological modeling with real-time data sources, including Google search trends.

I worked with a compartmental **SIRS model** together with an **Extended Kalman Filter (EKF)** to improve state estimation and dynamically update hospitalization forecasts as new observations became available.

The broader forecasting framework explored multiple modeling approaches, including:

- Naive forecasting strategies
- Compartmental epidemiological models
- Statistical time-series methods
- Machine learning approaches
- Temporal deep-learning models
- Multivariable temporal forecasting models

My work focused particularly on integrating the SIRS model with the EKF for real-time data assimilation, allowing the latent epidemic states to be continuously updated while accounting for uncertainty and noisy observations.

The project also involved processing and correcting CDC flu hospitalization data to support more reliable forecasting and evaluation.
