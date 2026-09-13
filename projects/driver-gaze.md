[← Back to Portfolio](../README.md)

# Multimodal Driver Gaze Understanding

**Ph.D. Research — Work in Progress**
**Computer Vision · Driver Monitoring · Multimodal Learning · Robustness**

## The Problem

Driver gaze is an important signal for understanding attention and distraction, but estimating gaze from an in-cabin camera remains difficult.

Changes in driver appearance, head orientation, occlusion, camera placement, and vehicle configuration can all affect model performance.

My research asks a broader question than simply:

> **Can a neural network classify where the driver is looking?**

I am investigating:

> **What visual and anatomical information should a driver-monitoring system preserve in order to understand gaze reliably?**

---

## Research Direction

My work explores complementary information at multiple anatomical scales, including:

* Head and upper-body visual context
* Periocular / eye-region information
* Pose-derived geometric relationships
* Temporal information across video
* Multimodal model fusion

Rather than evaluating only a final model, I use controlled experiments to understand **which sources of information contribute, when they help, and where they fail**.

---

## Evaluation

The research uses infrared driver-monitoring video and evaluates nine gaze zones using **subject-independent splits**, ensuring that validation participants are not seen during training.

The work also examines robustness across:

* Different participants
* Appearance conditions
* Temporal sequences
* Different vehicle and camera configurations

The current multimodal system achieves approximately **86% subject-independent gaze-zone classification accuracy**.

However, an important part of the research is understanding what happens when the deployment environment changes.

Cross-vehicle experiments show that strong performance on unseen drivers does **not necessarily imply strong generalization to unseen vehicle/camera configurations**.

That domain-shift problem is one of the directions I am actively investigating.

---

## Why This Research Matters

A driver-monitoring model may perform well in a conventional validation experiment while still relying on cues specific to:

* A particular camera placement
* Vehicle geometry
* Participant appearance
* Dataset-specific conditions

My research therefore focuses not only on improving classification performance, but also on understanding **what information the model uses and whether those representations remain useful when conditions change**.

---

## My Work

My contributions span:

**dataset preparation → computer-vision preprocessing → model development → pose-based geometric modeling → multimodal learning → temporal analysis → controlled ablation studies → robustness evaluation → error analysis**

The work builds on the SynDD driver-monitoring datasets that I helped develop at Iowa State University.

---

## Current Status

**Manuscript in preparation.**

Detailed experimental methodology and results will be made available following publication.

---

## Technologies

Python · PyTorch · OpenCV · ResNet · YOLO-based pose estimation · multimodal learning · temporal modeling

---

## Research Themes

**Driver Monitoring**
Understanding driver attention from in-cabin video.

**Context-Aware Vision**
Studying how local and global anatomical context affect visual recognition.

**Multimodal Learning**
Combining visual appearance and explicit geometric representations.

**Robustness & Generalization**
Testing whether models remain reliable across participants and deployment environments.
---

[← Back to Portfolio](../README.md)
