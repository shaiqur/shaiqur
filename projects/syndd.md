[← Back to Portfolio](../README.md)

# SynDD1 & SynDD2 — Building Driver-Monitoring Datasets from the Ground Up

**Role:** Researcher / Dataset Development Lead
**Organization:** Iowa State University — Reactor Lab
**Focus:** Driver Monitoring · Dataset Design · Data Collection · Annotation · Benchmarking

## The Problem

Computer-vision models are only as useful as the data available to train and evaluate them.

For distracted-driving and driver-gaze research, we needed datasets that captured realistic variations in driver behavior while also providing enough structure for controlled experimentation.

That meant solving a problem much larger than simply recording videos.

We needed to decide:

* What driver behaviors should be represented?
* What gaze zones should be defined?
* How should participants perform activities consistently?
* How should data collection be organized?
* How should videos be processed and annotated?
* How could the resulting dataset support reproducible benchmarking?

My work on the **SynDD1 and SynDD2 datasets** spanned this full lifecycle.

---

## Designing the Data Before Collecting It

One of the first challenges was defining exactly what the dataset should contain.

For distracted-driving research, loosely recording people performing arbitrary actions would not produce a useful benchmark.

The activities needed clear definitions and repeatable instructions.

I worked on defining the activity taxonomy and gaze-related categories used during data collection.

The goal was to create data that could later support problems such as:

**driver distraction recognition · gaze-zone estimation · temporal activity localization · model robustness**

This required thinking about the downstream machine-learning problem before the first video was recorded.

---

## Turning Research Definitions Into a Collection Protocol

Once the behavior classes were defined, they had to become instructions that participants could actually follow.

The collection process needed to be reasonably consistent across many participants while still producing natural variation.

I helped develop the activity protocol and participant instructions, including automated spoken instructions using text-to-speech where appropriate.

That allowed participants to move through predefined activities while the data-collection system recorded their behavior.

---

## Participant and Research Coordination

Dataset development also involved work outside model training.

I participated in the broader research process surrounding:

* Participant recruitment
* IRB-related data-collection requirements
* Scheduling and coordination
* Collection procedures
* Data organization

The SynDD work eventually covered a substantial collection of driver-monitoring video spanning many participants and multiple recordings per participant.

That scale created its own data-management challenges.

---

## From Raw Video to Research Dataset

The raw recordings were only the beginning.

To make the data usable for computer-vision experiments, I worked on processing workflows that transformed the recordings into structured research data.

The overall lifecycle looked roughly like:

```text
Participant recording
        ↓
Raw dashboard video
        ↓
Data organization
        ↓
Preprocessing / reduction
        ↓
Frame and clip preparation
        ↓
Annotation
        ↓
Quality checks
        ↓
Research-ready dataset
```

This work later supported multiple kinds of experiments rather than a single model.

---

## Annotation and Data Organization

A useful benchmark requires reliable labels.

The dataset therefore needed consistent mappings between recorded behavior and the labels used by machine-learning pipelines.

I worked on the preprocessing, reduction, organization, and annotation process required to turn long recordings into datasets that researchers could consume programmatically.

This experience influenced how I now think about machine learning:

> **Dataset design is part of model design.**

Choices made during collection and labeling determine what questions a model can meaningfully answer later.

---

## SynDD2 — Extending the Dataset

The second-generation SynDD dataset expanded the work to support additional driver-monitoring research, including gaze-related analysis.

Rather than starting from scratch, the later work built on lessons learned from the earlier dataset and collection process.

This included improving the organization and research utility of the data while maintaining a consistent framework for benchmarking.

---

## Supporting External Benchmarking

The datasets were not developed only for internal experiments.

They were used in connection with the **AI City Challenge** driver-behavior research community.

I also served as an evaluator for the driver-distraction / naturalistic-driving activity recognition track.

That provided a different perspective on dataset development:

