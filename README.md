# Hi, I'm Guojie Li 👋

I am a Master's student in Information and Communication Engineering, focusing on **Computer Vision**, **Industrial AI**, **3D Vision**, **Multimodal VLM**, **RAG Systems**, and **Edge Deployment**.

I am interested in applying deep learning and visual perception algorithms to real-world industrial scenarios — from defect classification to 3D reconstruction to edge deployment.

---

## 🔬 Research & Engineering Interests

- Instance Segmentation & Object Detection
- 3D Reconstruction & Point Cloud Processing
- RGB-D Vision & Camouflaged Segmentation
- Industrial Defect Detection (EBeam / X-ray)
- Long-tail & Imbalanced Classification
- Multimodal Vision-Language Models (VLM)
- RAG-based Local Knowledge Systems
- Edge Deployment (ONNX / INT8 Quantization)

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
- Point Cloud Processing (PointNet)
- RGB-D Perception

### Long-tail & Pre-training

- LDAM Loss
- DINOv2 / DINOv3
- CLIP / SigLIP
- Knowledge Distillation
- Fine-tuning Strategies (Layer Freezing)

### AI Agent & RAG

- LangChain
- Chroma
- CLIP Cross-modal Retrieval
- Local LLM Deployment (Qwen)
- Prompt Engineering
- MMR Retrieval & Query Rewriting

### Edge Deployment

- PyTorch → ONNX Export
- INT8 Dynamic Quantization
- ONNX Runtime Inference
- Model Lightweighting

---

## 💼 Experience

### CXMT — Deep Learning Algorithm Intern (2026.07 - Present)

EBeam wafer defect classification (5 classes, extreme long-tail — minority class only 2.9% of samples, 362 test images). Ran **29 controlled experiments** across 12 backbones (ConvNeXt / ResNet / ViT) and 4 pretraining paradigms (DINOv2 / DINOv3 / CLIP / SigLIP), plus Optuna AutoML search. Lifted accuracy **97.79% → 100.00%** (0 errors) via LDAM loss → DINOv2/SigLIP dual-track pretraining → knowledge distillation (25M ResNet50 Student surpassed 93M SigLIP Teacher). Settled a methodology — **"gentle guidance beats brute force on small long-tail data"** — where 8 aggressive strategies (DRW / SupCon / MIM / CLAHE / TTA / etc.) all failed, while structural compensation and external knowledge transfer won. FP16 inference throughput 609 img/s surpassed ResNet50.

