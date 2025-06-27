# 📡 Real-Time Animal Detection Using CCTV Camera (YOLOv8)


This project is an **open vision initiative** built using **YOLOv8**, a state-of-the-art object detection model developed by **Ultralytics**. It presents a complete pipeline for detecting animals from CCTV footage — suitable for both real-time and static image analysis. 

The system is designed to be modular, scalable, and easy to deploy, and is particularly useful for:

- 🐄 Farm and livestock monitoring  
- 🐘 Wildlife conservation and animal tracking  
- 🚧 Roadside animal presence alerts  
- 📷 General CCTV-based animal surveillance
---

## 🔍 Overview

This repository includes:

- ✅ Custom dataset loading and analysis
- ✅ Augmentation and data quality checks
- ✅ YOLOv8 model training and evaluation
- ✅ Inference interface for single images
- ✅ Example visualization of results

> 📌 Note: This notebook trains for 20 epochs using a public dataset for demonstration.  
In production, we used a **private CCTV dataset** and trained the model using **cloud-based GPUs** for performance and scale.

---

## 📦 Requirements

This project uses Python 3.8+ and runs in environments like **Kaggle**, **Colab**, or **Jupyter**. Install the following libraries:

```bash
pip install ultralytics albumentations opencv-python matplotlib seaborn
