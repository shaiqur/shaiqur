# Driver-View Car-Following Prototype

[← Back to Portfolio](../README.md)

## Overview

An exploratory computer-vision pipeline for identifying candidate
car-following periods from forward-facing driving video.

The system uses YOLOv8 vehicle detections together with a
camera-specific trapezoidal region of interest (ROI) and temporal
occupancy analysis to identify periods where a vehicle remains in
the forward driving region.

## What I Built

- Integrated YOLOv8 for car, bus, and truck detection.
- Designed a camera-specific trapezoidal ROI for forward-road analysis.
- Computed vehicle centroid and bounding-box area features.
- Developed temporal occupancy logic for candidate car-following periods.
- Generated CSV summaries and optional annotated videos.
- Built an AWS S3/SageMaker workflow for batch video processing.
- Modularized the pipeline into detection, geometry, temporal analysis,
  visualization, and cloud-processing components.

## Pipeline

Driver-view video → YOLOv8 detection → vehicle filtering →
ROI geometry → temporal occupancy analysis → candidate
car-following periods

## Technologies

Python · YOLOv8 · OpenCV · Pandas · AWS S3 · SageMaker

## Current Scope

This is an exploratory prototype. The current method uses image-space
ROI occupancy rather than calibrated inter-vehicle distance or
time-headway estimation.

The ROI is camera-specific and must be configured for the video source.

Future directions include vehicle tracking, lane-aware association,
depth estimation, and more advanced temporal modeling.

## Code

[View Source Code on GitHub](https://github.com/shaiqur/driver-view-car-following)

---

[← Back to Portfolio](../README.md)
