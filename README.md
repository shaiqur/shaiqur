# Hi, I'm Mohammed Shaiqur Rahman 👋

### Applied AI / Computer Vision Researcher · Research Software & ML Engineer

**Ph.D. Candidate in Computer Science @ Iowa State University — December 2026**

I build **computer-vision and machine-learning systems, research datasets, cloud-based research platforms, and large-scale data workflows**.

My work sits at the intersection of **AI research and practical engineering**: developing models and evaluation methods, building the data and infrastructure they depend on, and debugging the real systems required to make them usable.

[LinkedIn](https://www.linkedin.com/in/shaiqur) · [GitHub](https://github.com/shaiqur) · [shaiqur@iastate.edu](mailto:shaiqur@iastate.edu)

---

## What I Work On

🔬 **Applied AI & Computer Vision**
Multimodal driver monitoring, gaze understanding, pose-based reasoning, temporal video analysis, NLP, and robustness evaluation.

☁️ **Research Software & Cloud Systems**
Secure AWS research platforms, SageMaker environments, Dockerized ML workflows, access-controlled research data, CI/CD, and production troubleshooting.

📊 **Data & ML Engineering**
Large-scale PostgreSQL datasets, heterogeneous sensor/data integration, multi-terabyte research workflows, ETL, video processing, and reproducible ML pipelines.

🎓 **Teaching & Mentoring**
Programming, software engineering, capstone projects, distributed systems, and graduate research mentoring.

---

# Featured Work

## 🔐 Deep Insight — Secure AWS Research Platform

**Problem:** Researchers needed access to SageMaker and restricted project data without broad visibility into unrelated AWS resources or other researchers' environments.

**My work:**

* Helped build a secure portal providing researchers controlled access to assigned SageMaker environments.
* Implemented project-based authentication and authorization using AWS services including Cognito, IAM, S3, Lambda, and DynamoDB.
* Automated research-environment initialization, authorized data provisioning, and idle notebook shutdown.
* Supported researcher onboarding and became the lab's primary point of contact for AWS/SageMaker infrastructure and troubleshooting.
* Identified client-side AWS credential exposure and helped redesign privileged operations so they executed through IAM-controlled backend services rather than the browser.

**Outcome:** Reduced unnecessary SageMaker compute cost by approximately **30%** while improving researcher isolation, onboarding, and reproducibility.

**Stack:** `AWS` `SageMaker` `S3` `IAM` `Lambda` `Cognito` `DynamoDB` `Next.js` `TypeScript` `Docker`

➡️ [Read the Deep Insight case study](projects/ai-platform.md)

---

## 👁️ Multimodal Driver Monitoring & Gaze Understanding

My Ph.D. research examines how complementary visual and geometric information can improve driver-monitoring systems.

The work combines:

* visual appearance representations,
* context-enriched information,
* pose-derived geometric reasoning,
* temporal information,
* multimodal fusion, and
* robustness analysis across participants and deployment conditions.

A major focus is understanding **what information a model needs to retain** and whether strong subject-independent performance continues to hold when vehicles, cameras, appearance conditions, or other aspects of the deployment environment change.

The current work evaluates **nine-zone driver gaze understanding** using subject-independent and cross-domain protocols.

**Stack:** `PyTorch` `OpenCV` `ResNet` `YOLO` `Pose Estimation` `Multimodal Learning` `Temporal Modeling`

📄 Manuscript in preparation.

➡️ [Read the driver-gaze research overview](projects/gaze-detection.md)

---

## 🌱 SoilSerdem — Full-Stack Scientific Processing Platform

Worked as a **Full Stack Developer** on a cloud-based platform supporting scientific and geospatial data-processing workflows.

**My work included:**

* full-stack application development,
* backend APIs and relational data models,
* authentication and hierarchical access control,
* scientific file-upload and processing workflows,
* Dockerization of **four scientific/GIS workflows** using GDAL, GRASS GIS, and SAGA GIS,
* AWS-based on-demand processing,
* CI/CD and production deployment.

One production constraint was a low-memory EC2 host that could not reliably compile the application. Instead of increasing server capacity, I moved application compilation into **GitHub Actions** and deployed only the production artifacts.

I also diagnosed a production backend failure caused by differences between development assumptions and the actual production database state, using deployment logs, rollback, correction, and redeployment.

**Stack:** `Next.js` `TypeScript` `Node.js` `Prisma` `SQL` `Docker` `AWS` `GitHub Actions` `NGINX` `PM2` `GDAL` `GRASS GIS` `SAGA GIS`

➡️ [Read the software/cloud case study](projects/webCreation.md)

---

# Research & Open Data

## 🚗 SynDD1 / SynDD2

Led major portions of the lifecycle for open driver-monitoring datasets spanning:

* **99 participants**
* **396 videos**
* distracted-driving behaviors,
* driver gaze,
* pose,
* temporal behavior analysis, and
* multimodal driver-monitoring research.

My contributions included activity/gaze taxonomy design, research protocols, participant recruitment, data collection, preprocessing, annotation, reduction, quality control, and benchmark preparation.

The datasets have supported research associated with the **6th, 7th, and 8th AI City Challenges**.

I also served as an evaluator for the Naturalistic Driving Action Recognition / driver-distraction track.

---

## 🎥 DeepLocalization

**First author — CVPR Workshops 2024**

*DeepLocalization: Using Change Point Detection for Temporal Action Localization*

Investigated temporal localization of driver activities in long videos using pose-based representations and change-point detection.

I led development and Dockerization of the inference/experimental workflow for reproducible evaluation.

➡️ [Read more about the pose/video workflow](projects/yolopose-detection.md)

---

## 📝 Crash Narrative NLP

Developed the **BERT-based NLP analysis** for research studying inconsistencies between free-text crash narratives and structured seatbelt records.

* Fine-tuned and evaluated BERT-based classifiers.
* Achieved approximately **89% classification accuracy**.
* Used narrative information to help identify potential mismatch in structured crash records.

**Accepted:** Road Safety and Simulation Conference, 2026.

---

# Data & ML Engineering

Alongside model development, much of my work has involved building the data systems required to support research.

### Large-scale analytical data

* Integrated GPS, sensor, participant, vehicle, trip, roadway, and related research data from heterogeneous sources.
* Aligned data at approximately **one-second resolution**.
* Built a PostgreSQL analytical dataset containing approximately **30 million rows and 60+ columns**.
* Built another sensitive research dataset exceeding **70 million rows**.
* Implemented project-specific database access controls.

### Multi-terabyte research workflows

* Automated on-premises TrueNAS → AWS S3 synchronization.
* Built large-scale S3 retrieval and processing workflows.
* Supported video/frame extraction and cloud-based computer-vision processing.
* Built Dockerized ML inference environments using AWS ECR and SageMaker.

---

# Teaching & Mentoring

Teaching has been an important part of my time at Iowa State University.

Courses supported include:

* **COM S 104** — Introduction to Python
* **COM S 227** — Object-Oriented Programming
* **COM S 309** — Software Development Practices
* **COM S 402C** — Senior Design / Capstone
* **COM S 510** — Distributed Software Development
* **COM S 599** — Graduate Creative Component / Research

I have mentored **100+ undergraduate and graduate students**, including capstone and research teams.

My teaching work has included:

* curriculum and assessment development,
* quizzes, labs, exam material, and grading rubrics,
* debugging and code reviews,
* software architecture and API design,
* databases and cloud deployment,
* capstone project mentoring,
* graduate research guidance.

🏆 **Teaching Excellence Award — Iowa State University, COM S 309, Spring 2021**

---

# Selected Publications

### DeepLocalization: Using Change Point Detection for Temporal Action Localization

**First Author — IEEE/CVF CVPR Workshops, 2024**
DOI: `10.1109/CVPRW63382.2024.00721`

### Synthetic Distracted Driving (SynDD1) Dataset for Analyzing Distracted Behaviors and Various Gaze Zones of a Driver

**First Author — Data in Brief, 2023**
DOI: `10.1016/j.dib.2022.108793`

### Synthetic Distracted Driving (SynDD2) Dataset for Analyzing Distracted Behaviors and Various Gaze Zones of a Driver

**First Author — 2023**
DOI: `10.48550/arXiv.2204.08096`

### Deep Insight: A Cloud-Based Big Data Analytics Platform for Naturalistic Driving Studies

**International Journal of Automotive Engineering, 2023**

### Improving Crash Data Accuracy by Identifying Seatbelt Inference Mismatch Using NLP and Behavioral Modeling

**Accepted — Road Safety and Simulation Conference, 2026**
My contribution: BERT-based NLP modeling and evaluation.

---

# Technical Toolbox

**Programming**
`Python` `Java` `SQL` `TypeScript` `JavaScript` `R` `Shell`

**Machine Learning & Computer Vision**
`PyTorch` `OpenCV` `scikit-learn` `CNNs` `ResNet` `YOLO` `Pose Estimation` `BERT` `Transformers` `Multimodal Learning` `Temporal Modeling`

**Data**
`PostgreSQL` `pandas` `NumPy` `ETL` `Relational Data Modeling` `Large-Scale Data Processing`

**Cloud & ML Systems**
`AWS SageMaker` `S3` `EC2` `Lambda` `IAM` `Cognito` `RDS` `ECR` `DataSync` `Batch/Fargate`

**Software & DevOps**
`Next.js` `React` `Node.js` `Express` `Docker` `GitHub Actions` `CI/CD` `Linux` `NGINX` `PM2` `Git`

---

# Earlier Professional Experience

## IBM India Private Limited

**System Engineer / Associate System Engineer · 2011–2016**

Worked on enterprise integration and production systems using IBM Message Broker, IBM MQ, Java, and database-backed applications.

Experience included application migrations, CSV/data-ingestion workflows, functional testing, staged releases, production incident response, and scheduled on-call support.

🏆 **IBM “Putting Clients First” Award — 2015**

---

# Explore More

This profile is intentionally a summary. Individual project pages contain deeper technical context, architecture decisions, constraints, debugging stories, and lessons learned.

* 🔐 [Secure AI / AWS Research Platform](projects/ai-platform.md)
* 👁️ [Driver Gaze & Multimodal Vision](projects/gaze-detection.md)
* 🌱 [Full-Stack / Scientific Processing Platform](projects/webCreation.md)
* 🎥 [Pose & Driver-Behavior Processing](projects/yolopose-detection.md)
* 📚 [Publications](publications/)
* 🎓 [Teaching](teaching/)

---

## Let's Connect

I am interested in opportunities involving:

**Computer Vision · Applied Machine Learning · Data Science · Research Software · ML Platforms · Cloud Engineering**

📧 [shaiqur@iastate.edu](mailto:shaiqur@iastate.edu)
🔗 [LinkedIn](https://www.linkedin.com/in/shaiqur)
