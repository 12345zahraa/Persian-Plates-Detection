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

### معرفی پروژه
این پروژه یک سیستم هوشمند برای تشخیص پلاک خودروهای ایرانی و استخراج نویسه‌های آن (اعداد و حروف) است. با استفاده از معماری پیشرفته **YOLO11**، این مدل قادر است در شرایط نوری مختلف و زوایای متفاوت، پلاک را با دقت بسیار بالا شناسایی کند.

---

## 🚀 ویژگی‌های کلیدی (Key Features)
- ✅ **تشخیص پلاک:** مکان‌یابی دقیق مستطیل پلاک.
- ✅ **بازخوانی نویسه‌ها:** تشخیص تکی تمام اعداد و حروف فارسی پلاک.
- ✅ **سرعت بالا:** بهینه‌شده برای اجرا روی GPU.

---

## 📂 ساختار فایل‌ها (File Structure)
- `best.pt`: فایل نهایی وزن‌های مدل آموزش‌دیده (۵.۳ مگابایت).
- `result.png`: تصویر نمونه از خروجی تشخیص پلاک.
- `README.md`: توضیحات و راهنمای پروژه.

---

## 🛠 نحوه استفاده (Usage)
```python
from ultralytics import YOLO

# بارگذاری مدل آموزش‌دیده
model = YOLO('best.pt')

# پیش‌بینی روی عکس جدید
results = model.predict(source='your_image.jpg', save=True)
