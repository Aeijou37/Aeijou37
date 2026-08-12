# Hi, I'm Guojie Li 👋

I am a Master's student in Information and Communication Engineering, focusing on **Computer Vision**, **Industrial AI**, **Instance Segmentation**, **3D Reconstruction**, and **Point Cloud Processing**.

I am interested in applying deep learning and visual perception algorithms to real-world industrial scenarios.

---

## 🔬 Research & Engineering Interests

- Instance Segmentation
- Object Detection
- Single-view and Multi-view 3D Reconstruction
- RGB-D Vision
- Point Cloud Processing
- Industrial Defect Detection (EBeam / X-ray)
- Long-tail & Imbalanced Classification
- Self-supervised & Multimodal Pre-training (DINOv2 / CLIP / SigLIP)
- Lightweight Model Deployment
- RAG-based Local Knowledge Systems

---

## 🛠️ Technical Skills

### Programming Languages

- Python
- C++

### Deep Learning Frameworks

- PyTorch
- TensorFlow
- MMDetection
- Ultralytics YOLO
- timm

### Computer Vision

- YOLO Series
- SAM Series
- Instance Segmentation
- Object Detection
- 3D Reconstruction
- Point Cloud Feature Extraction
- RGB-D Perception

### Long-tail & Pre-training

- LDAM Loss
- DINOv2 / DINOv3
- CLIP / SigLIP
- Fine-tuning Strategies (Layer Freezing)

### AI Agent & RAG

- LangChain
- Chroma
- Local LLM Deployment
- Prompt Engineering
- Multi-document Retrieval

---

## 💼 Experience

### CXMT — Deep Learning Algorithm Intern (2026.07 - Present)

EBeam wafer defect classification (5 classes, extreme long-tail — minority class only 2.9% of samples, 362 test images). Ran **29 controlled experiments** across 12 backbones (ConvNeXt / ResNet / ViT) and 4 pretraining paradigms (DINOv2 / DINOv3 / CLIP / SigLIP), plus Optuna AutoML search. Lifted accuracy **97.79% → 100.00%** (0 errors) via LDAM loss → DINOv2/SigLIP dual-track pretraining → knowledge distillation (25M ResNet50 Student surpassed 93M SigLIP Teacher). Settled a methodology — **"gentle guidance beats brute force on small long-tail data"** — where 8 aggressive strategies (DRW / SupCon / MIM / CLAHE / TTA / etc.) all failed, while structural compensation and external knowledge transfer won. FP16 inference throughput 609 img/s surpassed ResNet50.

