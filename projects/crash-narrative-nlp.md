[← Back to Portfolio](../README.md)

# Crash Narrative NLP — Identifying Seatbelt Record Mismatches

**Role:** NLP / Machine Learning Researcher
**Focus:** BERT · Text Classification · Crash Data Quality · Model Evaluation

## The Problem

Crash databases often contain both:

* structured fields, and
* free-text crash narratives.

Those two sources do not always agree.

One example involves **seatbelt-use information**.

A structured crash record may indicate one value, while the officer's narrative may describe something different.

That creates a data-quality problem for researchers and agencies that rely on structured crash records for analysis.

The research question became:

> **Can natural-language processing help identify records where the narrative and structured seatbelt information may be inconsistent?**

---

## My Contribution

My contribution to the project focused specifically on the **BERT-based NLP analysis**.

I worked on:

* Preparing narrative text for modeling
* Fine-tuning BERT-based classifiers
* Evaluating model performance
* Comparing predictions with structured crash information
* Supporting analysis of likely mismatch cases

The broader study also contained behavioral and crash-data analysis performed by the research team; my primary responsibility was the NLP component.

---

## Approach

Conceptually, the workflow was:

```text
Crash narrative
      ↓
Text preprocessing
      ↓
Fine-tuned BERT model
      ↓
Seatbelt-related prediction
      ↓
Compare against structured crash field
      ↓
Potential mismatch identified
```

Rather than manually reading every crash narrative, the NLP model provided a scalable way to identify records that deserved additional review.

---

## Result

The BERT-based analysis achieved approximately **89% classification accuracy** on the crash-narrative task.

The larger value, however, was not simply the accuracy number.

The work demonstrated how unstructured text could be used as a **secondary source of evidence for validating structured transportation records**.

---

## Why This Matters

Transportation databases are often treated as though structured fields are automatically correct.

But free-text narratives may contain information that reveals:

* coding inconsistencies,
* ambiguous records,
* or possible data-entry errors.

NLP can help surface those cases without requiring analysts to manually inspect every report.

---

## What This Project Demonstrates

**Natural Language Processing** — fine-tuning transformer-based language models on domain-specific text.

**Applied Machine Learning** — using ML to solve a practical data-quality problem rather than classification for its own sake.

**Research Evaluation** — assessing model predictions in the context of structured transportation records.

**Interdisciplinary Research** — applying computer-science methods to transportation-safety data.

---

## Publication

**Improving Crash Data Accuracy by Identifying Seatbelt Inference Mismatch Using NLP and Behavioral Modeling**

*Road Safety and Simulation Conference, 2026*

My contribution focused on the **BERT-based NLP modeling and analysis**.
---

[← Back to Portfolio](../README.md)
