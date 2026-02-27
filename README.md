# Persian-Plates-Detection
AI-based Persian car plate and digit recognition using YOLO11

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python">
  <img src="https://img.shields.io/badge/YOLO-v11-0077b6?style=for-the-badge">
  <img src="https://img.shields.io/badge/Kaggle-GPU_T4-20BEFF?style=for-the-badge&logo=kaggle">
</div>

![نتایج تشخیص پلاک](result.png)

<div dir="rtl">

## 📘 معرفی پروژه
این پروژه یک سیستم هوشمند برای تشخیص پلاک خودروهای ایرانی و استخراج نویسه‌های آن (اعداد و حروف) است که با استفاده از معماری YOLO11 پیاده‌سازی شده است.

### 🚀 ویژگی‌های کلیدی
* ✅ **تشخیص پلاک:** مکان‌یابی دقیق مستطیل پلاک
* ✅ **بازخوانی نویسه‌ها:** تشخیص تمام اعداد و حروف فارسی
* ✅ **سرعت بالا:** بهینه‌شده برای اجرا روی GPU (Kaggle T4)

### 📂 ساختار فایل‌ها
* `best.pt`: فایل نهایی وزن‌های مدل (۵.۳ مگابایت)
* `result.png`: تصویر نمونه از خروجی تشخیص پلاک

</div>

---

## 🛠 Usage
```python
from ultralytics import YOLO
model = YOLO('best.pt')
results = model.predict(source='result.png', save=True)
model = YOLO('best.pt')

# Predict on an image
results = model.predict(source='result.png', save=True)