> Deep-dive note: [EBeam Wafer Defect Classification — A Long-Tail Breakthrough](https://github.com/Aeijou37/cv-algorithm-notes/blob/main/articles/01-cxmt-wafer-defect-classification.md)

### iFLYTEK — Industrial AI Algorithm Engineer Intern (2026.05 - 2026.07)

Automated X-ray film evaluation for industrial NDT (small sample, ultra-large images, 10 defect classes). Built a two-stage pipeline: joint image enhancement for small-defect recall + RF-DETR optimization (mAP +1.8%), then a rule-based defect-distribution → workpiece-grade mapping. Owned the full loop from data augmentation to qualitative-rule validation.

> ⚠️ Code unavailable due to company NDA. Happy to discuss the technical approach in detail.

### Anhui Huipeng New Energy — Engineering Intern (2023.08 - 2023.09)

Hands-on with new-energy commercial vehicle swappable-chassis battery systems, electrical architecture, BMS safety, and smart swap-station operations. Built cross-domain engineering context for vision-sensing and perception-algorithm deployment.

---

## 🚀 Selected Projects

### Vision-based Shoe Sole Gluing Robot System

This project focuses on low-cost and high-precision visual perception for automated shoe sole gluing production lines.

Main work:

- Designed lightweight instance segmentation models for shoe sole localization.
- Built RGB-D based perception pipelines for industrial visual guidance.
- Developed 3D reconstruction and point cloud processing methods.
- Extracted smooth and continuous 3D gluing trajectories based on geometric analysis.
- Optimized model inference for real-time industrial deployment.

Results:

- Achieved over 99% recognition accuracy.
- Reached gluing trajectory positioning accuracy within 1 mm.
- Completed the full pipeline from data collection, algorithm development, to production-line validation.
- 2 granted patents (as first & second author).

> 🔗 Code available upon request (university project, pending advisor approval)

---

### Industrial X-ray Defect Detection and Analysis System

This project focuses on automated film evaluation for industrial X-ray non-destructive testing.

Main work:

- Designed image preprocessing and enhancement methods for large-resolution X-ray images.
- Improved small-defect detection under small-sample conditions.
- Optimized RF-DETR detection and segmentation models (mAP +1.8%).
- Built a rule-based pipeline from defect-level results to workpiece-level qualitative assessment.

> ⚠️ Code unavailable due to company NDA. Happy to discuss the technical approach in detail.

---

### Local Academic Knowledge Base QA Agent Based on RAG

This project aims to build a local academic document question-answering system with optional retrieval enhancement.

Main work:

- Built document parsing, embedding, vector storage, and retrieval pipelines using LangChain and Chroma.
- Implemented multi-document retrieval, MMR retrieval, query rewriting, and source tracing.
- Designed constrained system prompts and post-processing mechanisms to improve response quality.
- Supported local model deployment and multi-turn academic document QA.

> 🔗 Repository: [rag-academic-qa-agent](https://github.com/Aeijou37/rag-academic-qa-agent)

---

## 📝 Technical Deep-Dive Notes

I write each project as a long-form note structured as **Problem → Baseline → Method → Ablation → Lessons** — including the experiments that *failed* and why. Interviewers care less about what I did and more about **why I tried it, where it failed, and where it worked**.

Repo: [**cv-algorithm-notes**](https://github.com/Aeijou37/cv-algorithm-notes)

- [EBeam Wafer Defect Classification — A Long-Tail Breakthrough](https://github.com/Aeijou37/cv-algorithm-notes/blob/main/articles/01-cxmt-wafer-defect-classification.md) — 97.79% → 100.00% via LDAM + DINOv2/SigLIP + distillation; 8 failed strategies documented.
- *Coming: iFLYTEK X-ray two-stage evaluation / Shoe-robot vision & 3D / RAG agent.*

---

## 📚 Publications & Patents

- Patent (First Inventor, published): Vision-based single-line laser shoe sole 3D gluing contour extraction system and method. [CN120852582A](https://patents.google.com/patent/CN120852582A)
- Patent (Second Inventor, granted): Point cloud generation method for shoe sole gluing area based on RGB-D instance segmentation. [CN120823398B](https://patents.google.com/patent/CN120823398B)
- Paper (First Author, under review): Instance Segmentation Network Based on Dynamic Routing and Topological Aggregation.

> 📌 Patent application numbers: CN202511339618.5 / CN202511331565.2

---

## 🎓 Education

### Anhui University

M.S. in Information and Communication Engineering
Research Direction: Image Processing / Computer Vision
2024.09 - 2027.06

### Anhui University

B.Eng. in Electronic Information Engineering
2020.09 - 2024.06

Graduation Project: Point-wise Rotation-invariant Feature Extraction for Point Clouds

---

## 🔭 Currently Working On

- EBeam wafer defect classification at CXMT (LDAM + DINOv2/SigLIP + distillation, 100.00% accuracy)
- Single-view 3D reconstruction for industrial trajectories
- RAG-based academic QA agent (LangChain + Chroma)
- Lightweight model deployment for edge devices

---

## 📊 GitHub Stats

[![](https://camo.githubusercontent.com/49f1d5cd61fd8ce52f29f43fdf3bbe070c51d3484823b3fcff6c7184e0e6a352/68747470733a2f2f6769746875622d726561646d652d73746174732e76657263656c2e6170702f6170692f746f702d6c616e6775616765732f3f757365726e616d653d4165696a6f753337266c61796f75743d636f6d70616374267468656d653d64656661756c74)](https://camo.githubusercontent.com/49f1d5cd61fd8ce52f29f43fdf3bbe070c51d3484823b3fcff6c7184e0e6a352/68747470733a2f2f6769746875622d726561646d652d73746174732e76657263656c2e6170702f6170692f746f702d6c616e6775616765732f3f757365726e616d653d4165696a6f753337266c61796f75743d636f6d70616374267468656d653d64656661756c74)
[![](https://camo.githubusercontent.com/d29801f1142c53a550eda52f0885da8ddfc0d1ea7ed7c3b723a0f56a998d81a0/68747470733a2f2f6769746875622d726561646d652d73746174732e76657263656c2e6170702f6170693f757365726e616d653d4165696a6f7533372673686f775f69636f6e733d74727565267468656d653d64656661756c74)](https://camo.githubusercontent.com/d29801f1142c53a550eda52f0885da8ddfc0d1ea7ed7c3b723a0f56a998d81a0/68747470733a2f2f6769746875622d726561646d652d73746174732e76657263656c2e6170702f6170693f757365726e616d653d4165696a6f7533372673686f775f69636f6e733d74727565267468656d653d64656661756c74)

---

## 📫 Contact

- GitHub: [Aeijou37](https://github.com/Aeijou37)
- Email: [Leeguojiea@gmail.com](mailto:Leeguojiea@gmail.com)

> Always open to discussions on industrial AI, computer vision, and RAG systems.

## About

No description, website, or topics provided.
