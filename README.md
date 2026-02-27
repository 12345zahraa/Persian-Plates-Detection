# Persian-Plates-Detection
AI-based Persian car plate and digit recognition using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle">
</div>

---

## 📘 معرفی پروژه
این پروژه یک سیستم هوشمند برای تشخیص پلاک خودروهای ایرانی و استخراج نویسه‌های آن (اعداد و حروف) است که با استفاده از معماری YOLO11 پیاده‌سازی شده است.

### 🚀 ویژگی‌های کلیدی
* ✅ **دقت بالا:** تشخیص نویسه‌ها با mAP 99%.
* ✅ **سرعت بالا:** بهینه‌شده برای اجرا روی GPU.

---

## 🛠 Usage
```python
from ultralytics import YOLO
model = YOLO('best.pt')
results = model.predict(source='result.jpg', save=True)