I was not only thinking about whether our own models could use the data, but also whether the dataset and evaluation process were understandable and usable by other research teams.

---

## Why This Work Matters

Dataset papers can sometimes make data collection appear straightforward.

In practice, building a dataset requires coordinating many interdependent decisions:

```text
Research question
      ↓
Class definitions
      ↓
Collection protocol
      ↓
Participant instructions
      ↓
Recording
      ↓
Data management
      ↓
Preprocessing
      ↓
Annotation
      ↓
Quality control
      ↓
Benchmark
```

A mistake near the beginning can become extremely expensive later.

For example, unclear activity definitions can create ambiguous labels.

Poor file organization can make large-scale processing difficult.

A train/test split that ignores participant identity can produce misleading performance.

The SynDD projects gave me experience thinking about the entire machine-learning lifecycle rather than only the model-training stage.

---

## My Contributions

My work included:

**activity and gaze-zone definition → collection-protocol development → participant recruitment and coordination → data collection → preprocessing → data reduction → annotation workflows → benchmark preparation → downstream computer-vision experimentation**

I also used these datasets in later research involving driver distraction, gaze classification, pose modeling, video understanding, and robustness.

---

## Research Impact

The SynDD datasets supported work in areas including:

* Distracted-driving recognition
* Driver gaze estimation
* Temporal driver-activity localization
* Pose-based driver understanding
* Multimodal computer vision
* Research benchmarking

They also became the foundation for several of my later research projects, including my work on driver gaze understanding.

---

## What I Learned

This project changed the way I approach machine learning.

Before training a model, I now ask:

> What population does this dataset represent?

> What variation exists in the data?

> Are the labels actually measuring the concept we care about?

> Could the evaluation accidentally leak participant information?

> What conditions are missing?

> Will another researcher understand how this data was produced?

Those questions often matter as much as architecture selection.

---

## What This Project Demonstrates

**Dataset engineering** — building structured research datasets from raw multimodal video.

**Experimental design** — defining behaviors and collection protocols around downstream research questions.

**Research operations** — coordinating participants, collection procedures, processing, and annotation.

**Computer vision** — creating data specifically for driver-monitoring and video-understanding problems.

**Reproducibility** — organizing datasets and benchmarks so they can support research beyond a single experiment.

**Research leadership** — contributing across the complete dataset lifecycle rather than only consuming an existing dataset.

---

## Publications & Benchmark Use

The SynDD datasets were developed not only for internal research but also to support broader driver-monitoring benchmarking.

### Dataset Publications

**Synthetic Distracted Driving (SynDD1) Dataset for Analyzing Distracted Behaviors and Various Gaze Zones of a Driver**
*Data in Brief, 2023*
[DOI: 10.1016/j.dib.2022.108793](https://doi.org/10.1016/j.dib.2022.108793)

**Synthetic Distracted Driving (SynDD2) Dataset for Analyzing Distracted Behaviors and Various Gaze Zones of a Driver**
*arXiv, 2023*
[DOI: 10.48550/arXiv.2204.08096](https://doi.org/10.48550/arXiv.2204.08096)

### AI City Challenge

The datasets supported driver-behavior research associated with multiple editions of the **AI City Challenge**, including:

* **6th AI City Challenge — CVPR Workshops 2022**
* **7th AI City Challenge — CVPR Workshops 2023**
* **8th AI City Challenge — CVPR Workshops 2024**

I also served as an **evaluator for the Naturalistic Driving Action Recognition / driver-distraction track**, giving me experience with the dataset from both the development and benchmark-evaluation perspectives.

### Why This Matters

External benchmark use was important because it moved the dataset beyond a single research group.

It required thinking about whether:

* activity definitions were understandable to outside teams,
* the dataset organization was reproducible,
* evaluation protocols were sufficiently clear,
* labels were useful for independent model development,
* and the data could support research questions beyond the experiments for which it was originally collected.

---

[← Back to Portfolio](../README.md)
