# End-to-End Self-Driving Perception

This project demonstrates an **integrated perception pipeline** for autonomous driving, combining **object detection**, **traffic light color classification**, and **road segmentation** into a single framework. The goal is to produce a **unified annotated view** of the driving scene that highlights **cars**, **traffic lights (with state labels)**, and the **drivable road area**.  

By merging these tasks, the system provides a foundation for downstream decision-making and control in self-driving cars.

---

## Introduction

Modern self-driving systems rely on multiple perception modules that must operate together in real time.  
This project builds a **complete perception stack** by connecting three core components:

1. **YOLOv8 (Detection)** – Detects objects of interest, specifically **cars** and **traffic lights**.  
2. **Traffic Light Color Classifier** – Determines the **state** of each traffic light (red, yellow, green) using color heuristics or a small CNN.  
3. **SegFormer (Segmentation)** – Identifies the **drivable road surface** with transformer-based semantic segmentation.  

The outputs of these models are merged into a **single annotated image** that provides:  
- Bounding boxes for **cars**  
- Colored bounding boxes + labels for **traffic lights**  
- Teal overlay for the **drivable road area**

This pipeline demonstrates how **detection, classification, and segmentation** can be integrated to improve scene understanding for autonomous navigation.

---

## Features

- **Real-time object detection** with YOLOv8.  
- **Traffic light state awareness** (red/yellow/green).  
- **Transformer-based segmentation** (SegFormer) for robust road marking.  
- **Unified visualization** of all outputs in one image.  
- Easy-to-extend pipeline for other object classes or segmentation tasks.  
