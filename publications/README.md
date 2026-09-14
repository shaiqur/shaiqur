[← Back to Portfolio](../README.md)

# Research & Publications

My research spans **computer vision, multimodal machine learning, video understanding, driver monitoring, research datasets, NLP, and research computing infrastructure**.

A recurring theme across my work is building systems that connect the full research lifecycle:

**problem formulation → data collection → dataset engineering → modeling → evaluation → robustness analysis → reproducible infrastructure**

My current Ph.D. research focuses on driver-monitoring systems for **gaze understanding and distracted-driving analysis**.

---

# Current Research

## Multimodal Driver Gaze Understanding

**Work in progress / manuscript in preparation**

My current research investigates how different forms of anatomical and visual context contribute to driver gaze understanding.

The work explores:

* Head and upper-body visual context
* Eye-region information
* Pose-derived geometric relationships
* Multimodal learning
* Temporal information
* Subject-independent evaluation
* Camera generalization

The current multimodal system achieves approximately **86% subject-independent accuracy across nine gaze zones**.

A major focus of the ongoing work is understanding **robustness and domain shift**, particularly whether models that generalize to unseen drivers also generalize to unseen vehicle and camera configurations.

Detailed methodology and experimental results will be released with the corresponding publication.

[Research case study →](../projects/driver-gaze.md)

---

# Research Themes

## Driver Monitoring & Computer Vision

I work on models for understanding driver behavior from in-cabin video, including:

* Gaze-zone classification
* Distracted-driving recognition
* Human pose estimation
* Multimodal visual reasoning
* Temporal modeling
* Robustness across participants

My goal is not only to improve model performance, but also to understand **what information the models rely on and when those assumptions fail**.

---

## Video Understanding & Temporal Reasoning

Driver behavior unfolds over time.

My work has therefore also explored:

* Temporal action localization
* Change-point detection
* Sequence modeling
* Temporal probability smoothing
* Event segmentation
* Video-level behavior interpretation

This includes the **DeepLocalization** project published at CVPR Workshops 2024.

[DeepLocalization case study →](../projects/deep-localization.md)

---

## Dataset Development

I helped lead the development of the **SynDD1 and SynDD2 driver-monitoring datasets**.

My work spanned:

**behavior/gaze taxonomy → participant recruitment → data-collection protocol → preprocessing → annotation → reduction → benchmark preparation**

The datasets have supported research in distracted-driving recognition, gaze estimation, temporal localization, and AI City Challenge benchmarking.

[SynDD case study →](../projects/syndd.md)

---

## NLP for Transportation Data Quality

I have also applied transformer-based NLP to crash narratives.

My contribution focused on fine-tuning and evaluating **BERT-based models** to identify inconsistencies between structured crash records and information described in free-text narratives.

This work demonstrates how unstructured text can be used to help validate structured transportation data.

[Crash Narrative NLP case study →](../projects/crash-narrative-nlp.md)

---

## Research Computing & Reproducibility

My research work also includes building the infrastructure needed to make large-scale experimentation possible.

This has included:

* Dockerized computer-vision inference environments
* AWS SageMaker research environments
* Large-scale S3 data pipelines
* Multi-terabyte data processing
* PostgreSQL analytical datasets
* Secure research access
* Reproducible model execution

I view research infrastructure as part of the scientific process: experiments are more valuable when they can be reproduced, inspected, and executed reliably.

---

# Selected Publications

## DeepLocalization: Using Change Point Detection for Temporal Action Localization

**M. S. Rahman, I. F. Shihab, L. Chu, and A. Sharma**
*IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshops (CVPRW), 2024*

Explores temporal localization of driver activities using pose estimation, change-point detection, and video-level reasoning.

**My contributions included computer-vision inference pipeline development, Dockerization, experiment execution, and integration of pose-based temporal processing.**

