# Persian-Plates-Detection
AI-based Persian car plate and digit recognition using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle">
</div>

<p align="center">
  <img src="result.png" width="600">
</p>

## 📘 معرفی پروژه
این پروژه یک سیستم هوشمند برای **تشخیص پلاک خودروهای ایرانی** و استخراج نویسه‌های آن (اعداد و حروف) است که با مدل **YOLO11** آموزش دیده است.

* ✅ **دقت بالا:** شناسایی دقیق در شرایط نوری مختلف.
* ✅ **سرعت:** بهینه‌شده برای اجرا روی GPU (Kaggle T4).
* ✅ **خروجی:** تشخیص همزمان پلاک و تک‌تک اعداد.

---

## 🛠 Usage
```python
from ultralytics import YOLO

# بارگذاری مدل
model = YOLO('best.pt')

# پیش‌بینی روی عکس
results = model.predict(source='result.png', save=True)
