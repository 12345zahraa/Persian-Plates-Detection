# Persian-Plates-Detection
 AI-based Persian car plate and digit recognition using YOLO11
# 🚗 Persian Car Plate & Digits Detection using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge" alt="YOLO11">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle" alt="Kaggle">
</div>

---
![نتایج تشخیص پلاک](result.png)

## 📘 معرفی پروژه (Project Overview)
این پروژه یک سیستم هوشمند برای **تشخیص پلاک خودروهای ایرانی** و استخراج نویسه‌های آن (اعداد و حروف) است. با استفاده از معماری پیشرفته **YOLO11**، این مدل قادر است در شرایط نوری مختلف و زوایای متفاوت، پلاک را با دقت بسیار بالا شناسایی کند.

<div style="background-color: #f0f9ff; padding: 15px; border-radius: 10px; color: #0077b6;">
🔹 <b>هدف:</b> تبدیل تصاویر خودرو به داده‌های متنی پلاک با دقت ۹۹٪.
</div>

---

## 🚀 ویژگی‌های کلیدی (Key Features)
- ✅ **تشخیص پلاک (Object Detection):** مکان‌یابی دقیق مستطیل پلاک.
- ✅ **بازخوانی نویسه‌ها (OCR/Digit Recognition):** تشخیص تکی تمام اعداد و حروف فارسی پلاک.
- ✅ **سرعت بالا:** بهینه‌شده برای اجرا روی پردازنده‌های گرافیکی (GPU).
- ✅ **دقت عالی:** آموزش دیده بر روی دیتاست تخصصی پلاک‌های ایرانی.

---

## 📊 نتایج آموزش (Training Results)
مدل بر روی دو کلاس (Plate & Digits) آموزش دیده است. نتایج ماتریس درهم‌ریختگی و نمودارهای دقت به شرح زیر است:

| Metric | Value |
| :--- | :--- |
| **mAP50** | ~0.99 (99%) |
| **Precision** | Very High |
| **Recall** | Stable |

---

## 📂 ساختار فایل‌ها (File Structure)
- `persian-plates-detection-yolo11.ipynb`: نوت‌بوک کامل آموزش و تست در محیط کگل.
- `best.pt`: فایل نهایی وزن‌های مدل آموزش‌دیده.
- `README.md`: توضیحات و راهنمای پروژه.

---

## 🛠 نحوه استفاده (Usage)
برای اجرای مدل روی عکس‌های خودتان، ابتدا کتابخانه `ultralytics` را نصب کرده و سپس از کد زیر استفاده کنید:

```python
from ultralytics import YOLO

# بارگذاری مدل آموزش‌دیده
model = YOLO('best.pt')

# پیش‌بینی روی عکس جدید
results = model.predict(source='your_image.jpg', save=True)
