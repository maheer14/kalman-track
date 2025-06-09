# 🚗 KalmanTrack: AI-Powered Multi-Object Tracking System

KalmanTrack is a real-time vehicle tracking system that combines Kalman filters, motion detection, and AI-based threshold calibration to detect and track moving objects in surveillance video footage. This project was built with performance, precision, and visualization in mind — ideal for smart traffic analysis, surveillance, and computer vision research.

---

## 🔍 Features

- 🎯 **Multi-object tracking using Kalman filters**  
  Predict and update object positions across frames even with occlusions or noise.

- 🧠 **AI-based motion threshold tuning**  
  Trained a CNN model using TensorFlow on 50,000+ labeled frames to dynamically calibrate motion sensitivity (`tau`).

- 📊 **92.3% mAP accuracy** on test footage  
  Evaluated against multiple lighting and motion scenarios to maximize tracking reliability.

- 🎥 **Efficient triple-frame motion detection**  
  Uses frame differencing, morphological dilation, and region filtering to isolate motion areas.

- 🧮 **Real-time performance: <40ms/frame latency**  
  Optimized using NumPy vectorization and memory-efficient Kalman update cycles.

- 🖥️ **PySide6-powered GUI**  
  Clean, interactive interface with frame-by-frame playback, blue bounding box overlays, and slider navigation.

---

## 🧠 AI/ML Details

- **Motion Threshold Calibration (ML Component):**  
  A lightweight CNN was trained to classify motion vs. non-motion patterns. The model was used to auto-tune threshold values (`tau`) based on live frame features, increasing robustness to environmental variation (lighting, shadows, etc.).

- **Data:**  
  - 50,000+ custom-labeled frame samples (motion vs. no-motion)
  - 10,000+ frames of evaluation data from urban traffic surveillance
  - Augmented dataset using synthetic frame noise and lighting variation

- **Technologies:**  
  - `TensorFlow`, `scikit-learn`, `NumPy`, `OpenCV`, `PySide6`
  - Model trained and evaluated using GPU acceleration (NVIDIA RTX 3060)

---