> Deep-dive note: [EBeam Wafer Defect Classification — A Long-Tail Breakthrough](https://github.com/Aeijou37/cv-algorithm-notes/blob/main/articles/01-cxmt-wafer-defect-classification.md)

### iFLYTEK — Industrial AI Algorithm Engineer Intern (2026.05 - 2026.07)

Industrial X-ray NDT automated film evaluation (~500 ultra-large images >2000×2000, 10 defect classes merged to 3 for viable baseline). Built a two-stage pipeline: Stage 1 — AHTF adaptive high-overlap tiling + YOLO26-Seg with SDE/DAF modules (B-class Mask Recall +21%, 0.238→0.288); Stage 2 — rule-based defect-distribution → workpiece-grade mapping. Early Mask R-CNN baseline (mAP 6.8%) and Boundary-aware Loss both abandoned after rigorous ablation. Settled methodology: **data strategy > model enhancement > loss function** for large-image small-defect tasks. FP16 deployable; Qt review software prototype delivered.

> Deep-dive note: [Industrial X-ray Defect Detection — Two-Stage Pipeline](https://github.com/Aeijou37/cv-algorithm-notes/blob/main/articles/02-iflytek-xray-defect-detection.md)
> ⚠️ Code unavailable due to company NDA. Happy to discuss the technical approach in detail.

### Anhui Huipeng New Energy — Engineering Intern (2023.08 - 2023.09)

Hands-on with new-energy commercial vehicle swappable-chassis battery systems, electrical architecture, BMS safety, and smart swap-station operations. Built cross-domain engineering context for vision-sensing and perception-algorithm deployment.

---

## 🚀 Selected Projects

### Multimodal RAG Academic QA Agent

A **multimodal** academic document question-answering agent. Upload papers → ask questions with **text or image** → get answers with source tracing. PDF charts/figures are automatically extracted, described by VLM, and indexed via CLIP for cross-modal retrieval.

- **Multimodal**: PDF image extraction + VLM description + CLIP cross-modal encoding
- **Retrieval**: MMR (similarity + diversity) + query rewriting (dual-path merge)
- **Generation**: chat_template for instruction leakage prevention + constrained prompt + post-processing
- **Source tracing**: Every answer includes document name + page/paragraph reference
- Fully local, no external API needed

> 🔗 Repository: [rag-academic-qa-agent](https://github.com/Aeijou37/rag-academic-qa-agent)

---

### Industrial Defect Multimodal Diagnosis Agent

Upgrades traditional defect classification (output: class label) to natural language **diagnosis report generation** (output: type + location + severity + cause + recommendation). Based on CXMT defect classification experience.

- **Data**: NEU-DET steel defect dataset + domain-knowledge-based templated diagnosis labels
- **VLM**: Qwen-VL-Chat + LoRA fine-tuning (r=8)
- **Hallucination control**: 3-layer protection (input quality check + constrained prompt + output post-processing)
- **Evaluation**: 3D framework (classification accuracy + location accuracy + hallucination rate)
- **Comparison experiment**: Pure classification (ResNet50) vs VLM diagnosis, proving business value of VLM diagnosis

> 🔗 Repository: [defect-diagnosis-agent](https://github.com/Aeijou37/defect-diagnosis-agent)

---

### 3D Point Cloud Classification & Segmentation Demo

PointNet-based 3D point cloud demo with Gradio interface. Upload a point cloud or pick a preset shape → get classification (ModelNet40) + part segmentation (ShapeNet Part) with 3D visualization.

- **PointNet**: Max-pooling symmetric function for permutation invariance
- **Classification**: ModelNet40 (40 object classes), Top-5 predictions
- **Segmentation**: ShapeNet Part (16 categories, 50 parts), per-point labels
- **Interactive**: Gradio web interface with 3D visualization
- Colab-ready, HuggingFace deployable

> 🔗 Repository: [pointcloud-demo](https://github.com/Aeijou37/pointcloud-demo)

---

### Edge Deployment Demo

PyTorch → ONNX → INT8 quantization pipeline with inference benchmark. Compare 3 inference paths (PyTorch / ONNX FP32 / ONNX INT8) on accuracy, latency, and model size.

- **Export**: PyTorch → ONNX (opset 17, dynamic batch)
- **Quantization**: INT8 dynamic quantization (4x smaller, no accuracy loss)
- **Benchmark**: Average / P50 / P95 / P99 latency + FPS comparison
- **Results**: 13.27 MB → 3.41 MB (3.9x compression), Top-1 prediction consistency 100%
- Colab-ready, HuggingFace deployable

> 🔗 Repository: [edge-deployment-demo](https://github.com/Aeijou37/edge-deployment-demo)

---

### Vision-based Shoe Sole Gluing Robot System

This project focuses on low-cost and high-precision visual perception for automated shoe sole gluing production lines.

Main work:

- Designed lightweight instance segmentation models for shoe sole localization (RGB-D camouflaged segmentation).
- Built single-view 3D reconstruction with collaborative encoding architecture.
- Developed multi-plane projection + geometric feature fusion for point cloud contour extraction.
- Extracted smooth and continuous 3D gluing trajectories with GAN-based error correction.
- Optimized model inference for real-time industrial deployment (3s/cycle).

Results:

- Achieved over 99% recognition accuracy.
- Reached gluing trajectory positioning accuracy within 1 mm.
- Completed the full pipeline from data collection, algorithm development, to production-line validation.
- 2 granted patents (as first & second inventor) + 1 paper under review (first author).

> 🔗 Code available upon request (university project, pending advisor approval)
> Deep-dive note: [Shoe-robot Vision: Instance Segmentation to 3D Trajectory](https://github.com/Aeijou37/cv-algorithm-notes/blob/main/articles/03-shoe-robot-vision.md)

---

## 📝 Technical Deep-Dive Notes

I write each project as a long-form note structured as **Problem → Baseline → Method → Ablation → Lessons** — including the experiments that *failed* and why. Interviewers care less about what I did and more about **why I tried it, where it failed, and where it worked**.

Repo: [**cv-algorithm-notes**](https://github.com/Aeijou37/cv-algorithm-notes)

- [EBeam Wafer Defect Classification — A Long-Tail Breakthrough](https://github.com/Aeijou37/cv-algorithm-notes/blob/main/articles/01-cxmt-wafer-defect-classification.md) — 97.79% → 100.00% via LDAM + DINOv2/SigLIP + distillation; 8 failed strategies documented.
- [Industrial X-ray Defect Detection — Two-Stage Pipeline](https://github.com/Aeijou37/cv-algorithm-notes/blob/main/articles/02-iflytek-xray-defect-detection.md) — AHTF tiling + YOLO26-Seg SDE/DAF (B-class Recall +21%); Boundary Loss failed; data strategy > model > loss.
- [Shoe-robot Vision: Instance Segmentation to 3D Trajectory](https://github.com/Aeijou37/cv-algorithm-notes/blob/main/articles/03-shoe-robot-vision.md) — RGB-D camouflaged segmentation → single-view 3D reconstruction → multi-plane projection trajectory extraction; 2 patents + 1 paper.
- [Multimodal RAG Academic QA Agent](https://github.com/Aeijou37/cv-algorithm-notes/blob/main/articles/04-rag-academic-qa-agent.md) — MMR + query rewriting + chat_template + post-processing; retrieval quality > generation quality > prompt engineering.

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
- RAG agent optimization (Reranker + evaluation framework)
- Point cloud demo training (ModelNet40 + ShapeNet Part)
- Edge deployment pipeline (ONNX + INT8 quantization)

---

## 📊 GitHub Stats

[![Top Languages](https://github-readme-stats.vercel.app/api/top-languages/?username=Aeijou37&layout=compact&theme=default)](https://github.com/Aeijou37)

[![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Aeijou37&show_icons=true&theme=default)](https://github.com/Aeijou37)

---

## 📫 Contact

- GitHub: [Aeijou37](https://github.com/Aeijou37)
- Email: [Leeguojiea@gmail.com](mailto:Leeguojiea@gmail.com)

> Always open to discussions on industrial AI, computer vision, RAG systems, and edge deployment.