[DOI: 10.1109/CVPRW63382.2024.00721](https://doi.org/10.1109/CVPRW63382.2024.00721)

[Case study →](../projects/deep-insight.md)

---

## Synthetic Distracted Driving (SynDD1) Dataset for Analyzing Distracted Behaviors and Various Gaze Zones of a Driver

**M. S. Rahman et al.**
*Data in Brief, 2023*

A driver-monitoring dataset developed to support research in distracted-driving recognition and gaze analysis.

My work included major contributions across dataset design, activity definition, participant/data-collection workflows, preprocessing, and benchmark preparation.

[DOI: 10.1016/j.dib.2022.108793](https://doi.org/10.1016/j.dib.2022.108793)

[Dataset case study →](../projects/syndd.md)

---

## Synthetic Distracted Driving (SynDD2) Dataset for Analyzing Distracted Behaviors and Various Gaze Zones of a Driver

**M. S. Rahman, J. Wang, S. V. Gursoy, D. Anastasiu, S. Wang, and A. Sharma**

The second-generation SynDD dataset extended the driver-monitoring research framework and supported additional work in distracted-driving and gaze analysis.

[DOI: 10.48550/arXiv.2204.08096](https://doi.org/10.48550/arXiv.2204.08096)

[Dataset case study →](../projects/syndd.md)

---

## Deep Insight: A Cloud-Based Big Data Analytics Platform for Naturalistic Driving Studies

*International Journal of Automotive Engineering, 2023*

Research infrastructure for managing and analyzing large-scale naturalistic-driving data in the cloud.

My related engineering work has included secure SageMaker access, AWS research infrastructure, large-scale data pipelines, automated environment provisioning, and research-computing support.

[Deep Insight case study →](../projects/deep-insight.md)

---

## Improving Crash Data Accuracy by Identifying Seatbelt Inference Mismatch Using NLP and Behavioral Modeling

*Road Safety and Simulation Conference, 2026*

Investigates inconsistencies between structured seatbelt information and crash narratives.

**My contribution focused on the BERT-based NLP analysis and model evaluation.**

[Crash Narrative NLP case study →](../projects/crash-narrative-nlp.md)

---

# Datasets & Benchmarking

## SynDD1 / SynDD2

The SynDD datasets have supported research and benchmarking in driver-behavior analysis.

They were associated with multiple editions of the **AI City Challenge**, including:

* 6th AI City Challenge — 2022
* 7th AI City Challenge — 2023
* 8th AI City Challenge — 2024

I also served as an **evaluator for the Naturalistic Driving Action Recognition / driver-distraction track**.

This gave me experience on both sides of research benchmarking:

**building data for evaluation** and **evaluating research submissions that use benchmark data**.

---

# Exploratory Research

## Vision-Based Car-Following Analysis

I explored whether computer vision could identify car-following behavior from roadway video.

The approach worked under simpler straight-road conditions, but experiments revealed limitations:

* Road curvature complicated geometric reasoning.
* Intermittent YOLO vehicle misses disrupted temporal continuity.

The work did not become a complete robust system, but it helped identify requirements for stronger tracking and road-geometry modeling.

I include exploratory work like this because negative and partial results are part of research.

Understanding **why a method fails** can be as important as demonstrating when it succeeds.

---

# Earlier Research

## Master's Thesis — Activity Recognition and Animation of ADL

My master's research explored activity representation and visualization.

The work included:

* ANTLR-based parsing
* Activity-of-daily-living representation
* JavaScript-based visualization
* 3D interactive models

This work preceded my later focus on computer vision and driver-monitoring systems.

---

# Research Philosophy

Across these projects, several principles guide how I work.

### Evaluate the representation, not only the model

Preprocessing, crop design, pose representations, and dataset construction can determine what information a model is even capable of learning.

### Treat evaluation design as part of the research

A high accuracy number means little if train/test leakage or domain similarity makes the problem artificially easy.

### Investigate failures

Cross-vehicle degradation, missing detections, ambiguous data, and unsuccessful experiments often reveal the next research question.

### Build reproducible systems

Research should not depend entirely on one person's laptop or undocumented setup.

Containerization, structured data pipelines, and controlled environments make experimentation more reliable.

### Connect research to real-world constraints

My work is motivated by systems that eventually need to operate with changing drivers, cameras, vehicles, datasets, and infrastructure.

---

# Research Skills

**Computer Vision**
Image classification · pose estimation · driver monitoring · video understanding · temporal localization

**Machine Learning**
Multimodal learning · CNNs · MLPs · transformers · BERT · model fusion

**Research Evaluation**
Ablation studies · subject-independent evaluation · domain generalization · error analysis · robustness testing

**Dataset Engineering**
Data collection · annotation · preprocessing · participant-independent splitting · benchmark preparation

**Research Infrastructure**
PyTorch · OpenCV · Docker · AWS SageMaker · S3 · ECR · PostgreSQL · large-scale data pipelines

---

# Academic Service

**Evaluator — AI City Challenge**

Contributed to evaluation of submissions in the naturalistic-driving / driver-distraction research track across multiple challenge editions.

---

# Research Links

[Google Scholar](https://scholar.google.com/citations?user=5kvdX3oAAAAJ&hl=en).
[ORCID](#).
[GitHub](https://github.com/shaiqur).
[Full CV](#)


---

[← Back to Portfolio](../README.md)
