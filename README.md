# 🚗 Persian Car Plate & Digits Detection using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge" alt="YOLO11">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle" alt="Kaggle">
</div>

---

## 📘 معرفی پروژه (Project Overview)
این پروژه یک سیستم هوشمند برای **تشخیص پلاک خودروهای ایرانی** و استخراج نویسه‌های آن است. با استفاده از معماری **YOLO11**، این مدل پلاک‌ها را در شرایط نوری مختلف با دقت بسیار بالا شناسایی می‌کند.

<div style="background-color: #f0f9ff; padding: 15px; border-radius: 10px; color: #0077b6;">
🔹 <b>هدف:</b> تبدیل تصاویر خودرو به داده‌های متنی پلاک با دقت ۹۹٪.
</div>

---

## 🖼 خروجی و نتایج مدل (Inference Results)
در تصویر زیر، پیش‌بینی‌های مدل روی تصاویر بخش Validation را مشاهده می‌کنید. مدل با دقت بالا کادر پلاک‌ها را شناسایی کرده است:

<p align="center">
  <img src="image_0a645c.jpg" width="100%" style="max-width: 850px; border-radius: 10px; box-shadow: 0 4px 8px rgba(0,0,0,0.1);">
  <br>
  <em>شکل ۱: نمونه شناسایی پلاک‌ها در دسته‌های مختلف (Validation Batch Labels)</em>
</p>

---

## 🚀 ویژگی‌های کلیدی (Key Features)
- ✅ **Object Detection:** مکان‌یابی دقیق مستطیل پلاک.
- ✅ **OCR Ready:** تشخیص تکی تمام اعداد و حروف فارسی پلاک.
- ✅ **High Speed:** بهینه‌شده برای اجرا روی پردازنده‌های گرافیکی (GPU).
- ✅ **Robust:** عملکرد پایدار در زوایای مختلف و فواصل متفاوت.

---

## 📊 آمار آموزش (Training Stats)
| Metric | Value | Status |
| :--- | :--- | :---: |
| **mAP50** | ~0.99 (99%) | 🎯 |
| **Precision** | Very High | ✅ |
| **Recall** | Stable | ✅ |

---

## 🛠 نحوه استفاده (Usage)
```python
from ultralytics import YOLO

# بارگذاری مدل
model = YOLO('best.pt')

# پیش‌بینی روی عکس جدید
results = model.predict(source='your_image.jpg', save=True, conf=0.5)
