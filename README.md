# 🚗 Persian Car Plate & Digits Detection using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge" alt="YOLO11">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle" alt="Kaggle">
</div>

---

## 📘 معرفی پروژه (Project Overview)
این پروژه یک سیستم هوشمند برای **تشخیص پلاک خودروهای ایرانی** است که با استفاده از الگوریتم **YOLO11** توسعه یافته است.

---

## 🖼 خروجی مدل (Detection Result)
<p align="center">
  <img src="image_0a645c.jpg" width="100%">
</p>

---

## 🚀 ویژگی‌های کلیدی
- ✅ **تشخیص پلاک (Object Detection):** مکان‌یابی دقیق مستطیل پلاک.
- ✅ **سرعت بالا:** بهینه‌شده برای اجرا روی GPU.
- ✅ **دقت عالی:** آموزش دیده بر روی دیتاست پلاک‌های ایرانی.

---

## 🛠 نحوه استفاده (Usage)
```python
from ultralytics import YOLO

# بارگذاری مدل و پیش‌بینی
model = YOLO('best.pt')
results = model.predict(source='car.jpg', save=True)
