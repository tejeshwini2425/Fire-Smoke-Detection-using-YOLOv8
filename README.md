# 🔥 Fire & Smoke Detection Using YOLOv8  

Real-time fire and smoke detection system using **YOLOv8**, trained on a custom Roboflow dataset. Supports **image inference**, **test dataset evaluation**, and **live webcam detection** with automatic frame saving when fire is detected.

---

## 🚀 Features  
- Detects **fire** and **smoke**  
- Works with images, test dataset, and webcam feed  
- Automatically saves frames with fire detection  
- Trained on a **custom Roboflow dataset**  

---

## 🛠️ Installation  
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
python -m venv venv
venv\Scripts\activate   # Windows
pip install ultralytics opencv-python jupyter

from ultralytics import YOLO

# Train
model = YOLO("yolov8n.pt")
model.train(data="dataset/data.yaml", epochs=30, imgsz=640)

# Predict on test images
model.predict(source="dataset/test/images", conf=0.25, save=True)

# Real-time webcam
model.predict(source=0, conf=0.25, show=True)

YOLO_Project/
 ┣ dataset/
 ┣ notebooks/
 ┣ runs/
 ┗ fire_smoke_detection.ipynb
