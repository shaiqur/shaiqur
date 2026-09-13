[← Back to Portfolio](../README.md)

# DeepLocalization — Temporal Action Localization in Driver Videos

**Published at CVPR Workshops 2024**

**Role:** Researcher / Computer Vision Engineer
**Focus:** Video Understanding · Pose Estimation · Temporal Localization · Change-Point Detection

---

## The Problem

Recognizing an activity in a short video clip is one problem.

Finding **when that activity begins and ends inside a longer video** is a different and more difficult problem.

In driver-monitoring video, a recording may contain a sequence such as:

```text
Driving normally
      ↓
Reaching for an object
      ↓
Using a phone
      ↓
Returning attention to the road
```

A traditional video classifier might tell us that a distracted-driving activity appears somewhere in the video.

But many real applications require:

> **Where exactly did the activity occur?**

That is the temporal action localization problem.

---

## The Research Question

Instead of analyzing every frame independently, our work investigated whether changes in the driver's pose and behavior could help identify meaningful boundaries between activities.

The central idea was:

> **A change in human behavior should often produce a detectable change in the temporal pattern of pose information.**

This led us to combine pose-based representations with **change-point detection**.

---

# From Video to Pose Representation

The first stage involved extracting human pose information from the video.

A YOLO-based pose-estimation model detected body keypoints for each frame.

Conceptually:

```text
Driver video
     ↓
Video frames
     ↓
YOLO pose estimation
     ↓
Frame-level keypoints
     ↓
Temporal pose representation
```

Rather than treating raw image appearance as the only signal, pose provided a more structured description of how the driver's body was changing over time.

---

# Why Pose?

Different distracted-driving activities often involve characteristic body movements.

Examples might include:

* reaching toward another part of the vehicle,
* moving a hand toward the face,
* turning the torso,
* changing arm configuration,
* interacting with an object.

These changes can produce temporal structure in the pose sequence.

That made pose a useful signal for asking:

> **Has the driver's behavior changed enough that we may have entered a new activity?**

---

# Detecting Behavioral Transitions

Once pose information had been extracted, the next challenge was locating transitions.

Instead of requiring frame-by-frame manual reasoning, we applied **change-point detection** to the temporal representation.

Conceptually:

```text
Pose sequence over time

───────────────╲
                ╲
                 ───────────────
                                ╲
                                 ───────────

                 ↑
            possible behavior
               transition
```

A detected change point represented a location in the video where the underlying behavioral pattern changed significantly.

These points could then be used as candidate boundaries between activities.

---

# Why Change-Point Detection?

A straightforward approach to temporal localization might require predicting an action label for every frame and then trying to infer boundaries from noisy predictions.

Change-point detection provides a different perspective.

Instead of initially asking:

> Which activity is happening at this frame?

we can first ask:

> **When does the behavior change?**

That separates the problem into two parts:

```text
Long video
   ↓
Find meaningful temporal boundaries
   ↓
Create candidate activity segments
   ↓
Interpret / classify the segments
```

This can reduce the search space for downstream activity understanding.

---

# From Change Points to Temporal Segments

Once meaningful transitions were detected, the longer video could be divided into shorter candidate segments.

For example:

```text
Full video
│
├── Segment 1
│
├── Segment 2
│
├── Segment 3
│
└── Segment 4
```

Each segment represented a period during which the driver's behavior was comparatively consistent.

Those segments could then be analyzed independently.

---

# Adding Higher-Level Video Understanding

The project also explored higher-level interpretation of the generated video segments.

The broader pipeline combined:

* Pose estimation
* Temporal change detection
* Segment generation
* Video/activity interpretation

This allowed us to investigate a hybrid approach in which structured motion information identified **where something changed**, while downstream video understanding helped interpret **what happened during that segment**.

---

# My Contribution

My work included substantial engineering around the computer-vision and inference pipeline.

I worked on:

* Preparing the video-processing workflow
* Integrating pose estimation
* Building and testing inference pipelines
* Packaging the environment using Docker
* Supporting reproducible execution
* Running experiments on driver-monitoring video
* Evaluating the temporal localization workflow
* Helping integrate change-point-based segmentation with downstream analysis

One important part of my contribution was making the research pipeline reproducible enough to execute consistently rather than remaining a collection of manually configured experiments.

---

# Engineering the Research Pipeline

Research code frequently depends on many libraries, model versions, system packages, and runtime assumptions.

To reduce environment inconsistencies, I worked on containerizing the inference pipeline.

Conceptually:

```text
Video data
    ↓
Dockerized inference environment
    ↓
Pose estimation
    ↓
Temporal feature generation
    ↓
Change-point detection
    ↓
Candidate segments
    ↓
Downstream interpretation
```

This made experiments easier to reproduce and execute across computing environments.

---

# Why This Was Interesting

The project brought together two different ways of thinking about video.

### Computer Vision

Extract meaningful information about the driver's pose and behavior.

### Time-Series / Temporal Reasoning

Determine where the statistical pattern of that behavior changes.

Rather than asking a deep network to solve the entire problem in one step, the pipeline decomposed temporal localization into interpretable stages.

---

# What I Learned

DeepLocalization reinforced several ideas that influenced my later work.

### Video is not just a collection of images

Adjacent frames are related, and changes over time can contain information that is invisible when frames are treated independently.

### Intermediate representations can be valuable

Pose provides a structured representation that can sometimes make temporal behavior easier to reason about than raw pixels.

### Localization and classification are different problems

Knowing **what** happened does not automatically tell us **when** it happened.

### Hybrid methods are still useful

Deep learning does not need to replace every component of a system.

Combining learned visual representations with classical temporal algorithms such as change-point detection can sometimes produce useful and interpretable pipelines.

---

# Architecture Overview

```mermaid
flowchart LR

    VIDEO[Driver Video]
        --> FRAME[Frame Processing]

    FRAME
        --> POSE[YOLO Pose Estimation]

    POSE
        --> SERIES[Temporal Pose Representation]

    SERIES
        --> CP[Change-Point Detection]

    CP
        --> SEG[Candidate Video Segments]

    SEG
        --> UNDERSTAND[Video / Activity Interpretation]

    UNDERSTAND
        --> OUTPUT[Temporal Activity Localization]
```

---

# What This Project Demonstrates

### Video Understanding

Reasoning about activities across time rather than treating frames independently.

### Pose Estimation

Using human keypoints as a structured behavioral representation.

### Temporal Modeling

Applying change-point detection to discover meaningful behavioral transitions.

### Research Engineering

Turning experimental components into a reproducible processing pipeline.

### Hybrid AI Systems

Combining computer-vision models with classical temporal-analysis techniques.

### Reproducibility

Using containerized environments to make complex inference workflows easier to execute consistently.

---

# Publication

**DeepLocalization: Using Change Point Detection for Temporal Action Localization**
Mohammed Shaiqur Rahman, I. F. Shihab, L. Chu, and A. Sharma
*IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshops (CVPRW), 2024*

[DOI: 10.1109/CVPRW63382.2024.00721](https://doi.org/10.1109/CVPRW63382.2024.00721)


---

[← Back to Portfolio](../README.md)
