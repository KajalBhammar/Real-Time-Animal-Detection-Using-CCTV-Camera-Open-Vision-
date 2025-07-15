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

---

## 🗂️ Dataset Info

**Source**: Private Dataset

**Classes**:
```python
['Bird', 'Cats', 'Cow', 'Deer', 'Dog', 'Elephant', 'Giraffe', 'Person', 'Pig', 'Sheep']
```

**Folder Structure**:
```
/train/images/
/train/labels/
/valid/images/
/valid/labels/
/test/images/
/test/labels/
```

**Label Format (YOLO)**:
```
<class_id> <x_center> <y_center> <width> <height>   # All values normalized (0–1)
```

---

## 🛠️ Step-by-Step Usage

### 1️⃣ Clone or Upload the Project
- Upload the `.ipynb` notebook to [Kaggle](https://kaggle.com) or run locally with Jupyter.

### 2️⃣ Install Required Packages

```bash
pip install ultralytics albumentations opencv-python matplotlib seaborn
```

### 3️⃣ Load and Explore Dataset
- Dataset structure check  
- Class distribution visualization  
- Sample image bounding box rendering  
- Augmentation and quality validation

### 4️⃣ Train the YOLOv8 Model
- Loads pretrained `yolov8s.pt`  
- Trains for 20 epochs, `imgsz=640`, `batch=16`  
- Saves outputs to `runs/detect/animal-detection-yolov8/`

### 5️⃣ Visualize Training Results
Generates plots automatically:
- 📈 F1 Curve  
- 🎯 Precision-Recall Curve  
- ✅ Precision and Recall

### 6️⃣ Inference Interface
- Run inference on a static image  
- Output is visualized directly using `matplotlib`  
- Extendable to webcam/video input

---

## 📸 Example Output

Sample YOLOv8 output with bounding boxes on animal classes:

```
📷 Image: valid/images/sample.jpg
→ Detected: Cow, Dog, Sheep with confidence > 0.5
→ Rendered bounding boxes in real-time
```

> (Include screenshots in your repo for visual clarity)

---

## 🧠 Model Performance

YOLOv8 provides performance metrics during and after training, including:

- `mAP@0.5`, `mAP@0.5:0.95`
- Precision, Recall, and F1 score
- Loss curves for training and validation

All metrics are logged automatically and plots are available under:
```
runs/detect/animal-detection-yolov8/
```

---

## 📦 Requirements

This project uses Python 3.8+ and runs in environments like **Kaggle**, **Colab**, or **Jupyter**.

### Install Libraries:

```bash
pip install ultralytics albumentations opencv-python matplotlib seaborn
```

---

## 🚀 Deployment (Optional)

To deploy this project for real-time use:

- Wrap the inference logic in a **Streamlit** or **Flask** app  
- Use a webcam or CCTV video stream as input  
- Optimize the trained YOLOv8 model with **ONNX** or **TensorRT** for edge devices  
- Host it on a cloud server or local edge device like Jetson Nano / Raspberry Pi

---

## 🧑‍💻 Author

**Kajal Bhammar**  
AI/ML Engineer  
📧 Email: kajalbhammar@gmail.com  

Feel free to reach out for collaboration or inquiries.

---

